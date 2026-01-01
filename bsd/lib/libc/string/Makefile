# Makefile for Libc getopt

COMPONENT = libc_string

# The list of source/object files defaults to TARGET, which again is often
# the case for single-file programs. But we don't want our source file to be
# called !RunImage.
OBJS = getopt

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
