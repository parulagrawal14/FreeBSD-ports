# Created by: gahr
# $FreeBSD$

PORTNAME=	markasjunk2
PORTVERSION=	1.11.2
CATEGORIES=	mail
PKGNAMEPREFIX=	roundcube-
PKGNAMESUFFIX=	${PHP_PKGNAMESUFFIX}

MAINTAINER=	gahr@FreeBSD.org
COMMENT=	Roundcube mark-as-junk / mark-as-not-junk plugin

LICENSE=	GPLv3

BUILD_DEPENDS=	roundcube${PHP_PKGNAMESUFFIX}>=1.3.6:mail/roundcube@${PHP_FLAVOR}
RUN_DEPENDS=	roundcube${PHP_PKGNAMESUFFIX}>=1.3.6:mail/roundcube@${PHP_FLAVOR}

USES=	php:flavors
USE_GITHUB=	yes
GH_ACCOUNT=	johndoh
GH_PROJECT=	roundcube-markasjunk2

NO_BUILD=	yes
NO_ARCH=	yes

WWWDIR=		${PREFIX}/www/roundcube/plugins/markasjunk2

do-install:
	${MKDIR} ${STAGEDIR}${WWWDIR}
	cd ${WRKSRC} && ${PAX} -r -w . ${STAGEDIR}${WWWDIR}

.include <bsd.port.mk>
