# $FreeBSD$

PORTNAME=	goshare
DISTVERSION=	0.2
CATEGORIES=	sysutils

MAINTAINER=	vulcan@wired.sh
COMMENT=	Command-line utility to easily upload screeshots/files over sftp

LICENSE=	BSD3CLAUSE
LICENSE_FILE=	${WRKSRC}/LICENSE

RUN_DEPENDS=	maim:graphics/maim \
		xclipboard:x11/xclipboard

USES=		go:modules

USE_GITLAB=	yes
GL_ACCOUNT=	nihilism
GL_COMMIT=	308f73934318176baf8b74d0a7bd0fb66a540af6

USE_GITHUB=	nodefault
GH_TUPLE=	atotto:clipboard:v0.1.2:atotto_clipboard/vendor/github.com/atotto/clipboard \
		golang:crypto:9756ffdc2472:golang_crypto/vendor/golang.org/x/crypto \
		golang:sys:97732733099d:golang_sys/vendor/golang.org/x/sys \
		jessevdk:go-flags:v1.4.0:jessevdk_go_flags/vendor/github.com/jessevdk/go-flags \
		kr:fs:v0.1.0:kr_fs/vendor/github.com/kr/fs \
		pkg:errors:v0.8.1:pkg_errors/vendor/github.com/pkg/errors \
		pkg:sftp:v1.10.1:pkg_sftp/vendor/github.com/pkg/sftp

SUB_FILES=	pkg-message

PLIST_FILES=	bin/goshare
PORTEXAMPLES=	settings.json

OPTIONS_DEFINE=	EXAMPLES

EXAMPLES_DESC=	Install example goshare configuration file

post-install-EXAMPLES-on:
	@${MKDIR} ${STAGEDIR}${EXAMPLESDIR}
	${INSTALL_DATA} ${WRKSRC}/${PORTEXAMPLES} \
		${STAGEDIR}${EXAMPLESDIR}

.include <bsd.port.mk>
