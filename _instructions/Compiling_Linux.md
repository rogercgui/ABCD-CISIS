# Compiling CISIS in Linux



1. ./generateAll642.sh
- deletes all .o files
- deletes all mk*.sh files
- deletes xmk file
- deletes xls file
- runs mx.mak to create mx executable for further use during compilation script
- deletes *.0 and other files created for mx.mak
- finally : runs makemake64.sh


2. makemake64.sh
- This scripts puts all later .mak commands in xls-file as lines :
mx.mak
wxis.mak
(etc.)

- creates xmk.xsh script with instructions to create subdirectories and move finally the created executables in there :
export LC_ALL=POSIX
and creates subdirectories :
mkdir utl
mkdir utl/linux64
and creates for each CISIS-version a script .xsh
mkisis1660_64.xsh
in which dedicated subdirectories are created : 
mkdir utl/linux64/isis1660
etc.

Then, for each CISIS-version, mx (created earlier on) is used to read a line from the file xls as input, with a fixed PFT  $1 and the destination folder as $2 
pft='sh -x mxmake64.xsh utl/linux64/isis '


3. mxmake64.xsh

make -f $2.mak CC=gcc             $3 $4 $5 $6 $7 $8 $9 ${10} ${11} ${12} ${13}

instructions to run mxmake64.xsh to make final executable) : 
e.g. to create mx for isis1660 in Linux 64-bits the command will be : 
sh -x mxmake64.xsh utl/linux64/isis1660 mx CIFFI=0 LIND=0 LIND4=0 ISISXL=1 ISISXL512=0  SIXTY_FOUR=1 _FILE_OFFSET_BITS=00 _LARGEFILE64_SOURCE=0) 

4. Finally xmk.xsh copies wxis-executable in its own directory wxis.

