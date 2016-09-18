# 说明
* Linux 严格区分大小写.
* 一切内容皆文件.
* 系统并不依赖扩展名区分文件类型, 而是权限. 但为方便管理员查看, 坚持按规范写成默认形式.
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

**`根目录及 usr 目录下都有 bin/sbin`**

**`proc/sys 不可直接操作, 用于保存内存的过载点`**

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


Command |	Example |	Description
------- | ------- | -----------
1.     ls |	ls<br>ls -alF |	Lists files in current directory<br>List in long format
2.     cd |	cd tempdir<br>cd ..<br>cd ~dhyatt/web-docs |	Change directory to tempdir<br>Move back one directory<br>Move into dhyatt's web-docs directory
3.     mkdir |	mkdir graphics |	Make a directory called graphics
4.     rmdir |	rmdir emptydir |	Remove directory (must be empty)
5.     cp |	cp file1 web-docs<br>cp file1 file1.bak |	Copy file into directory<br>Make backup of file1
6.     rm |	rm file1.bak<br>rm *.tmp |	Remove or delete file<br>Remove all file
7.     mv |	mv old.html new.html |	Move or rename files
8.     more |	more index.html |	Look at file, one page at a time
9.     lpr |	lpr index.html |	Send file to printer
10.   man |	man ls |	Online manual (help) about command 

Command |	Example |	Description
--------|---------|------------
1.     grep <str><files> |	grep "bad word" * |	Find which files contain a certain word
2.     chmod <opt> <file> |	chmod 644 *.html<br>chmod 755 file.exe |	Change file permissions read only<br>Change file permissions to executable
3.     passwd |	passwd |	Change passwd
4.     ps <opt> |	ps aux<br>ps aux   \|   grep dhyatt |	List all running processes by #ID<br>List process #ID's running by dhyatt
5.     kill <opt> <ID> |	kill -9 8453 | 	Kill process with ID #8453
6.     gcc (g++) <source> |	gcc file.c -o file<br>g++ fil2.cpp -o fil2 |	Compile a program written in C<br>Compile a program written in C++
7.     gzip <file> |	gzip bigfile<br>gunzip bigfile.gz |	Compress file<br>Uncompress file
8.     mail<br>(pine) |	mail me@tjhsst.edu \< file1<br>pine |	Send file1 by email to someone<br>Read mail using pine
9.     telnet <host><br>ssh <host> | telnet vortex.tjhsst.edu<br>ssh -l dhyatt<br>jazz.tjhsst.edu |	Open a connection to vortex<br>Open a secure connection to jazz as user dhyatt
10.   ftp <host><br>ncftp <host/directory> |	ftp station1.tjhsst.edu<br>ncftp metalab.unc.edu |	Upload or Download files to station1<br>Connect to archives at UNC 


Command |	Example |	Description
------- | ------- | -----------
1.     who |	who |	Lists who is logged on your machine
2.     finger |	finger |	Lists who is on computers in the lab
3.     ytalk <user@place> |	ytalk dhyatt@threat |	Talk online with dhyatt who is on threat
4.     history |	history |	Lists commands you've done recently
5.     fortune |	fortune |	Print random humerous message
6.     date |	date |	Print out current date
7.     cal <mo> <yr> |	cal 9 2000 |	Print calendar for September 2000
8.     xeyes |	xeyes & |	Keep track of cursor (in "background")
9.     xcalc |	xcalc & |	Calculator ("background" process)
10.   mpage <opt> <file> |	mpage -8 file1   \|  lpr |	Print 8 pages on a single sheet and send to printer (the font will be small!) 


Command |	Example |	Description
------- | ------- | -----------
1.     netscape |	netscape & |	Run Netscape browser
2.     xv |	xv & |	Run graphics file converter
3.     xfig / xpaint |	xfig & (xpaint &) |	Run drawing program
4.     gimp |	gimp & |	Run photoshop type program
5.     ispell <fname> |	ispell file1 |	Spell check file1
6.     latex <fname> |	latex file.tex |	Run LaTeX, a scientific document tool
7.     xemacs / pico |	xemacs (or pico) |	Different editors
8.     soffice |	soffice & |	Run StarOffice, a full word processor
9.     m-tools (mdir, mcopy,mdel, mformat, etc. ) |	mdir a:<br>mcopy file1   a: |	DOS commands from UNIX (dir A:)<br>Copy file1 to A:
10.   gnuplot |	gnuplot |	Plot data graphically 


Command |	Example |	Description
--------| ------- | -----------
1.     df |	df |	See how much free disk space
2.     du |	du -b subdir |	Estimate disk usage of directory in Bytes
3.     alias |	alias lls="ls -alF" |	Create new command "lls" for long format of ls
4.     xhost |	xhost + threat.tjhsst.edu<br>xhost - |	Permit window to display from x-window program from threat<br>Allow no x-window access from other systems
5.     fold |	fold -s file1   \|   lpr |	Fold or break long lines at 60 characters and send to printer
6.     tar |	tar -cf subdir.tar subdir<br>tar -xvf subdir.tar |	Create an archive called subdir.tar of a directory<br>Extract files from an archive file
7.     ghostview (gv) |	gv filename.ps |	View a Postscript file
8.     ping (traceroute) | 	ping threat.tjhsst.edu<br>traceroute www.yahoo.com |	See if machine is alive<br>Print data path to a machine
9.     top |	top |	Print system usage and top resource hogs
10.   logout (exit) | 	logout or exit |	How to quit a UNIX shell. 





