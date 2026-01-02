# Makefile for Bluetooh Libs

COMPONENT = libbt

# The list of source/object files defaults to TARGET, which again is often
# the case for single-file programs. But we don't want our source file to be
# called !RunImage.
OBJS = bluetooth


LIBDIREC = <BTBSD$Root>.bsd
# There are two bases for BT in NetBSD these are in sys/dev and sys/netbt
LIBNETBT = <BTBSD$Root>.bsd.sys.sys
LIBBT = <BTBSD$Root>.bsd.lib.libbluetooth.
# The netbsd include folder
LIBINCL = <BTBSD$Root>.bsd.include.
# The netbt include folder
LIBSYSNTBT = <BTBSD$Root>.bsd.sys

include CLibrary

#Suppress non ANSI warnings
cflags+=-Wp

CINCLUDES += -I${LIBNETBT},${LIBBT},${LIBINCL},${LIBSYSNTBT},${LIBDIREC}

clean::
	${WIPE} ${INSTAPP} ${WFLAGS}

# Dynamic dependencies:
oz.bluetooth:	c.bluetooth
oz.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
oz.bluetooth:	<BTBSD$Root>.bsd.include.machine.h.cdefs
oz.bluetooth:	<BTBSD$Root>.bsd.include.arm.h.cdefs
oz.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.fcntl
oz.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.bsdfix
oz.bluetooth:	<BTBSD$Root>.bsd.lib.libbluetooth.h.bluetooth
oz.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
oz.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
oz.bluetooth:	<BTBSD$Root>.bsd.include.machine.h.types
oz.bluetooth:	<BTBSD$Root>.bsd.include.arm.h.types
oz.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
oz.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
oz.bluetooth:	<BTBSD$Root>.bsd.include.arm.h.int_types
oz.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_int_types
oz.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
oz.bluetooth:	<BTBSD$Root>.bsd.include.machine.h.ansi
oz.bluetooth:	<BTBSD$Root>.bsd.include.arm.h.ansi
oz.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_ansi
oz.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
oz.bluetooth:	<BTBSD$Root>.bsd.include.machine.h.int_types
oz.bluetooth:	<BTBSD$Root>.bsd.include.arm.h.int_types
oz.bluetooth:	<BTBSD$Root>.bsd.include.machine.h.int_types
oz.bluetooth:	<BTBSD$Root>.bsd.include.arm.h.int_types
oz.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.ansi
oz.bluetooth:	<BTBSD$Root>.bsd.include.machine.h.ansi
oz.bluetooth:	<BTBSD$Root>.bsd.include.arm.h.ansi
oz.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_ansi
oz.bluetooth:	<BTBSD$Root>.bsd.include.machine.h.endian
oz.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.endian
oz.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
oz.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.ansi
oz.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
oz.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.stdint
oz.bluetooth:	<BTBSD$Root>.bsd.include.machine.h.endian_machdep
oz.bluetooth:	<BTBSD$Root>.bsd.include.arm.h.endian_machdep
oz.bluetooth:	<BTBSD$Root>.bsd.include.machine.h.bswap
oz.bluetooth:	<BTBSD$Root>.bsd.include.arm.h.bswap
oz.bluetooth:	<BTBSD$Root>.bsd.include.arm.h.byte_swap
oz.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
oz.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.bswap
oz.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.stdint
oz.bluetooth:	<BTBSD$Root>.bsd.include.machine.h.bswap
oz.bluetooth:	<BTBSD$Root>.bsd.include.arm.h.bswap
oz.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.stdbool
oz.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.fd_set
oz.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
oz.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
oz.bluetooth:	<BTBSD$Root>.bsd.include.machine.h.int_types
oz.bluetooth:	<BTBSD$Root>.bsd.include.arm.h.int_types
oz.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.endian
oz.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.socket
oz.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
oz.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.ansi
oz.bluetooth:	<BTBSD$Root>.bsd.include.machine.h.ansi
oz.bluetooth:	<BTBSD$Root>.bsd.include.arm.h.ansi
oz.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_ansi
oz.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.uio
oz.bluetooth:	<BTBSD$Root>.bsd.include.machine.h.ansi
oz.bluetooth:	<BTBSD$Root>.bsd.include.arm.h.ansi
oz.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_ansi
oz.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
oz.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.ansi
oz.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
oz.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.sigtypes
oz.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
oz.bluetooth:	<BTBSD$Root>.bsd.include.machine.h.int_types
oz.bluetooth:	<BTBSD$Root>.bsd.include.arm.h.int_types
oz.bluetooth:	<BTBSD$Root>.bsd.include.machine.h.ansi
oz.bluetooth:	<BTBSD$Root>.bsd.include.arm.h.ansi
oz.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_ansi
oz.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
oz.bluetooth:	<BTBSD$Root>.bsd.sys.netbt.h.bluetooth
oz.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.socket
oz.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
oz.bluetooth:	<BTBSD$Root>.bsd.sys.netbt.h.hci
oz.bluetooth:	<BTBSD$Root>.bsd.sys.netbt.h.bluetooth
oz.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.ioccom
oz.bluetooth:	<BTBSD$Root>.bsd.sys.netbt.h.l2cap
oz.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
oz.bluetooth:	<BTBSD$Root>.bsd.include.h.netdb
o.bluetooth:	c.bluetooth
o.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.bluetooth:	<BTBSD$Root>.bsd.include.machine.h.cdefs
o.bluetooth:	<BTBSD$Root>.bsd.include.arm.h.cdefs
o.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.fcntl
o.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.bsdfix
o.bluetooth:	<BTBSD$Root>.bsd.lib.libbluetooth.h.bluetooth
o.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
o.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.bluetooth:	<BTBSD$Root>.bsd.include.machine.h.types
o.bluetooth:	<BTBSD$Root>.bsd.include.arm.h.types
o.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.bluetooth:	<BTBSD$Root>.bsd.include.arm.h.int_types
o.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_int_types
o.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.bluetooth:	<BTBSD$Root>.bsd.include.machine.h.ansi
o.bluetooth:	<BTBSD$Root>.bsd.include.arm.h.ansi
o.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_ansi
o.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.bluetooth:	<BTBSD$Root>.bsd.include.machine.h.int_types
o.bluetooth:	<BTBSD$Root>.bsd.include.arm.h.int_types
o.bluetooth:	<BTBSD$Root>.bsd.include.machine.h.int_types
o.bluetooth:	<BTBSD$Root>.bsd.include.arm.h.int_types
o.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.ansi
o.bluetooth:	<BTBSD$Root>.bsd.include.machine.h.ansi
o.bluetooth:	<BTBSD$Root>.bsd.include.arm.h.ansi
o.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_ansi
o.bluetooth:	<BTBSD$Root>.bsd.include.machine.h.endian
o.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.endian
o.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.ansi
o.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.stdint
o.bluetooth:	<BTBSD$Root>.bsd.include.machine.h.endian_machdep
o.bluetooth:	<BTBSD$Root>.bsd.include.arm.h.endian_machdep
o.bluetooth:	<BTBSD$Root>.bsd.include.machine.h.bswap
o.bluetooth:	<BTBSD$Root>.bsd.include.arm.h.bswap
o.bluetooth:	<BTBSD$Root>.bsd.include.arm.h.byte_swap
o.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
o.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.bswap
o.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.stdint
o.bluetooth:	<BTBSD$Root>.bsd.include.machine.h.bswap
o.bluetooth:	<BTBSD$Root>.bsd.include.arm.h.bswap
o.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.stdbool
o.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.fd_set
o.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.bluetooth:	<BTBSD$Root>.bsd.include.machine.h.int_types
o.bluetooth:	<BTBSD$Root>.bsd.include.arm.h.int_types
o.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.endian
o.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.socket
o.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.ansi
o.bluetooth:	<BTBSD$Root>.bsd.include.machine.h.ansi
o.bluetooth:	<BTBSD$Root>.bsd.include.arm.h.ansi
o.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_ansi
o.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.uio
o.bluetooth:	<BTBSD$Root>.bsd.include.machine.h.ansi
o.bluetooth:	<BTBSD$Root>.bsd.include.arm.h.ansi
o.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_ansi
o.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.ansi
o.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.sigtypes
o.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.bluetooth:	<BTBSD$Root>.bsd.include.machine.h.int_types
o.bluetooth:	<BTBSD$Root>.bsd.include.arm.h.int_types
o.bluetooth:	<BTBSD$Root>.bsd.include.machine.h.ansi
o.bluetooth:	<BTBSD$Root>.bsd.include.arm.h.ansi
o.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_ansi
o.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.bluetooth:	<BTBSD$Root>.bsd.sys.netbt.h.bluetooth
o.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.socket
o.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
o.bluetooth:	<BTBSD$Root>.bsd.sys.netbt.h.hci
o.bluetooth:	<BTBSD$Root>.bsd.sys.netbt.h.bluetooth
o.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.ioccom
o.bluetooth:	<BTBSD$Root>.bsd.sys.netbt.h.l2cap
o.bluetooth:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
o.bluetooth:	<BTBSD$Root>.bsd.include.h.netdb
