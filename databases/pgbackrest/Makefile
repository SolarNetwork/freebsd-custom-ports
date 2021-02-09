# $FreeBSD$

PORTNAME=		pgbackrest
DISTVERSIONPREFIX=	release/
DISTVERSION=		2.32
PORTREVISION=		1
CATEGORIES=		databases

MAINTAINER=	matt@solarnetwork.net
COMMENT=	Reliable PostgreSQL Backup & Restore

LICENSE=	MIT
LICENSE_FILE=	${WRKSRC}/../LICENSE

USES=		compiler:c++11-lang gmake perl5 pkgconfig pgsql ssl
GNU_CONFIGURE=	yes
WRKSRC_SUBDIR=	src
ALL_TARGET=	pgbackrest

MY_DEPENDS=	git:devel/git \
		p5-YAML>=0:textproc/p5-YAML \
		rsync:net/rsync
LIB_DEPENDS=	liblz4.so:archivers/liblz4 \
		libpqxx.so:databases/postgresql-libpqxx \
		libxml2.so:textproc/libxml2 \
		libzstd.so:archivers/zstd
BUILD_DEPENDS=	${MY_DEPENDS}
RUN_DEPENDS=	${MY_DEPENDS}

USE_GITHUB=	YES
GH_ACCOUNT=	pgbackrest

PLIST_SUB=	PORTVERSION=${PORTVERSION}
SUB_LIST=	PORTVERSION=${PORTVERSION}

WANT_PGSQL=	server

.include <bsd.port.mk>
