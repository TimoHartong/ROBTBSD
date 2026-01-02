# Makefile for common lib libc

COMPONENT = common_string

# The list of source/object files defaults to TARGET, which again is often
# the case for single-file programs. But we don't want our source file to be
# called !RunImage.
OBJS = strlcpy strcasecmp


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
oz.strlcpy:	c.strlcpy
oz.strlcpy:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
oz.strlcpy:	<BTBSD$Root>.bsd.include.machine.h.cdefs
oz.strlcpy:	<BTBSD$Root>.bsd.include.arm.h.cdefs
oz.strlcpy:	<BTBSD$Root>.bsd.sys.sys.sys.h.fcntl
oz.strlcpy:	<BTBSD$Root>.bsd.sys.sys.sys.h.bsdfix
oz.strlcpy:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
oz.strlcpy:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
oz.strlcpy:	<BTBSD$Root>.bsd.include.machine.h.types
oz.strlcpy:	<BTBSD$Root>.bsd.include.arm.h.types
oz.strlcpy:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
oz.strlcpy:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
oz.strlcpy:	<BTBSD$Root>.bsd.include.arm.h.int_types
oz.strlcpy:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_int_types
oz.strlcpy:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
oz.strlcpy:	<BTBSD$Root>.bsd.include.machine.h.ansi
oz.strlcpy:	<BTBSD$Root>.bsd.include.arm.h.ansi
oz.strlcpy:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_ansi
oz.strlcpy:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
oz.strlcpy:	<BTBSD$Root>.bsd.include.machine.h.int_types
oz.strlcpy:	<BTBSD$Root>.bsd.include.arm.h.int_types
oz.strlcpy:	<BTBSD$Root>.bsd.include.machine.h.int_types
oz.strlcpy:	<BTBSD$Root>.bsd.include.arm.h.int_types
oz.strlcpy:	<BTBSD$Root>.bsd.sys.sys.sys.h.ansi
oz.strlcpy:	<BTBSD$Root>.bsd.include.machine.h.ansi
oz.strlcpy:	<BTBSD$Root>.bsd.include.arm.h.ansi
oz.strlcpy:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_ansi
oz.strlcpy:	<BTBSD$Root>.bsd.include.machine.h.endian
oz.strlcpy:	<BTBSD$Root>.bsd.sys.sys.sys.h.endian
oz.strlcpy:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
oz.strlcpy:	<BTBSD$Root>.bsd.sys.sys.sys.h.ansi
oz.strlcpy:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
oz.strlcpy:	<BTBSD$Root>.bsd.sys.sys.sys.h.stdint
oz.strlcpy:	<BTBSD$Root>.bsd.include.machine.h.endian_machdep
oz.strlcpy:	<BTBSD$Root>.bsd.include.arm.h.endian_machdep
oz.strlcpy:	<BTBSD$Root>.bsd.include.machine.h.bswap
oz.strlcpy:	<BTBSD$Root>.bsd.include.arm.h.bswap
oz.strlcpy:	<BTBSD$Root>.bsd.include.arm.h.byte_swap
oz.strlcpy:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
oz.strlcpy:	<BTBSD$Root>.bsd.sys.sys.sys.h.bswap
oz.strlcpy:	<BTBSD$Root>.bsd.sys.sys.sys.h.stdint
oz.strlcpy:	<BTBSD$Root>.bsd.include.machine.h.bswap
oz.strlcpy:	<BTBSD$Root>.bsd.include.arm.h.bswap
oz.strlcpy:	<BTBSD$Root>.bsd.sys.sys.sys.h.stdbool
oz.strlcpy:	<BTBSD$Root>.bsd.sys.sys.sys.h.fd_set
oz.strlcpy:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
oz.strlcpy:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
oz.strlcpy:	<BTBSD$Root>.bsd.include.machine.h.int_types
oz.strlcpy:	<BTBSD$Root>.bsd.include.arm.h.int_types
oz.strcasecmp:	c.strcasecmp
oz.strcasecmp:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
oz.strcasecmp:	<BTBSD$Root>.bsd.include.machine.h.cdefs
oz.strcasecmp:	<BTBSD$Root>.bsd.include.arm.h.cdefs
oz.strcasecmp:	<BTBSD$Root>.bsd.sys.sys.sys.h.fcntl
oz.strcasecmp:	<BTBSD$Root>.bsd.sys.sys.sys.h.bsdfix
oz.strcasecmp:	<BTBSD$Root>.bsd.include.machine.h.limits
oz.strcasecmp:	<BTBSD$Root>.bsd.include.arm.h.limits
oz.strcasecmp:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.strlcpy:	c.strlcpy
o.strlcpy:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.strlcpy:	<BTBSD$Root>.bsd.include.machine.h.cdefs
o.strlcpy:	<BTBSD$Root>.bsd.include.arm.h.cdefs
o.strlcpy:	<BTBSD$Root>.bsd.sys.sys.sys.h.fcntl
o.strlcpy:	<BTBSD$Root>.bsd.sys.sys.sys.h.bsdfix
o.strlcpy:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
o.strlcpy:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.strlcpy:	<BTBSD$Root>.bsd.include.machine.h.types
o.strlcpy:	<BTBSD$Root>.bsd.include.arm.h.types
o.strlcpy:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.strlcpy:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.strlcpy:	<BTBSD$Root>.bsd.include.arm.h.int_types
o.strlcpy:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_int_types
o.strlcpy:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.strlcpy:	<BTBSD$Root>.bsd.include.machine.h.ansi
o.strlcpy:	<BTBSD$Root>.bsd.include.arm.h.ansi
o.strlcpy:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_ansi
o.strlcpy:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.strlcpy:	<BTBSD$Root>.bsd.include.machine.h.int_types
o.strlcpy:	<BTBSD$Root>.bsd.include.arm.h.int_types
o.strlcpy:	<BTBSD$Root>.bsd.include.machine.h.int_types
o.strlcpy:	<BTBSD$Root>.bsd.include.arm.h.int_types
o.strlcpy:	<BTBSD$Root>.bsd.sys.sys.sys.h.ansi
o.strlcpy:	<BTBSD$Root>.bsd.include.machine.h.ansi
o.strlcpy:	<BTBSD$Root>.bsd.include.arm.h.ansi
o.strlcpy:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_ansi
o.strlcpy:	<BTBSD$Root>.bsd.include.machine.h.endian
o.strlcpy:	<BTBSD$Root>.bsd.sys.sys.sys.h.endian
o.strlcpy:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.strlcpy:	<BTBSD$Root>.bsd.sys.sys.sys.h.ansi
o.strlcpy:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.strlcpy:	<BTBSD$Root>.bsd.sys.sys.sys.h.stdint
o.strlcpy:	<BTBSD$Root>.bsd.include.machine.h.endian_machdep
o.strlcpy:	<BTBSD$Root>.bsd.include.arm.h.endian_machdep
o.strlcpy:	<BTBSD$Root>.bsd.include.machine.h.bswap
o.strlcpy:	<BTBSD$Root>.bsd.include.arm.h.bswap
o.strlcpy:	<BTBSD$Root>.bsd.include.arm.h.byte_swap
o.strlcpy:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
o.strlcpy:	<BTBSD$Root>.bsd.sys.sys.sys.h.bswap
o.strlcpy:	<BTBSD$Root>.bsd.sys.sys.sys.h.stdint
o.strlcpy:	<BTBSD$Root>.bsd.include.machine.h.bswap
o.strlcpy:	<BTBSD$Root>.bsd.include.arm.h.bswap
o.strlcpy:	<BTBSD$Root>.bsd.sys.sys.sys.h.stdbool
o.strlcpy:	<BTBSD$Root>.bsd.sys.sys.sys.h.fd_set
o.strlcpy:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.strlcpy:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.strlcpy:	<BTBSD$Root>.bsd.include.machine.h.int_types
o.strlcpy:	<BTBSD$Root>.bsd.include.arm.h.int_types
o.strcasecmp:	c.strcasecmp
o.strcasecmp:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.strcasecmp:	<BTBSD$Root>.bsd.include.machine.h.cdefs
o.strcasecmp:	<BTBSD$Root>.bsd.include.arm.h.cdefs
o.strcasecmp:	<BTBSD$Root>.bsd.sys.sys.sys.h.fcntl
o.strcasecmp:	<BTBSD$Root>.bsd.sys.sys.sys.h.bsdfix
o.strcasecmp:	<BTBSD$Root>.bsd.include.machine.h.limits
o.strcasecmp:	<BTBSD$Root>.bsd.include.arm.h.limits
o.strcasecmp:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
