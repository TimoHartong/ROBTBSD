# Makefile for LibProp

COMPONENT = libprop

# The list of source/object files defaults to TARGET, which again is often
# the case for single-file programs. But we don't want our source file to be
# called !RunImage.
OBJS = prop_array prop_array_util prop_bool prop_data prop_dictionary prop_dictionary_util prop_ingest prop_kern prop_number prop_object prop_stack prop_string

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


include CLibrary

#Suppress non ANSI warnings
cflags+=-Wp

CINCLUDES += -I${LIBNETBT},${LIBBT},${LIBINCL},${LIBSYSNTBT}

clean::
	${WIPE} ${INSTAPP} ${WFLAGS}

# Dynamic dependencies:
o.prop_stack:	c.prop_stack
o.prop_stack:	h.prop_object_impl
o.prop_stack:	h.prop_stack
o.prop_stack:	<BTBSD$Root>.bsd.sys.sys.sys.h.queue
o.prop_stack:	<BTBSD$Root>.bsd.include.prop.h.prop_object
o.prop_stack:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
o.prop_stack:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.prop_stack:	<BTBSD$Root>.bsd.include.machine.h.types
o.prop_stack:	<BTBSD$Root>.bsd.include.arm.h.types
o.prop_stack:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.prop_stack:	<BTBSD$Root>.bsd.include.machine.h.cdefs
o.prop_stack:	<BTBSD$Root>.bsd.include.arm.h.cdefs
o.prop_stack:	<BTBSD$Root>.bsd.sys.sys.sys.h.fcntl
o.prop_stack:	<BTBSD$Root>.bsd.sys.sys.sys.h.bsdfix
o.prop_stack:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.prop_stack:	<BTBSD$Root>.bsd.include.arm.h.int_types
o.prop_stack:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_int_types
o.prop_stack:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.prop_stack:	<BTBSD$Root>.bsd.include.machine.h.ansi
o.prop_stack:	<BTBSD$Root>.bsd.include.arm.h.ansi
o.prop_stack:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_ansi
o.prop_stack:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.prop_stack:	<BTBSD$Root>.bsd.include.machine.h.int_types
o.prop_stack:	<BTBSD$Root>.bsd.include.arm.h.int_types
o.prop_stack:	<BTBSD$Root>.bsd.include.machine.h.int_types
o.prop_stack:	<BTBSD$Root>.bsd.include.arm.h.int_types
o.prop_stack:	<BTBSD$Root>.bsd.sys.sys.sys.h.ansi
o.prop_stack:	<BTBSD$Root>.bsd.include.machine.h.ansi
o.prop_stack:	<BTBSD$Root>.bsd.include.arm.h.ansi
o.prop_stack:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_ansi
o.prop_stack:	<BTBSD$Root>.bsd.include.machine.h.endian
o.prop_stack:	<BTBSD$Root>.bsd.sys.sys.sys.h.endian
o.prop_stack:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.prop_stack:	<BTBSD$Root>.bsd.sys.sys.sys.h.ansi
o.prop_stack:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.prop_stack:	<BTBSD$Root>.bsd.sys.sys.sys.h.stdint
o.prop_stack:	<BTBSD$Root>.bsd.include.machine.h.endian_machdep
o.prop_stack:	<BTBSD$Root>.bsd.include.arm.h.endian_machdep
o.prop_stack:	<BTBSD$Root>.bsd.include.machine.h.bswap
o.prop_stack:	<BTBSD$Root>.bsd.include.arm.h.bswap
o.prop_stack:	<BTBSD$Root>.bsd.include.arm.h.byte_swap
o.prop_stack:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
o.prop_stack:	<BTBSD$Root>.bsd.sys.sys.sys.h.bswap
o.prop_stack:	<BTBSD$Root>.bsd.sys.sys.sys.h.stdint
o.prop_stack:	<BTBSD$Root>.bsd.include.machine.h.bswap
o.prop_stack:	<BTBSD$Root>.bsd.include.arm.h.bswap
o.prop_stack:	<BTBSD$Root>.bsd.sys.sys.sys.h.stdbool
o.prop_stack:	<BTBSD$Root>.bsd.sys.sys.sys.h.fd_set
o.prop_stack:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.prop_stack:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.prop_stack:	<BTBSD$Root>.bsd.include.machine.h.int_types
o.prop_stack:	<BTBSD$Root>.bsd.include.arm.h.int_types
o.prop_stack:	h.prop_stack
o.prop_string:	c.prop_string
o.prop_string:	h.prop_object_impl
o.prop_string:	h.prop_stack
o.prop_string:	<BTBSD$Root>.bsd.sys.sys.sys.h.queue
o.prop_string:	<BTBSD$Root>.bsd.include.prop.h.prop_object
o.prop_string:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
o.prop_string:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.prop_string:	<BTBSD$Root>.bsd.include.machine.h.types
o.prop_string:	<BTBSD$Root>.bsd.include.arm.h.types
o.prop_string:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.prop_string:	<BTBSD$Root>.bsd.include.machine.h.cdefs
o.prop_string:	<BTBSD$Root>.bsd.include.arm.h.cdefs
o.prop_string:	<BTBSD$Root>.bsd.sys.sys.sys.h.fcntl
o.prop_string:	<BTBSD$Root>.bsd.sys.sys.sys.h.bsdfix
o.prop_string:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.prop_string:	<BTBSD$Root>.bsd.include.arm.h.int_types
o.prop_string:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_int_types
o.prop_string:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.prop_string:	<BTBSD$Root>.bsd.include.machine.h.ansi
o.prop_string:	<BTBSD$Root>.bsd.include.arm.h.ansi
o.prop_string:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_ansi
o.prop_string:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.prop_string:	<BTBSD$Root>.bsd.include.machine.h.int_types
o.prop_string:	<BTBSD$Root>.bsd.include.arm.h.int_types
o.prop_string:	<BTBSD$Root>.bsd.include.machine.h.int_types
o.prop_string:	<BTBSD$Root>.bsd.include.arm.h.int_types
o.prop_string:	<BTBSD$Root>.bsd.sys.sys.sys.h.ansi
o.prop_string:	<BTBSD$Root>.bsd.include.machine.h.ansi
o.prop_string:	<BTBSD$Root>.bsd.include.arm.h.ansi
o.prop_string:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_ansi
o.prop_string:	<BTBSD$Root>.bsd.include.machine.h.endian
o.prop_string:	<BTBSD$Root>.bsd.sys.sys.sys.h.endian
o.prop_string:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.prop_string:	<BTBSD$Root>.bsd.sys.sys.sys.h.ansi
o.prop_string:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.prop_string:	<BTBSD$Root>.bsd.sys.sys.sys.h.stdint
o.prop_string:	<BTBSD$Root>.bsd.include.machine.h.endian_machdep
o.prop_string:	<BTBSD$Root>.bsd.include.arm.h.endian_machdep
o.prop_string:	<BTBSD$Root>.bsd.include.machine.h.bswap
o.prop_string:	<BTBSD$Root>.bsd.include.arm.h.bswap
o.prop_string:	<BTBSD$Root>.bsd.include.arm.h.byte_swap
o.prop_string:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
o.prop_string:	<BTBSD$Root>.bsd.sys.sys.sys.h.bswap
o.prop_string:	<BTBSD$Root>.bsd.sys.sys.sys.h.stdint
o.prop_string:	<BTBSD$Root>.bsd.include.machine.h.bswap
o.prop_string:	<BTBSD$Root>.bsd.include.arm.h.bswap
o.prop_string:	<BTBSD$Root>.bsd.sys.sys.sys.h.stdbool
o.prop_string:	<BTBSD$Root>.bsd.sys.sys.sys.h.fd_set
o.prop_string:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.prop_string:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.prop_string:	<BTBSD$Root>.bsd.include.machine.h.int_types
o.prop_string:	<BTBSD$Root>.bsd.include.arm.h.int_types
o.prop_string:	<BTBSD$Root>.bsd.include.prop.h.prop_string
o.prop_string:	<BTBSD$Root>.bsd.include.prop.h.prop_object
o.prop_string:	<BTBSD$Root>.bsd.sys.sys.sys.h.rbtree
o.prop_string:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
o.prop_string:	<BTBSD$Root>.bsd.sys.sys.sys.h.queue
o.prop_string:	<BTBSD$Root>.bsd.sys.sys.sys.h.endian
o.prop_string:	<BTBSD$Root>.bsd.sys.sys.sys.h.stdarg
o.prop_string:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.prop_string:	<BTBSD$Root>.bsd.sys.sys.sys.h.ansi
o.prop_string:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.prop_object:	c.prop_object
o.prop_object:	h.prop_object_impl
o.prop_object:	h.prop_stack
o.prop_object:	<BTBSD$Root>.bsd.sys.sys.sys.h.queue
o.prop_object:	<BTBSD$Root>.bsd.include.prop.h.prop_object
o.prop_object:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
o.prop_object:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.prop_object:	<BTBSD$Root>.bsd.include.machine.h.types
o.prop_object:	<BTBSD$Root>.bsd.include.arm.h.types
o.prop_object:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.prop_object:	<BTBSD$Root>.bsd.include.machine.h.cdefs
o.prop_object:	<BTBSD$Root>.bsd.include.arm.h.cdefs
o.prop_object:	<BTBSD$Root>.bsd.sys.sys.sys.h.fcntl
o.prop_object:	<BTBSD$Root>.bsd.sys.sys.sys.h.bsdfix
o.prop_object:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.prop_object:	<BTBSD$Root>.bsd.include.arm.h.int_types
o.prop_object:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_int_types
o.prop_object:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.prop_object:	<BTBSD$Root>.bsd.include.machine.h.ansi
o.prop_object:	<BTBSD$Root>.bsd.include.arm.h.ansi
o.prop_object:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_ansi
o.prop_object:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.prop_object:	<BTBSD$Root>.bsd.include.machine.h.int_types
o.prop_object:	<BTBSD$Root>.bsd.include.arm.h.int_types
o.prop_object:	<BTBSD$Root>.bsd.include.machine.h.int_types
o.prop_object:	<BTBSD$Root>.bsd.include.arm.h.int_types
o.prop_object:	<BTBSD$Root>.bsd.sys.sys.sys.h.ansi
o.prop_object:	<BTBSD$Root>.bsd.include.machine.h.ansi
o.prop_object:	<BTBSD$Root>.bsd.include.arm.h.ansi
o.prop_object:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_ansi
o.prop_object:	<BTBSD$Root>.bsd.include.machine.h.endian
o.prop_object:	<BTBSD$Root>.bsd.sys.sys.sys.h.endian
o.prop_object:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.prop_object:	<BTBSD$Root>.bsd.sys.sys.sys.h.ansi
o.prop_object:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.prop_object:	<BTBSD$Root>.bsd.sys.sys.sys.h.stdint
o.prop_object:	<BTBSD$Root>.bsd.include.machine.h.endian_machdep
o.prop_object:	<BTBSD$Root>.bsd.include.arm.h.endian_machdep
o.prop_object:	<BTBSD$Root>.bsd.include.machine.h.bswap
o.prop_object:	<BTBSD$Root>.bsd.include.arm.h.bswap
o.prop_object:	<BTBSD$Root>.bsd.include.arm.h.byte_swap
o.prop_object:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
o.prop_object:	<BTBSD$Root>.bsd.sys.sys.sys.h.bswap
o.prop_object:	<BTBSD$Root>.bsd.sys.sys.sys.h.stdint
o.prop_object:	<BTBSD$Root>.bsd.include.machine.h.bswap
o.prop_object:	<BTBSD$Root>.bsd.include.arm.h.bswap
o.prop_object:	<BTBSD$Root>.bsd.sys.sys.sys.h.stdbool
o.prop_object:	<BTBSD$Root>.bsd.sys.sys.sys.h.fd_set
o.prop_object:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.prop_object:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.prop_object:	<BTBSD$Root>.bsd.include.machine.h.int_types
o.prop_object:	<BTBSD$Root>.bsd.include.arm.h.int_types
o.prop_object:	<BTBSD$Root>.bsd.include.prop.h.prop_object
o.prop_object:	<BTBSD$Root>.bsd.sys.sys.sys.h.mman
o.prop_object:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.prop_object:	<BTBSD$Root>.bsd.include.machine.h.ansi
o.prop_object:	<BTBSD$Root>.bsd.include.arm.h.ansi
o.prop_object:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_ansi
o.prop_object:	<BTBSD$Root>.bsd.sys.sys.sys.h.ansi
o.prop_object:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.prop_object:	<BTBSD$Root>.bsd.sys.sys.sys.h.stat
o.prop_object:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.prop_object:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
o.prop_object:	<BTBSD$Root>.bsd.sys.sys.sys.h.time
o.prop_object:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.prop_object:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
o.prop_object:	<BTBSD$Root>.bsd.sys.sys.sys.h.timespec
o.prop_object:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.prop_object:	<BTBSD$Root>.bsd.sys.sys.sys.h.errno
o.prop_object:	<BTBSD$Root>.bsd.include.h.fcntl
o.prop_object:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
o.prop_object:	<BTBSD$Root>.bsd.sys.sys.sys.h.stat
o.prop_object:	<BTBSD$Root>.bsd.include.h.unistd
o.prop_object:	<BTBSD$Root>.bsd.include.machine.h.ansi
o.prop_object:	<BTBSD$Root>.bsd.include.arm.h.ansi
o.prop_object:	<BTBSD$Root>.bsd.sys.sys.sys.h.common_ansi
o.prop_object:	<BTBSD$Root>.bsd.include.machine.h.int_types
o.prop_object:	<BTBSD$Root>.bsd.include.arm.h.int_types
o.prop_object:	<BTBSD$Root>.bsd.sys.sys.sys.h.cdefs
o.prop_object:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.prop_object:	<BTBSD$Root>.bsd.sys.sys.sys.h.types
o.prop_object:	<BTBSD$Root>.bsd.sys.sys.sys.h.unistd
o.prop_object:	<BTBSD$Root>.bsd.sys.sys.sys.h.featuretest
o.prop_object:	<BTBSD$Root>.bsd.include.h.unistd
