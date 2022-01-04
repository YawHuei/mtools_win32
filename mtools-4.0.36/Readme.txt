Introduction

This directory contains Uncompressed Programs than Compile with MinGW64. 

Use method

./buildMingw.sh
./configure --host=i686-w32-mingw32msvc --disable-floppyd --without-x 


Edit	Makefile
line:=25 Add	USERCFLAGS = -ffunction-sections -fdata-sections
line:=60 Add	LDFLAGS     = -Wl,--gc-sections -Wl,--strip-all
line:=61 Add	LIBS        = -static

make
make install

{upx.exe -9 *.exe} to compress it.

This end.
