# $FreeBSD$

PORTNAME=	dspdfviewer
PORTVERSION=	1.15.1
CATEGORIES=	graphics

MAINTAINER=	santhosh.raju@gmail.com
COMMENT=	Dual-Screen PDF Viewer for latex-beamer

LICENSE=	GPLv2
LICENSE_FILE=	${WRKSRC}/COPYING

USE_QT5=	buildtools_build core gui qmake_build linguisttools widgets xml
LIB_DEPENDS=	libpoppler-qt5.so:graphics/poppler-qt5 \
		libboost_program_options.so:devel/boost-libs

BUILD_WRKSRC=		${WRKSRC}/build
CONFIGURE_WRKSRC=	${WRKSRC}/build
INSTALL_WRKSRC= 	${WRKSRC}/build

USES=		cmake pkgconfig
CMAKE_ARGS=	-DPOPPLER_LIBRARIES=${LOCALBASE}/lib/libpoppler-qt5.so -DBuildTests=OFF
USE_LDCONFIG=	yes

CMAKE_VERBOSE=	yes

USE_GITHUB=	yes
GH_ACCOUNT=	dannyedel
GH_PROJECT=	dspdfviewer
GH_TAGNAME=	v1.15.1

.include <bsd.port.mk>
