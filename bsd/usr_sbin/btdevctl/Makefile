# Makefile for btdevctl

COMPONENT = btdevctl

# The name of the linked file defaults to COMPONENT, which is often the case
# for single-file programs. But when the linked file lives in an application
# directory, it is normally called !RunImage.
TARGET = BTDevCtl

# The list of source/object files defaults to TARGET, which again is often
# the case for single-file programs. But we don't want our source file to be
# called !RunImage.
OBJS = btdevctl db print sdp

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

# Includes
CINCLUDES += -I${LIBNETBT},${LIBBT},${LIBINCL},${LIBSYSNTBT},${LIBDIREC}.lib.libusbhid
# Add bluetooth lib
LIBS += ${LIBBT}o.bluetooth 
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
# Add Clib string
LIBS += ${LIBCROOT}.string.o.strdup 
# Add Common CLib - String That is something else then Clib in Lib
LIBS += ${COMMONLIB}.libc.string.o.strlcpy ${COMMONLIB}.libc.string.o.strcasecmp
# Add LibUtil 
LIBS += ${LIBDIREC}.lib.libutil.o.pidfile ${LIBDIREC}.lib.libutil.o.pid_fix
# Add BSD Fixes
LIBS += ${LIBDIREC}.lib.bsdfix.o.fix


clean::
	${WIPE} ${INSTAPP} ${WFLAGS}

# Dynamic dependencies:
o.db:	c.db
o.db:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.db:	<BTBSD$Root>.bsd.include.machine.h.cdefs
o.db:	<BTBSD$Root>.bsd.include.arm.h.cdefs
o.db:	<BTBSD$Root>.bsd.sys.sys.sys.h.fcntl
o.db:	<BTBSD$Root>.bsd.sys.sys.sys.h.bsdfix
o.db:	<BTBSD$Root>.bsd.lib.libbluetooth.h.bluetooth
o.db:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
o.db:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.db:	<BTBSD$Root>.bsd.include.machine.h.types
o.db:	<BTBSD$Root>.bsd.include.arm.h.types
o.db:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.db:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.db:	<BTBSD$Root>.bsd.include.arm.h.int_types
o.db:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_int_types
o.db:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.db:	<BTBSD$Root>.bsd.include.machine.h.ansi
o.db:	<BTBSD$Root>.bsd.include.arm.h.ansi
o.db:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_ansi
o.db:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.db:	<BTBSD$Root>.bsd.include.machine.h.int_types
o.db:	<BTBSD$Root>.bsd.include.arm.h.int_types
o.db:	<BTBSD$Root>.bsd.include.machine.h.int_types
o.db:	<BTBSD$Root>.bsd.include.arm.h.int_types
o.db:	<BTBSD$Root>.bsd.sys.sys.sys.h.ansi
o.db:	<BTBSD$Root>.bsd.include.machine.h.ansi
o.db:	<BTBSD$Root>.bsd.include.arm.h.ansi
o.db:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_ansi
o.db:	<BTBSD$Root>.bsd.include.machine.h.endian
o.db:	<BTBSD$Root>.bsd.sys.sys.sys.h.endian
o.db:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.db:	<BTBSD$Root>.bsd.sys.sys.sys.h.ansi
o.db:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.db:	<BTBSD$Root>.bsd.sys.sys.sys.h.stdint
o.db:	<BTBSD$Root>.bsd.include.machine.h.endian_machdep
o.db:	<BTBSD$Root>.bsd.include.arm.h.endian_machdep
o.db:	<BTBSD$Root>.bsd.include.machine.h.bswap
o.db:	<BTBSD$Root>.bsd.include.arm.h.bswap
o.db:	<BTBSD$Root>.bsd.include.arm.h.byte_swap
o.db:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
o.db:	<BTBSD$Root>.bsd.sys.sys.sys.h.bswap
o.db:	<BTBSD$Root>.bsd.sys.sys.sys.h.stdint
o.db:	<BTBSD$Root>.bsd.include.machine.h.bswap
o.db:	<BTBSD$Root>.bsd.include.arm.h.bswap
o.db:	<BTBSD$Root>.bsd.sys.sys.sys.h.stdbool
o.db:	<BTBSD$Root>.bsd.sys.sys.sys.h.fd_set
o.db:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.db:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.db:	<BTBSD$Root>.bsd.include.machine.h.int_types
o.db:	<BTBSD$Root>.bsd.include.arm.h.int_types
o.db:	<BTBSD$Root>.bsd.sys.sys.sys.h.endian
o.db:	<BTBSD$Root>.bsd.sys.sys.sys.h.socket
o.db:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.db:	<BTBSD$Root>.bsd.sys.sys.sys.h.ansi
o.db:	<BTBSD$Root>.bsd.include.machine.h.ansi
o.db:	<BTBSD$Root>.bsd.include.arm.h.ansi
o.db:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_ansi
o.db:	<BTBSD$Root>.bsd.sys.sys.sys.h.uio
o.db:	<BTBSD$Root>.bsd.include.machine.h.ansi
o.db:	<BTBSD$Root>.bsd.include.arm.h.ansi
o.db:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_ansi
o.db:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.db:	<BTBSD$Root>.bsd.sys.sys.sys.h.ansi
o.db:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.db:	<BTBSD$Root>.bsd.sys.sys.sys.h.sigtypes
o.db:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.db:	<BTBSD$Root>.bsd.include.machine.h.int_types
o.db:	<BTBSD$Root>.bsd.include.arm.h.int_types
o.db:	<BTBSD$Root>.bsd.include.machine.h.ansi
o.db:	<BTBSD$Root>.bsd.include.arm.h.ansi
o.db:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_ansi
o.db:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.db:	<BTBSD$Root>.bsd.sys.netbt.h.bluetooth
o.db:	<BTBSD$Root>.bsd.sys.sys.sys.h.socket
o.db:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
o.db:	<BTBSD$Root>.bsd.sys.netbt.h.hci
o.db:	<BTBSD$Root>.bsd.sys.netbt.h.bluetooth
o.db:	<BTBSD$Root>.bsd.sys.sys.sys.h.ioccom
o.db:	<BTBSD$Root>.bsd.sys.netbt.h.l2cap
o.db:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
o.db:	<BTBSD$Root>.bsd.include.h.netdb
o.db:	<BTBSD$Root>.bsd.include.h.err
o.db:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.db:	<BTBSD$Root>.bsd.include.prop.h.proplib
o.db:	<BTBSD$Root>.bsd.include.prop.h.prop_array
o.db:	<BTBSD$Root>.bsd.include.prop.h.prop_object
o.db:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
o.db:	<BTBSD$Root>.bsd.include.prop.h.prop_bool
o.db:	<BTBSD$Root>.bsd.include.prop.h.prop_object
o.db:	<BTBSD$Root>.bsd.include.prop.h.prop_data
o.db:	<BTBSD$Root>.bsd.include.prop.h.prop_object
o.db:	<BTBSD$Root>.bsd.include.prop.h.prop_dictionary
o.db:	<BTBSD$Root>.bsd.include.prop.h.prop_object
o.db:	<BTBSD$Root>.bsd.include.prop.h.prop_array
o.db:	<BTBSD$Root>.bsd.include.prop.h.prop_number
o.db:	<BTBSD$Root>.bsd.include.prop.h.prop_object
o.db:	<BTBSD$Root>.bsd.include.prop.h.prop_string
o.db:	<BTBSD$Root>.bsd.include.prop.h.prop_object
o.db:	<BTBSD$Root>.bsd.include.prop.h.prop_ingest
o.db:	<BTBSD$Root>.bsd.include.prop.h.prop_dictionary
o.db:	<BTBSD$Root>.bsd.include.prop.h.plistref
o.db:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
o.db:	<BTBSD$Root>.bsd.sys.dev.bluetooth.h.btdev
o.db:	<BTBSD$Root>.bsd.sys.sys.sys.h.ioccom
o.db:	<BTBSD$Root>.bsd.sys.dev.bluetooth.h.bthidev
o.db:	<BTBSD$Root>.bsd.sys.dev.bluetooth.h.btsco
o.db:	<BTBSD$Root>.bsd.sys.sys.sys.h.ioccom
o.db:	<BTBSD$Root>.bsd.sys.netbt.h.bluetooth
o.db:	h.btdevctl
o.print:	c.print
o.print:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.print:	<BTBSD$Root>.bsd.include.machine.h.cdefs
o.print:	<BTBSD$Root>.bsd.include.arm.h.cdefs
o.print:	<BTBSD$Root>.bsd.sys.sys.sys.h.fcntl
o.print:	<BTBSD$Root>.bsd.sys.sys.sys.h.bsdfix
o.print:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
o.print:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.print:	<BTBSD$Root>.bsd.include.machine.h.types
o.print:	<BTBSD$Root>.bsd.include.arm.h.types
o.print:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.print:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.print:	<BTBSD$Root>.bsd.include.arm.h.int_types
o.print:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_int_types
o.print:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.print:	<BTBSD$Root>.bsd.include.machine.h.ansi
o.print:	<BTBSD$Root>.bsd.include.arm.h.ansi
o.print:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_ansi
o.print:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.print:	<BTBSD$Root>.bsd.include.machine.h.int_types
o.print:	<BTBSD$Root>.bsd.include.arm.h.int_types
o.print:	<BTBSD$Root>.bsd.include.machine.h.int_types
o.print:	<BTBSD$Root>.bsd.include.arm.h.int_types
o.print:	<BTBSD$Root>.bsd.sys.sys.sys.h.ansi
o.print:	<BTBSD$Root>.bsd.include.machine.h.ansi
o.print:	<BTBSD$Root>.bsd.include.arm.h.ansi
o.print:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_ansi
o.print:	<BTBSD$Root>.bsd.include.machine.h.endian
o.print:	<BTBSD$Root>.bsd.sys.sys.sys.h.endian
o.print:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.print:	<BTBSD$Root>.bsd.sys.sys.sys.h.ansi
o.print:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.print:	<BTBSD$Root>.bsd.sys.sys.sys.h.stdint
o.print:	<BTBSD$Root>.bsd.include.machine.h.endian_machdep
o.print:	<BTBSD$Root>.bsd.include.arm.h.endian_machdep
o.print:	<BTBSD$Root>.bsd.include.machine.h.bswap
o.print:	<BTBSD$Root>.bsd.include.arm.h.bswap
o.print:	<BTBSD$Root>.bsd.include.arm.h.byte_swap
o.print:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
o.print:	<BTBSD$Root>.bsd.sys.sys.sys.h.bswap
o.print:	<BTBSD$Root>.bsd.sys.sys.sys.h.stdint
o.print:	<BTBSD$Root>.bsd.include.machine.h.bswap
o.print:	<BTBSD$Root>.bsd.include.arm.h.bswap
o.print:	<BTBSD$Root>.bsd.sys.sys.sys.h.stdbool
o.print:	<BTBSD$Root>.bsd.sys.sys.sys.h.fd_set
o.print:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.print:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.print:	<BTBSD$Root>.bsd.include.machine.h.int_types
o.print:	<BTBSD$Root>.bsd.include.arm.h.int_types
o.print:	<BTBSD$Root>.bsd.sys.dev.bluetooth.h.btdev
o.print:	<BTBSD$Root>.bsd.sys.sys.sys.h.ioccom
o.print:	<BTBSD$Root>.bsd.sys.dev.bluetooth.h.bthidev
o.print:	<BTBSD$Root>.bsd.sys.dev.bluetooth.h.btsco
o.print:	<BTBSD$Root>.bsd.sys.sys.sys.h.ioccom
o.print:	<BTBSD$Root>.bsd.sys.netbt.h.bluetooth
o.print:	<BTBSD$Root>.bsd.sys.sys.sys.h.socket
o.print:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.print:	<BTBSD$Root>.bsd.sys.sys.sys.h.ansi
o.print:	<BTBSD$Root>.bsd.include.machine.h.ansi
o.print:	<BTBSD$Root>.bsd.include.arm.h.ansi
o.print:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_ansi
o.print:	<BTBSD$Root>.bsd.sys.sys.sys.h.uio
o.print:	<BTBSD$Root>.bsd.include.machine.h.ansi
o.print:	<BTBSD$Root>.bsd.include.arm.h.ansi
o.print:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_ansi
o.print:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.print:	<BTBSD$Root>.bsd.sys.sys.sys.h.ansi
o.print:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.print:	<BTBSD$Root>.bsd.sys.sys.sys.h.sigtypes
o.print:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.print:	<BTBSD$Root>.bsd.include.machine.h.int_types
o.print:	<BTBSD$Root>.bsd.include.arm.h.int_types
o.print:	<BTBSD$Root>.bsd.include.machine.h.ansi
o.print:	<BTBSD$Root>.bsd.include.arm.h.ansi
o.print:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_ansi
o.print:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.print:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
o.print:	<BTBSD$Root>.bsd.sys.dev.usb.h.usb
o.print:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
o.print:	<BTBSD$Root>.bsd.sys.sys.sys.h.time
o.print:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.print:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
o.print:	<BTBSD$Root>.bsd.sys.sys.sys.h.timespec
o.print:	<BTBSD$Root>.bsd.sys.sys.sys.h.ioctl
o.print:	<BTBSD$Root>.bsd.sys.sys.sys.h.ttycom
o.print:	<BTBSD$Root>.bsd.sys.sys.sys.h.syslimits
o.print:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.print:	<BTBSD$Root>.bsd.sys.sys.sys.h.ioccom
o.print:	<BTBSD$Root>.bsd.sys.sys.sys.h.ioccom
o.print:	<BTBSD$Root>.bsd.sys.sys.sys.h.dkio
o.print:	<BTBSD$Root>.bsd.sys.sys.sys.h.filio
o.print:	<BTBSD$Root>.bsd.sys.sys.sys.h.sockio
o.print:	<BTBSD$Root>.bsd.sys.sys.sys.h.ioccom
o.print:	<BTBSD$Root>.bsd.sys.dev.hid.h.hid
o.print:	<BTBSD$Root>.bsd.include.prop.h.proplib
o.print:	<BTBSD$Root>.bsd.include.prop.h.prop_array
o.print:	<BTBSD$Root>.bsd.include.prop.h.prop_object
o.print:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
o.print:	<BTBSD$Root>.bsd.include.prop.h.prop_bool
o.print:	<BTBSD$Root>.bsd.include.prop.h.prop_object
o.print:	<BTBSD$Root>.bsd.include.prop.h.prop_data
o.print:	<BTBSD$Root>.bsd.include.prop.h.prop_object
o.print:	<BTBSD$Root>.bsd.include.prop.h.prop_dictionary
o.print:	<BTBSD$Root>.bsd.include.prop.h.prop_object
o.print:	<BTBSD$Root>.bsd.include.prop.h.prop_array
o.print:	<BTBSD$Root>.bsd.include.prop.h.prop_number
o.print:	<BTBSD$Root>.bsd.include.prop.h.prop_object
o.print:	<BTBSD$Root>.bsd.include.prop.h.prop_string
o.print:	<BTBSD$Root>.bsd.include.prop.h.prop_object
o.print:	<BTBSD$Root>.bsd.include.prop.h.prop_ingest
o.print:	<BTBSD$Root>.bsd.include.prop.h.prop_dictionary
o.print:	<BTBSD$Root>.bsd.include.prop.h.plistref
o.print:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
o.print:	<BTBSD$Root>.bsd.lib.libbluetooth.h.bluetooth
o.print:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
o.print:	<BTBSD$Root>.bsd.sys.sys.sys.h.endian
o.print:	<BTBSD$Root>.bsd.sys.sys.sys.h.socket
o.print:	<BTBSD$Root>.bsd.sys.netbt.h.bluetooth
o.print:	<BTBSD$Root>.bsd.sys.netbt.h.hci
o.print:	<BTBSD$Root>.bsd.sys.netbt.h.bluetooth
o.print:	<BTBSD$Root>.bsd.sys.sys.sys.h.ioccom
o.print:	<BTBSD$Root>.bsd.sys.netbt.h.l2cap
o.print:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
o.print:	<BTBSD$Root>.bsd.include.h.netdb
o.print:	<BTBSD$Root>.bsd.include.h.err
o.print:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.print:	<BTBSD$Root>.bsd.lib.libusbhid.h.usbhid
o.print:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.print:	h.btdevctl
o.sdp:	c.sdp
o.sdp:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.sdp:	<BTBSD$Root>.bsd.include.machine.h.cdefs
o.sdp:	<BTBSD$Root>.bsd.include.arm.h.cdefs
o.sdp:	<BTBSD$Root>.bsd.sys.sys.sys.h.fcntl
o.sdp:	<BTBSD$Root>.bsd.sys.sys.sys.h.bsdfix
o.sdp:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
o.sdp:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.sdp:	<BTBSD$Root>.bsd.include.machine.h.types
o.sdp:	<BTBSD$Root>.bsd.include.arm.h.types
o.sdp:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.sdp:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.sdp:	<BTBSD$Root>.bsd.include.arm.h.int_types
o.sdp:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_int_types
o.sdp:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.sdp:	<BTBSD$Root>.bsd.include.machine.h.ansi
o.sdp:	<BTBSD$Root>.bsd.include.arm.h.ansi
o.sdp:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_ansi
o.sdp:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.sdp:	<BTBSD$Root>.bsd.include.machine.h.int_types
o.sdp:	<BTBSD$Root>.bsd.include.arm.h.int_types
o.sdp:	<BTBSD$Root>.bsd.include.machine.h.int_types
o.sdp:	<BTBSD$Root>.bsd.include.arm.h.int_types
o.sdp:	<BTBSD$Root>.bsd.sys.sys.sys.h.ansi
o.sdp:	<BTBSD$Root>.bsd.include.machine.h.ansi
o.sdp:	<BTBSD$Root>.bsd.include.arm.h.ansi
o.sdp:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_ansi
o.sdp:	<BTBSD$Root>.bsd.include.machine.h.endian
o.sdp:	<BTBSD$Root>.bsd.sys.sys.sys.h.endian
o.sdp:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.sdp:	<BTBSD$Root>.bsd.sys.sys.sys.h.ansi
o.sdp:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.sdp:	<BTBSD$Root>.bsd.sys.sys.sys.h.stdint
o.sdp:	<BTBSD$Root>.bsd.include.machine.h.endian_machdep
o.sdp:	<BTBSD$Root>.bsd.include.arm.h.endian_machdep
o.sdp:	<BTBSD$Root>.bsd.include.machine.h.bswap
o.sdp:	<BTBSD$Root>.bsd.include.arm.h.bswap
o.sdp:	<BTBSD$Root>.bsd.include.arm.h.byte_swap
o.sdp:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
o.sdp:	<BTBSD$Root>.bsd.sys.sys.sys.h.bswap
o.sdp:	<BTBSD$Root>.bsd.sys.sys.sys.h.stdint
o.sdp:	<BTBSD$Root>.bsd.include.machine.h.bswap
o.sdp:	<BTBSD$Root>.bsd.include.arm.h.bswap
o.sdp:	<BTBSD$Root>.bsd.sys.sys.sys.h.stdbool
o.sdp:	<BTBSD$Root>.bsd.sys.sys.sys.h.fd_set
o.sdp:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.sdp:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.sdp:	<BTBSD$Root>.bsd.include.machine.h.int_types
o.sdp:	<BTBSD$Root>.bsd.include.arm.h.int_types
o.sdp:	<BTBSD$Root>.bsd.sys.dev.bluetooth.h.btdev
o.sdp:	<BTBSD$Root>.bsd.sys.sys.sys.h.ioccom
o.sdp:	<BTBSD$Root>.bsd.sys.dev.bluetooth.h.bthidev
o.sdp:	<BTBSD$Root>.bsd.sys.dev.bluetooth.h.btsco
o.sdp:	<BTBSD$Root>.bsd.sys.sys.sys.h.ioccom
o.sdp:	<BTBSD$Root>.bsd.sys.netbt.h.bluetooth
o.sdp:	<BTBSD$Root>.bsd.sys.sys.sys.h.socket
o.sdp:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.sdp:	<BTBSD$Root>.bsd.sys.sys.sys.h.ansi
o.sdp:	<BTBSD$Root>.bsd.include.machine.h.ansi
o.sdp:	<BTBSD$Root>.bsd.include.arm.h.ansi
o.sdp:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_ansi
o.sdp:	<BTBSD$Root>.bsd.sys.sys.sys.h.uio
o.sdp:	<BTBSD$Root>.bsd.include.machine.h.ansi
o.sdp:	<BTBSD$Root>.bsd.include.arm.h.ansi
o.sdp:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_ansi
o.sdp:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.sdp:	<BTBSD$Root>.bsd.sys.sys.sys.h.ansi
o.sdp:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.sdp:	<BTBSD$Root>.bsd.sys.sys.sys.h.sigtypes
o.sdp:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.sdp:	<BTBSD$Root>.bsd.include.machine.h.int_types
o.sdp:	<BTBSD$Root>.bsd.include.arm.h.int_types
o.sdp:	<BTBSD$Root>.bsd.include.machine.h.ansi
o.sdp:	<BTBSD$Root>.bsd.include.arm.h.ansi
o.sdp:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_ansi
o.sdp:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.sdp:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
o.sdp:	<BTBSD$Root>.bsd.sys.dev.usb.h.usb
o.sdp:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
o.sdp:	<BTBSD$Root>.bsd.sys.sys.sys.h.time
o.sdp:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.sdp:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
o.sdp:	<BTBSD$Root>.bsd.sys.sys.sys.h.timespec
o.sdp:	<BTBSD$Root>.bsd.sys.sys.sys.h.ioctl
o.sdp:	<BTBSD$Root>.bsd.sys.sys.sys.h.ttycom
o.sdp:	<BTBSD$Root>.bsd.sys.sys.sys.h.syslimits
o.sdp:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.sdp:	<BTBSD$Root>.bsd.sys.sys.sys.h.ioccom
o.sdp:	<BTBSD$Root>.bsd.sys.sys.sys.h.ioccom
o.sdp:	<BTBSD$Root>.bsd.sys.sys.sys.h.dkio
o.sdp:	<BTBSD$Root>.bsd.sys.sys.sys.h.filio
o.sdp:	<BTBSD$Root>.bsd.sys.sys.sys.h.sockio
o.sdp:	<BTBSD$Root>.bsd.sys.sys.sys.h.ioccom
o.sdp:	<BTBSD$Root>.bsd.sys.dev.usb.h.usbhid
o.sdp:	<BTBSD$Root>.bsd.sys.dev.hid.h.hid
o.sdp:	<BTBSD$Root>.bsd.sys.sys.sys.h.ioccom
o.sdp:	<BTBSD$Root>.bsd.sys.dev.hid.h.hid
o.sdp:	<BTBSD$Root>.bsd.include.prop.h.proplib
o.sdp:	<BTBSD$Root>.bsd.include.prop.h.prop_array
o.sdp:	<BTBSD$Root>.bsd.include.prop.h.prop_object
o.sdp:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
o.sdp:	<BTBSD$Root>.bsd.include.prop.h.prop_bool
o.sdp:	<BTBSD$Root>.bsd.include.prop.h.prop_object
o.sdp:	<BTBSD$Root>.bsd.include.prop.h.prop_data
o.sdp:	<BTBSD$Root>.bsd.include.prop.h.prop_object
o.sdp:	<BTBSD$Root>.bsd.include.prop.h.prop_dictionary
o.sdp:	<BTBSD$Root>.bsd.include.prop.h.prop_object
o.sdp:	<BTBSD$Root>.bsd.include.prop.h.prop_array
o.sdp:	<BTBSD$Root>.bsd.include.prop.h.prop_number
o.sdp:	<BTBSD$Root>.bsd.include.prop.h.prop_object
o.sdp:	<BTBSD$Root>.bsd.include.prop.h.prop_string
o.sdp:	<BTBSD$Root>.bsd.include.prop.h.prop_object
o.sdp:	<BTBSD$Root>.bsd.include.prop.h.prop_ingest
o.sdp:	<BTBSD$Root>.bsd.include.prop.h.prop_dictionary
o.sdp:	<BTBSD$Root>.bsd.include.prop.h.plistref
o.sdp:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
o.sdp:	<BTBSD$Root>.bsd.lib.libbluetooth.h.bluetooth
o.sdp:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
o.sdp:	<BTBSD$Root>.bsd.sys.sys.sys.h.endian
o.sdp:	<BTBSD$Root>.bsd.sys.sys.sys.h.socket
o.sdp:	<BTBSD$Root>.bsd.sys.netbt.h.bluetooth
o.sdp:	<BTBSD$Root>.bsd.sys.netbt.h.hci
o.sdp:	<BTBSD$Root>.bsd.sys.netbt.h.bluetooth
o.sdp:	<BTBSD$Root>.bsd.sys.sys.sys.h.ioccom
o.sdp:	<BTBSD$Root>.bsd.sys.netbt.h.l2cap
o.sdp:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
o.sdp:	<BTBSD$Root>.bsd.include.h.netdb
o.sdp:	<BTBSD$Root>.bsd.include.h.err
o.sdp:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.sdp:	<BTBSD$Root>.bsd.sys.sys.sys.h.errno
o.sdp:	<BTBSD$Root>.bsd.lib.libbluetooth.h.sdp
o.sdp:	<BTBSD$Root>.bsd.include.h.uuid
o.sdp:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
o.sdp:	<BTBSD$Root>.bsd.sys.sys.sys.h.uuid
o.sdp:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.sdp:	<BTBSD$Root>.bsd.sys.sys.sys.h.stdint
o.sdp:	<BTBSD$Root>.bsd.lib.libbluetooth.h.bluetooth
o.sdp:	<BTBSD$Root>.bsd.include.h.strings
o.sdp:	<BTBSD$Root>.bsd.include.machine.h.ansi
o.sdp:	<BTBSD$Root>.bsd.include.arm.h.ansi
o.sdp:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_ansi
o.sdp:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.sdp:	<BTBSD$Root>.bsd.lib.libusbhid.h.usbhid
o.sdp:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.sdp:	h.btdevctl
o.btdevctl:	c.btdevctl
o.btdevctl:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.btdevctl:	<BTBSD$Root>.bsd.include.machine.h.cdefs
o.btdevctl:	<BTBSD$Root>.bsd.include.arm.h.cdefs
o.btdevctl:	<BTBSD$Root>.bsd.sys.sys.sys.h.fcntl
o.btdevctl:	<BTBSD$Root>.bsd.sys.sys.sys.h.bsdfix
o.btdevctl:	<BTBSD$Root>.bsd.include.prop.h.proplib
o.btdevctl:	<BTBSD$Root>.bsd.include.prop.h.prop_array
o.btdevctl:	<BTBSD$Root>.bsd.include.prop.h.prop_object
o.btdevctl:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
o.btdevctl:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.btdevctl:	<BTBSD$Root>.bsd.include.machine.h.types
o.btdevctl:	<BTBSD$Root>.bsd.include.arm.h.types
o.btdevctl:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.btdevctl:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.btdevctl:	<BTBSD$Root>.bsd.include.arm.h.int_types
o.btdevctl:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_int_types
o.btdevctl:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.btdevctl:	<BTBSD$Root>.bsd.include.machine.h.ansi
o.btdevctl:	<BTBSD$Root>.bsd.include.arm.h.ansi
o.btdevctl:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_ansi
o.btdevctl:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.btdevctl:	<BTBSD$Root>.bsd.include.machine.h.int_types
o.btdevctl:	<BTBSD$Root>.bsd.include.arm.h.int_types
o.btdevctl:	<BTBSD$Root>.bsd.include.machine.h.int_types
o.btdevctl:	<BTBSD$Root>.bsd.include.arm.h.int_types
o.btdevctl:	<BTBSD$Root>.bsd.sys.sys.sys.h.ansi
o.btdevctl:	<BTBSD$Root>.bsd.include.machine.h.ansi
o.btdevctl:	<BTBSD$Root>.bsd.include.arm.h.ansi
o.btdevctl:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_ansi
o.btdevctl:	<BTBSD$Root>.bsd.include.machine.h.endian
o.btdevctl:	<BTBSD$Root>.bsd.sys.sys.sys.h.endian
o.btdevctl:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.btdevctl:	<BTBSD$Root>.bsd.sys.sys.sys.h.ansi
o.btdevctl:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.btdevctl:	<BTBSD$Root>.bsd.sys.sys.sys.h.stdint
o.btdevctl:	<BTBSD$Root>.bsd.include.machine.h.endian_machdep
o.btdevctl:	<BTBSD$Root>.bsd.include.arm.h.endian_machdep
o.btdevctl:	<BTBSD$Root>.bsd.include.machine.h.bswap
o.btdevctl:	<BTBSD$Root>.bsd.include.arm.h.bswap
o.btdevctl:	<BTBSD$Root>.bsd.include.arm.h.byte_swap
o.btdevctl:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
o.btdevctl:	<BTBSD$Root>.bsd.sys.sys.sys.h.bswap
o.btdevctl:	<BTBSD$Root>.bsd.sys.sys.sys.h.stdint
o.btdevctl:	<BTBSD$Root>.bsd.include.machine.h.bswap
o.btdevctl:	<BTBSD$Root>.bsd.include.arm.h.bswap
o.btdevctl:	<BTBSD$Root>.bsd.sys.sys.sys.h.stdbool
o.btdevctl:	<BTBSD$Root>.bsd.sys.sys.sys.h.fd_set
o.btdevctl:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.btdevctl:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.btdevctl:	<BTBSD$Root>.bsd.include.machine.h.int_types
o.btdevctl:	<BTBSD$Root>.bsd.include.arm.h.int_types
o.btdevctl:	<BTBSD$Root>.bsd.include.prop.h.prop_bool
o.btdevctl:	<BTBSD$Root>.bsd.include.prop.h.prop_object
o.btdevctl:	<BTBSD$Root>.bsd.include.prop.h.prop_data
o.btdevctl:	<BTBSD$Root>.bsd.include.prop.h.prop_object
o.btdevctl:	<BTBSD$Root>.bsd.include.prop.h.prop_dictionary
o.btdevctl:	<BTBSD$Root>.bsd.include.prop.h.prop_object
o.btdevctl:	<BTBSD$Root>.bsd.include.prop.h.prop_array
o.btdevctl:	<BTBSD$Root>.bsd.include.prop.h.prop_number
o.btdevctl:	<BTBSD$Root>.bsd.include.prop.h.prop_object
o.btdevctl:	<BTBSD$Root>.bsd.include.prop.h.prop_string
o.btdevctl:	<BTBSD$Root>.bsd.include.prop.h.prop_object
o.btdevctl:	<BTBSD$Root>.bsd.include.prop.h.prop_ingest
o.btdevctl:	<BTBSD$Root>.bsd.include.prop.h.prop_dictionary
o.btdevctl:	<BTBSD$Root>.bsd.include.prop.h.plistref
o.btdevctl:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
o.btdevctl:	<BTBSD$Root>.bsd.sys.sys.sys.h.ioctl
o.btdevctl:	<BTBSD$Root>.bsd.sys.sys.sys.h.ttycom
o.btdevctl:	<BTBSD$Root>.bsd.sys.sys.sys.h.syslimits
o.btdevctl:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.btdevctl:	<BTBSD$Root>.bsd.sys.sys.sys.h.ioccom
o.btdevctl:	<BTBSD$Root>.bsd.sys.sys.sys.h.ioccom
o.btdevctl:	<BTBSD$Root>.bsd.sys.sys.sys.h.dkio
o.btdevctl:	<BTBSD$Root>.bsd.sys.sys.sys.h.filio
o.btdevctl:	<BTBSD$Root>.bsd.sys.sys.sys.h.sockio
o.btdevctl:	<BTBSD$Root>.bsd.sys.sys.sys.h.ioccom
o.btdevctl:	<BTBSD$Root>.bsd.lib.libbluetooth.h.bluetooth
o.btdevctl:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
o.btdevctl:	<BTBSD$Root>.bsd.sys.sys.sys.h.endian
o.btdevctl:	<BTBSD$Root>.bsd.sys.sys.sys.h.socket
o.btdevctl:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.btdevctl:	<BTBSD$Root>.bsd.sys.sys.sys.h.ansi
o.btdevctl:	<BTBSD$Root>.bsd.include.machine.h.ansi
o.btdevctl:	<BTBSD$Root>.bsd.include.arm.h.ansi
o.btdevctl:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_ansi
o.btdevctl:	<BTBSD$Root>.bsd.sys.sys.sys.h.uio
o.btdevctl:	<BTBSD$Root>.bsd.include.machine.h.ansi
o.btdevctl:	<BTBSD$Root>.bsd.include.arm.h.ansi
o.btdevctl:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_ansi
o.btdevctl:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.btdevctl:	<BTBSD$Root>.bsd.sys.sys.sys.h.ansi
o.btdevctl:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.btdevctl:	<BTBSD$Root>.bsd.sys.sys.sys.h.sigtypes
o.btdevctl:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.btdevctl:	<BTBSD$Root>.bsd.include.machine.h.int_types
o.btdevctl:	<BTBSD$Root>.bsd.include.arm.h.int_types
o.btdevctl:	<BTBSD$Root>.bsd.include.machine.h.ansi
o.btdevctl:	<BTBSD$Root>.bsd.include.arm.h.ansi
o.btdevctl:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_ansi
o.btdevctl:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.btdevctl:	<BTBSD$Root>.bsd.sys.netbt.h.bluetooth
o.btdevctl:	<BTBSD$Root>.bsd.sys.sys.sys.h.socket
o.btdevctl:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
o.btdevctl:	<BTBSD$Root>.bsd.sys.netbt.h.hci
o.btdevctl:	<BTBSD$Root>.bsd.sys.netbt.h.bluetooth
o.btdevctl:	<BTBSD$Root>.bsd.sys.sys.sys.h.ioccom
o.btdevctl:	<BTBSD$Root>.bsd.sys.netbt.h.l2cap
o.btdevctl:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
o.btdevctl:	<BTBSD$Root>.bsd.include.h.netdb
o.btdevctl:	<BTBSD$Root>.bsd.include.h.err
o.btdevctl:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.btdevctl:	<BTBSD$Root>.bsd.include.h.fcntl
o.btdevctl:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
o.btdevctl:	<BTBSD$Root>.bsd.sys.sys.sys.h.stat
o.btdevctl:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.btdevctl:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
o.btdevctl:	<BTBSD$Root>.bsd.sys.sys.sys.h.time
o.btdevctl:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.btdevctl:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
o.btdevctl:	<BTBSD$Root>.bsd.sys.sys.sys.h.timespec
o.btdevctl:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.btdevctl:	<BTBSD$Root>.bsd.include.h.unistd
o.btdevctl:	<BTBSD$Root>.bsd.include.machine.h.ansi
o.btdevctl:	<BTBSD$Root>.bsd.include.arm.h.ansi
o.btdevctl:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_ansi
o.btdevctl:	<BTBSD$Root>.bsd.include.machine.h.int_types
o.btdevctl:	<BTBSD$Root>.bsd.include.arm.h.int_types
o.btdevctl:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.btdevctl:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.btdevctl:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
o.btdevctl:	<BTBSD$Root>.bsd.sys.sys.sys.h.unistd
o.btdevctl:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.btdevctl:	<BTBSD$Root>.bsd.include.h.unistd
o.btdevctl:	<BTBSD$Root>.bsd.sys.dev.bluetooth.h.btdev
o.btdevctl:	<BTBSD$Root>.bsd.sys.sys.sys.h.ioccom
o.btdevctl:	h.btdevctl
