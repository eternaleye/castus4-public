#                                               -*- Autoconf -*-
# Process this file with autoconf to produce a configure script.

# COMMENCE
AC_PREREQ(2.60)
AC_INIT(castus4-public, 0.0.1, jonathan@castus.tv)
AM_INIT_AUTOMAKE([subdir-objects])
AC_CONFIG_SRCDIR([configure.ac])
AC_CONFIG_MACRO_DIR([m4])
AC_PREFIX_DEFAULT(/usr/local)

# Checks for programs.
AC_PROG_CC
AC_PROG_CXX
AM_PROG_CC_C_O
m4_ifdef([AM_PROG_AR], [AM_PROG_AR])

# Initialize libtool
LT_INIT
LT_PREREQ([2.4.2])

# Checks for header files.
AC_HEADER_STDC
AC_CHECK_HEADERS([fcntl.h stdint.h stdlib.h string.h sys/socket.h unistd.h sys/fanotify.h sys/inotify.h])

# Checks for typedefs, structures, and compiler characteristics.
AC_TYPE_INT64_T
AC_TYPE_UINT32_T
AC_TYPE_UINT8_T

# Checks for library functions.
AC_FUNC_MALLOC
AC_FUNC_MEMCMP
AC_CHECK_FUNCS([memset])

# variables for multi-target
AM_CONDITIONAL(WIN32,false)
AM_CONDITIONAL(LINUX,true)

# Platform behavior
AC_SYS_LARGEFILE

LIBS=-lm

AC_CONFIG_FILES(castus4-public.pc)
AC_CONFIG_FILES(Makefile)

AC_OUTPUT


