# $FreeBSD$

PORTNAME=	ansible-kld
DISTVERSION=	0.1
CATEGORIES=	sysutils
PKGNAMEPREFIX=	${PYTHON_PKGNAMEPREFIX}

MAINTAINER=	vulcan@wired.sh
COMMENT=	Ansible module to load kernel modules or update /boot/loader.conf

LICENSE=	MIT
LICENSE_FILE=	${WRKSRC}/LICENSE

RUN_DEPENDS=	${PYTHON_PKGNAMEPREFIX}ansible>0:sysutils/ansible@${PY_FLAVOR}

USES=		python shebangfix
USE_GITHUB=	yes
GH_ACCOUNT=	dlundgren
GH_PROJECT=	ansible-freebsd-modules
GH_TAGNAME=	cf37fc1e16fc03852abc8933e7959b22b51a5c90

SHEBANG_FILES=	library/kld

NO_ARCH=	yes
NO_BUILD=	yes

PLIST_FILES=	${ANSIBLE_MOD}/kld

ANSIBLE_MOD=	share/${PYTHON_PKGNAMEPREFIX}ansible/plugins/modules

do-install:
	${MKDIR} ${STAGEDIR}${PREFIX}/${ANSIBLE_MOD}
	${INSTALL_SCRIPT} ${WRKSRC}/library/kld \
		${STAGEDIR}${PREFIX}/${ANSIBLE_MOD}/kld

.include <bsd.port.mk>
