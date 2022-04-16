# ABCD CISIS

## About CISIS

Library of functions developed by BIREME in C language  to allow the manipulation of ISIS databases without using or installing CDS/ISIS - MicroISIS/WinISIS (UNESCO).

## CISIS Utilities

It consists of a set of executable programs developed with CISIS library that extends and makes it significantly easier to generate, manipulate and transform data within ISIS database model, empowering it with functions not yet available in CDS/ISIS.

### **Standard (10/30)**

It works with master files (.mst) with records up to 32 Kbytes in size - fully compatible with CDS/ISIS for Windows. It has short keys up to 10 characters and long keys ranging from 11 to 30 characters long.

### **Extended**

#### **Long keys (16/60)**

Ditto the standard one, except for the inverted key sizes. The short keys may be up to 16 characters and the long ones from 17 to 60 characters long.

#### **LIND (16/60)**

Ditto the long keys version, except for resources such as field restriction search, occurrence and proximity search, all of them put aside in order to increase search performance and inverted file size. The extensions to some files that comprises the inverted architecture have been modified to make it easier its identification.

#### **FFI (16/60)**

Ditto the LIND version, except for the master file control record whose structure have been changed to increase the record size up to 1 Mbyte long, making it uncompatible with whatever version of CDS/ISIS up to date.

#### BigISIS

Only Linux.

## CISIS - Compilation

### Linux Platform

No configuration is required.

1.  64 bit version.

Only call _**generateApp64.sh**_ script. The applications will be generated into utl/linux64 directory.

1.  32 bit version.

Only call _**generateApp32.sh**_ script. The applications will be generated into utl/linux directory.

---

### Windows

1.  Change _**cisis.h**_ preprocessor settings.

Open _**cisis.h**_ file and change the default configuration to the following one:

```
GCC=0
PC=1
DOS32BITS=1
MSC=0 or 1 (1 if Microsoft Visual Studio and 0 if other compiler is used)
UNIX=0
```

Set compiler configurations.

```
data alignment => byte
calling conventions => C
unsigned char => set
```

Set project preprocessor directives.

a) ISIS version

b) ISIS1660 version

c) LIND version

d) FFI version

wxis: 

**WIN32**

```
WWWISIS=1
CIFFI = 1
LIND = 1
LIND4 = 0
ISISXL = 1
ISISXL512 = 0
LINDLUX = 0
PROCXSLT = 0
_FILE_OFFSET_BITS = 0
_LARGEFILE64_SOURCE = 0
CIWTF=0
INCPROCX=1
INCPRECX=1
```

mx: 

**WIN32**

```
WWWISIS=0
CIFFI=1;
LIND=1;
LIND4=0;
ISISXL=1;
ISISXL512=0;
_FILE_OFFSET_BITS=0;
_LARGEFILE64_SOURCE=0;
CIWTF=1;
INCPROCX=1;
INCPRECX=1;
EXCFMCGI=0;
EXCFMXML=0
```

other applications: 

**WIN32**

```
WWWISIS=0
CIFFI=1;
LIND=1;
LIND4=0;
ISISXL=1;
ISISXL512=0;
_FILE_OFFSET_BITS=0;
_LARGEFILE64_SOURCE=0;
CIWTF=0;
INCPROCX=0;
INCPRECX=0;
EXCFMCGI=1;
EXCFMXML=1;
MXFUN=0;
IFLOADFUN=0;
```

wxis: 

**WIN32**

```
WWWISIS=1
CIFFI = 0
LIND = 1
LIND4 = 0
ISISXL = 1
ISISXL512 = 0
LINDLUX = 0
PROCXSLT = 0
_FILE_OFFSET_BITS = 0
_LARGEFILE64_SOURCE = 0
CIWTF=0
INCPROCX=1
INCPRECX=1
```

mx: 

**WIN32**

```
WWWISIS=0
CIFFI=0;
LIND=1;
LIND4=0;
ISISXL=1;
ISISXL512=0;
_FILE_OFFSET_BITS=0;
_LARGEFILE64_SOURCE=0;
CIWTF=1;
INCPROCX=1;
INCPRECX=1;
EXCFMCGI=0;
EXCFMXML=0
```

other applications: 

**WIN32**

```
WWWISIS=0
CIFFI=0;
LIND=1;
LIND4=0;
ISISXL=1;
ISISXL512=0;
_FILE_OFFSET_BITS=0;
_LARGEFILE64_SOURCE=0;
CIWTF=0;
INCPROCX=0;
INCPRECX=0;
EXCFMCGI=1;
EXCFMXML=1;
MXFUN=0;
IFLOADFUN=0;
```

wxis: 

**WIN32**

```
WWWISIS=1
CIFFI = 0
LIND = 0
LIND4 = 0
ISISXL = 1
ISISXL512 = 0
LINDLUX = 0
PROCXSLT = 0
_FILE_OFFSET_BITS = 0
_LARGEFILE64_SOURCE = 0
CIWTF=0
INCPROCX=1
INCPRECX=1
```

mx: 

**WIN32**

```
WWWISIS=0
CIFFI=0;
LIND=0;
LIND4=0;
ISISXL=1;
ISISXL512=0;
_FILE_OFFSET_BITS=0;
_LARGEFILE64_SOURCE=0;
CIWTF=1;
INCPROCX=1;
INCPRECX=1;
EXCFMCGI=0;
EXCFMXML=0
```

other applications: 

**WIN32**

```
WWWISIS=0
CIFFI=0;
LIND=0;
LIND4=0;
ISISXL=1;
ISISXL512=0;
_FILE_OFFSET_BITS=0;
_LARGEFILE64_SOURCE=0;
CIWTF=1;
INCPROCX=1;
INCPRECX=1;
EXCFMCGI=0;
EXCFMXML=0;
MXFUN=0;
IFLOADFUN=0;
```

wxis: 

**WIN32**

```
WWWISIS=1
CIFFI = 0
LIND = 0
LIND4 = 0
ISISXL = 0
ISISXL512 = 0
LINDLUX = 0
PROCXSLT = 0
_FILE_OFFSET_BITS = 0
_LARGEFILE64_SOURCE = 0
CIWTF=0
INCPROCX=1
INCPRECX=1
```

mx: 

**WIN32**

```
WWWISIS=0
CIFFI=0;
LIND=0;
LIND4=0;
ISISXL=0;
ISISXL512=0;
_FILE_OFFSET_BITS=0;
_LARGEFILE64_SOURCE=0;
CIWTF=1;
INCPROCX=1;
INCPRECX=1;
EXCFMCGI=0;
EXCFMXML=0
```

other applications 

**WIN32**

```
WWWISIS=0
CIFFI=0;
LIND=0;
LIND4=0;
ISISXL=0;
ISISXL512=0;
_FILE_OFFSET_BITS=0;
_LARGEFILE64_SOURCE=0;
CIWTF=0;
INCPROCX=0;
INCPRECX=0;
EXCFMCGI=1;
EXCFMXML=1;
MXFUN=0;
IFLOADFUN=0;
```
