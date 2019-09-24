# $FreeBSD$

PORTNAME=	ansible-sysrc
DISTVERSION=	0.1
CATEGORIES=	sysutils
PKGNAMEPREFIX=	${PYTHON_PKGNAMEPREFIX}

MAINTAINER=	vulcan@wired.sh
COMMENT=	Ansible module to set sysvars in rc.conf

LICENSE=	MIT
LICENSE_FILE=	${WRKSRC}/LICENSE

RUN_DEPENDS=	${PYTHON_PKGNAMEPREFIX}ansible>0:sysutils/ansible@${PY_FLAVOR}

USE_GITHUB=	yes
GH_ACCOUNT=	dlundgren
GH_PROJECT=	ansible-freebsd-modules
GH_TAGNAME=	cf37fc1e16fc03852abc8933e7959b22b51a5c90

USES=		python
NO_ARCH=	yes
NO_BUILD=	yes

ANSIBLE_MOD=	$$(ansible-config-${PYTHON_VER} dump | ${EGREP} -o '${PREFIX}/share/${PYTHON_PKGNAMEPREFIX}ansible/plugins/modules')

PLIST_FILES=	$$(${ECHO_CMD} ${ANSIBLE_MOD} | ${SED} -e 's|${PREFIX}/||')/sysrc

do-install:
	${MKDIR} ${STAGEDIR}${ANSIBLE_MOD}
	${INSTALL_SCRIPT} ${WRKSRC}/library/sysrc ${STAGEDIR}${ANSIBLE_MOD}/sysrc

.include <bsd.port.mk>
