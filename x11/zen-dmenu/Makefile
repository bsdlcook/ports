# $FreeBSD$

PORTNAME=	zen-dmenu
DISTVERSION=	4.9
CATEGORIES=	x11

MAINTAINER=	vulcan@wired.sh
COMMENT=	Custom fork of dmenu

LICENSE=	MIT
LICENSE_FILE=	${WRKSRC}/../LICENSE

LIB_DEPENDS=	libfontconfig.so:x11-fonts/fontconfig
RUN_DEPENDS=	firacode>0:x11-fonts/firacode

USES=		xorg

USE_GITLAB=	yes
GL_ACCOUNT=	lcook
GL_PROJECT=	freebsd
GL_COMMIT=	12232a628c4ce1358af699889f813ce040b2be91

USE_XORG=	x11 xft xinerama

CONFLICTS=	dmenu*

WRKSRC_SUBDIR=	dmenu

PLIST_FILES=	bin/dmenu \
		bin/dmenu_path \
		bin/dmenu_run \
		bin/stest

post-install:
	${STRIP_CMD} ${STAGEDIR}${PREFIX}/bin/dmenu

.include <bsd.port.mk>
