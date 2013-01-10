/* -*- c++ -*- */
/* 
 * Copyright 2013 <+YOU OR YOUR COMPANY+>.
 * 
 * This is free software; you can redistribute it and/or modify
 * it under the terms of the GNU General Public License as published by
 * the Free Software Foundation; either version 3, or (at your option)
 * any later version.
 * 
 * This software is distributed in the hope that it will be useful,
 * but WITHOUT ANY WARRANTY; without even the implied warranty of
 * MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 * GNU General Public License for more details.
 * 
 * You should have received a copy of the GNU General Public License
 * along with this software; see the file COPYING.  If not, write to
 * the Free Software Foundation, Inc., 51 Franklin Street,
 * Boston, MA 02110-1301, USA.
 */

#ifndef INCLUDED_PTT_PTT_H
#define INCLUDED_PTT_PTT_H

#include <ptt_api.h>
#include <gr_block.h>

//*********************************PROTOTYPE CLASS DEFINITIONS*********************************//
class ptt_PTT;
typedef boost::shared_ptr<ptt_PTT> ptt_PTT_sptr;


//*********************************SPTR AND MAKE_PTT CLASS DEFINITION PROTOTYPE****************//
PTT_API ptt_PTT_sptr ptt_make_PTT(float k=1);
// PTT_API defined w/ preprocessor statements in ptt_api.h as either __GR_ATTR_EXPORT or __GR_ATTR_IMPORT


//*********************************ptt_PTT CLASS DEFINITION************************************//
class PTT_API ptt_PTT : public gr_block
{
 private:
	friend PTT_API ptt_PTT_sptr ptt_make_PTT(float k);
	ptt_PTT (float k);  //<-- PRIVATE CONSTRUCTOR
	float d_k;

 public:
	~ptt_PTT (); //<-- PUBLIC DECONSTRUCTOR
	float k();
	void set_k(float k);

 virtual int general_work (int noutput_items,
		    gr_vector_int &ninput_items,
		    gr_vector_const_void_star &input_items,
		    gr_vector_void_star &output_items);
};

#endif /* INCLUDED_PTT_PTT_H */

