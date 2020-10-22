# $FreeBSD$

PORTNAME=	zen-dwm
DISTVERSION=	6.2
CATEGORIES=	x11-wm

MAINTAINER=	vulcan@wired.sh
COMMENT=	Custom fork of dwm

LICENSE=	MIT
LICENSE_FILE=	${WRKSRC}/../LICENSE

LIB_DEPENDS=	libfontconfig.so:x11-fonts/fontconfig
RUN_DEPENDS=	firacode>0:x11-fonts/firacode

USES=		xorg

USE_GITLAB=	yes
GL_ACCOUNT=	lcook
GL_PROJECT=	freebsd
GL_COMMIT=	c83a2b79876d975420cdfca0db55797b220d6eab

USE_XORG=	x11 xft xinerama

CONFLICTS=	dwm*

WRKSRC_SUBDIR=	dwm

PLIST_FILES=	bin/dwm

post-install:
	${STRIP_CMD} ${STAGEDIR}${PREFIX}/bin/dwm

.include <bsd.port.mk>
