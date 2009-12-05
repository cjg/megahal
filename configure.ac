#                                               -*- Autoconf -*-
# Process this file with autoconf to produce a configure script.

AC_PREREQ(2.61)
AC_INIT(megahal, git, cjg@cruxppc.org)
AC_CONFIG_SRCDIR([src/megahal.c])
AC_CONFIG_HEADER([config.h])

AM_INIT_AUTOMAKE(megahal, git)

# Conditional building
AC_ARG_ENABLE(debug,
        [  --enable-debug            Turn on debugging ], 
        [case "${enableval}" in
              yes) debug=true ;;
              no) debug=false ;;
              *) AC_MSG_ERROR(bad value ${enableval} for --enable-debug) ;;
        esac], 
        [debug=false])
AM_CONDITIONAL(DEBUG, test x$debug = xtrue)

AM_PATH_PYTHON
AM_CHECK_PYTHON_HEADERS([PYSUBDIR=python],[])
AC_SUBST(PYSUBDIR)
 
# Checks for programs.
AC_PROG_CC
AM_PROG_CC_C_O
AC_PROG_LIBTOOL

# Checks for libraries.

# Checks for header files.
AC_HEADER_STDC
AC_CHECK_HEADERS([fcntl.h malloc.h stdlib.h string.h unistd.h])

# Checks for typedefs, structures, and compiler characteristics.
AC_HEADER_STDBOOL
AC_C_CONST
AC_TYPE_SIZE_T
AC_STRUCT_TM

# Checks for library functions.
AC_FUNC_ERROR_AT_LINE
AC_FUNC_MALLOC
AC_FUNC_REALLOC
AC_TYPE_SIGNAL
AC_FUNC_STAT
AC_FUNC_STRFTIME
AC_FUNC_VPRINTF
AC_CHECK_FUNCS([floor memset mkdir sqrt strchr strdup])

AC_CONFIG_FILES([Makefile
                 src/Makefile
		 data/Makefile
		 doc/Makefile
       		 python/Makefile])
AC_OUTPUT
