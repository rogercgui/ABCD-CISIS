# Comparison of cisis source codes: Bireme x ABCD

The report below shows a comparison between the source files of the cisis repository at Bireme and the cisis repository at ABCD.

Some files were modified by Bireme after the changes for modifications to ABCD.

# Different files between versions:

1.  aotmsa2.mak
2.  appeasy.c
3.  b7.mak
4.  chkterm.mak
5.  cib70.h
6.  cib72.c
7.  cicgi.c
8.  cidbx.c
9.  cifm2.c
10.  cifm3.c
11.  cifst.c
12.  cigiz.c
13.  ciifl.c
14.  cirun.h
15.  cisis.h
16.  cisisx.c
17.  ciupdmark.c
18.  ciupdsplt.c
19.  decs9a.mak
20.  decs9b.mak
21.  decsex.mak
22.  fxl0.mak
23.  generateAll64.sh
24.  ifkeys.c
25.  ifkeys.mak
26.  ifp1.mak
27.  ifupd.mak
28.  mdlmf.mak
29.  mkBigIsis\_64.xsh
30.  mkffi1660\_64.xsh
31.  mkffi512\_64.xsh
32.  mkffi512G4\_64.xsh
33.  mkffi\_64.xsh
34.  mkffiG4\_64.xsh
35.  mkisis1660\_64.xsh
36.  mkisis\_64.xsh
37.  mkisisG\_64.xsh
38.  mklind512\_64.xsh
39.  mklind512G4\_64.xsh
40.  mklind\_64.xsh
41.  mklindG4\_64.xsh
42.  msrt.c
43.  mx.mak
44.  mxaot.c
45.  mxbol.c
46.  mxget.mak
47.  mxgw.mak
48.  mxrel.c
49.  mxtb.mak
50.  myzcru.mak
51.  mz.mak
52.  splitm.mak
53.  w2.c
54.  wtrig1.mak
55.  wtrig2.mak
56.  wxis.mak
57.  xls
58.  xmk.xsh

# Cisis x Cisis\_UTF8

## msrt.c

### Line 224

  
_**cisis Bireme:**_  
`seek = (((off_t)(wcomb-1))<<MSBSHIFT);`

  
_**cisis UTF8:**_  
`seek = (off_t)((wcomb-1)<<MSBSHIFT);`

### Line 224

_**cisis Bireme:**_  
`seek = (((off_t)(wcomb-1))<<MSBSHIFT);`

_**cisis UTF8**_  
`seek = (off_t)((wcomb-1)<<MSBSHIFT);`

---

## cigiz.c

### Line 563

_cisis Bireme_

```
    sprintf((char *)batchp,"H%u 00000000 ",tag); batchp+=strlen((CONST char *)batchp);
    fuplenp=batchp-1-8; fuplen=0; /* fuplenp points to 00000000 */
```

_cisis UTF8_

```
    sprintf((char *)batchp,"H%u 000000 ",tag); batchp+=strlen((CONST char *)batchp);
    fuplenp=batchp-1-6; fuplen=0; /* fuplenp points to 000000 */
```

### Line 631

_cisis Bireme:_  
`sprintf((char *)fuplenp,"%08d",fuplen); *(fuplenp+8)=' ';`

_cisis UTF8:_  
`sprintf((char *)fuplenp,"%06d",fuplen); *(fuplenp+6)=' ';`

---

## xmk.xsh

cisis Bireme:  
Much more content.

cisis\_UTF8:  
Displays Github conflicts.
