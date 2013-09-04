INCLUDES = -I$(top_srcdir) \
           -I$(top_srcdir)/interface \
           -I$(top_srcdir)/common \
           -I$(top_srcdir)/codecparsers 

libvacodec_decoder_source_c = \
        vaapipicture.cpp \
        vaapidecoder_base.cpp \
        vaapidecoder_h264.cpp \
        vaapidecoder_h264_dpb.cpp \
        vaapidecoder_host.cpp \
        vaapisurfacebuf_pool.cpp \
	$(NULL)

libvacodec_decoder_source_h = \
        vaapipicture.h    \
        vaapidecoder_base.h \
        vaapidecoder_h264.h \
        vaapidecoder_host.h \
        vaapisurfacebuf_pool.h \
	$(NULL)

libvacodec_decoder_ldflags = \
        $(LIBVA_LIBS) \
        $(LIBVA_X11_LIBS) \
        $(NULL)

libvacodec_decoder_cppflags = \
        $(LIBVA_CFLAGS) \
        $(LIBVA_X11_CFLAGS) \
        -fpermissive \
	$(NULL)


lib_LTLIBRARIES			  = libvacodec_decoder.la
libvacodec_decoderincludedir      = $(includedir)/libvacodec_decoder
libvacodec_decoderinclude_HEADERS = $(libvacodec_decoder_source_h)
libvacodec_decoder_la_SOURCES	  = $(libvacodec_decoder_source_c)
libvacodec_decoder_la_LDFLAGS	  = $(libvacodec_decoder_ldflags)
libvacodec_decoder_la_CPPFLAGS    = $(libvacodec_decoder_cppflags)

DISTCLEANFILES = \
	Makefile.in 

