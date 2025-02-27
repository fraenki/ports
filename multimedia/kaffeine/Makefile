PORTNAME=	kaffeine
DISTVERSION=	2.0.18
PORTREVISION=	5
CATEGORIES=	multimedia kde
MASTER_SITES=	KDE/stable/${PORTNAME}

MAINTAINER=	kde@FreeBSD.org
COMMENT=	Multimedia player based on KDE and VLC
WWW=		https://www.kde.org/applications/multimedia/kaffeine/

LICENSE=	GPLv2+
LICENSE_FILE=	${WRKSRC}/COPYING

BUILD_DEPENDS=	v4l_compat>=1.18.0:multimedia/v4l_compat
LIB_DEPENDS=	libvlc.so:multimedia/vlc \
		libdvbv5.so:multimedia/libv4l

USES=		cmake compiler:c++11-lang cpe desktop-file-utils gettext \
		pkgconfig kde:5 qt:5 tar:xz xorg
USE_KDE=	auth bookmarks codecs completion config configwidgets \
		coreaddons i18n itemviews kio solid dbusaddons jobwidgets \
		phonon service widgetsaddons windowsystem xmlgui \
		doctools:build ecm:build
USE_QT=		concurrent core dbus gui network sql svg x11extras xml \
		widgets qmake:build buildtools:build
USE_XORG=	x11 xscrnsaver

CPE_VENDOR=	kaffeine
CPE_PRODUCT=	kaffeine_player

post-patch:
	@${RM} -r ${WRKSRC}/include

post-build:
	# Cleanup translated manpages, we don't want them
	${RM} ${STAGEDIR}/man/{ca,id,it,nl,pt,pt_BR,sv,uk}/man1/kaffeine.1.gz

.include <bsd.port.mk>
