# $FreeBSD$

PORTNAME=	ansible-iocage
DISTVERSION=	0.1
CATEGORIES=	sysutils
PKGNAMEPREFIX=	${PYTHON_PKGNAMEPREFIX}

MAINTAINER=	vulcan@wired.sh
COMMENT=	Ansible module for iocage

LICENSE=	MIT
LICENSE_FILE=	${WRKSRC}/LICENSE

RUN_DEPENDS=	${PYTHON_PKGNAMEPREFIX}ansible>0:sysutils/ansible@${PY_FLAVOR}

USES=		python shebangfix
SHEBANG_FILES=	iocage

USE_GITHUB=	yes
GH_ACCOUNT=	fractalcells
GH_TAGNAME=	d6db8a0eb895c3d83da964fcbe8acc0e5e2ccfeb

NO_ARCH=	yes
NO_BUILD=	yes

ANSIBLE_MOD=	share/${PYTHON_PKGNAMEPREFIX}ansible/plugins/modules

PLIST_FILES=	${ANSIBLE_MOD}/iocage

do-install:
	${MKDIR} ${STAGEDIR}${PREFIX}/${ANSIBLE_MOD}
	${INSTALL_SCRIPT} ${WRKSRC}/iocage \
		${STAGEDIR}${PREFIX}/${ANSIBLE_MOD}/iocage

.include <bsd.port.mk>
