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
# Add Common CLib - String That is something else then Clib in Lib
LIBS += ${COMMONLIB}.libc.string.o.strlcpy ${COMMONLIB}.libc.string.o.strcasecmp
# Add LibUtil 
LIBS += ${LIBDIREC}.lib.libutil.o.pidfile ${LIBDIREC}.lib.libutil.o.pid_fix
# Add BSD Fixes
LIBS += ${LIBDIREC}.lib.bsdfix.o.fix


clean::
	${WIPE} ${INSTAPP} ${WFLAGS}

# Dynamic dependencies:
