# $FreeBSD$

PORTNAME=		vernemq
DISTVERSION=		1.12.1
PORTREVISION=		1
CATEGORIES=		net

MAINTAINER=	matt@solarnetwork.net
COMMENT=	A high-performance, distributed MQTT broker.

LICENSE=	APACHE20
LICENSE_FILE=	${WRKSRC}/LICENSE.txt

USES=		compiler:c++11-lang gmake pkgconfig perl5 ssl
ALL_TARGET=	rel

MY_DEPENDS=	erlang-runtime22>0:lang/erlang-runtime22
BUILD_DEPENDS=	${MY_DEPENDS} \
		git>0:devel/git
RUN_DEPENDS=	${MY_DEPENDS}

LIB_DEPENDS=	libsnappy.so:archivers/snappy

USE_GITHUB=	YES
GH_ACCOUNT=	vernemq

USE_PERL5=	build

.include <bsd.port.mk>

