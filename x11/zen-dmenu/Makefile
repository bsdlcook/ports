# $FreeBSD$

PORTNAME=	zen-dmenu
DISTVERSION=	4.9
CATEGORIES=	x11

MAINTAINER=	vulcan@wired.sh
COMMENT=	Custom fork of dmenu

LICENSE=	MIT
LICENSE_FILE=	${WRKSRC}/../LICENSE

LIB_DEPENDS=	libfontconfig.so:x11-fonts/fontconfig
RUN_DEPENDS=	iosevka>0:x11-fonts/iosevka

USES=		xorg

USE_GITLAB=	yes
GL_ACCOUNT=	lcook
GL_PROJECT=	freebsd
GL_COMMIT=	a961b2036022ca5d578dd53a3d9fb2b49dcf1a19

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
