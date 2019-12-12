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
RUN_DEPENDS=	iosevka>0:x11-fonts/iosevka

USES=		pkgconfig xorg

USE_GITLAB=	yes
GL_ACCOUNT=	lcook
GL_PROJECT=	freebsd
GL_COMMIT=	eabd03f929b8d24b832d28c77498390dffea1793

USE_XORG=	x11 xext xft

CONFLICTS=	sterm*

WRKSRC_SUBDIR=	st

PLIST_FILES=	bin/st

post-install:
	@${STRIP_CMD} ${STAGEDIR}${PREFIX}/bin/st

.include <bsd.port.mk>
