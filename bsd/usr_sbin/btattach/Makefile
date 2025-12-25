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
LIBNETBT = <BTBSD$Root>.bsd.sys.
LIBBT = <BTBSD$Root>.bsd.lib.libbluetooth.
# The netbsd include folder
LIBINCL = <BTBSD$Root>.bsd.include


# You need to specify all the files that go into the application directory.
# The shared makefiles handle merging the various subdirectories of the
# Resources directory for you.
INSTAPP_FILES = !Boot !Run !Sprites !Sprites11 !Sprites22 !RunImage

include CApp

CINCLUDES += -ITCPIPLibs:,TCPIPLibs:sys,${LIBBT},${LIBNETBT},${LIBINCL}
|LIBS += ${LIBDIREC}.o.zvectorlib

clean::
	${WIPE} ${INSTAPP} ${WFLAGS}

# Dynamic dependencies:
o.btattach:	c.btattach
o.btattach:	TCPIPLibs:sys.h.cdefs
o.btattach:	TCPIPLibs:sys.h.ioctl
o.btattach:	TCPIPLibs:sys.h.ttycom
o.btattach:	TCPIPLibs:sys.h.ioccom
o.btattach:	TCPIPLibs:sys.h.ioccom
o.btattach:	TCPIPLibs:sys.h.filio
o.btattach:	TCPIPLibs:sys.h.ioccom
o.btattach:	TCPIPLibs:sys.h.sockio
o.btattach:	TCPIPLibs:sys.h.ioccom
o.btattach:	TCPIPLibs:sys.h.cdefs
o.btattach:	TCPIPLibs:sys.h.param
o.btattach:	TCPIPLibs:sys.h.types
o.btattach:	TCPIPLibs:sys.h.cdefs
o.btattach:	TCPIPLibs:machine.h.endian
o.btattach:	TCPIPLibs:machine.h.ansi
o.btattach:	TCPIPLibs:machine.h.types
o.btattach:	TCPIPLibs:sys.h.syslimits
o.btattach:	TCPIPLibs:sys.h.signal
o.btattach:	TCPIPLibs:machine.h.signal
o.btattach:	TCPIPLibs:sys.h.cdefs
o.btattach:	TCPIPLibs:machine.h.param
o.btattach:	TCPIPLibs:machine.h.limits
o.btattach:	TCPIPLibs:sys.h.uio
o.btattach:	TCPIPLibs:sys.h.cdefs
o.btattach:	<BTBSD$Root>.bsd.lib.libbluetooth.h.bluetooth
o.btattach:	TCPIPLibs:sys.h.types
o.btattach:	TCPIPLibs:sys.h.endian
o.btattach:	TCPIPLibs:sys.h.socket
o.btattach:	TCPIPLibs:sys.h.cdefs
o.btattach:	<BTBSD$Root>.bsd.sys.netbt.h.bluetooth
o.btattach:	TCPIPLibs:sys.h.socket
o.btattach:	TCPIPLibs:sys.h.types
o.btattach:	<BTBSD$Root>.bsd.sys.netbt.h.hci
o.btattach:	<BTBSD$Root>.bsd.sys.netbt.h.bluetooth
o.btattach:	TCPIPLibs:sys.h.ioccom
o.btattach:	<BTBSD$Root>.bsd.sys.netbt.h.l2cap
o.btattach:	TCPIPLibs:sys.h.types
o.btattach:	TCPIPLibs:h.netdb
o.btattach:	TCPIPLibs:sys.h.cdefs
o.btattach:	TCPIPLibs:h.err
o.btattach:	TCPIPLibs:machine.h.ansi
o.btattach:	TCPIPLibs:sys.h.cdefs
o.btattach:	TCPIPLibs:sys.h.fcntl
o.btattach:	TCPIPLibs:sys.h.types
o.btattach:	TCPIPLibs:sys.h.cdefs
o.btattach:	TCPIPLibs:sys.h.termios
o.btattach:	TCPIPLibs:sys.h.cdefs
o.btattach:	TCPIPLibs:sys.h.ttycom
o.btattach:	TCPIPLibs:sys.h.ttydefaults
o.btattach:	TCPIPLibs:h.unistd
o.btattach:	TCPIPLibs:sys.h.cdefs
o.btattach:	TCPIPLibs:sys.h.types
o.btattach:	TCPIPLibs:sys.h.unistd
o.btattach:	TCPIPLibs:sys.h._posix
o.btattach:	<BTBSD$Root>.bsd.include.h.util
o.btattach:	TCPIPLibs:sys.h.cdefs
o.btattach:	TCPIPLibs:sys.h.types
o.btattach:	h.btattach
o.btattach:	TCPIPLibs:sys.h.types
