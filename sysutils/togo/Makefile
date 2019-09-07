# $FreeBSD$

PORTNAME=	togo
DISTVERSION=	0.2.1
CATEGORIES=	sysutils

MAINTAINER=	vulcan@wired.sh
COMMENT=	Command-line utility to review annotations from sourcefiles

LICENSE=	BSD3CLAUSE

USES=		compiler go:modules

USE_GITLAB=	yes
GL_ACCOUNT=	nihilism
GL_COMMIT= 	17e9a565963a737fbc85dce131d54510bab0d7f9

USE_GITHUB=	nodefault
GH_TUPLE=	\
		golang:sys:a9d3bda3a223:golang_sys/src/golang.org/x/sys \
		mattn:go-colorable:v0.1.2:mattn_go_colorable/src/github.com/mattn/go-colorable \
		mattn:go-isatty:v0.0.8:mattn_go_isatty/src/github.com/mattn/go-isatty \
		mgutz:ansi:9520e82c474b:mgutz_ansi/src/github.com/mgutz/ansi

PLIST_FILES=	bin/${PORTNAME}

do-build:
	cd ${WRKSRC} && \
		${SETENV} GOCACHE=${WRKSRC}/cache CGO_ENABLED=0 GOPATH=${WRKSRC} \
		go build -o ${PORTNAME}

do-install:
	${INSTALL_PROGRAM} ${WRKSRC}/${PORTNAME} ${STAGEDIR}${PREFIX}/bin/${PORTNAME}

.include <bsd.port.mk>
