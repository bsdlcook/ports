# $FreeBSD$

PORTNAME=	zen-dwm
DISTVERSION=	6.2
CATEGORIES=	x11-wm

MAINTAINER=	vulcan@wired.sh
COMMENT=	Custom fork of dwm

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

CONFLICTS=	dwm*

WRKSRC_SUBDIR=	dwm

PLIST_FILES=	bin/dwm

post-install:
	${STRIP_CMD} ${STAGEDIR}${PREFIX}/bin/dwm

.include <bsd.port.mk>
