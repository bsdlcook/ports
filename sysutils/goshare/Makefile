# $FreeBSD$

PORTNAME=	goshare
DISTVERSIONPREFIX=	v
DISTVERSION=	0.4
CATEGORIES=	sysutils

MAINTAINER=	vulcan@wired.sh
COMMENT=	Command-line utility to easily upload screeshots/files over sftp

LICENSE=	BSD3CLAUSE
LICENSE_FILE=	${WRKSRC}/LICENSE

RUN_DEPENDS=	maim:graphics/maim \
		xclipboard:x11/xclipboard

USES=		go:modules

USE_GITHUB=	nodefault
GH_TUPLE=	atotto:clipboard:v0.1.2:atotto_clipboard/vendor/github.com/atotto/clipboard \
		golang:crypto:530e935923ad:golang_crypto/vendor/golang.org/x/crypto \
		golang:sys:59e60aa80a0c:golang_sys/vendor/golang.org/x/sys \
		jessevdk:go-flags:v1.4.0:jessevdk_go_flags/vendor/github.com/jessevdk/go-flags \
		kr:fs:v0.1.0:kr_fs/vendor/github.com/kr/fs \
		pkg:errors:v0.9.1:pkg_errors/vendor/github.com/pkg/errors \
		pkg:sftp:v1.11.0:pkg_sftp/vendor/github.com/pkg/sftp

USE_GITLAB=	yes
GL_ACCOUNT=	lcook
GL_COMMIT=	b632a3cfa75ad3ec5d719d83ccda339ae922e490

SUB_FILES=	pkg-message
PLIST_FILES=	bin/goshare

PORTEXAMPLES=	settings.json

OPTIONS_DEFINE=		EXAMPLES
OPTIONS_DEFAULT=	EXAMPLES

EXAMPLES_DESC=	Install example goshare configuration file

post-install-EXAMPLES-on:
	@${MKDIR} ${STAGEDIR}${EXAMPLESDIR}
	${INSTALL_DATA} ${WRKSRC}/${PORTEXAMPLES} ${STAGEDIR}${EXAMPLESDIR}

.include <bsd.port.mk>
