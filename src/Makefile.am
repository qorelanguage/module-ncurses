if COND_SINGLE_COMPILATION_UNIT
NCURSES_SOURCES = single-compilation-unit.cc
else
NCURSES_SOURCES = ncurses.cc QC_Window.cc QC_Panel.cc
endif

lib_LTLIBRARIES = ncurses.la
ncurses_la_SOURCES = $(NCURSES_SOURCES)
ncurses_la_LDFLAGS = -module -avoid-version ${NCURSES_LIBS}

INCLUDES = -I$(top_srcdir)/include

AM_CPPFLAGS= ${NCURSES_CPPFLAGS} $(QORE_CPPFLAGS)

if COND_PROFILE
AM_CXXFLAGS=-g -pg
else
if COND_DEBUG
AM_CXXFLAGS=-g
endif
endif

install-exec-hook:
	mv $(DESTDIR)$(libdir)/ncurses.$(MODULE_SUFFIX) $(DESTDIR)$(libdir)/ncurses-api-$(MODULE_API).qmod
	rm -f $(DESTDIR)$(libdir)/ncurses.la
