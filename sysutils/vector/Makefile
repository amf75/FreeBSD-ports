# $FreeBSD$

PORTNAME=	vector
DISTVERSIONPREFIX=	v
DISTVERSION=	0.7.1
PORTREVISION=	5
CATEGORIES=	sysutils

MAINTAINER=	greg@unrelenting.technology
COMMENT=	High performance logs, metrics, and events router

LICENSE=	APACHE20
LICENSE_FILE=	${WRKSRC}/LICENSE

BROKEN_FreeBSD_12_powerpc64=	fails to link: /usr/local/bin/ld: cannot find -lc++

BUILD_DEPENDS=	protoc:devel/protobuf
LIB_DEPENDS=	libonig.so:devel/oniguruma \
		librdkafka.so:net/librdkafka

USES=		cargo lua:53 ssl
USE_GITHUB=	yes
GH_ACCOUNT=	timberio

PLIST_FILES=	bin/vector

GH_TUPLE=		timberio:leveldb:64265815bcf1b69f30e6cb35bf687fbd6dd64afb:leveldb \
			timberio:leveldb-sys:0f226b0cce86aff28f255ef89082916e4fdda4c7:leveldbsys \
			timberio:rlua:c41bfa06cfaf3df543796d3104ec910dd1a24c44:rlua \
			tokio-rs:tracing:8720792dbdf3158c4dbfcaf879e28da7af67c3f7:tracingfutures
CARGO_CRATES=	adler32-1.0.4 \
		aho-corasick-0.7.6 \
		ansi_term-0.11.0 \
		antidote-1.0.0 \
		approx-0.3.2 \
		arc-swap-0.4.3 \
		arrayref-0.3.5 \
		arrayvec-0.4.12 \
		assert_matches-1.3.0 \
		atty-0.2.13 \
		autocfg-0.1.7 \
		backtrace-0.3.40 \
		backtrace-sys-0.1.32 \
		base64-0.9.3 \
		base64-0.10.1 \
		base64-0.11.0 \
		bit-set-0.5.1 \
		bit-vec-0.5.1 \
		bitflags-1.2.1 \
		blake2b_simd-0.5.8 \
		block-buffer-0.7.3 \
		block-padding-0.1.4 \
		bstr-0.2.8 \
		buf_redux-0.8.4 \
		build_const-0.2.1 \
		built-0.3.2 \
		byte-tools-0.3.1 \
		byteorder-1.3.2 \
		bytes-0.4.12 \
		bytesize-1.0.0 \
		c2-chacha-0.2.3 \
		cast-0.2.2 \
		cc-1.0.46 \
		cfg-if-0.1.10 \
		chrono-0.4.9 \
		clap-2.33.0 \
		cloudabi-0.0.3 \
		cmake-0.1.42 \
		colored-1.9.0 \
		constant_time_eq-0.1.4 \
		cookie-0.12.0 \
		cookie_store-0.7.0 \
		core-foundation-0.6.4 \
		core-foundation-sys-0.6.2 \
		crc-1.8.1 \
		crc32fast-1.2.0 \
		criterion-0.2.11 \
		criterion-0.3.0 \
		criterion-plot-0.3.1 \
		criterion-plot-0.4.0 \
		crossbeam-channel-0.3.9 \
		crossbeam-deque-0.7.1 \
		crossbeam-epoch-0.7.2 \
		crossbeam-queue-0.1.2 \
		crossbeam-utils-0.6.6 \
		crypto-mac-0.7.0 \
		csv-1.1.1 \
		csv-core-0.1.6 \
		ctor-0.1.12 \
		data-encoding-2.1.2 \
		data-encoding-macro-0.1.7 \
		data-encoding-macro-internal-0.1.7 \
		db-key-0.0.5 \
		derivative-1.0.3 \
		derive_is_enum_variant-0.1.1 \
		difference-2.0.0 \
		digest-0.8.1 \
		dirs-1.0.5 \
		doc-comment-0.3.1 \
		dtoa-0.4.4 \
		either-1.5.3 \
		elastic_responses-0.20.10 \
		encoding_rs-0.8.20 \
		endian-type-0.1.2 \
		enum-as-inner-0.2.1 \
		env_logger-0.5.13 \
		env_logger-0.6.2 \
		erased-serde-0.3.9 \
		error-chain-0.12.1 \
		evmap-7.1.2 \
		exitcode-1.1.2 \
		failure-0.1.6 \
		failure_derive-0.1.6 \
		fake-simd-0.1.2 \
		fallible-iterator-0.2.0 \
		fallible-streaming-iterator-0.1.9 \
		filetime-0.2.7 \
		fixedbitset-0.1.9 \
		flate2-1.0.12 \
		fnv-1.0.6 \
		foreign-types-0.3.2 \
		foreign-types-shared-0.1.1 \
		fs_extra-1.1.0 \
		fuchsia-cprng-0.1.1 \
		fuchsia-zircon-0.3.3 \
		fuchsia-zircon-sys-0.3.3 \
		futures-0.1.29 \
		futures-0.3.1 \
		futures-channel-0.3.1 \
		futures-core-0.3.1 \
		futures-cpupool-0.1.8 \
		futures-io-0.3.1 \
		futures-sink-0.3.1 \
		futures-task-0.3.1 \
		futures-util-0.3.1 \
		futures01-0.1.29 \
		generic-array-0.12.3 \
		getrandom-0.1.13 \
		ghost-0.1.1 \
		git2-0.10.1 \
		glob-0.2.11 \
		glob-0.3.0 \
		goauth-0.6.0 \
		grok-1.0.1 \
		h2-0.1.26 \
		hashbrown-0.1.8 \
		hdrhistogram-6.3.4 \
		headers-0.2.3 \
		headers-core-0.1.1 \
		heck-0.3.1 \
		hermit-abi-0.1.3 \
		hex-0.3.2 \
		hmac-0.7.1 \
		hostname-0.1.5 \
		hotmic-0.8.2 \
		http-0.1.19 \
		http-body-0.1.0 \
		http-connection-0.1.0 \
		httparse-1.3.4 \
		humantime-1.3.0 \
		hyper-0.12.35 \
		hyper-openssl-0.7.1 \
		hyper-tls-0.3.2 \
		hyperlocal-0.6.0 \
		idna-0.1.5 \
		idna-0.2.0 \
		indexmap-1.3.0 \
		input_buffer-0.2.0 \
		inventory-0.1.4 \
		inventory-impl-0.1.4 \
		iovec-0.1.4 \
		ipconfig-0.2.1 \
		itertools-0.7.11 \
		itertools-0.8.1 \
		itoa-0.4.4 \
		jemalloc-sys-0.3.2 \
		jemallocator-0.3.2 \
		jobserver-0.1.17 \
		k8s-openapi-0.5.1 \
		kernel32-sys-0.2.2 \
		kube-0.16.1 \
		lazy_static-1.4.0 \
		leveldb-sys-2.0.5 \
		lexical-core-0.4.6 \
		libc-0.2.65 \
		libgit2-sys-0.9.1 \
		libsqlite3-sys-0.16.0 \
		libz-sys-1.0.25 \
		linked-hash-map-0.5.2 \
		linked_hash_set-0.1.3 \
		listenfd-0.3.3 \
		lock_api-0.1.5 \
		lock_api-0.3.1 \
		log-0.3.9 \
		log-0.4.8 \
		lz4-sys-1.8.3 \
		logfmt-0.0.2 \
		lru-cache-0.1.2 \
		matchers-0.0.1 \
		matches-0.1.8 \
		maxminddb-0.13.0 \
		md5-0.6.1 \
		memchr-2.2.1 \
		memoffset-0.5.2 \
		mime-0.2.6 \
		mime-0.3.14 \
		mime_guess-1.8.7 \
		mime_guess-2.0.1 \
		miniz_oxide-0.3.5 \
		mio-0.6.19 \
		mio-named-pipes-0.1.6 \
		mio-uds-0.6.7 \
		miow-0.2.1 \
		miow-0.3.3 \
		multimap-0.4.0 \
		multipart-0.16.1 \
		native-tls-0.2.3 \
		net2-0.2.33 \
		new_debug_unreachable-1.0.3 \
		nibble_vec-0.0.4 \
		nodrop-0.1.14 \
		nom-4.2.3 \
		nom-5.0.1 \
		num-integer-0.1.41 \
		num-traits-0.2.8 \
		num_cpus-0.2.13 \
		num_cpus-1.11.0 \
		onig-4.3.3 \
		onig_sys-69.1.0 \
		opaque-debug-0.2.3 \
		openssl-0.10.26 \
		openssl-probe-0.1.2 \
		openssl-src-111.6.0+1.1.1d \
		openssl-sys-0.9.53 \
		ordered-float-1.0.2 \
		output_vt100-0.1.2 \
		owning_ref-0.4.0 \
		parking_lot-0.7.1 \
		parking_lot-0.9.0 \
		parking_lot_core-0.4.0 \
		parking_lot_core-0.6.2 \
		percent-encoding-1.0.1 \
		percent-encoding-2.1.0 \
		petgraph-0.4.13 \
		phf-0.7.24 \
		phf_codegen-0.7.24 \
		phf_generator-0.7.24 \
		phf_shared-0.7.24 \
		pin-project-0.4.6 \
		pin-project-internal-0.4.6 \
		pin-utils-0.1.0-alpha.4 \
		pkg-config-0.3.16 \
		ppv-lite86-0.2.6 \
		precomputed-hash-0.1.1 \
		pretty_assertions-0.6.1 \
		proc-macro-hack-0.5.11 \
		proc-macro2-0.4.30 \
		proc-macro2-1.0.6 \
		proptest-0.9.4 \
		prost-0.4.0 \
		prost-0.5.0 \
		prost-build-0.4.0 \
		prost-derive-0.4.0 \
		prost-derive-0.5.0 \
		prost-types-0.4.0 \
		prost-types-0.5.0 \
		publicsuffix-1.5.3 \
		rdkafka-0.22.0 \
		rdkafka-sys-1.2.2 \
		quanta-0.2.0 \
		quick-error-1.2.2 \
		quickcheck-0.6.2 \
		quote-0.3.15 \
		quote-0.6.13 \
		quote-1.0.2 \
		radix_trie-0.1.5 \
		rand-0.4.6 \
		rand-0.5.6 \
		rand-0.6.5 \
		rand-0.7.2 \
		rand_chacha-0.1.1 \
		rand_chacha-0.2.1 \
		rand_core-0.3.1 \
		rand_core-0.4.2 \
		rand_core-0.5.1 \
		rand_hc-0.1.0 \
		rand_hc-0.2.0 \
		rand_isaac-0.1.1 \
		rand_jitter-0.1.4 \
		rand_os-0.1.3 \
		rand_os-0.2.2 \
		rand_pcg-0.1.2 \
		rand_xorshift-0.1.1 \
		rand_xoshiro-0.1.0 \
		rand_xoshiro-0.3.1 \
		rayon-1.2.0 \
		rayon-core-1.6.0 \
		rdrand-0.4.0 \
		redox_syscall-0.1.56 \
		redox_users-0.3.1 \
		regex-1.3.1 \
		regex-automata-0.1.8 \
		regex-syntax-0.6.12 \
		remove_dir_all-0.5.2 \
		reqwest-0.9.22 \
		resolv-conf-0.6.2 \
		rusoto_cloudwatch-0.41.0 \
		rusoto_core-0.41.0 \
		rusoto_credential-0.41.1 \
		rusoto_firehose-0.41.0 \
		rusoto_kinesis-0.41.0 \
		rusoto_logs-0.41.0 \
		rusoto_s3-0.41.0 \
		rusoto_sts-0.41.0 \
		rusqlite-0.20.0 \
		rust-argon2-0.5.1 \
		rustc-demangle-0.1.16 \
		rustc_version-0.2.3 \
		rusty-fork-0.2.2 \
		ryu-1.0.2 \
		safemem-0.3.3 \
		same-file-1.0.5 \
		scan_fmt-0.2.4 \
		schannel-0.1.16 \
		scoped-tls-1.0.0 \
		scopeguard-0.3.3 \
		scopeguard-1.0.0 \
		seahash-3.0.6 \
		security-framework-0.3.1 \
		security-framework-sys-0.3.1 \
		semver-0.9.0 \
		semver-parser-0.7.0 \
		serde-1.0.102 \
		serde-value-0.6.0 \
		serde_derive-1.0.102 \
		serde_json-1.0.41 \
		serde_urlencoded-0.5.5 \
		serde_urlencoded-0.6.1 \
		serde_yaml-0.8.11 \
		sha-1-0.8.1 \
		sha2-0.8.0 \
		shiplift-0.6.0 \
		shlex-0.1.1 \
		signal-hook-0.1.11 \
		signal-hook-registry-1.1.1 \
		siphasher-0.2.3 \
		slab-0.4.2 \
		smallvec-0.6.12 \
		smallvec-1.0.0 \
		smpl_jwt-0.4.0 \
		snafu-0.4.4 \
		snafu-derive-0.4.4 \
		socket2-0.3.11 \
		spin-0.5.2 \
		stable_deref_trait-1.1.1 \
		static_assertions-0.3.4 \
		stream-cancel-0.4.4 \
		string-0.2.1 \
		string_cache-0.7.5 \
		string_cache_codegen-0.4.4 \
		string_cache_shared-0.3.0 \
		strip-ansi-escapes-0.1.0 \
		strsim-0.8.0 \
		structopt-0.2.18 \
		structopt-derive-0.2.18 \
		subtle-1.0.0 \
		syn-0.11.11 \
		syn-0.14.9 \
		syn-0.15.44 \
		syn-1.0.7 \
		synom-0.11.3 \
		synstructure-0.12.1 \
		syslog_rfc5424-0.6.1 \
		tar-0.4.26 \
		tempdir-0.3.7 \
		tempfile-3.1.0 \
		termcolor-1.0.5 \
		textwrap-0.11.0 \
		thread_local-0.3.6 \
		time-0.1.42 \
		tinytemplate-1.0.2 \
		tokio-0.1.22 \
		tokio-buf-0.1.1 \
		tokio-codec-0.1.1 \
		tokio-current-thread-0.1.6 \
		tokio-executor-0.1.8 \
		tokio-fs-0.1.6 \
		tokio-io-0.1.12 \
		tokio-openssl-0.3.0 \
		tokio-process-0.2.4 \
		tokio-reactor-0.1.10 \
		tokio-retry-0.2.0 \
		tokio-signal-0.2.7 \
		tokio-sync-0.1.7 \
		tokio-tcp-0.1.3 \
		tokio-threadpool-0.1.16 \
		tokio-timer-0.2.11 \
		tokio-tls-0.2.1 \
		tokio-udp-0.1.5 \
		tokio-uds-0.2.5 \
		tokio01-test-0.1.1 \
		toml-0.4.10 \
		toml-0.5.5 \
		tower-0.1.1 \
		tower-buffer-0.1.2 \
		tower-discover-0.1.0 \
		tower-http-util-0.1.0 \
		tower-hyper-0.1.1 \
		tower-layer-0.1.0 \
		tower-limit-0.1.1 \
		tower-load-shed-0.1.0 \
		tower-retry-0.1.0 \
		tower-service-0.2.0 \
		tower-test-0.1.0 \
		tower-timeout-0.1.1 \
		tower-util-0.1.0 \
		tracing-0.1.10 \
		tracing-attributes-0.1.5 \
		tracing-core-0.1.7 \
		tracing-futures-0.2.0 \
		tracing-log-0.1.1 \
		tracing-subscriber-0.1.6 \
		trust-dns-0.17.0 \
		trust-dns-proto-0.8.0 \
		trust-dns-resolver-0.12.0 \
		trust-dns-server-0.17.0 \
		try-lock-0.2.2 \
		try_from-0.3.2 \
		tungstenite-0.9.2 \
		twoway-0.1.8 \
		typenum-1.11.2 \
		typetag-0.1.4 \
		typetag-impl-0.1.4 \
		unicase-1.4.2 \
		unicase-2.5.1 \
		unicode-bidi-0.3.4 \
		unicode-normalization-0.1.8 \
		unicode-segmentation-1.5.0 \
		unicode-width-0.1.6 \
		unicode-xid-0.0.4 \
		unicode-xid-0.1.0 \
		unicode-xid-0.2.0 \
		url-1.7.2 \
		url-2.1.0 \
		urlencoding-1.0.0 \
		utf-8-0.7.5 \
		utf8-ranges-1.0.4 \
		utf8parse-0.1.1 \
		uuid-0.6.5 \
		uuid-0.7.4 \
		vcpkg-0.2.7 \
		vec_map-0.8.1 \
		version_check-0.1.5 \
		vte-0.3.3 \
		wait-timeout-0.2.0 \
		walkdir-2.2.9 \
		want-0.2.0 \
		warp-0.1.20 \
		wasi-0.7.0 \
		which-2.0.1 \
		widestring-0.4.0 \
		winapi-0.2.8 \
		winapi-0.3.8 \
		winapi-build-0.1.1 \
		winapi-i686-pc-windows-gnu-0.4.0 \
		winapi-util-0.1.2 \
		winapi-x86_64-pc-windows-gnu-0.4.0 \
		wincolor-1.0.2 \
		winreg-0.6.2 \
		winutil-0.1.1 \
		ws2_32-sys-0.2.1 \
		xattr-0.2.2 \
		xml-rs-0.8.0 \
		yaml-rust-0.4.3
CARGO_USE_GITHUB=	yes
CARGO_GIT_SUBDIR=	tracingfutures:tracing-futures:tracing-futures \
			tracingfutures:tracing-tower:tracing-tower

post-patch:
	${REINPLACE_CMD} -e 's|.probe("lua")|.probe("lua-5.3")|' \
		${WRKSRC_rlua}/build.rs

post-install:
	${STRIP_CMD} ${STAGEDIR}${PREFIX}/bin/vector

.include <bsd.port.mk>
