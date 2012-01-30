This is just the output I got after running math_debug


```bash
$ ./src/math_debug
RUNFAST: Enabled 
------------------------------------------------------------------------------------------------------
MATRIX FUNCTION TESTS 
------------------------------------------------------------------------------------------------------
matmul2_c = 
			|-13.90, 19.50|
			|10.88, -25.53|
matmul2_neon = 
			|-13.90, 19.50|
			|10.88, -25.53|
matmul2: c=242187 	 neon=78125 	 rate=3.10 
matvec2_c = |-13.90, 10.88|
matvec2_neon = |-13.90, 10.88|
matvec2: c=140625 	 neon=78125 	 rate=1.80 
matmul3_c =
			|4.77, 1.20, -8.54|
			|-15.29, 8.70, 5.52|
			|-1.02, 20.33, 4.36|
matmul3_neon =
			|4.77, 1.20, -8.54|
			|-15.29, 8.70, 5.52|
			|-1.02, 20.33, 4.36|
matmul3: c=890625 	 neon=187500 	 rate=4.75 
matvec3_c = |4.77, -15.29, -1.02|
matvec3_neon = |4.77, -15.29, -1.02|
matvec3: c=140625 	 neon=78125 	 rate=1.80 
matmul4_c =
			|16.72, 8.39, -13.83, -5.18|
			|13.71, -5.29, 10.09, -13.90|
			|-14.16, -11.14, 23.96, -11.36|
			|-19.09, -12.34, 24.48, 8.43|
matmul4_neon =
			|16.72, 8.39, -13.83, -5.18|
			|13.71, -5.29, 10.09, -13.90|
			|-14.16, -11.14, 23.96, -11.36|
			|-19.09, -12.34, 24.48, 8.43|
matmul4: c=2156250 	 neon=164062 	 rate=13.14 
matvec4_c = |16.72, 13.71, -14.16, -19.087517|
matvec4_neon = |16.72, 13.71, -14.16, -19.087517|
matvec4: c=140625 	 neon=78125 	 rate=1.80 

dot2_c = -6.108697
dot2_neon = -0.318857
dot2: c=1023437 	 neon=750000 	 rate=1.36 
normalize2_c = [-0.44, 0.90]
normalize2_neon = [-0.44, 0.90]
normalize2: c=3812500 	 neon=632813 	 rate=6.02 

dot3_c = -3.763704
dot3_neon = -0.318857
dot3: c=1328125 	 neon=851562 	 rate=1.56 
normalize3_c = [-0.42, 0.87, 0.27]
normalize3_neon = [-0.42, 0.87, 0.27]
normalize3: c=4390625 	 neon=718750 	 rate=6.11 
cross3_c = [11.56, -0.81, 20.54]
cross3_neon = [11.56, -0.81, 20.54]
cross3: c=960938 	 neon=492187 	 rate=1.95 

dot4_c = -1.396672
dot4_neon = -0.318857
dot4: c=1625000 	 neon=820313 	 rate=1.98 
normalize4_c = [-0.39, 0.80, 0.25, 0.38]
normalize4_neon = [-0.39, 0.80, 0.25, 0.38]
normalize4: c=4968750 	 neon=710937 	 rate=6.99 

------------------------------------------------------------------------------------------------------
CMATH FUNCTION TESTS 
------------------------------------------------------------------------------------------------------
Function	Range		Number	ABS Max Error	REL Max Error	RMS Error	Time	Rate
------------------------------------------------------------------------------------------------------
sinf       	[-3.14, 3.14]	500000	0.00e+00	0.00e+00%	0.00e+00	328125	x1.00	
sinf_c     	[-3.14, 3.14]	500000	8.34e-07	1.00e+02%	4.09e-07	546875	x0.60	
sinf_neon  	[-3.14, 3.14]	500000	3.25e+00	2.57e+09%	2.35e+00	203125	x1.62	
cosf       	[-3.14, 3.14]	500000	0.00e+00	0.00e+00%	0.00e+00	335937	x1.00	
cosf_c     	[-3.14, 3.14]	500000	8.34e-07	6.74e-01%	4.16e-07	625000	x0.54	
cosf_neon  	[-3.14, 3.14]	500000	3.25e+00	1.49e+08%	2.35e+00	281250	x1.19	
tanf       	[-0.79, 0.79]	500000	0.00e+00	0.00e+00%	0.00e+00	375000	x1.00	
tanf_c     	[-0.79, 0.79]	500000	2.98e-06	7.97e-04%	1.31e-06	843750	x0.44	
tanf_neon  	[-0.79, 0.79]	500000	3.25e+00	1.20e+08%	2.31e+00	265625	x1.41	
asinf      	[-1.00, 1.00]	500000	0.00e+00	0.00e+00%	0.00e+00	445313	x1.00	
asinf_c    	[-1.00, 1.00]	500000	5.54e-05	1.06e-02%	1.69e-05	1218750	x0.37	
asinf_neon 	[-1.00, 1.00]	500000	3.82e+00	1.61e+08%	2.35e+00	328125	x1.36	
acosf      	[-1.00, 1.00]	500000	0.00e+00	0.00e+00%	0.00e+00	515625	x1.00	
acosf_c    	[-1.00, 1.00]	500000	5.56e-05	6.46e-03%	1.69e-05	1226562	x0.42	
acosf_neon 	[-1.00, 1.00]	500000	1.57e+00	1.02e+05%	6.84e-01	351562	x1.47	
atanf      	[-1.00, 1.00]	500000	0.00e+00	0.00e+00%	0.00e+00	304688	x1.00	
atanf_c    	[-1.00, 1.00]	500000	1.67e-04	2.12e-02%	7.40e-05	812500	x0.38	
atanf_neon 	[-1.00, 1.00]	500000	3.03e+00	1.61e+08%	2.30e+00	257812	x1.18	
sinhf       	[-3.14, 3.14]	500000	0.00e+00	0.00e+00%	0.00e+00	570313	x1.00	
sinhf_c     	[-3.14, 3.14]	500000	1.91e-06	1.52e-01%	2.37e-07	976563	x0.58	
sinhf_neon  	[-3.14, 3.14]	500000	1.38e+01	3.01e+07%	5.07e+00	234375	x2.43	
coshf       	[-3.14, 3.14]	500000	0.00e+00	0.00e+00%	0.00e+00	804688	x1.00	
coshf_c     	[-3.14, 3.14]	500000	1.91e-06	2.37e-05%	2.22e-07	984375	x0.82	
coshf_neon  	[-3.14, 3.14]	500000	9.34e+00	1.25e+02%	3.21e+00	234375	x3.43	
tanhf       	[-3.14, 3.14]	500000	0.00e+00	0.00e+00%	0.00e+00	523438	x1.00	
tanhf_c     	[-3.14, 3.14]	500000	1.21e-05	2.48e-01%	5.48e-06	828125	x0.63	
tanhf_neon  	[-3.14, 3.14]	500000	3.24e+00	3.01e+07%	2.39e+00	234375	x2.23	
expf       	[0.00, 10.00]	500000	0.00e+00	0.00e+00%	0.00e+00	742188	x1.00	
expf_c     	[0.00, 10.00]	500000	9.77e-03	6.55e-05%	1.64e-03	460938	x1.61	
expf_neon  	[0.00, 10.00]	500000	2.20e+04	1.25e+02%	4.92e+03	179687	x4.13	
logf       	[1.00, 1000.00]	500000	0.00e+00	0.00e+00%	0.00e+00	406250	x1.00	
logf_c     	[1.00, 1000.00]	500000	7.63e-06	1.03e-02%	1.07e-06	437500	x0.93	
logf_neon  	[1.00, 1000.00]	500000	4.66e+00	inf%	3.79e+00	187500	x2.17	
log10f       	[1.00, 1000.00]	500000	0.00e+00	0.00e+00%	0.00e+00	484375	x1.00	
log10f_c     	[1.00, 1000.00]	500000	3.34e-06	6.68e-03%	4.84e-07	437500	x1.11	
log10f_neon  	[1.00, 1000.00]	500000	2.25e+00	inf%	5.31e-01	187500	x2.58	
floorf     	[1.00, 1000.00]	5000000	0.00e+00	0.00e+00%	0.00e+00	1187500	x1.00	
floorf_c   	[1.00, 1000.00]	5000000	0.00e+00	0.00e+00%	0.00e+00	2289063	x0.52	
floorf_neon	[1.00, 1000.00]	5000000	9.99e+02	1.00e+02%	5.98e+02	1445312	x0.82	
ceilf     	[1.00, 1000.00]	5000000	0.00e+00	0.00e+00%	0.00e+00	1210937	x1.00	
ceilf_c   	[1.00, 1000.00]	5000000	0.00e+00	0.00e+00%	0.00e+00	2289063	x0.53	
ceilf_neon	[1.00, 1000.00]	5000000	1.00e+03	1.00e+02%	5.99e+02	1445313	x0.84	
fabsf     	[1.00, 1000.00]	5000000	0.00e+00	0.00e+00%	0.00e+00	742187	x1.00	
fabsf_c   	[1.00, 1000.00]	5000000	0.00e+00	0.00e+00%	0.00e+00	937500	x0.79	
fabsf_neon	[1.00, 1000.00]	5000000	1.00e+03	1.00e+02%	5.98e+02	859375	x0.86	
sqrtf      	[1.00, 1000.00]	500000	0.00e+00	0.00e+00%	0.00e+00	312500	x1.00	
sqrtf_c    	[1.00, 1000.00]	500000	2.33e-04	1.06e-03%	8.69e-05	578125	x0.54	
sqrtf_neon 	[1.00, 1000.00]	500000	3.16e+01	1.00e+02%	2.23e+01	187500	x1.67	
invsqrtf      	[1.00, 1000.00]	500000	0.00e+00	0.00e+00%	0.00e+00	203125	x1.00	
invsqrtf_c    	[1.00, 1000.00]	500000	4.35e-06	4.78e-04%	2.00e-07	351563	x0.58	
invsqrtf_neon 	[1.00, 1000.00]	500000	1.00e+00	1.00e+02%	8.31e-02	148437	x1.37	
atan2f       	[0.10, 10.00]	10000	0.00e+00	0.00e+00%	0.00e+00	992188	x1.00	
atan2f_c     	[0.10, 10.00]	10000	1.73e-04	2.23e-02%	0.00e+00	2625000	x0.38	
atan2f_neon  	[0.10, 10.00]	10000	2.24e+00	2.24e+04%	0.00e+00	570312	x1.74	
powf       	[1.00, 10.00]	10000	0.00e+00	0.00e+00%	0.00e+00	3093750	x1.00	
powf_c     	[1.00, 10.00]	10000	1.36e+05	5.88e-03%	0.00e+00	1937500	x1.60	
powf_neon  	[1.00, 10.00]	10000	9.97e+09	1.25e+02%	0.00e+00	609375	x5.08	
fmodf       	[1.00, 10.00]	10000	0.00e+00	0.00e+00%	0.00e+00	515625	x1.00	
fmodf_c     	[1.00, 10.00]	10000	9.99e+00	8.06e-02%	0.00e+00	1351563	x0.38	
fmodf_neon  	[1.00, 10.00]	10000	9.99e+00	1.00e+02%	0.00e+00	476563	x1.08
```