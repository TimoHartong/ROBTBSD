# Makefile for btconfig

COMPONENT = btconfig

# The name of the linked file defaults to COMPONENT, which is often the case
# for single-file programs. But when the linked file lives in an application
# directory, it is normally called !RunImage.
TARGET = BTConfig

# The list of source/object files defaults to TARGET, which again is often
# the case for single-file programs. But we don't want our source file to be
# called !RunImage.
OBJS = btconfig

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
LIBCROOT = <LibC$Root>
COMMONLIB = <CommonLib$Root>


# You need to specify all the files that go into the application directory.
# The shared makefiles handle merging the various subdirectories of the
# Resources directory for you.
INSTAPP_FILES = !Boot !Run !Sprites !Sprites11 !Sprites22 !RunImage

include CApp

#Suppress non ANSI warnings
cflags+=-Wp

CINCLUDES += -I${LIBNETBT},${LIBBT},${LIBINCL},${LIBSYSNTBT}
# Add bluetooth lib
LIBS += ${LIBBT}o.bluetooth 
LIBS += ${LIBBT}o.bt_dev
# Add stdlib libraries
LIBS += ${LIBCROOT}.stdlib.o.getopt 
# Add Clib gen library
LIBS += ${LIBCROOT}.gen.o.errx ${LIBCROOT}.gen.o.err ${LIBCROOT}.gen.o.alarm 
LIBS += ${LIBCROOT}.gen.o.daemon ${LIBCROOT}.gen.o.getprogname  ${LIBCROOT}.gen.o.sleep 
LIBS += ${LIBCROOT}.gen.o.warn 
# Add Clib Termios
LIBS += ${LIBCROOT}.termios.o.tcdrain ${LIBCROOT}.termios.o.tcflush 
LIBS += ${LIBCROOT}.termios.o.tcgetattr ${LIBCROOT}.termios.o.tcsetattr 
LIBS += ${LIBCROOT}.termios.o.cfmakeraw ${LIBCROOT}.termios.o.cfsetspeed
# Add Clib stdio
LIBS += ${LIBCROOT}.stdio.o.dprintf
# Add Common CLib - String That is something else then Clib in Lib
LIBS += ${COMMONLIB}.libc.string.o.strlcpy ${COMMONLIB}.libc.string.o.strcasecmp
# Add LibUtil 
LIBS += ${LIBDIREC}.lib.libutil.o.pidfile ${LIBDIREC}.lib.libutil.o.pid_fix
# Add BSD Fixes
LIBS += ${LIBDIREC}.lib.bsdfix.o.fix

clean::
	${WIPE} ${INSTAPP} ${WFLAGS}

# Dynamic dependencies:
o.btconfig:	c.btconfig
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.btconfig:	<BTBSD$Root>.bsd.include.machine.h.cdefs
o.btconfig:	<BTBSD$Root>.bsd.include.arm.h.cdefs
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.fcntl
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.bsdfix
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.ioctl
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.ttycom
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.syslimits
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.ioccom
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.ioccom
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.dkio
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.filio
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.sockio
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.ioccom
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.param
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.null
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.inttypes
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.stdint
o.btconfig:	<BTBSD$Root>.bsd.include.machine.h.int_fmtio
o.btconfig:	<BTBSD$Root>.bsd.include.arm.h.int_fmtio
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_int_fmtio
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.btconfig:	<BTBSD$Root>.bsd.include.machine.h.types
o.btconfig:	<BTBSD$Root>.bsd.include.arm.h.types
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.btconfig:	<BTBSD$Root>.bsd.include.arm.h.int_types
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_int_types
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.btconfig:	<BTBSD$Root>.bsd.include.machine.h.ansi
o.btconfig:	<BTBSD$Root>.bsd.include.arm.h.ansi
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_ansi
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.btconfig:	<BTBSD$Root>.bsd.include.machine.h.int_types
o.btconfig:	<BTBSD$Root>.bsd.include.arm.h.int_types
o.btconfig:	<BTBSD$Root>.bsd.include.machine.h.int_types
o.btconfig:	<BTBSD$Root>.bsd.include.arm.h.int_types
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.ansi
o.btconfig:	<BTBSD$Root>.bsd.include.machine.h.ansi
o.btconfig:	<BTBSD$Root>.bsd.include.arm.h.ansi
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_ansi
o.btconfig:	<BTBSD$Root>.bsd.include.machine.h.endian
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.endian
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.ansi
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.stdint
o.btconfig:	<BTBSD$Root>.bsd.include.machine.h.endian_machdep
o.btconfig:	<BTBSD$Root>.bsd.include.arm.h.endian_machdep
o.btconfig:	<BTBSD$Root>.bsd.include.machine.h.bswap
o.btconfig:	<BTBSD$Root>.bsd.include.arm.h.bswap
o.btconfig:	<BTBSD$Root>.bsd.include.arm.h.byte_swap
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.bswap
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.stdint
o.btconfig:	<BTBSD$Root>.bsd.include.machine.h.bswap
o.btconfig:	<BTBSD$Root>.bsd.include.arm.h.bswap
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.stdbool
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.fd_set
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.btconfig:	<BTBSD$Root>.bsd.include.machine.h.int_types
o.btconfig:	<BTBSD$Root>.bsd.include.arm.h.int_types
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.syslimits
o.btconfig:	<BTBSD$Root>.bsd.include.machine.h.param
o.btconfig:	<BTBSD$Root>.bsd.include.arm.arm32.h.param
o.btconfig:	<BTBSD$Root>.bsd.include.machine.h.limits
o.btconfig:	<BTBSD$Root>.bsd.include.arm.h.limits
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.errno
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.time
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.timespec
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.resource
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.ucred
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.uio
o.btconfig:	<BTBSD$Root>.bsd.include.machine.h.ansi
o.btconfig:	<BTBSD$Root>.bsd.include.arm.h.ansi
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_ansi
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.ansi
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.btconfig:	<BTBSD$Root>.bsd.include.uvm.h.uvm_param
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.signal
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.sigtypes
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.btconfig:	<BTBSD$Root>.bsd.include.machine.h.int_types
o.btconfig:	<BTBSD$Root>.bsd.include.arm.h.int_types
o.btconfig:	<BTBSD$Root>.bsd.include.machine.h.ansi
o.btconfig:	<BTBSD$Root>.bsd.include.arm.h.ansi
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_ansi
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.siginfo
o.btconfig:	<BTBSD$Root>.bsd.include.machine.h.signal
o.btconfig:	<BTBSD$Root>.bsd.include.arm.h.signal
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.sigtypes
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.queue
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.ucontext
o.btconfig:	<BTBSD$Root>.bsd.include.machine.h.signal
o.btconfig:	<BTBSD$Root>.bsd.include.arm.h.signal
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.socket
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.ansi
o.btconfig:	<BTBSD$Root>.bsd.include.machine.h.ansi
o.btconfig:	<BTBSD$Root>.bsd.include.arm.h.ansi
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_ansi
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.uio
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.sigtypes
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.btconfig:	<BTBSD$Root>.bsd.lib.libbluetooth.h.bluetooth
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.endian
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.socket
o.btconfig:	<BTBSD$Root>.bsd.sys.netbt.h.bluetooth
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.socket
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
o.btconfig:	<BTBSD$Root>.bsd.sys.netbt.h.hci
o.btconfig:	<BTBSD$Root>.bsd.sys.netbt.h.bluetooth
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.ioccom
o.btconfig:	<BTBSD$Root>.bsd.sys.netbt.h.l2cap
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
o.btconfig:	<BTBSD$Root>.bsd.include.h.netdb
o.btconfig:	<BTBSD$Root>.bsd.include.h.err
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.errno
o.btconfig:	<BTBSD$Root>.bsd.include.h.unistd
o.btconfig:	<BTBSD$Root>.bsd.include.machine.h.ansi
o.btconfig:	<BTBSD$Root>.bsd.include.arm.h.ansi
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_ansi
o.btconfig:	<BTBSD$Root>.bsd.include.machine.h.int_types
o.btconfig:	<BTBSD$Root>.bsd.include.arm.h.int_types
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.unistd
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.btconfig:	<BTBSD$Root>.bsd.include.h.util
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.ansi
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.inttypes
o.btconfig:	<BTBSD$Root>.bsd.sys.sys.sys.h.bsdfix
