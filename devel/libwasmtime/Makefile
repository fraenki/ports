PORTNAME=	lib${GH_PROJECT}
PORTVERSION=	16.0.0
DISTVERSIONPREFIX=	v
PORTREVISION=	1
CATEGORIES=	devel

MAINTAINER=	osa@FreeBSD.org
COMMENT=	Library for fast and secure runtime for WebAssembly
WWW=		https://wasmtime.dev/

LICENSE=	APACHE20
LICENSE_FILE=	${WRKSRC}/LICENSE

NOT_FOR_ARCHS=	i386
NOT_FOR_ARCHS_REASON=	build currently failing

USES=		cargo cpe
CPE_VENDOR=	bytecodealliance

USE_LDCONFIG=	yes

USE_GITHUB=	yes
GH_ACCOUNT=	bytecodealliance
GH_PROJECT=	wasmtime

CARGO_BUILD_ARGS=	-p wasmtime-c-api

CARGO_CRATES=	addr2line-0.21.0 \
		adler-1.0.2 \
		ahash-0.8.2 \
		aho-corasick-1.0.2 \
		ambient-authority-0.0.2 \
		anes-0.1.6 \
		anstream-0.3.2 \
		anstyle-1.0.1 \
		anstyle-parse-0.2.1 \
		anstyle-query-1.0.0 \
		anstyle-wincon-1.0.1 \
		anyhow-1.0.75 \
		arbitrary-1.3.1 \
		async-trait-0.1.71 \
		atty-0.2.14 \
		autocfg-1.1.0 \
		backtrace-0.3.69 \
		base64-0.21.0 \
		bincode-1.3.3 \
		bit-set-0.5.2 \
		bit-vec-0.6.3 \
		bitflags-1.3.2 \
		bitflags-2.4.1 \
		block-buffer-0.10.2 \
		bstr-1.6.0 \
		bumpalo-3.12.0 \
		byteorder-1.4.3 \
		bytes-1.4.0 \
		bytesize-1.3.0 \
		camino-1.1.4 \
		cap-fs-ext-2.0.0 \
		cap-net-ext-2.0.0 \
		cap-primitives-2.0.0 \
		cap-rand-2.0.0 \
		cap-std-2.0.0 \
		cap-tempfile-2.0.0 \
		cap-time-ext-2.0.0 \
		capstone-0.9.0 \
		capstone-sys-0.13.0 \
		cargo-platform-0.1.2 \
		cargo_metadata-0.15.3 \
		cast-0.3.0 \
		cc-1.0.73 \
		cfg-if-1.0.0 \
		ciborium-0.2.0 \
		ciborium-io-0.2.0 \
		ciborium-ll-0.2.0 \
		clap-4.3.12 \
		clap_builder-4.3.12 \
		clap_derive-4.3.12 \
		clap_lex-0.5.0 \
		codespan-reporting-0.11.1 \
		colorchoice-1.0.0 \
		console-0.15.0 \
		cpp_demangle-0.3.5 \
		cpufeatures-0.2.7 \
		crc32fast-1.3.2 \
		criterion-0.5.1 \
		criterion-plot-0.5.0 \
		crossbeam-deque-0.8.1 \
		crossbeam-epoch-0.9.15 \
		crossbeam-utils-0.8.10 \
		crypto-common-0.1.6 \
		cty-0.2.2 \
		debugid-0.8.0 \
		derive_arbitrary-1.3.1 \
		digest-0.10.3 \
		directories-next-2.0.0 \
		dirs-next-2.0.0 \
		dirs-sys-next-0.1.2 \
		downcast-rs-1.2.0 \
		egg-0.6.0 \
		either-1.6.1 \
		encode_unicode-0.3.6 \
		encoding_rs-0.8.31 \
		env_logger-0.7.1 \
		env_logger-0.10.0 \
		equivalent-1.0.1 \
		errno-0.3.6 \
		fallible-iterator-0.3.0 \
		fastrand-2.0.1 \
		fd-lock-4.0.0 \
		file-per-thread-logger-0.2.0 \
		filecheck-0.5.0 \
		filetime-0.2.16 \
		flagset-0.4.3 \
		fnv-1.0.7 \
		form_urlencoded-1.1.0 \
		fs-set-times-0.20.0 \
		fslock-0.1.8 \
		futures-0.3.27 \
		futures-channel-0.3.27 \
		futures-core-0.3.27 \
		futures-io-0.3.28 \
		futures-sink-0.3.27 \
		futures-task-0.3.27 \
		futures-util-0.3.27 \
		fxhash-0.2.1 \
		fxprof-processed-profile-0.6.0 \
		generic-array-0.14.5 \
		getrandom-0.2.9 \
		gimli-0.28.0 \
		glob-0.3.0 \
		h2-0.4.0 \
		half-1.8.2 \
		hashbrown-0.12.3 \
		hashbrown-0.13.2 \
		hashbrown-0.14.0 \
		heck-0.4.0 \
		hermit-abi-0.1.19 \
		hermit-abi-0.3.0 \
		http-1.0.0 \
		http-body-1.0.0 \
		http-body-util-0.1.0 \
		httparse-1.8.0 \
		httpdate-1.0.2 \
		humantime-1.3.0 \
		humantime-2.1.0 \
		hyper-1.0.1 \
		id-arena-2.2.1 \
		idna-0.3.0 \
		indexmap-1.9.1 \
		indexmap-2.0.0 \
		indexmap-nostd-0.4.0 \
		indicatif-0.13.0 \
		instant-0.1.12 \
		io-extras-0.18.0 \
		io-lifetimes-2.0.2 \
		ipnet-2.5.0 \
		is-terminal-0.4.9 \
		itertools-0.10.3 \
		itoa-1.0.1 \
		ittapi-0.4.0 \
		ittapi-sys-0.4.0 \
		jobserver-0.1.24 \
		js-sys-0.3.57 \
		lazy_static-1.4.0 \
		leb128-0.2.5 \
		libc-0.2.149 \
		libfuzzer-sys-0.4.5 \
		libloading-0.7.3 \
		libm-0.2.7 \
		linux-raw-sys-0.4.10 \
		listenfd-1.0.0 \
		log-0.4.17 \
		mach-0.3.2 \
		matchers-0.1.0 \
		maybe-owned-0.3.4 \
		memchr-2.5.0 \
		memfd-0.6.4 \
		memmap2-0.2.3 \
		memoffset-0.9.0 \
		miniz_oxide-0.7.1 \
		mio-0.8.8 \
		nu-ansi-term-0.46.0 \
		num-traits-0.2.15 \
		num_cpus-1.16.0 \
		number_prefix-0.3.0 \
		object-0.32.0 \
		ocaml-boxroot-sys-0.2.0 \
		ocaml-interop-0.8.8 \
		ocaml-sys-0.22.3 \
		once_cell-1.18.0 \
		oorandom-11.1.3 \
		openvino-0.5.0 \
		openvino-finder-0.5.0 \
		openvino-sys-0.5.0 \
		overload-0.1.1 \
		paste-1.0.7 \
		percent-encoding-2.2.0 \
		pin-project-lite-0.2.9 \
		pin-utils-0.1.0 \
		plotters-0.3.1 \
		plotters-backend-0.3.2 \
		plotters-svg-0.3.1 \
		ppv-lite86-0.2.16 \
		pretty_env_logger-0.4.0 \
		pretty_env_logger-0.5.0 \
		proc-macro2-1.0.63 \
		proptest-1.0.0 \
		psm-0.1.18 \
		quick-error-1.2.3 \
		quick-error-2.0.1 \
		quote-1.0.29 \
		rand-0.8.5 \
		rand_chacha-0.3.1 \
		rand_core-0.6.3 \
		rand_xorshift-0.3.0 \
		rayon-1.5.3 \
		rayon-core-1.12.0 \
		redox_syscall-0.2.13 \
		redox_syscall-0.3.5 \
		redox_users-0.4.3 \
		regalloc2-0.9.3 \
		regex-1.9.1 \
		regex-automata-0.1.10 \
		regex-automata-0.3.3 \
		regex-syntax-0.6.25 \
		regex-syntax-0.7.4 \
		region-2.2.0 \
		ring-0.16.20 \
		rustc-demangle-0.1.21 \
		rustc-hash-1.1.0 \
		rustix-0.38.21 \
		rustls-0.21.6 \
		rustls-webpki-0.101.4 \
		rusty-fork-0.3.0 \
		ryu-1.0.9 \
		same-file-1.0.6 \
		scopeguard-1.1.0 \
		sct-0.7.0 \
		semver-1.0.17 \
		serde-1.0.188 \
		serde_derive-1.0.188 \
		serde_json-1.0.107 \
		sha2-0.10.2 \
		sharded-slab-0.1.4 \
		shellexpand-2.1.0 \
		shuffling-allocator-1.1.2 \
		signal-hook-registry-1.4.1 \
		similar-2.2.0 \
		slab-0.4.7 \
		slice-group-by-0.3.1 \
		smallvec-1.11.0 \
		socket2-0.4.9 \
		souper-ir-2.1.0 \
		spdx-0.10.1 \
		spin-0.5.2 \
		spin-0.9.4 \
		sptr-0.3.2 \
		stable_deref_trait-1.2.0 \
		static_assertions-1.1.0 \
		strsim-0.10.0 \
		symbolic_expressions-5.0.3 \
		syn-1.0.92 \
		syn-2.0.32 \
		system-interface-0.26.0 \
		target-lexicon-0.12.12 \
		tempfile-3.8.0 \
		termcolor-1.1.3 \
		terminal_size-0.1.17 \
		test-log-0.2.11 \
		thiserror-1.0.43 \
		thiserror-impl-1.0.43 \
		thread_local-1.1.4 \
		tinytemplate-1.2.1 \
		tinyvec-1.6.0 \
		tinyvec_macros-0.1.0 \
		tokio-1.29.1 \
		tokio-macros-2.1.0 \
		tokio-rustls-0.24.0 \
		tokio-util-0.7.4 \
		toml-0.5.9 \
		tracing-0.1.37 \
		tracing-attributes-0.1.26 \
		tracing-core-0.1.31 \
		tracing-log-0.1.3 \
		tracing-subscriber-0.3.17 \
		try-lock-0.2.4 \
		typenum-1.15.0 \
		unicode-bidi-0.3.8 \
		unicode-ident-1.0.8 \
		unicode-normalization-0.1.21 \
		unicode-segmentation-1.10.1 \
		unicode-width-0.1.9 \
		unicode-xid-0.2.3 \
		untrusted-0.7.1 \
		url-2.3.1 \
		utf8parse-0.2.1 \
		uuid-1.0.0 \
		v8-0.74.1 \
		valuable-0.1.0 \
		version_check-0.9.4 \
		wait-timeout-0.2.0 \
		walkdir-2.3.3 \
		want-0.3.0 \
		wasi-0.11.0+wasi-snapshot-preview1 \
		wasm-bindgen-0.2.87 \
		wasm-bindgen-backend-0.2.87 \
		wasm-bindgen-macro-0.2.87 \
		wasm-bindgen-macro-support-0.2.87 \
		wasm-bindgen-shared-0.2.87 \
		wasm-encoder-0.38.1 \
		wasm-metadata-0.10.14 \
		wasm-mutate-0.2.42 \
		wasm-smith-0.13.1 \
		wasmi-0.20.0 \
		wasmi_arena-0.1.0 \
		wasmi_core-0.5.0 \
		wasmparser-0.118.1 \
		wasmparser-nostd-0.91.0 \
		wasmprinter-0.2.75 \
		wast-35.0.2 \
		wast-69.0.1 \
		wat-1.0.82 \
		web-sys-0.3.57 \
		webpki-roots-0.25.2 \
		which-4.2.5 \
		winapi-0.3.9 \
		winapi-i686-pc-windows-gnu-0.4.0 \
		winapi-util-0.1.5 \
		winapi-x86_64-pc-windows-gnu-0.4.0 \
		windows-sys-0.48.0 \
		windows-targets-0.48.0 \
		windows_aarch64_gnullvm-0.48.0 \
		windows_aarch64_msvc-0.48.0 \
		windows_i686_gnu-0.48.0 \
		windows_i686_msvc-0.48.0 \
		windows_x86_64_gnu-0.48.0 \
		windows_x86_64_gnullvm-0.48.0 \
		windows_x86_64_msvc-0.48.0 \
		winx-0.36.1 \
		wit-bindgen-0.15.0 \
		wit-bindgen-core-0.15.0 \
		wit-bindgen-rust-0.15.0 \
		wit-bindgen-rust-macro-0.15.0 \
		wit-component-0.18.2 \
		wit-component-0.19.0 \
		wit-parser-0.13.0 \
		zstd-0.11.1+zstd.1.5.2 \
		zstd-safe-5.0.1+zstd.1.5.2 \
		zstd-sys-2.0.1+zstd.1.5.2

GH_TUPLE=	WebAssembly:wasm-c-api:c9d3128:wasm_c_api/crates/c-api/wasm-c-api \
		WebAssembly:WASI:0ba0c5e:WASI/crates/wasi-common/WASI \
		WebAssembly:wasi-nn:e2310b8:wasi_nn/crates/wasi-nn/spec \
		WebAssembly:testsuite:7ef86dd:testsuite/tests/spec_testsuite \
		WebAssembly:wasi-testsuite:09517e5:wasi_testsuite/tests/wasi_testsuite/wasi-common \
		WebAssembly:wasi-threads:e1893c0:wasi_threads/tests/wasi_testsuite/wasi-threads

PLIST_FILES=	include/doc-wasm.h \
		include/wasi.h \
		include/wasm.h \
		include/wasmtime.h \
		include/wasmtime/async.h \
		include/wasmtime/config.h \
		include/wasmtime/engine.h \
		include/wasmtime/error.h \
		include/wasmtime/extern.h \
		include/wasmtime/func.h \
		include/wasmtime/global.h \
		include/wasmtime/instance.h \
		include/wasmtime/linker.h \
		include/wasmtime/memory.h \
		include/wasmtime/module.h \
		include/wasmtime/store.h \
		include/wasmtime/table.h \
		include/wasmtime/trap.h \
		include/wasmtime/val.h \
		lib/libwasmtime.a \
		lib/libwasmtime.so

do-install:
	${MKDIR} ${STAGEDIR}${PREFIX}/include/wasmtime
	${INSTALL_DATA} ${WRKSRC}/crates/c-api/wasm-c-api/include/wasm.h ${STAGEDIR}${PREFIX}/include
	(cd ${WRKSRC}/crates/c-api/include && ${COPYTREE_SHARE} . ${STAGEDIR}${PREFIX}/include)
	${INSTALL_LIB} ${WRKDIR}/target/*-unknown-freebsd/release/libwasmtime.a ${STAGEDIR}${PREFIX}/lib
	${INSTALL_LIB} ${WRKDIR}/target/*-unknown-freebsd/release/libwasmtime.so ${STAGEDIR}${PREFIX}/lib

.include <bsd.port.mk>
