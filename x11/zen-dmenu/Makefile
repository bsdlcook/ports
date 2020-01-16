# $FreeBSD$

PORTNAME=	zen-dmenu
DISTVERSION=	4.9
CATEGORIES=	x11

MAINTAINER=	vulcan@wired.sh
COMMENT=	Custom fork of dmenu

LICENSE=	MIT
LICENSE_FILE=	${WRKSRC}/../LICENSE

LIB_DEPENDS=	libfontconfig.so:x11-fonts/fontconfig
RUN_DEPENDS=	victor-mono-ttf>0:x11-fonts/victor-mono-ttf

USES=		xorg

USE_GITLAB=	yes
GL_ACCOUNT=	lcook
GL_PROJECT=	freebsd
GL_COMMIT=	2b26b13f8577c301378ad9a139dad9681cd8b2bb

USE_XORG=	x11 xft xinerama

CONFLICTS=	dmenu*

WRKSRC_SUBDIR=	dmenu

PLIST_FILES=	bin/dmenu

post-install:
	${STRIP_CMD} ${STAGEDIR}${PREFIX}/bin/dmenu

.include <bsd.port.mk>
