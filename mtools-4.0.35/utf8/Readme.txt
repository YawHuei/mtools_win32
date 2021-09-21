Introduction

This directory contains Uncompressed Programs than Compile with MinGW32. 

Use method

Install libiconv
download libiconv-1.16.tar.gz from https://ftp.gnu.org/gnu/libiconv/libiconv-1.16.tar.gz
See https://www.gnu.org/software/libiconv/#TOCdownloading
decompress to e:\libiconv
in MinGW32
cd /e/libiconv
./configure
make
make install

./configure HAVE_ICONV_H=1 --host=i686-w32-mingw32msvc --disable-floppyd --without-x 

/* Define to 1 if you have the <iconv.h> header file. */

Modify charsetConv.c
at line:=341
//li = nl_langinfo(CODESET);
+ li = "utf8";


Edit	Makefile
line:=25 Add	USERCFLAGS = -ffunction-sections -fdata-sections
line:=60 Add	LDFLAGS     = -Wl,--gc-sections -Wl,--strip-all
line:=61 Add	LIBS        = -static -liconv

Make

Consider {upx.exe -9 *.exe} to compress it.

This end. 

