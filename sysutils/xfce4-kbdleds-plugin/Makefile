# $FreeBSD$

PORTNAME=	kbdleds-plugin
DISTVERSION=	0.0.6
CATEGORIES=	sysutils xfce
MASTER_SITES=	https://git.xfce.org/archive/xfce4-${PORTNAME}/snapshot/
PKGNAMEPREFIX=	xfce4-
DISTNAME=	${PKGNAMEPREFIX}${PORTNAME}-${PORTVERSION}
DIST_SUBDIR=	xfce4

MAINTAINER=	xfce@FreeBSD.org
COMMENT=	Xfce keyboard LEDs panel plugin

LICENSE=	GPLv2
LICENSE_FILE=	${WRKSRC}/COPYING

BROKEN=		Fails to compile with XFCE 4.16
DEPRECATED=	Unsupported upstream, cannot work with XFCE 4.16
EXPIRATION_DATE=	2021-01-31

LIB_DEPENDS=	libfontconfig.so:x11-fonts/fontconfig \
		libfreetype.so:print/freetype2

USES=		compiler:c11 gettext-tools gmake gnome libtool pkgconfig \
		xfce xorg
GNU_CONFIGURE=	yes
USE_GNOME=	cairo gdkpixbuf2 glib20 gtk20 intltool pango
USE_XORG=	ice sm x11
USE_XFCE=	panel
INSTALLS_ICONS=	yes

OPTIONS_DEFINE=		NLS
OPTIONS_SUB=		yes

NLS_CONFIGURE_ENABLE=	nls
NLS_USES=		gettext-runtime

.include <bsd.port.mk>
