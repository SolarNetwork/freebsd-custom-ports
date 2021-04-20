# $FreeBSD$

PORTNAME=		pgbackrest
DISTVERSIONPREFIX=	release/
DISTVERSION=		2.33
PORTREVISION=		1
CATEGORIES=		databases

MAINTAINER=	matt@solarnetwork.net
COMMENT=	Reliable PostgreSQL Backup & Restore

LICENSE=	MIT
LICENSE_FILE=	${WRKSRC}/../LICENSE

USES=		compiler:c++11-lang gmake pkgconfig pgsql ssl
GNU_CONFIGURE=	yes
WRKSRC_SUBDIR=	src
ALL_TARGET=	pgbackrest
CONFIGURE_ARGS+=--with-configdir=/usr/local/etc

LIB_DEPENDS=	liblz4.so:archivers/liblz4 \
		libpqxx.so:databases/postgresql-libpqxx \
		libxml2.so:textproc/libxml2

USE_GITHUB=	YES
GH_ACCOUNT=	pgbackrest

WANT_PGSQL=	server

OPTIONS_DEFINE+=	ZSTD
ZSTD_DESC=		Build with zstd compression support
ZSTD_LIB_DEPENDS=	libzstd.so:archivers/zstd

.include <bsd.port.mk>

