PORTNAME=		aggs_for_vecs
DISTVERSION=		1.3.0
DISTVERSIONPREFIX=	v
PORTREVISION=		1
CATEGORIES=		databases
PKGNAMEPREFIX=		postgresql-

MAINTAINER=	matt@solarnetwork.net
COMMENT=	Aggregate functions for array inputs.

LICENSE=	MIT
LICENSE_FILE=	${WRKSRC}/LICENSE

USES=		gmake pgsql

USE_GITHUB=	YES
GH_ACCOUNT=	pjungwir

WANT_PGSQL=	server

post-install:
	${STRIP_CMD} ${STAGEDIR}${PREFIX}/lib/postgresql/aggs_for_vecs.so

.include <bsd.port.mk>
