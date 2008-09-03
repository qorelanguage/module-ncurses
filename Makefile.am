AUTOMAKE_OPTIONS = foreign

SUBDIRS = src

noinst_HEADERS = src/ncurses-module.h \
	src/QC_Panel.h \
	src/QC_Window.h

EXTRA_DIST = COPYING ChangeLog AUTHORS README \
	test/ncurses.q \
	examples/hanoi.q \
	examples/worm.q \
	qore-ncurses-module.spec

libtool: $(LIBTOOL_DEPS)
	$(SHELL) ./config.status --recheck
