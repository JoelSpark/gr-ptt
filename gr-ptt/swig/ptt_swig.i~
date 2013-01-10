/* -*- c++ -*- */

#define PTT_API

%include "gnuradio.i"			// the common stuff

%{
#include "ptt_PTT.h"
%}

GR_SWIG_BLOCK_MAGIC(ptt,PTT);
%include "ptt_PTT.h"

#if SWIGGUILE
%scheme %{
(load-extension-global "libguile-gnuradio-ptt_swig" "scm_init_gnuradio_ptt_swig_module")
%}

%goops %{
(use-modules (gnuradio gnuradio_core_runtime))
%}
#endif
