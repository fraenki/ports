PORTNAME=	nll
PORTVERSION=	20231210a
CATEGORIES=	lang
MASTER_SITES=	https://kozos.jp/nlux/archive/
DISTNAME=	nlux-alpha-20231210

MAINTAINER=	kozos@kozos.jp
COMMENT=	Simple language for programming learning
WWW=		https://kozos.jp/nll/

LICENSE=	ZLIB
LICENSE_FILE=	${WRKSRC}/LICENSE

FLAVORS=	default nosdl
FLAVOR?=	${FLAVORS:[1]}
nosdl_PKGNAMESUFFIX=	-nosdl

USES=		zip
WRKSRC=		${WRKDIR}/nlux/${PORTNAME}
MAKE_ARGS=	BUILD= ARCH= CCOMPILER=${CC}

PORTDOCS=	README.txt AUDIO.txt
PORTEXAMPLES=	*.nll

PLIST_FILES=	bin/${PORTNAME} man/man1/${PORTNAME}.1.gz

OPTIONS_DEFINE=	DOCS EXAMPLES NCURSES SYSTEM SYSCALL NETWORK
OPTIONS_DEFAULT?=	NCURSES SYSTEM LIBEDIT SDL2

OPTIONS_RADIO=	LINEEDIT
OPTIONS_RADIO_LINEEDIT=	LIBEDIT READLINE NLLINE GETLINE FGETS

LINEEDIT_DESC=	Line editor
NLLINE_DESC=	Internal readline compatible library
GETLINE_DESC=	Use getline
FGETS_DESC=	Use fgets()

NCURSES_USES=	ncurses

SYSTEM_DESC=	System function support
SYSCALL_DESC=	System call function support
NETWORK_DESC=	Network support

LIBEDIT_USES=	libedit
READLINE_USES=	readline

NCURSES_MAKE_ARGS=
NCURSES_MAKE_ARGS_OFF=	USE_CURSES=

SYSTEM_MAKE_ARGS=	USE_SYSTEM_FUNCTION=yes
SYSTEM_MAKE_ARGS_OFF=	USE_SYSTEM_FUNCTION=
SYSCALL_MAKE_ARGS=	USE_SYSCALL_FUNCTION=yes
SYSCALL_MAKE_ARGS_OFF=	USE_SYSCALL_FUNCTION=
NETWORK_MAKE_ARGS=	USE_NETWORK_FUNCTION=yes
NETWORK_MAKE_ARGS_OFF=	USE_NETWORK_FUNCTION=

LIBEDIT_MAKE_ARGS=	READLINE=libedit READLINEDIR=${LOCALBASE}
READLINE_MAKE_ARGS=	READLINE=readline READLINEDIR=${LOCALBASE}
NLLINE_MAKE_ARGS=	READLINE=nlline
GETLINE_MAKE_ARGS=	READLINE=getline
FGETS_MAKE_ARGS=	READLINE=fgets

.if ${FLAVOR} == default
OPTIONS_RADIO+=	SDLVER
OPTIONS_RADIO_SDLVER=	NOSDL SDL1 SDL2

SDLVER_DESC=	SDL version
NOSDL_DESC=	Disable SDL (limited graphic and audio function)
SDL1_DESC=	Use SDL 1.2
SDL2_DESC=	Use SDL 2.0

SDL1_USES=	sdl xorg
SDL1_USE=	XORG=x11 SDL=sdl
SDL2_USES=	sdl xorg
SDL2_USE=	XORG=x11 SDL=sdl2

NOSDL_MAKE_ARGS=	USE_SDL1= USE_SDL2=
NOSDL_MAKE_ARGS_OFF=
SDL1_MAKE_ARGS=	USE_SDL1=yes SDLDIR=${LOCALBASE}
SDL1_MAKE_ARGS_OFF=	USE_SDL1=
SDL2_MAKE_ARGS=	USE_SDL2=yes SDLDIR=${LOCALBASE}
SDL2_MAKE_ARGS_OFF=	USE_SDL2=
.endif

.if ${FLAVOR} == nosdl
COMMENT+=	(limited graphic and audio function)
MAKE_ARGS=	USE_SDL1= USE_SDL2=
.endif

post-install:
	${INSTALL_PROGRAM} ${WRKDIR}/nlux/bin/${PORTNAME} \
		${STAGEDIR}${PREFIX}/bin
	${INSTALL_MAN} ${WRKDIR}/nlux/man/man1/${PORTNAME}.1 \
		${STAGEDIR}${MANPREFIX}/man/man1

post-install-DOCS-on:
	${MKDIR} ${STAGEDIR}${DOCSDIR}
	${INSTALL_DATA} ${PORTDOCS:S/^/${WRKSRC}\//} ${STAGEDIR}${DOCSDIR}

post-install-EXAMPLES-on:
	${MKDIR} ${STAGEDIR}${EXAMPLESDIR}
	${INSTALL_DATA} ${PORTEXAMPLES:S/^/${WRKSRC}\/samples\//} ${STAGEDIR}${EXAMPLESDIR}
	${INSTALL_DATA} ${PORTEXAMPLES:S/^/${WRKSRC}\/samples\/graphic\//} ${STAGEDIR}${EXAMPLESDIR}
	${INSTALL_DATA} ${PORTEXAMPLES:S/^/${WRKSRC}\/samples\/audio\//} ${STAGEDIR}${EXAMPLESDIR}
	${INSTALL_DATA} ${PORTEXAMPLES:S/^/${WRKSRC}\/samples\/network\//} ${STAGEDIR}${EXAMPLESDIR}

.include <bsd.port.mk>
