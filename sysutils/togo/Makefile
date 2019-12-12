# $FreeBSD$

PORTNAME=	togo
DISTVERSION=	0.2.1
CATEGORIES=	sysutils

MAINTAINER=	vulcan@wired.sh
COMMENT=	Command-line utility to easily review source code annotations

LICENSE=	BSD3CLAUSE
LICENSE_FILE=	${WRKSRC}/LICENSE

USES=		go:modules

USE_GITHUB=	nodefault
GH_TUPLE=	golang:sys:a9d3bda3a223:golang_sys/vendor/golang.org/x/sys \
		mattn:go-colorable:v0.1.2:mattn_go_colorable/vendor/github.com/mattn/go-colorable \
		mattn:go-isatty:v0.0.8:mattn_go_isatty/vendor/github.com/mattn/go-isatty \
		mgutz:ansi:9520e82c474b:mgutz_ansi/vendor/github.com/mgutz/ansi

USE_GITLAB=	yes
GL_ACCOUNT=	lcook
GL_COMMIT=	a5c92568bc118170388c09e3331222f0d4e9c23a

PLIST_FILES=	bin/togo

.include <bsd.port.mk>
