if DEBUG
DEBUG_FLAG = -DDEBUG 
endif

noinst_LTLIBRARIES = libmegahal.la
libmegahal_la_SOURCES =\
	debug.c\
	debug.h\
	megahal.c\
	megahal.h 

bin_PROGRAMS = megahal
megahal_SOURCES =\
	main.c
megahal_LDADD = libmegahal.la
megahal_DEPENDENCIES = libmegahal.la
	
AM_CFLAGS = $(DEBUG_FLAG)