# $FreeBSD$

PORTNAME=	zen-dwm
DISTVERSION=	6.2
CATEGORIES=	x11-wm

MAINTAINER=	vulcan@wired.sh
COMMENT=	Custom fork of dwm

LICENSE=	MIT
LICENSE_FILE=	${WRKSRC}/../LICENSE

LIB_DEPENDS=	libfontconfig.so:x11-fonts/fontconfig
RUN_DEPENDS=	iosevka>0:x11-fonts/iosevka

USES=		xorg

USE_GITLAB=	yes
GL_ACCOUNT=	lcook
GL_PROJECT=	freebsd
GL_COMMIT=	eabd03f929b8d24b832d28c77498390dffea1793	

USE_XORG=	x11 xft

CONFLICTS=	dwm*

WRKSRC_SUBDIR=	dwm

PLIST_FILES=	bin/dwm

post-install:
	${STRIP_CMD} ${STAGEDIR}${PREFIX}/bin/dwm

.include <bsd.port.mk>
