Tried the  https://askubuntu.com/questions/420981/how-do-i-save-terminal-output-to-a-file from Kak Wilfrid but didn't succeed

![image](https://github.com/bmw-ece-ntust/internship/assets/123353805/7e3d5291-f4dd-4480-9220-28b04883bfa7)


Thus i copy all the script from terminal and paste it here,

```
gisela@gisela:~$ gcc --version
gcc (Ubuntu 11.4.0-1ubuntu1~22.04) 11.4.0
Copyright (C) 2021 Free Software Foundation, Inc.
This is free software; see the source for copying conditions.  There is NO
warranty; not even for MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.

gisela@gisela:~$ sudo apt-get install -y build-essential
[sudo] password for gisela: 
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
The following additional packages will be installed:
  dpkg-dev fakeroot g++ g++-11 libalgorithm-diff-perl
  libalgorithm-diff-xs-perl libalgorithm-merge-perl libdpkg-perl libfakeroot
  libfile-fcntllock-perl libstdc++-11-dev lto-disabled-list
Suggested packages:
  debian-keyring gcc-11-doc bzr libstdc++-11-doc
The following NEW packages will be installed:
  build-essential dpkg-dev fakeroot g++ g++-11 libalgorithm-diff-perl
  libalgorithm-diff-xs-perl libalgorithm-merge-perl libdpkg-perl libfakeroot
  libfile-fcntllock-perl libstdc++-11-dev lto-disabled-list
0 upgraded, 13 newly installed, 0 to remove and 0 not upgraded.
1 not fully installed or removed.
Need to get 14,6 MB of archives.
After this operation, 52,7 MB of additional disk space will be used.
Get:1 http://id.ports.ubuntu.com/ubuntu-ports jammy-updates/main arm64 libstdc++-11-dev arm64 11.4.0-1ubuntu1~22.04 [2.088 kB]
Get:2 http://id.ports.ubuntu.com/ubuntu-ports jammy-updates/main arm64 g++-11 arm64 11.4.0-1ubuntu1~22.04 [11,1 MB]
Get:3 http://id.ports.ubuntu.com/ubuntu-ports jammy/main arm64 g++ arm64 4:11.2.0-1ubuntu1 [1.394 B]
Get:4 http://id.ports.ubuntu.com/ubuntu-ports jammy-updates/main arm64 libdpkg-perl all 1.21.1ubuntu2.2 [237 kB]
Get:5 http://id.ports.ubuntu.com/ubuntu-ports jammy/main arm64 lto-disabled-list all 24 [12,5 kB]
Get:6 http://id.ports.ubuntu.com/ubuntu-ports jammy-updates/main arm64 dpkg-dev all 1.21.1ubuntu2.2 [922 kB]
Get:7 http://id.ports.ubuntu.com/ubuntu-ports jammy/main arm64 build-essential arm64 12.9ubuntu3 [4.740 B]
Get:8 http://id.ports.ubuntu.com/ubuntu-ports jammy/main arm64 libfakeroot arm64 1.28-1ubuntu1 [31,5 kB]
Get:9 http://id.ports.ubuntu.com/ubuntu-ports jammy/main arm64 fakeroot arm64 1.28-1ubuntu1 [60,5 kB]
Get:10 http://id.ports.ubuntu.com/ubuntu-ports jammy/main arm64 libalgorithm-diff-perl all 1.201-1 [41,8 kB]
Get:11 http://id.ports.ubuntu.com/ubuntu-ports jammy/main arm64 libalgorithm-diff-xs-perl arm64 0.04-6build3 [11,7 kB]
Get:12 http://id.ports.ubuntu.com/ubuntu-ports jammy/main arm64 libalgorithm-merge-perl all 0.08-3 [12,0 kB]
Get:13 http://id.ports.ubuntu.com/ubuntu-ports jammy/main arm64 libfile-fcntllock-perl arm64 0.22-3build7 [33,7 kB]
Fetched 14,6 MB in 33s (437 kB/s)                                              
Selecting previously unselected package libstdc++-11-dev:arm64.
(Reading database ... 175975 files and directories currently installed.)
Preparing to unpack .../00-libstdc++-11-dev_11.4.0-1ubuntu1~22.04_arm64.deb ...
Unpacking libstdc++-11-dev:arm64 (11.4.0-1ubuntu1~22.04) ...
Selecting previously unselected package g++-11.
Preparing to unpack .../01-g++-11_11.4.0-1ubuntu1~22.04_arm64.deb ...
Unpacking g++-11 (11.4.0-1ubuntu1~22.04) ...
Selecting previously unselected package g++.
Preparing to unpack .../02-g++_4%3a11.2.0-1ubuntu1_arm64.deb ...
Unpacking g++ (4:11.2.0-1ubuntu1) ...
Selecting previously unselected package libdpkg-perl.
Preparing to unpack .../03-libdpkg-perl_1.21.1ubuntu2.2_all.deb ...
Unpacking libdpkg-perl (1.21.1ubuntu2.2) ...
Selecting previously unselected package lto-disabled-list.
Preparing to unpack .../04-lto-disabled-list_24_all.deb ...
Unpacking lto-disabled-list (24) ...
Selecting previously unselected package dpkg-dev.
Preparing to unpack .../05-dpkg-dev_1.21.1ubuntu2.2_all.deb ...
Unpacking dpkg-dev (1.21.1ubuntu2.2) ...
Selecting previously unselected package build-essential.
Preparing to unpack .../06-build-essential_12.9ubuntu3_arm64.deb ...
Unpacking build-essential (12.9ubuntu3) ...
Selecting previously unselected package libfakeroot:arm64.
Preparing to unpack .../07-libfakeroot_1.28-1ubuntu1_arm64.deb ...
Unpacking libfakeroot:arm64 (1.28-1ubuntu1) ...
Selecting previously unselected package fakeroot.
Preparing to unpack .../08-fakeroot_1.28-1ubuntu1_arm64.deb ...
Unpacking fakeroot (1.28-1ubuntu1) ...
Selecting previously unselected package libalgorithm-diff-perl.
Preparing to unpack .../09-libalgorithm-diff-perl_1.201-1_all.deb ...
Unpacking libalgorithm-diff-perl (1.201-1) ...
Selecting previously unselected package libalgorithm-diff-xs-perl.
Preparing to unpack .../10-libalgorithm-diff-xs-perl_0.04-6build3_arm64.deb ...
Unpacking libalgorithm-diff-xs-perl (0.04-6build3) ...
Selecting previously unselected package libalgorithm-merge-perl.
Preparing to unpack .../11-libalgorithm-merge-perl_0.08-3_all.deb ...
Unpacking libalgorithm-merge-perl (0.08-3) ...
Selecting previously unselected package libfile-fcntllock-perl.
Preparing to unpack .../12-libfile-fcntllock-perl_0.22-3build7_arm64.deb ...
Unpacking libfile-fcntllock-perl (0.22-3build7) ...
Setting up lto-disabled-list (24) ...
Setting up libfile-fcntllock-perl (0.22-3build7) ...
Setting up libalgorithm-diff-perl (1.201-1) ...
Setting up libfakeroot:arm64 (1.28-1ubuntu1) ...
Setting up fakeroot (1.28-1ubuntu1) ...
update-alternatives: using /usr/bin/fakeroot-sysv to provide /usr/bin/fakeroot (fakeroot) in auto mode
Setting up netopeer2 (2.0.35-1ubuntu1) ...
/usr/share/netopeer2/merge_hostkey.sh: line 29: /dev/null: restricted: cannot redirect output
dpkg: error processing package netopeer2 (--configure):
 installed netopeer2 package post-installation script subprocess returned error exit status 1
Setting up libdpkg-perl (1.21.1ubuntu2.2) ...
Setting up libstdc++-11-dev:arm64 (11.4.0-1ubuntu1~22.04) ...
Setting up libalgorithm-diff-xs-perl (0.04-6build3) ...
Setting up libalgorithm-merge-perl (0.08-3) ...
Setting up g++-11 (11.4.0-1ubuntu1~22.04) ...
Setting up dpkg-dev (1.21.1ubuntu2.2) ...
Setting up g++ (4:11.2.0-1ubuntu1) ...
update-alternatives: using /usr/bin/g++ to provide /usr/bin/c++ (c++) in auto mode
Setting up build-essential (12.9ubuntu3) ...
Processing triggers for man-db (2.10.2-1) ...
Processing triggers for libc-bin (2.35-0ubuntu3.6) ...
Errors were encountered while processing:
 netopeer2
E: Sub-process /usr/bin/dpkg returned an error code (1)
gisela@gisela:~$ sudo apt-get install -y libpcap-dev
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
The following additional packages will be installed:
  libdbus-1-dev libpcap0.8-dev pkg-config
The following NEW packages will be installed:
  libdbus-1-dev libpcap-dev libpcap0.8-dev pkg-config
0 upgraded, 4 newly installed, 0 to remove and 0 not upgraded.
1 not fully installed or removed.
Need to get 507 kB of archives.
After this operation, 1.986 kB of additional disk space will be used.
Get:1 http://id.ports.ubuntu.com/ubuntu-ports jammy/main arm64 pkg-config arm64 0.29.2-1ubuntu3 [47,4 kB]
Get:2 http://id.ports.ubuntu.com/ubuntu-ports jammy-updates/main arm64 libdbus-1-dev arm64 1.12.20-2ubuntu4.1 [192 kB]
Get:3 http://id.ports.ubuntu.com/ubuntu-ports jammy/main arm64 libpcap0.8-dev arm64 1.10.1-4build1 [264 kB]
Get:4 http://id.ports.ubuntu.com/ubuntu-ports jammy/main arm64 libpcap-dev arm64 1.10.1-4build1 [3.328 B]
Fetched 507 kB in 3s (177 kB/s)         
Selecting previously unselected package pkg-config.
(Reading database ... 177352 files and directories currently installed.)
Preparing to unpack .../pkg-config_0.29.2-1ubuntu3_arm64.deb ...
Unpacking pkg-config (0.29.2-1ubuntu3) ...
Selecting previously unselected package libdbus-1-dev:arm64.
Preparing to unpack .../libdbus-1-dev_1.12.20-2ubuntu4.1_arm64.deb ...
Unpacking libdbus-1-dev:arm64 (1.12.20-2ubuntu4.1) ...
Selecting previously unselected package libpcap0.8-dev:arm64.
Preparing to unpack .../libpcap0.8-dev_1.10.1-4build1_arm64.deb ...
Unpacking libpcap0.8-dev:arm64 (1.10.1-4build1) ...
Selecting previously unselected package libpcap-dev:arm64.
Preparing to unpack .../libpcap-dev_1.10.1-4build1_arm64.deb ...
Unpacking libpcap-dev:arm64 (1.10.1-4build1) ...
Setting up netopeer2 (2.0.35-1ubuntu1) ...
/usr/share/netopeer2/merge_hostkey.sh: line 29: /dev/null: restricted: cannot redirect output
dpkg: error processing package netopeer2 (--configure):
 installed netopeer2 package post-installation script subprocess returned error exit status 1
Setting up pkg-config (0.29.2-1ubuntu3) ...
Setting up libdbus-1-dev:arm64 (1.12.20-2ubuntu4.1) ...
Processing triggers for man-db (2.10.2-1) ...
Processing triggers for sgml-base (1.30) ...
Setting up libpcap0.8-dev:arm64 (1.10.1-4build1) ...
Setting up libpcap-dev:arm64 (1.10.1-4build1) ...
Errors were encountered while processing:
 netopeer2
E: Sub-process /usr/bin/dpkg returned an error code (1)
gisela@gisela:~$ pwd
/home/gisela
gisela@gisela:~$ mkdir O-DU/ High/ Directory\
> 
mkdir: cannot create directory \u2018O-DU/\u2019: File exists
mkdir: cannot create directory \u2018High/\u2019: File exists
mkdir: cannot create directory \u2018Directory\u2019: File exists
gisela@gisela:~$ mkdir ~/O-DU_High_Directory\
> 
mkdir: cannot create directory \u2018/home/gisela/O-DU_High_Directory\u2019: File exists
gisela@gisela:~$ git clone https://github.com/o-ran-sc/o-du-l2.git
Cloning into 'o-du-l2'...
remote: Enumerating objects: 23253, done.
remote: Counting objects: 100% (610/610), done.
remote: Compressing objects: 100% (362/362), done.
remote: Total 23253 (delta 444), reused 355 (delta 243), pack-reused 22643
Receiving objects: 100% (23253/23253), 24.28 MiB | 1.45 MiB/s, done.
Resolving deltas: 100% (21135/21135), done.
gisela@gisela:~$ pwd
/home/gisela
gisela@gisela:~$ mv o-du-l2 O-DU_High_Directory
mv: cannot move 'o-du-l2' to 'O-DU_High_Directory/o-du-l2': Directory not empty
gisela@gisela:~$ cd O-DU_High_Directory/l2/build/scripts
bash: cd: O-DU_High_Directory/l2/build/scripts: No such file or directory
gisela@gisela:~$ pwd
/home/gisela
gisela@gisela:~$ cd O-DU_High_Directory/o-du-l2/build/scripts
gisela@gisela:~/O-DU_High_Directory/o-du-l2/build/scripts$ sudo ./add_netconf_user.sh
The system user `netconf' already exists. Exiting.
BAD PASSWORD: The password contains the user name in some form
Generating public/private dsa key pair.
/home/netconf/.ssh/id_dsa already exists.
Overwrite (y/n)? y
Your identification has been saved in /home/netconf/.ssh/id_dsa
Your public key has been saved in /home/netconf/.ssh/id_dsa.pub
The key fingerprint is:
SHA256:hEFL0Q/SHsvVfHuVEl2MoL7om//aPGLFpm3jHUQrpaE root@gisela
The key's randomart image is:
+---[DSA 1024]----+
|     .=+   o.ooo+|
|     ..+= ..o.ooo|
|      o+.*. ..+..|
|       .+... =...|
|        S E.o o. |
|         . .+o   |
|        . .=  .  |
|       . .+o=. . |
|        ++o*=o.  |
+----[SHA256]-----+
gisela@gisela:~/O-DU_High_Directory/o-du-l2/build/scripts$ sudo ./netopeer-server.sh start
gisela@gisela:~/O-DU_High_Directory/o-du-l2/build/scripts$ cd
gisela@gisela:~$ cd <O-DU High Directory>/o-du-l2/build/odu
bash: /o-du-l2/build/odu: No such file or directory
gisela@gisela:~$ cd O-DU_High_Directory/o-du-l2/build/scripts
gisela@gisela:~/O-DU_High_Directory/o-du-l2/build/scripts$ make clean_odu MACHINE=BIT64 MODE=FDD
make: *** No rule to make target 'clean_odu'.  Stop.
gisela@gisela:~/O-DU_High_Directory/o-du-l2/build/scripts$ make clean_odu MACHINE=BIT64 MODE=FDD
make: *** No rule to make target 'clean_odu'.  Stop.
gisela@gisela:~/O-DU_High_Directory/o-du-l2/build/scripts$ clean_odu/MACHINE=BIT64/MODE=FDD
bash: clean_odu/MACHINE=BIT64/MODE=FDD
bash: clean_odu/MACHINE=BIT64/MODE=FDD: No such file or directory
Command 'bash:' not found, did you mean:
  command 'bash' from deb bash (5.1-6ubuntu1)
Try: sudo apt install <deb name>
gisela@gisela:~/O-DU_High_Directory/o-du-l2/build/scripts$ make odu MACHINE=BIT64 MODE=FDD O1_ENABLE=YES
make: *** No rule to make target 'odu'.  Stop.
gisela@gisela:~/O-DU_High_Directory/o-du-l2/build/scripts$ make odu MACHINE=BIT64 MODE=FDD
make: *** No rule to make target 'odu'.  Stop.
gisela@gisela:~/O-DU_High_Directory/o-du-l2/build/scripts$ cd
gisela@gisela:~$ cd O-DU_High_Directory/o-du-l2/build/odu    
gisela@gisela:~/O-DU_High_Directory/o-du-l2/build/odu$ make odu MACHINE=BIT64 MODE=FDD
-e Preparing directories for build...
-e Directories are successfully prepared
make[1]: Entering directory '/home/gisela/O-DU_High_Directory/o-du-l2/build/odu'
-e Compiling  /home/gisela/O-DU_High_Directory/o-du-l2/src/codec_utils/common/ANY.c 
-e Compiling  /home/gisela/O-DU_High_Directory/o-du-l2/src/codec_utils/common/asn_application.c 
-e Compiling  /home/gisela/O-DU_High_Directory/o-du-l2/src/codec_utils/common/asn_bit_data.c 
gcc: error: unrecognized command-line option \u2018-m64\u2019
gcc: error: unrecognized command-line option \u2018-m64\u2019
make[1]: *** [/home/gisela/O-DU_High_Directory/o-du-l2/build/odu/../common/compile.mak:83: /home/gisela/O-DU_High_Directory/o-du-l2/build/odu/obj/odu/ANY.o] Error 1
make[1]: *** Waiting for unfinished jobs....
make[1]: *** [/home/gisela/O-DU_High_Directory/o-du-l2/build/odu/../common/compile.mak:83: /home/gisela/O-DU_High_Directory/o-du-l2/build/odu/obj/odu/asn_application.o] Error 1
-e Compiling  /home/gisela/O-DU_High_Directory/o-du-l2/src/codec_utils/common/asn_codecs_prim.c 
gcc: error: unrecognized command-line option \u2018-m64\u2019
gcc: error: unrecognized command-line option \u2018-m64\u2019
make[1]: *** [/home/gisela/O-DU_High_Directory/o-du-l2/build/odu/../common/compile.mak:84: /home/gisela/O-DU_High_Directory/o-du-l2/build/odu/obj/odu/asn_bit_data.o] Error 1
make[1]: *** [/home/gisela/O-DU_High_Directory/o-du-l2/build/odu/../common/compile.mak:84: /home/gisela/O-DU_High_Directory/o-du-l2/build/odu/obj/odu/asn_codecs_prim.o] Error 1
make[1]: Leaving directory '/home/gisela/O-DU_High_Directory/o-du-l2/build/odu'
make: *** [makefile:192: du] Error 2
gisela@gisela:~/O-DU_High_Directory/o-du-l2/build/odu$ make clean_odu MACHINE=BIT64 MODE=FDD
make[1]: Entering directory '/home/gisela/O-DU_High_Directory/o-du-l2/build/odu'
-e Cleaning DU APP
/home/gisela/O-DU_High_Directory/o-du-l2/src/du_app/ /home/gisela/O-DU_High_Directory/o-du-l2/src/cm
make[1]: Leaving directory '/home/gisela/O-DU_High_Directory/o-du-l2/build/odu'
make[1]: Entering directory '/home/gisela/O-DU_High_Directory/o-du-l2/build/odu'
-e Cleaning ASN
/home/gisela/O-DU_High_Directory/o-du-l2/src/codec_utils/common /home/gisela/O-DU_High_Directory/o-du-l2/src/cm
make[1]: Leaving directory '/home/gisela/O-DU_High_Directory/o-du-l2/build/odu'
make[1]: Entering directory '/home/gisela/O-DU_High_Directory/o-du-l2/build/odu'
-e Cleaning ASN
/home/gisela/O-DU_High_Directory/o-du-l2/src/codec_utils/F1AP /home/gisela/O-DU_High_Directory/o-du-l2/src/cm
make[1]: Leaving directory '/home/gisela/O-DU_High_Directory/o-du-l2/build/odu'
make[1]: Entering directory '/home/gisela/O-DU_High_Directory/o-du-l2/build/odu'
-e Cleaning ASN
/home/gisela/O-DU_High_Directory/o-du-l2/src/codec_utils/E2AP /home/gisela/O-DU_High_Directory/o-du-l2/src/cm
make[1]: Leaving directory '/home/gisela/O-DU_High_Directory/o-du-l2/build/odu'
make[1]: Entering directory '/home/gisela/O-DU_High_Directory/o-du-l2/build/odu'
-e Cleaning ASN
/home/gisela/O-DU_High_Directory/o-du-l2/src/codec_utils/E2SM_KPM /home/gisela/O-DU_High_Directory/o-du-l2/src/cm
make[1]: Leaving directory '/home/gisela/O-DU_High_Directory/o-du-l2/build/odu'
make[1]: Entering directory '/home/gisela/O-DU_High_Directory/o-du-l2/build/odu'
-e Cleaning ASN
/home/gisela/O-DU_High_Directory/o-du-l2/src/codec_utils/RRC /home/gisela/O-DU_High_Directory/o-du-l2/src/cm
make[1]: Leaving directory '/home/gisela/O-DU_High_Directory/o-du-l2/build/odu'
make[1]: Entering directory '/home/gisela/O-DU_High_Directory/o-du-l2/build/odu'
-e Cleaning RLC
make[1]: Leaving directory '/home/gisela/O-DU_High_Directory/o-du-l2/build/odu'
make[1]: Entering directory '/home/gisela/O-DU_High_Directory/o-du-l2/build/odu'
-e Cleaning CPUH CM
-e  
make[1]: Leaving directory '/home/gisela/O-DU_High_Directory/o-du-l2/build/odu'
make[1]: Entering directory '/home/gisela/O-DU_High_Directory/o-du-l2/build/odu'
-e Cleaing MAC
make[1]: Leaving directory '/home/gisela/O-DU_High_Directory/o-du-l2/build/odu'
make[1]: Entering directory '/home/gisela/O-DU_High_Directory/o-du-l2/build/odu'
-e Cleaing MAC
make[1]: Leaving directory '/home/gisela/O-DU_High_Directory/o-du-l2/build/odu'
make[1]: Entering directory '/home/gisela/O-DU_High_Directory/o-du-l2/build/odu'
-e Cleaning SSI from /home/gisela/O-DU_High_Directory/o-du-l2/build/odu/obj/odu
make[1]: Leaving directory '/home/gisela/O-DU_High_Directory/o-du-l2/build/odu'
make[1]: Entering directory '/home/gisela/O-DU_High_Directory/o-du-l2/build/odu'

-e Cleaning PHY stub
/home/gisela/O-DU_High_Directory/o-du-l2/src/phy_stub/ /home/gisela/O-DU_High_Directory/o-du-l2/src/cm
make[1]: Leaving directory '/home/gisela/O-DU_High_Directory/o-du-l2/build/odu'
-e ***** ODU CLEAN COMPLETE *****
gisela@gisela:~/O-DU_High_Directory/o-du-l2/build/odu$ make odu MACHINE=BIT64 MODE=FDD
-e Preparing directories for build...
-e Directories are successfully prepared
make[1]: Entering directory '/home/gisela/O-DU_High_Directory/o-du-l2/build/odu'
-e Compiling  /home/gisela/O-DU_High_Directory/o-du-l2/src/codec_utils/common/ANY.c 
-e Compiling  /home/gisela/O-DU_High_Directory/o-du-l2/src/codec_utils/common/asn_application.c 
-e Compiling  /home/gisela/O-DU_High_Directory/o-du-l2/src/codec_utils/common/asn_bit_data.c 
-e Compiling  /home/gisela/O-DU_High_Directory/o-du-l2/src/codec_utils/common/asn_codecs_prim.c 
-e Compiling  /home/gisela/O-DU_High_Directory/o-du-l2/src/codec_utils/common/asn_internal.c 
gcc: error: unrecognized command-line option \u2018-m64\u2019
gcc: error: unrecognized command-line option \u2018-m64\u2019
make[1]: *** [/home/gisela/O-DU_High_Directory/o-du-l2/build/odu/../common/compile.mak:84: /home/gisela/O-DU_High_Directory/o-du-l2/build/odu/obj/odu/asn_application.o] Error 1
make[1]: *** Waiting for unfinished jobs....
make[1]: *** [/home/gisela/O-DU_High_Directory/o-du-l2/build/odu/../common/compile.mak:84: /home/gisela/O-DU_High_Directory/o-du-l2/build/odu/obj/odu/ANY.o] Error 1
gcc: error: unrecognized command-line option \u2018-m64\u2019
make[1]: *** [/home/gisela/O-DU_High_Directory/o-du-l2/build/odu/../common/compile.mak:84: /home/gisela/O-DU_High_Directory/o-du-l2/build/odu/obj/odu/asn_bit_data.o] Error 1
gcc: error: unrecognized command-line option \u2018-m64\u2019
gcc: error: unrecognized command-line option \u2018-m64\u2019
make[1]: *** [/home/gisela/O-DU_High_Directory/o-du-l2/build/odu/../common/compile.mak:84: /home/gisela/O-DU_High_Directory/o-du-l2/build/odu/obj/odu/asn_codecs_prim.o] Error 1
make[1]: *** [/home/gisela/O-DU_High_Directory/o-du-l2/build/odu/../common/compile.mak:84: /home/gisela/O-DU_High_Directory/o-du-l2/build/odu/obj/odu/asn_internal.o] Error 1
make[1]: Leaving directory '/home/gisela/O-DU_High_Directory/o-du-l2/build/odu'
make: *** [makefile:192: du] Error 2
gisela@gisela:~/O-DU_High_Directory/o-du-l2/build/odu$ cd
gisela@gisela:~$ command > osc.txt
gisela@gisela:~$ script output.txt
Script started, output log file is 'output.txt'.
gisela@gisela:~$ ls
Desktop    Downloads  O-DU                 osc.txt     Public     Videos
Directory  High       O-DU_High_Directory  output.txt  snap
Documents  Music      o-du-l2              Pictures    Templates
gisela@gisela:~$ exit
exit
Script done.
gisela@gisela:~$ script terminal
Script started, output log file is 'terminal'.
gisela@gisela:~$
```

