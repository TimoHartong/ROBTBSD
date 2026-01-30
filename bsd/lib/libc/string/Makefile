# Makefile for Libc string

COMPONENT = libc_string

# The list of source/object files defaults to TARGET, which again is often
# the case for single-file programs. But we don't want our source file to be
# called !RunImage.
OBJS = strdup

# There are two bases for BT in NetBSD these are in sys/dev and sys/netbt
LIBNETBT = <BTBSD$Root>.bsd.sys.sys
#LIBBT = <BTBSD$Root>.bsd.lib.libbluetooth.
# The netbsd include folder
LIBINCL = <BTBSD$Root>.bsd.include.
# The netbt include folder
#LIBSYSNTBT = <BTBSD$Root>.bsd.sys

include CLibrary

CINCLUDES += -I${LIBINCL},${LIBNETBT}

clean::
	${WIPE} ${INSTAPP} ${WFLAGS}

# Dynamic dependencies:
oz.strdup:	c.strdup
oz.strdup:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
oz.strdup:	<BTBSD$Root>.bsd.include.machine.h.cdefs
oz.strdup:	<BTBSD$Root>.bsd.include.arm.h.cdefs
oz.strdup:	<BTBSD$Root>.bsd.sys.sys.sys.h.fcntl
oz.strdup:	<BTBSD$Root>.bsd.sys.sys.sys.h.bsdfix
o.strdup:	c.strdup
o.strdup:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.strdup:	<BTBSD$Root>.bsd.include.machine.h.cdefs
o.strdup:	<BTBSD$Root>.bsd.include.arm.h.cdefs
o.strdup:	<BTBSD$Root>.bsd.sys.sys.sys.h.fcntl
o.strdup:	<BTBSD$Root>.bsd.sys.sys.sys.h.bsdfix
