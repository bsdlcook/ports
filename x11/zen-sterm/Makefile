# $FreeBSD$

PORTNAME=	zen-sterm
DISTVERSION=	0.8.4
CATEGORIES=	x11

MAINTAINER=	vulcan@wired.sh
COMMENT=	Custom fork of st

LICENSE=	MIT
LICENSE_FILE=	${WRKSRC}/../LICENSE

LIB_DEPENDS=	libfontconfig.so:x11-fonts/fontconfig \
		libfreetype.so:print/freetype2 \
		libharfbuzz.so:print/harfbuzz
RUN_DEPENDS=	firacode:x11-fonts/firacode

USES=		pkgconfig xorg

USE_GITLAB=	yes
GL_ACCOUNT=	lcook
GL_PROJECT=	freebsd
GL_COMMIT=	c83a2b79876d975420cdfca0db55797b220d6eab
USE_XORG=	x11 xext xft

CONFLICTS=	sterm*

WRKSRC_SUBDIR=	st

PLIST_FILES=	bin/st

post-install:
	@${STRIP_CMD} ${STAGEDIR}${PREFIX}/bin/st

.include <bsd.port.mk>
