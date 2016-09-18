# 说明
* Linux 严格区分大小写.
* 一切内容皆文件.
* 系统并不依赖扩展名区分文件类型, 而是权限. 但为方便管理员查看, 坚持按规范写成mo默认形式.
* 字符界面相对于图形界面占用的系统资源更少, 因此减少出错及攻击的可能性.
* 普通用户提示符: \$; 超级用户提示符: \#.

First Header | Second Header
------------ | -------------
Content cell 1 | Content cell 2
Content column 1 | Content column 

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
|产品|价格|
|-|-|
|Leanote 高级账号|60元/年|
|Leanote 超级账号|120元/年|
