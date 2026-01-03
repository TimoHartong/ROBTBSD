# Makefile for Libc stdio

COMPONENT = libc_stdio

# The list of source/object files defaults to TARGET, which again is often
# the case for single-file programs.

OBJS = dprintf

# There are two bases for BT in NetBSD these are in sys/dev and sys/netbt
LIBNETBT = <BTBSD$Root>.bsd.sys.sys
# The netbsd include folder
LIBINCL = <BTBSD$Root>.bsd.include.

include CLibrary

#Suppress non ANSI warnings
cflags+=-Wp

CINCLUDES += -I${LIBINCL},${LIBNETBT}

clean::
	${WIPE} ${INSTAPP} ${WFLAGS}

# Dynamic dependencies:
oz.dprintf:	c.dprintf
oz.dprintf:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
oz.dprintf:	<BTBSD$Root>.bsd.include.machine.h.cdefs
oz.dprintf:	<BTBSD$Root>.bsd.include.arm.h.cdefs
oz.dprintf:	<BTBSD$Root>.bsd.sys.sys.sys.h.fcntl
oz.dprintf:	<BTBSD$Root>.bsd.sys.sys.sys.h.bsdfix
oz.dprintf:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
oz.dprintf:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
oz.dprintf:	<BTBSD$Root>.bsd.include.machine.h.types
oz.dprintf:	<BTBSD$Root>.bsd.include.arm.h.types
oz.dprintf:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
oz.dprintf:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
oz.dprintf:	<BTBSD$Root>.bsd.include.arm.h.int_types
oz.dprintf:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_int_types
oz.dprintf:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
oz.dprintf:	<BTBSD$Root>.bsd.include.machine.h.ansi
oz.dprintf:	<BTBSD$Root>.bsd.include.arm.h.ansi
oz.dprintf:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_ansi
oz.dprintf:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
oz.dprintf:	<BTBSD$Root>.bsd.include.machine.h.int_types
oz.dprintf:	<BTBSD$Root>.bsd.include.arm.h.int_types
oz.dprintf:	<BTBSD$Root>.bsd.include.machine.h.int_types
oz.dprintf:	<BTBSD$Root>.bsd.include.arm.h.int_types
oz.dprintf:	<BTBSD$Root>.bsd.sys.sys.sys.h.ansi
oz.dprintf:	<BTBSD$Root>.bsd.include.machine.h.ansi
oz.dprintf:	<BTBSD$Root>.bsd.include.arm.h.ansi
oz.dprintf:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_ansi
oz.dprintf:	<BTBSD$Root>.bsd.include.machine.h.endian
oz.dprintf:	<BTBSD$Root>.bsd.sys.sys.sys.h.endian
oz.dprintf:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
oz.dprintf:	<BTBSD$Root>.bsd.sys.sys.sys.h.ansi
oz.dprintf:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
oz.dprintf:	<BTBSD$Root>.bsd.sys.sys.sys.h.stdint
oz.dprintf:	<BTBSD$Root>.bsd.include.machine.h.endian_machdep
oz.dprintf:	<BTBSD$Root>.bsd.include.arm.h.endian_machdep
oz.dprintf:	<BTBSD$Root>.bsd.include.machine.h.bswap
oz.dprintf:	<BTBSD$Root>.bsd.include.arm.h.bswap
oz.dprintf:	<BTBSD$Root>.bsd.include.arm.h.byte_swap
oz.dprintf:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
oz.dprintf:	<BTBSD$Root>.bsd.sys.sys.sys.h.bswap
oz.dprintf:	<BTBSD$Root>.bsd.sys.sys.sys.h.stdint
oz.dprintf:	<BTBSD$Root>.bsd.include.machine.h.bswap
oz.dprintf:	<BTBSD$Root>.bsd.include.arm.h.bswap
oz.dprintf:	<BTBSD$Root>.bsd.sys.sys.sys.h.stdbool
oz.dprintf:	<BTBSD$Root>.bsd.sys.sys.sys.h.fd_set
oz.dprintf:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
oz.dprintf:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
oz.dprintf:	<BTBSD$Root>.bsd.include.machine.h.int_types
oz.dprintf:	<BTBSD$Root>.bsd.include.arm.h.int_types
o.dprintf:	c.dprintf
o.dprintf:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.dprintf:	<BTBSD$Root>.bsd.include.machine.h.cdefs
o.dprintf:	<BTBSD$Root>.bsd.include.arm.h.cdefs
o.dprintf:	<BTBSD$Root>.bsd.sys.sys.sys.h.fcntl
o.dprintf:	<BTBSD$Root>.bsd.sys.sys.sys.h.bsdfix
o.dprintf:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
o.dprintf:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.dprintf:	<BTBSD$Root>.bsd.include.machine.h.types
o.dprintf:	<BTBSD$Root>.bsd.include.arm.h.types
o.dprintf:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.dprintf:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.dprintf:	<BTBSD$Root>.bsd.include.arm.h.int_types
o.dprintf:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_int_types
o.dprintf:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.dprintf:	<BTBSD$Root>.bsd.include.machine.h.ansi
o.dprintf:	<BTBSD$Root>.bsd.include.arm.h.ansi
o.dprintf:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_ansi
o.dprintf:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.dprintf:	<BTBSD$Root>.bsd.include.machine.h.int_types
o.dprintf:	<BTBSD$Root>.bsd.include.arm.h.int_types
o.dprintf:	<BTBSD$Root>.bsd.include.machine.h.int_types
o.dprintf:	<BTBSD$Root>.bsd.include.arm.h.int_types
o.dprintf:	<BTBSD$Root>.bsd.sys.sys.sys.h.ansi
o.dprintf:	<BTBSD$Root>.bsd.include.machine.h.ansi
o.dprintf:	<BTBSD$Root>.bsd.include.arm.h.ansi
o.dprintf:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_ansi
o.dprintf:	<BTBSD$Root>.bsd.include.machine.h.endian
o.dprintf:	<BTBSD$Root>.bsd.sys.sys.sys.h.endian
o.dprintf:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.dprintf:	<BTBSD$Root>.bsd.sys.sys.sys.h.ansi
o.dprintf:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.dprintf:	<BTBSD$Root>.bsd.sys.sys.sys.h.stdint
o.dprintf:	<BTBSD$Root>.bsd.include.machine.h.endian_machdep
o.dprintf:	<BTBSD$Root>.bsd.include.arm.h.endian_machdep
o.dprintf:	<BTBSD$Root>.bsd.include.machine.h.bswap
o.dprintf:	<BTBSD$Root>.bsd.include.arm.h.bswap
o.dprintf:	<BTBSD$Root>.bsd.include.arm.h.byte_swap
o.dprintf:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
o.dprintf:	<BTBSD$Root>.bsd.sys.sys.sys.h.bswap
o.dprintf:	<BTBSD$Root>.bsd.sys.sys.sys.h.stdint
o.dprintf:	<BTBSD$Root>.bsd.include.machine.h.bswap
o.dprintf:	<BTBSD$Root>.bsd.include.arm.h.bswap
o.dprintf:	<BTBSD$Root>.bsd.sys.sys.sys.h.stdbool
o.dprintf:	<BTBSD$Root>.bsd.sys.sys.sys.h.fd_set
o.dprintf:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.dprintf:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.dprintf:	<BTBSD$Root>.bsd.include.machine.h.int_types
o.dprintf:	<BTBSD$Root>.bsd.include.arm.h.int_types
