PORTNAME=	html2text
PORTVERSION=	1.3.2a
PORTREVISION=	2
PORTEPOCH=	1
CATEGORIES=	textproc
MASTER_SITES=	SUNSITE/apps/www/converters \
		http://www.mbayer.de/html2text/downloads/

MAINTAINER=	bapt@FreeBSD.org
COMMENT=	Converts HTML documents into plain text
WWW=		http://www.mbayer.de/html2text/

LICENSE=	GPLv2+
LICENSE_FILE=	${WRKSRC}/COPYING

HAS_CONFIGURE=	yes
USE_CXXSTD=	gnu++98

PORTDOCS=	CHANGES CREDITS KNOWN_BUGS README TODO
PLIST_FILES=	bin/html2text share/man/man1/html2text.1.gz share/man/man5/html2textrc.5.gz

CONFLICTS=	py*-html2text py*-html2text2018 # bin/html2text

PORTSCOUT=	skipb:0 skipv:1.3.2

OPTIONS_DEFINE=	DOCS

post-patch:
	@${REINPLACE_CMD} -e '/echo=/s/ -e//' ${WRKSRC}/configure
.for fle in Makefile.in libstd/Makefile.in
	@${REINPLACE_CMD} -e '/^DEBUG/s/^/#/; \
		 /^CXXFLAGS/s/=/+=/' ${WRKSRC}/${fle}
.endfor
.for fle in Area.h HTMLControl.h Properties.h format.h
	@${REINPLACE_CMD} -e 's/<istream>/<iostream>/' ${WRKSRC}/${fle}
.endfor

do-install:
	${INSTALL_PROGRAM} ${WRKSRC}/html2text ${STAGEDIR}${PREFIX}/bin
	${INSTALL_MAN} ${WRKSRC}/html2text.1.gz ${STAGEDIR}${PREFIX}/share/man/man1
	${INSTALL_MAN} ${WRKSRC}/html2textrc.5.gz ${STAGEDIR}${PREFIX}/share/man/man5

do-install-DOCS-on:
	@${MKDIR} ${STAGEDIR}${DOCSDIR}
.for f in ${PORTDOCS}
	${INSTALL_DATA} ${WRKSRC}/${f} ${STAGEDIR}${DOCSDIR}
.endfor

.include <bsd.port.mk>
