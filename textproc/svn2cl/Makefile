PORTNAME=	svn2cl
PORTVERSION=	0.14
PORTREVISION=	1
CATEGORIES=	textproc
MASTER_SITES=	http://arthurdejong.org/svn2cl/

MAINTAINER=	ports@FreeBSD.org
COMMENT=	Subversion ChangeLog generator
WWW=		https://arthurdejong.org/svn2cl/

RUN_DEPENDS=	xsltproc:textproc/libxslt \
		svn:devel/subversion

NO_BUILD=	yes
PORTDOCS=	ChangeLog NEWS README TODO
DATAFILES=	authors.xml svn2cl.xsl svn2html.css svn2html.xsl

OPTIONS_DEFINE=	DOCS

post-patch:
	@${REINPLACE_CMD} -e 's|XSL="$$dir|XSL="${DATADIR}|' ${WRKSRC}/${PORTNAME}.sh

do-install:
	${INSTALL_SCRIPT} ${WRKSRC}/${PORTNAME}.sh ${STAGEDIR}${PREFIX}/bin/${PORTNAME}
	${INSTALL_MAN} ${WRKSRC}/svn2cl.1 ${STAGEDIR}${PREFIX}/share/man/man1
	@${MKDIR} ${STAGEDIR}${DATADIR}
.for i in ${DATAFILES}
	${INSTALL_DATA} ${WRKSRC}/${i} ${STAGEDIR}${DATADIR}
.endfor
	@${MKDIR} ${STAGEDIR}${DOCSDIR}
.for i in ${PORTDOCS}
	${INSTALL_DATA} ${WRKSRC}/${i} ${STAGEDIR}${DOCSDIR}
.endfor

.include <bsd.port.mk>
