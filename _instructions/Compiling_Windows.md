# Compilation for Windows

1.  Change cisis.h preprocessor settings.

Open cisis.h file and change the default configuration to the following one:

GCC=0 PC=1 DOS32BITS=1 MSC=0 or 1 (1 if Microsoft Visual Studio and 0 if other compiler is used) UNIX=0

1.  Set compiler configurations.

data alignment => byte calling conventions => C unsigned char => set

1.  Set project preprocessor directives.

a) ISIS version

wxis:

```
WIN32
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

```
WIN32
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

```
WIN32
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

b) ISIS1660 version

wxis:

```
WIN32
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

```
WIN32
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

```
WIN32
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

c) LIND version

wxis:

```
WIN32
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

```
WIN32
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

```
WIN32
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

d) FFI version

wxis:

```
WIN32
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

```
WIN32
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

```
WIN32
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
