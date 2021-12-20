PORTNAME=	aggs_for_vecs
DISTVERSION=	1.3.0
PORTREVISION=	1
CATEGORIES=	databases
PKGNAMEPREFIX=	postgresql-

MAINTAINER=	matt@solarnetwork.net
COMMENT=	Aggregate functions for array inputs.

LICENSE=	MIT
LICENSE_FILE=	${WRKSRC}/LICENSE

USES=		gmake pgsql

USE_GITHUB=	YES
GH_ACCOUNT=	SolarNetwork
GH_TAGNAME=	b0681580b042f9790de95a4eb04cb3b8217e1e01

WANT_PGSQL=	server

post-install:
	${STRIP_CMD} ${STAGEDIR}${PREFIX}/lib/postgresql/aggs_for_vecs.so

.include <bsd.port.mk>
