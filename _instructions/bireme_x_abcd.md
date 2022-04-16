# Comparison of cisis source codes: Bireme x ABCD 


The report below shows a comparison between the source files of the cisis repository at Bireme and the cisis repository at ABCD.

Some files were modified by Bireme after the changes for modifications to ABCD.



# Different files between versions:
aotmsa2.mak
appeasy.c
b7.mak
changes.txt
chkterm.mak
cib70.h
cib72.c
cicgi.c
cidbx.c
cifm2.c
cifm3.c
cifst.c
cigiz.c
ciifl.c
cirun.h
cisis.h
cisisx.c
ciupdmark.c
ciupdsplt.c
decs9a.mak
decs9b.mak
decsex.mak
fxl0.mak
generateAll64.sh
ifkeys.c
ifkeys.mak
ifp1.mak
ifupd.mak
mdlmf.mak
mkBigIsis_64.xsh
mkffi1660_64.xsh
mkffi512_64.xsh
mkffi512G4_64.xsh
mkffi_64.xsh
mkffiG4_64.xsh
mkisis1660_64.xsh
mkisis_64.xsh
mkisisG_64.xsh
mklind512_64.xsh
mklind512G4_64.xsh
mklind_64.xsh
mklindG4_64.xsh
msrt.c
mx.mak
mxaot.c
mxbol.c
mxget.mak
mxgw.mak
mxrel.c
mxtb.mak
myzcru.mak
mz.mak
splitm.mak
w2.c
wtrig1.mak
wtrig2.mak
wxis.mak
xls
xmk.xsh

# Cisis x Cisis_UTF8

## msrt.c

Line 224
*cisis Bireme:*
`seek = (((off_t)(wcomb-1))<<MSBSHIFT);`


*cisis UTF8*
`seek = (off_t)((wcomb-1)<<MSBSHIFT);`
---

## cigiz.c

Line 631

*cisis Bireme:*
`sprintf((char *)fuplenp,"%08d",fuplen); *(fuplenp+8)=' ';`

*cisis UTF8:*
`sprintf((char *)fuplenp,"%06d",fuplen); *(fuplenp+6)=' ';`

---
## xmk.xsh
cisis Bireme:
Much more content.

cisis_UTF8:
Displays Github conflicts.