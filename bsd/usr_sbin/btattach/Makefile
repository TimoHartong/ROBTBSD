# Makefile for exampleapp

COMPONENT = btattach

# The name of the linked file defaults to COMPONENT, which is often the case
# for single-file programs. But when the linked file lives in an application
# directory, it is normally called !RunImage.
TARGET = BTAttach

# The list of source/object files defaults to TARGET, which again is often
# the case for single-file programs. But we don't want our source file to be
# called !RunImage.
OBJS = btattach

INSTDIR ?= <Obey$Dir>

# The shared makefiles don't attempt to guess the application directory name
# Usually you'll want to place it inside INSTDIR, which is passed in from
# either the MkInstall file, or (for !Builder builds) the components file.
# SEP expands to the directory separator character - we use this instead of
# a literal '.' character to help with cross-compilation.
INSTAPP = ${INSTDIR}${SEP}!Example

LIBDIREC = <BTBSD$Root>.bsd
# There are two bases for BT in NetBSD these are in sys/dev and sys/netbt
LIBNETBT = <BTBSD$Root>.bsd.sys.sys.
LIBBT = <BTBSD$Root>.bsd.lib.libbluetooth.
# The netbsd include folder
LIBINCL = <BTBSD$Root>.bsd.include.
# The netbt include folder
LIBSYSNTBT = <BTBSD$Root>.bsd.sys


# You need to specify all the files that go into the application directory.
# The shared makefiles handle merging the various subdirectories of the
# Resources directory for you.
INSTAPP_FILES = !Boot !Run !Sprites !Sprites11 !Sprites22 !RunImage

include CApp

CINCLUDES += -I${LIBNETBT},${LIBBT},${LIBINCL},${LIBSYSNTBT}
|LIBS += ${LIBDIREC}.o.zvectorlib

clean::
	${WIPE} ${INSTAPP} ${WFLAGS}

# Dynamic dependencies:
o.btattach:	c.btattach
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.btattach:	<BTBSD$Root>.bsd.include.machine.h.cdefs
o.btattach:	<BTBSD$Root>.bsd.include.arm.h.cdefs
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.fcntl
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.bsdfix
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.ioctl
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.ttycom
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.syslimits
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.ioccom
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.ioccom
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.dkio
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.filio
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.sockio
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.ioccom
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.param
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.null
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.inttypes
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.stdint
o.btattach:	<BTBSD$Root>.bsd.include.machine.h.int_fmtio
o.btattach:	<BTBSD$Root>.bsd.include.arm.h.int_fmtio
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_int_fmtio
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.btattach:	<BTBSD$Root>.bsd.include.machine.h.types
o.btattach:	<BTBSD$Root>.bsd.include.arm.arm32.h.types
o.btattach:	<BTBSD$Root>.bsd.include.arm.h.types
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.btattach:	<BTBSD$Root>.bsd.include.arm.h.int_types
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_int_types
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.btattach:	<BTBSD$Root>.bsd.include.machine.h.ansi
o.btattach:	<BTBSD$Root>.bsd.include.arm.h.ansi
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_ansi
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.btattach:	<BTBSD$Root>.bsd.include.machine.h.int_types
o.btattach:	<BTBSD$Root>.bsd.include.arm.h.int_types
o.btattach:	<BTBSD$Root>.bsd.include.machine.h.int_types
o.btattach:	<BTBSD$Root>.bsd.include.arm.h.int_types
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.ansi
o.btattach:	<BTBSD$Root>.bsd.include.machine.h.ansi
o.btattach:	<BTBSD$Root>.bsd.include.arm.h.ansi
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_ansi
o.btattach:	<BTBSD$Root>.bsd.include.machine.h.endian
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.endian
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.ansi
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.stdint
o.btattach:	<BTBSD$Root>.bsd.include.machine.h.endian_machdep
o.btattach:	<BTBSD$Root>.bsd.include.arm.h.endian_machdep
o.btattach:	<BTBSD$Root>.bsd.include.machine.h.bswap
o.btattach:	<BTBSD$Root>.bsd.include.arm.h.bswap
o.btattach:	<BTBSD$Root>.bsd.include.arm.h.byte_swap
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.bswap
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.stdint
o.btattach:	<BTBSD$Root>.bsd.include.machine.h.bswap
o.btattach:	<BTBSD$Root>.bsd.include.arm.h.bswap
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.stdbool
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.fd_set
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.btattach:	<BTBSD$Root>.bsd.include.machine.h.int_types
o.btattach:	<BTBSD$Root>.bsd.include.arm.h.int_types
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.syslimits
o.btattach:	<BTBSD$Root>.bsd.include.machine.h.param
o.btattach:	<BTBSD$Root>.bsd.include.arm.arm32.h.param
o.btattach:	<BTBSD$Root>.bsd.include.machine.h.limits
o.btattach:	<BTBSD$Root>.bsd.include.arm.h.limits
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.errno
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.time
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.resource
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.ucred
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.uio
o.btattach:	<BTBSD$Root>.bsd.include.machine.h.ansi
o.btattach:	<BTBSD$Root>.bsd.include.arm.h.ansi
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_ansi
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.ansi
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.btattach:	<BTBSD$Root>.bsd.include.uvm.h.uvm_param
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.signal
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.sigtypes
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.btattach:	<BTBSD$Root>.bsd.include.machine.h.int_types
o.btattach:	<BTBSD$Root>.bsd.include.arm.h.int_types
o.btattach:	<BTBSD$Root>.bsd.include.machine.h.ansi
o.btattach:	<BTBSD$Root>.bsd.include.arm.h.ansi
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_ansi
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.siginfo
o.btattach:	<BTBSD$Root>.bsd.include.machine.h.signal
o.btattach:	<BTBSD$Root>.bsd.include.arm.h.signal
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.sigtypes
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.queue
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.ucontext
o.btattach:	<BTBSD$Root>.bsd.include.machine.h.signal
o.btattach:	<BTBSD$Root>.bsd.include.arm.h.signal
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.uio
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.select
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.fd_set
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.selinfo
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.signal
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.sigtypes
o.btattach:	<BTBSD$Root>.bsd.lib.libbluetooth.h.bluetooth
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.endian
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.socket
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.ansi
o.btattach:	<BTBSD$Root>.bsd.include.machine.h.ansi
o.btattach:	<BTBSD$Root>.bsd.include.arm.h.ansi
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_ansi
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.uio
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.sigtypes
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.btattach:	<BTBSD$Root>.bsd.sys.netbt.h.bluetooth
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.socket
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
o.btattach:	<BTBSD$Root>.bsd.sys.netbt.h.hci
o.btattach:	<BTBSD$Root>.bsd.sys.netbt.h.bluetooth
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.ioccom
o.btattach:	<BTBSD$Root>.bsd.sys.netbt.h.l2cap
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
o.btattach:	<BTBSD$Root>.bsd.include.h.netdb
o.btattach:	<BTBSD$Root>.bsd.include.h.err
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.btattach:	<BTBSD$Root>.bsd.include.h.fcntl
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.stat
o.btattach:	<BTBSD$Root>.bsd.include.h.unistd
o.btattach:	<BTBSD$Root>.bsd.include.machine.h.ansi
o.btattach:	<BTBSD$Root>.bsd.include.arm.h.ansi
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_ansi
o.btattach:	<BTBSD$Root>.bsd.include.machine.h.int_types
o.btattach:	<BTBSD$Root>.bsd.include.arm.h.int_types
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.unistd
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.btattach:	<BTBSD$Root>.bsd.include.h.termios
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.ansi
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.ttycom
o.btattach:	<BTBSD$Root>.bsd.include.h.unistd
o.btattach:	<BTBSD$Root>.bsd.include.h.util
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.ansi
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.inttypes
o.btattach:	h.btattach
o.btattach:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
