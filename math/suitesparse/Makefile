# Created by: Maho Nakata <maho@FreeBSD.org>
# $FreeBSD$

PORTNAME=	suitesparse
PORTVERSION=	5.7.2
PORTREVISION=	1
DISTVERSIONPREFIX=	v
CATEGORIES=	math

MAINTAINER=	fortran@FreeBSD.org
COMMENT=	Set of packages for sparse matrix calculation

LICENSE=	GPLv2 LGPL21
LICENSE_COMB=	dual

LIB_DEPENDS=	libmetis.so:math/metis

USE_GITHUB=	yes
GH_ACCOUNT=	DrTimothyAldenDavis
GH_PROJECT=	SuiteSparse

USES=		cmake:insource fortran gmake localbase:ldflags
USE_LDCONFIG=	yes
ALL_TARGET=	library # skip demos
INSTALL_TARGET=	install # skip USES=cmake
MAKE_ENV=	BLAS="${BLASLIB}" LAPACK="${LAPACKLIB}" \
		MY_METIS_LIB="-lmetis" \
		JOBS="${MAKE_JOBS_NUMBER}" \
		CMAKE_OPTIONS='${CMAKE_ARGS}' \
		INSTALL="${STAGEDIR}${PREFIX}" \
		INSTALL_DOC="${STAGEDIR}${DOCSDIR}" \
		INSTALL_INCLUDE="${STAGEDIR}${PREFIX}/include/${PORTNAME}"
CMAKE_ARGS=	-DCMAKE_INSTALL_INCLUDEDIR:PATH="include/${PORTNAME}"	\
		-DBUILD_GRB_STATIC_LIBRARY:BOOL=ON
LDFLAGS+=	-L${WRKSRC}/lib # prevent linking with shared libs from the preinstalled older versions

CONFLICTS_INSTALL=	mongoose plinkseq # bin/mongoose

OPTIONS_DEFINE=	DOCS OPENMP TBB
OPTIONS_RADIO=	BLAS
OPTIONS_RADIO_BLAS=	ATLAS GOTOBLAS NETLIB OPENBLAS
OPTIONS_DEFAULT=	OPENBLAS OPENMP TBB

ATLAS_USES=		blaslapack:atlas
GOTOBLAS_DESC=		Goto blas implementation
GOTOBLAS_USES=		blaslapack:gotoblas
NETLIB_USES=		blaslapack:netlib
OPENBLAS_USES=		blaslapack:openblas

OPENMP_USES=		compiler:openmp
OPENMP_MAKE_ENV_OFF=	CFOPENMP=
.if !exists(/usr/include/omp.h)
# XXX ports/199603: LLVM openmp in base doesn't support aarch64, armv6, armv7 yet
OPENMP_VARS=		OPENMP=gcc-
.endif

TBB_DESC=		Intel threading building blocks
TBB_LIB_DEPENDS=	libtbb.so:devel/tbb
TBB_MAKE_ENV=		TBB="-ltbb" SPQR_CONFIG="-DHAVE_TBB"

.include <bsd.port.options.mk>

.if ${ARCH} == i386
# See PR 230888 : Missing 64 bit atomic functions for i386
USES+=		compiler:gcc-c++11-lib
LDFLAGS+=	-latomic
.elif defined(PPC_ABI) && ${PPC_ABI} == ELFv1
USE_GCC=	yes
.else
USES+=	compiler:${OPENMP}c++11-lib
.endif

post-extract:
	${RM} -r ${WRKSRC}/metis-*

do-configure: # skip USES=cmake

post-patch-OPENMP-off:
	@${REINPLACE_CMD} -e '/find_package.*OpenMP/d' \
		${WRKSRC}/GraphBLAS/CMakeLists.txt

post-install:
	@${STRIP_CMD} ${STAGEDIR}${PREFIX}/bin/* ${STAGEDIR}${PREFIX}/lib/*.so

.include <bsd.port.mk>
