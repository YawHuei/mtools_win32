Introduction

This directory contains Uncompressed Programs than Compile with MinGW32. 

Use method
rename /include/iconv.h 
Because configure check iconv.h

./configure --host=i686-w32-mingw32msvc --disable-floppyd --without-x 

one more time check config.h line:=54  HAVE_ICONV_H must be undefined
/* Define to 1 if you have the <iconv.h> header file. */
// #undef HAVE_ICONV_H}

Edit	Makefile
line:=25 Add	USERCFLAGS = -ffunction-sections -fdata-sections
line:=60 Add	LDFLAGS     = -Wl,--gc-sections -Wl,--strip-all
line:=61 Add	LIBS        = -static

Make

Consider {upx.exe -9 *.exe} to compress it.

This end.
