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

USES=		python

USE_GITHUB=	yes
GH_ACCOUNT=	fractalcells
GH_PROJECT=	ansible-iocage
GH_TAGNAME=	b8114ae6670fefddf0612801fd16030595c24bb2

NO_ARCH=	yes
NO_BUILD=	yes

ANSIBLE_MOD=	$$(ansible-config-${PYTHON_VER} dump | ${EGREP} -o '${PREFIX}/share/${PYTHON_PKGNAMEPREFIX}ansible/plugins/modules')

PLIST_FILES=	$$(${ECHO_CMD} ${ANSIBLE_MOD} | ${SED} -e 's|${PREFIX}/||')/iocage

do-install:
	${MKDIR} ${STAGEDIR}${ANSIBLE_MOD}
	${INSTALL_SCRIPT} ${WRKSRC}/iocage ${STAGEDIR}${ANSIBLE_MOD}/iocage

.include <bsd.port.mk>
