# $FreeBSD$

PORTNAME=	zen-sterm
DISTVERSION=	0.8.1
CATEGORIES=	x11

MAINTAINER=	vulcan@wired.sh
COMMENT=	Custom fork of st

LICENSE=	MIT
LICENSE_FILE=	${WRKSRC}/../LICENSE

LIB_DEPENDS=	libfontconfig.so:x11-fonts/fontconfig \
		libfreetype.so:print/freetype2
RUN_DEENDS=	victor-mono-ttf:x11-fonts/victor-mono-ttf

USES=		pkgconfig xorg

USE_GITLAB=	yes
GL_ACCOUNT=	lcook
GL_PROJECT=	freebsd
GL_COMMIT=	2b26b13f8577c301378ad9a139dad9681cd8b2bb
USE_XORG=	x11 xext xft

CONFLICTS=	sterm*

WRKSRC_SUBDIR=	st

PLIST_FILES=	bin/st

post-install:
	@${STRIP_CMD} ${STAGEDIR}${PREFIX}/bin/st

.include <bsd.port.mk>
