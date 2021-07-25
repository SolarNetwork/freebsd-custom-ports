# $FreeBSD$

PORTNAME=		vernemq
DISTVERSION=		1.12.1
PORTREVISION=		1
CATEGORIES=		net

MAINTAINER=	matt@solarnetwork.net
COMMENT=	A high-performance, distributed MQTT broker.

LICENSE=	APACHE20
LICENSE_FILE=	${WRKSRC}/LICENSE.txt

# TODO: use vernemq user/group
USERS=		www
GROUPS=		www

USES=		compiler:c++11-lang pkgconfig gmake perl5 ssl

MAKE_ENV=	PATH=${LOCALBASE}/lib/erlang22/bin:${PATH}
ALL_TARGET=	rel

MY_DEPENDS=	erlang-runtime22>0:lang/erlang-runtime22
BUILD_DEPENDS=	${MY_DEPENDS} \
		git>0:devel/git
RUN_DEPENDS=	${MY_DEPENDS}

LIB_DEPENDS=	libsnappy.so:archivers/snappy

USE_GITHUB=	YES
GH_ACCOUNT=	vernemq

USE_PERL5=	build

pre-build:
	cd ${WRKSRC} && \
	cp vars.config vars.generated && \
	echo "{app_version, \"${DISTVERSION}\"}.">> vars.generated

.include <bsd.port.mk>

