# Makefile using Automake + Autoconf
# ----------------------------------
# $Id$

# To create statically linked executables (see configure.ac)
CXXLD=$(STATICTOOL) $(CXX)

bin_PROGRAMS=$(STDPROG)
EXTRA_PROGRAMS=FreeFem++-std

# FFCS:visualization stream redirection
FreeFem___std_SOURCES=../mpi/parallelempi-empty.cpp ../../../ffcsstream.cpp
EXTRA_FreeFem___std_SOURCES=../Graphics/Xrgraph.cpp ../Graphics/Pcrgraph.cpp  
FreeFem___std_DEPENDENCIES=../fflib/libff.a ../lglib/liblg.a @STD_GRAPH_OBJ@ 
LDADD=@STD_GRAPH_OBJ@ ../lglib/liblg.a ../fflib/libff.a \
	@UMFPACKLIBS@ @ARPACKLIBS@ @BLASLIBS@ @STD_LIBS@ @LIBSNOCONSOLE@
AM_CPPFLAGS=-I$(srcdir)/../fflib
AM_LDFLAGS=@STD_LDFLAGS@
