INCLUDES = $(PYTHON_INCLUDES) -I../src

pyexec_LTLIBRARIES = megahal.la
megahal_la_SOURCES = python-interface.c
megahal_la_LIBADD = -L../src -lmegahal
megahal_la_LDFLAGS = -avoid-version -module