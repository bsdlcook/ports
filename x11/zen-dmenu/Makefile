# $FreeBSD$

PORTNAME=	zen-dmenu
DISTVERSION=	6.2
CATEGORIES=	x11

MAINTAINER=	vulcan@wired.sh
COMMENT=	Custom fork of dmenu

LICENSE=	MIT
LICENSE_FILE=	${WRKSRC}/../LICENSE

LIB_DEPENDS=	libfontconfig.so:x11-fonts/fontconfig
RUN_DEPENDS=	iosevka:x11-fonts/iosevka

USES=		xorg

USE_GITLAB=	yes
GL_ACCOUNT=	lcook
GL_PROJECT=	freebsd
GL_COMMIT=	2ab778ece27a781a5d2d9198e5b4611067880b73		

USE_XORG=	x11 xft

CONFLICTS=	dmenu*

WRKSRC_SUBDIR=	dmenu

PLIST_FILES=	bin/dmenu

post-install:
	${STRIP_CMD} ${STAGEDIR}${PREFIX}/bin/dmenu

.include <bsd.port.mk>
