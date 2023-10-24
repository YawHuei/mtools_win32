Introduction

Mtools is a collection of utilities to access MS-DOS disks from GNU and Unix without mounting them.
View details at https://www.gnu.org/software/mtools/ .

This directory contains Compiled Programs that can be run in windows and MsDos.
They are Compiled with Mingw on Windows 10 amd64 for Windows.

They are Compiled with (Mingw + djgpp) on Windows 10 amd64 For MsDos. 

Usage examples:

under Windows
mtools.exe -c mcopy -bni c:\VhdMenu\datas.img ::/VHX ::/VHD .
Or 
mcopy.exe -bni c:\VhdMenu\datas.img ::/VHX ::/VHD .

mtools.exe -c mcopy -boi c:\VhdMenu\datas.img VHX VHD ::/
Or
mcopy.exe -boi c:\VhdMenu\datas.img VHX VHD ::/

mtools.exe -c mdir -i c:\VhdMenu\datas.img
Or
mdir.exe  -i c:\VhdMenu\datas.img  


under MsDos, need CWSDPMI
mtools.exe -c mcopy -bni c:/VhdMenu/datas.img ::/VHX ::/VHD .
Or 
mcopy.exe -bni c:/VhdMenu/datas.img ::/VHX ::/VHD .