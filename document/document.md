Title         : Linux 常用手册

[TITLE]

[TOC]
# 说明
* Linux 严格区分大小写.
* 一切内容皆文件.
* 系统并不依赖扩展名区分文件类型, 而是权限. 但为方便管理员查看, 坚持按规范写成mo默认形式.
* 字符界面相对于图形界面占用的系统资源更少, 因此减少出错及攻击的可能性.
* 普通用户提示符: \$; 超级用户提示符: \#.


# 目录名
* /home: HOME 普通用户的家目录
* / : ROOT 根目录 
* /boot: BOOT 启动目录
* /bin: BINaries 命令保存目录 （普通用户可读取的命令）
* /sbin: Super BINarise 命令保存目录 （超级用户可读取的命令）
* /dev: DEVices 设备文件保存目录
* /lib: LIBraries 系统库保存目录
* /mnt: MouNT 系统挂载目录
* /tmp: TeMPorary 临时目录
* /proc: PROCesses 直接写入内存目录
* /sys: SYSTEM 系统目录
* /usr: 系统软件资源目录
* /etc: ETCetera
* /run: RUN
* /srv: SeRVices
* /opt: OPTion
* /var: VARiable 系统相关文档内容
~ Note
根目录及 usr 目录下都有 bin/sbin; proc/sys 不可直接操作, 用于保存内存的过载点.
~

# 缩写
## 命令格式:
**`命令 [选项] [参数]`**

* 当多个选项时, 可以写在一起.
* 简化及完整选项: -a / -all

## 文件管理
* ls (LiSt)
* cd (Change Directory)
* pwd (Print Working Directory)
* mv (MoVe)
* rm (ReMove)
* pushd (PUSH to Directory)
* popd (POP from Directory )
* mkdir (MaKe DIRecotry)
* rmdir (ReMove DIRectory)
* cat (CATenate)
* sed (Stream EDitor)
* diff (DIFFerece)
* wc (Word Count)
* chmod (CHange MODe)
* chown (CHange MODe)
* chgrp (CHange GRouP)
* awk (Aho Weinberger and Kernighan)
* gawk (Gnu Aho Weinberger and Kernighan)
* grep (General Regular Expression Print)
* ln (LiNk)
* tar (TARball)

## 硬件管理
* df (Disk Free)
* du (Disk Usage)
* dd (Data Description)
* parted (PARTition EDitor)
* lspci (LiSt Peripheral Component Interconnect)
* lscpu (LiSt Universal Serial Bus)

## 软件及软件包管理
* man (MANual)
* apt (Advanced Packaging Tool)
* dpkg (Debian PacKaGe)
* yum (Yellow dog Updater, Modified)
* rpm (RPM Packaged Manager)

## 系统管理(内核)
* depmod (DEPend MODule)
* modprobe (MODule PROBE)
* lsmod (LiSt MODule)
* modinfo (MODule INFOrmation)
* insmod (INSert MODule)
* rmmod (ReMove MODule)
* ps (Processes Status)
* su (Substitute User)
* bash (Bourne Again SHell)
* init (INITialization)
* ssh (Secure SHell)
* wine (Wine Is Not an Emulator)
* exec (EXECute)
* fstab (FileSystem TABle)
* passwd (PASSWorD)
* tty (TeleTYpe)
* sudo (SuperUser DO)
* grub (GRand Unified Bootloader)
* tzselect (Time Zone SELECT)
* sync (SYNChronize)

## 编辑器
* ed (Editor)
* nano (Nano's ANOther editor)
* emacs (Editor MACroS)
* vi (VIsual)
* vim (Vi IMproved)

## 编码
* cc (C Compiler)
* gcc (Gnu Compiler Collection)
* gcc (Gnu C Compiler)
* g++ (Gnu c++ compiler)
* gcj (Gnu Complier for Java)
* yacc (Yet Another Complier Complier)
* guile (Gnu Ubiquitous Intelligent Lanugage for Extensions)
* php (PHP)
* ld (Link eDitor)
* gdb (Gnu DeBug)
* tcl (Tool Command Line)

## 图形界面
* gnome (GNu Object Model Environment)
* gdm (Gnome Display Manager)
* gtk (Graphic user interface ToolKit)

# 常用命令
##基本命令
|---------|--------------------------------------------|-------------------------------------------------------------------------------------------------|
| Command | Example                                    | Description                                                                                     |
+---------|:------------------------------------------:+-------------------------------------------------------------------------------------------------+
| ls      | ls<br>ls -alF                              | List files in current directory<br>List in long format                                          |
| cd      | cd tempdir<br>cd ..<br>cd ~dhyatt/web-docs | Change directory to tempdir<br>Move back one directory<br>Move into dhyatt's web-docs directory |
| mkdir   | mkdir graphics                             | Make a directory called graphics                                                                |
| rmdir   | rmdir emptydir                             | Remove directory (must be empty)                                                                |
| rm      | rm file1.bak<br>rm *.tmp                   | Remove or delete file<br>Remove all file                                                        |
| mv      | mv old.html new.html                       | Move or rename files                                                                            |
| more    | more index.html                            | Look at file, one page at a time                                                                |
| lpr     | lpr index.html                             | Send file to printer                                                                            |
| man     | man ls                                     | Online manual (help) about command                                                               |
| cp      | cp file1 web-docs<br>cp file1 file1.bak    | Copy file into directory<br>Make backup of file1                                                |
|---------|--------------------------------------------|-------------------------------------------------------------------------------------------------|
{  }

##实用的命令
|-------------------|-------------------|-----------------------------------------|
| Command           | Example           | Description                             |
+-------------------|:-----------------:+-----------------------------------------+
| grep <str><files> | grep "bad word" * | Find which files contain a certain word |
| chmod <opt> <file>            | chmod 644 *.html<br>chmod 755 file.exe           | Change file permissions read only<br>Change file permissions to executable                                  |
|        passwd           |    passwd                |         Change passwd                                 |
|      ps <opt>              |      ps aux<br>ps aux   \|   grep dhyatt              |    List all running processes by #ID<br>List process #ID's running by dhyatt                                 |
|     kill <opt> <ID>              |    kill -9 8453                |    Kill process with ID #8453                                      |
|       gcc (g++) <source>             |    gcc file.c -o file<br>g++ fil2.cpp -o fil2               |             Compile a program written in C<br>Compile a program written in C++                             |
|     gzip <file>                |     gzip bigfile<br>gunzip bigfile.gz               |  Compress file<br>Uncompress file                                        |
|   mail (pine)                |  mail me@tjhsst.edu < file1 pine                 |                  Send file1 by email to someone and read mail using pine                       |
|     telnet <host><br>ssh <host>               |   telnet vortex.tjhsst.edu<br>ssh -l dhyatt<br>jazz.tjhsst.edu                |          Open a connection to vortex<br>Open a secure connection to jazz as user dhyatt                                |
|   ftp <host><br>ncftp <host/directory>                |  ftp station1.tjhsst.edu<br>ncftp metalab.unc.edu                  |      Upload or Download files to station1<br>Connect to archives at UNC                                    |
|-------------------|-------------------|-----------------------------------------|
{  }

