# $FreeBSD$

PORTNAME=	goshare
DISTVERSION=	0.1
CATEGORIES=	sysutils

MAINTAINER=	vulcan@wired.sh
COMMENT=	Command-line utility to easily upload screeshots/files over sftp

LICENSE=	BSD3CLAUSE

RUN_DEPENDS=	xclipboard:x11/xclipboard \
		maim:graphics/maim

USES=		compiler go:modules

USE_GITLAB=	yes
GL_ACCOUNT=	nihilism
GL_COMMIT=	bfa12b3392a224bd7daca18703a604f179b7fdb0

USE_GITHUB=	nodefault
GH_TUPLE=	\
		atotto:clipboard:v0.1.2:atotto_clipboard/src/github.com/atotto/clipboard \
		golang:crypto:9756ffdc2472:golang_crypto/src/golang.org/x/crypto \
		golang:sys:97732733099d:golang_sys/src/golang.org/x/sys \
		jessevdk:go-flags:v1.4.0:jessevdk_go_flags/src/github.com/jessevdk/go-flags \
		kr:fs:v0.1.0:kr_fs/src/github.com/kr/fs \
		pkg:errors:v0.8.1:pkg_errors/src/github.com/pkg/errors \
		pkg:sftp:v1.10.1:pkg_sftp/src/github.com/pkg/sftp

PLIST_FILES=	bin/goshare
PORTEXAMPLES=	*

OPTIONS_DEFINE=	EXAMPLES

do-build:
	cd ${WRKSRC} && \
		${SETENV} GOCACHE=${WRKSRC}/cache CGO_ENABLED=0 GOPATH=${WRKSRC} \
		go build -o ${PORTNAME}

do-install:
	${INSTALL_PROGRAM} ${WRKSRC}/${PORTNAME} ${STAGEDIR}${PREFIX}/bin/${PORTNAME}

do-install-EXAMPLES-on:
	@${MKDIR} ${STAGEDIR}${EXAMPLESDIR}
	${INSTALL_DATA} ${WRKSRC}/settings.json.example ${STAGEDIR}${EXAMPLESDIR}

.include <bsd.port.mk>
