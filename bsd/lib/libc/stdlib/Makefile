# Makefile for Libc getopt

COMPONENT = libc_stdlib

# The list of source/object files defaults to TARGET, which again is often
# the case for single-file programs. But we don't want our source file to be
# called !RunImage.
OBJS = getopt


#LIBDIREC = <BTBSD$Root>.bsd
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
oz.getopt:	c.getopt
oz.getopt:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
oz.getopt:	<BTBSD$Root>.bsd.include.machine.h.cdefs
oz.getopt:	<BTBSD$Root>.bsd.include.arm.h.cdefs
oz.getopt:	<BTBSD$Root>.bsd.sys.sys.sys.h.fcntl
oz.getopt:	<BTBSD$Root>.bsd.sys.sys.sys.h.bsdfix
oz.getopt:	<BTBSD$Root>.bsd.include.h.unistd
oz.getopt:	<BTBSD$Root>.bsd.include.machine.h.ansi
oz.getopt:	<BTBSD$Root>.bsd.include.arm.h.ansi
oz.getopt:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_ansi
oz.getopt:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
oz.getopt:	<BTBSD$Root>.bsd.include.machine.h.int_types
oz.getopt:	<BTBSD$Root>.bsd.include.arm.h.int_types
oz.getopt:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_int_types
oz.getopt:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
oz.getopt:	<BTBSD$Root>.bsd.include.machine.h.int_types
oz.getopt:	<BTBSD$Root>.bsd.include.arm.h.int_types
oz.getopt:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
oz.getopt:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
oz.getopt:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
oz.getopt:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
oz.getopt:	<BTBSD$Root>.bsd.include.machine.h.types
oz.getopt:	<BTBSD$Root>.bsd.include.arm.h.types
oz.getopt:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
oz.getopt:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
oz.getopt:	<BTBSD$Root>.bsd.include.arm.h.int_types
oz.getopt:	<BTBSD$Root>.bsd.include.machine.h.ansi
oz.getopt:	<BTBSD$Root>.bsd.include.arm.h.ansi
oz.getopt:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_ansi
oz.getopt:	<BTBSD$Root>.bsd.include.machine.h.int_types
oz.getopt:	<BTBSD$Root>.bsd.include.arm.h.int_types
oz.getopt:	<BTBSD$Root>.bsd.sys.sys.sys.h.ansi
oz.getopt:	<BTBSD$Root>.bsd.include.machine.h.ansi
oz.getopt:	<BTBSD$Root>.bsd.include.arm.h.ansi
oz.getopt:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_ansi
oz.getopt:	<BTBSD$Root>.bsd.include.machine.h.endian
oz.getopt:	<BTBSD$Root>.bsd.sys.sys.sys.h.endian
oz.getopt:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
oz.getopt:	<BTBSD$Root>.bsd.sys.sys.sys.h.ansi
oz.getopt:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
oz.getopt:	<BTBSD$Root>.bsd.sys.sys.sys.h.stdint
oz.getopt:	<BTBSD$Root>.bsd.include.machine.h.endian_machdep
oz.getopt:	<BTBSD$Root>.bsd.include.arm.h.endian_machdep
oz.getopt:	<BTBSD$Root>.bsd.include.machine.h.bswap
oz.getopt:	<BTBSD$Root>.bsd.include.arm.h.bswap
oz.getopt:	<BTBSD$Root>.bsd.include.arm.h.byte_swap
oz.getopt:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
oz.getopt:	<BTBSD$Root>.bsd.sys.sys.sys.h.bswap
oz.getopt:	<BTBSD$Root>.bsd.sys.sys.sys.h.stdint
oz.getopt:	<BTBSD$Root>.bsd.include.machine.h.bswap
oz.getopt:	<BTBSD$Root>.bsd.include.arm.h.bswap
oz.getopt:	<BTBSD$Root>.bsd.sys.sys.sys.h.stdbool
oz.getopt:	<BTBSD$Root>.bsd.sys.sys.sys.h.fd_set
oz.getopt:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
oz.getopt:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
oz.getopt:	<BTBSD$Root>.bsd.include.machine.h.int_types
oz.getopt:	<BTBSD$Root>.bsd.include.arm.h.int_types
oz.getopt:	<BTBSD$Root>.bsd.sys.sys.sys.h.unistd
oz.getopt:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.getopt:	c.getopt
o.getopt:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.getopt:	<BTBSD$Root>.bsd.include.machine.h.cdefs
o.getopt:	<BTBSD$Root>.bsd.include.arm.h.cdefs
o.getopt:	<BTBSD$Root>.bsd.sys.sys.sys.h.fcntl
o.getopt:	<BTBSD$Root>.bsd.sys.sys.sys.h.bsdfix
o.getopt:	<BTBSD$Root>.bsd.include.h.unistd
o.getopt:	<BTBSD$Root>.bsd.include.machine.h.ansi
o.getopt:	<BTBSD$Root>.bsd.include.arm.h.ansi
o.getopt:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_ansi
o.getopt:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.getopt:	<BTBSD$Root>.bsd.include.machine.h.int_types
o.getopt:	<BTBSD$Root>.bsd.include.arm.h.int_types
o.getopt:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_int_types
o.getopt:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.getopt:	<BTBSD$Root>.bsd.include.machine.h.int_types
o.getopt:	<BTBSD$Root>.bsd.include.arm.h.int_types
o.getopt:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.getopt:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.getopt:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
o.getopt:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.getopt:	<BTBSD$Root>.bsd.include.machine.h.types
o.getopt:	<BTBSD$Root>.bsd.include.arm.h.types
o.getopt:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.getopt:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.getopt:	<BTBSD$Root>.bsd.include.arm.h.int_types
o.getopt:	<BTBSD$Root>.bsd.include.machine.h.ansi
o.getopt:	<BTBSD$Root>.bsd.include.arm.h.ansi
o.getopt:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_ansi
o.getopt:	<BTBSD$Root>.bsd.include.machine.h.int_types
o.getopt:	<BTBSD$Root>.bsd.include.arm.h.int_types
o.getopt:	<BTBSD$Root>.bsd.sys.sys.sys.h.ansi
o.getopt:	<BTBSD$Root>.bsd.include.machine.h.ansi
o.getopt:	<BTBSD$Root>.bsd.include.arm.h.ansi
o.getopt:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_ansi
o.getopt:	<BTBSD$Root>.bsd.include.machine.h.endian
o.getopt:	<BTBSD$Root>.bsd.sys.sys.sys.h.endian
o.getopt:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.getopt:	<BTBSD$Root>.bsd.sys.sys.sys.h.ansi
o.getopt:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.getopt:	<BTBSD$Root>.bsd.sys.sys.sys.h.stdint
o.getopt:	<BTBSD$Root>.bsd.include.machine.h.endian_machdep
o.getopt:	<BTBSD$Root>.bsd.include.arm.h.endian_machdep
o.getopt:	<BTBSD$Root>.bsd.include.machine.h.bswap
o.getopt:	<BTBSD$Root>.bsd.include.arm.h.bswap
o.getopt:	<BTBSD$Root>.bsd.include.arm.h.byte_swap
o.getopt:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
o.getopt:	<BTBSD$Root>.bsd.sys.sys.sys.h.bswap
o.getopt:	<BTBSD$Root>.bsd.sys.sys.sys.h.stdint
o.getopt:	<BTBSD$Root>.bsd.include.machine.h.bswap
o.getopt:	<BTBSD$Root>.bsd.include.arm.h.bswap
o.getopt:	<BTBSD$Root>.bsd.sys.sys.sys.h.stdbool
o.getopt:	<BTBSD$Root>.bsd.sys.sys.sys.h.fd_set
o.getopt:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.getopt:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.getopt:	<BTBSD$Root>.bsd.include.machine.h.int_types
o.getopt:	<BTBSD$Root>.bsd.include.arm.h.int_types
o.getopt:	<BTBSD$Root>.bsd.sys.sys.sys.h.unistd
o.getopt:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
