# $FreeBSD$

PORTNAME=	togo
DISTVERSION=	0.2.1
CATEGORIES=	sysutils
MASTER_SITES=	https://gitlab.com/nihilism/togo/

MAINTAINER=	vulcan@wired.sh
COMMENT=	Command-line utility to review annotations from sourcefiles

LICENSE=	BSD3CLAUSE

BUILD_DEPENDS=	go:lang/go

USE_GITLAB=	yes

GL_ACCOUNT=	nihilism
GL_COMMIT=	e96a6a94c7ef86da34b311fe7ef170682abd8142

PLIST_FILES=	bin/togo

do-build:
	cd ${WRKSRC} && \
		${SETENV} GOCACHE=${WRKSRC}/cache CGO_ENABLED=0 GOPATH=${WRKSRC} \
		go build -o ${PORTNAME}

do-install:
	${INSTALL_PROGRAM} ${WRKSRC}/${PORTNAME} ${STAGEDIR}${PREFIX}/bin/${PORTNAME}

.include <bsd.port.mk>
