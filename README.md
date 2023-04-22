busybox v${BUSYBOX_DIRNAME##busybox-} static binaries

```console
$ file ./busybox-aarch64-linux-gnu ./busybox-arm-linux-gnueabi ./busybox-arm-linux-gnueabihf ./busybox-mips-linux-gnu ./busybox-mips64-linux-gnuabi64 ./busybox-mips64el-linux-gnuabi64 ./busybox-mipsel-linux-gnu ./busybox-powerpc64le-linux-gnu ./busybox-riscv32-linux-gnu ./busybox-riscv64-linux-gnu ./busybox-x86_64-linux-gnu
./busybox-aarch64-linux-gnu:       ELF 64-bit LSB executable, ARM aarch64, version 1 (GNU/Linux), statically linked, BuildID[sha1]=d40e8a696e1a5e577099ffa76bbedc11d8c8abb2, for GNU/Linux 3.7.0, stripped
./busybox-arm-linux-gnueabi:       ELF 32-bit LSB executable, ARM, EABI5 version 1 (SYSV), statically linked, BuildID[sha1]=ef4917382c36676858ec28876cf8b037494e5f40, for GNU/Linux 3.2.0, stripped
./busybox-arm-linux-gnueabihf:     ELF 32-bit LSB executable, ARM, EABI5 version 1 (GNU/Linux), statically linked, BuildID[sha1]=3105bfa82875fc285f051eca6411009be4296b3c, for GNU/Linux 3.2.0, stripped
./busybox-mips-linux-gnu:          ELF 32-bit MSB executable, MIPS, MIPS32 rel2 version 1 (SYSV), statically linked, BuildID[sha1]=0c2484c65550482de413a296526da16cab1488fe, for GNU/Linux 3.2.0, stripped
./busybox-mips64-linux-gnuabi64:   ELF 64-bit MSB executable, MIPS, MIPS64 rel2 version 1 (SYSV), statically linked, BuildID[sha1]=ee155acc18269ce28afa8cf62230516a8955cf48, for GNU/Linux 3.2.0, stripped
./busybox-mips64el-linux-gnuabi64: ELF 64-bit LSB executable, MIPS, MIPS64 rel2 version 1 (SYSV), statically linked, BuildID[sha1]=a578dce6efc2e7ec55a7b9cf635134a7791a4d96, for GNU/Linux 3.2.0, stripped
./busybox-mipsel-linux-gnu:        ELF 32-bit LSB executable, MIPS, MIPS32 rel2 version 1 (SYSV), statically linked, BuildID[sha1]=876715b0aeffb49b9e0813485c3d5f7691ee341a, for GNU/Linux 3.2.0, stripped
./busybox-powerpc64le-linux-gnu:   ELF 64-bit LSB executable, 64-bit PowerPC or cisco 7500, OpenPOWER ELF V2 ABI, version 1 (GNU/Linux), statically linked, BuildID[sha1]=e696f56e63e5a6bcc63dfe466373d72a92965b22, for GNU/Linux 3.10.0, stripped
./busybox-riscv32-linux-gnu:       ELF 32-bit LSB executable, UCB RISC-V, RVC, double-float ABI, version 1 (SYSV), statically linked, for GNU/Linux 5.4.179, stripped
./busybox-riscv64-linux-gnu:       ELF 64-bit LSB executable, UCB RISC-V, RVC, double-float ABI, version 1 (SYSV), statically linked, BuildID[sha1]=1f8d3e0c937fb9d0ea14cdcd8a31890477b443fe, for GNU/Linux 4.15.0, stripped
./busybox-x86_64-linux-gnu:        ELF 64-bit LSB executable, x86-64, version 1 (GNU/Linux), statically linked, BuildID[sha1]=1860bcacd2b763e88f0691b809b9204e0a858842, for GNU/Linux 3.2.0, stripped
```

# bundled commands
```console
$ qemu-aarch64-static ./busybox-aarch64-linux-gnu
BusyBox v1.36.0 (2023-04-22 07:41:30 UTC) multi-call binary.
BusyBox is copyrighted by many authors between 1998-2015.
Licensed under GPLv2. See source distribution for detailed
copyright notices.

Usage: busybox [function [arguments]...]
   or: busybox --list[-full]
   or: busybox --show SCRIPT
   or: busybox --install [-s] [DIR]
   or: function [arguments]...

	BusyBox is a multi-call binary that combines many common Unix
	utilities into a single executable.  Most people will create a
	link to busybox for each function they wish to use and BusyBox
	will act like whatever it was invoked as.

Currently defined functions:
	[, [[, acpid, add-shell, addgroup, adduser, adjtimex, arch, arp,
	arping, ascii, ash, awk, base32, base64, basename, bc, beep,
	blkdiscard, blkid, blockdev, bootchartd, brctl, bunzip2, bzcat, bzip2,
	cal, cat, chat, chattr, chgrp, chmod, chown, chpasswd, chpst, chroot,
	chrt, chvt, cksum, clear, cmp, comm, conspy, cp, cpio, crc32, crond,
	crontab, cryptpw, cttyhack, cut, date, dc, dd, deallocvt, delgroup,
	deluser, depmod, devmem, df, dhcprelay, diff, dirname, dmesg, dnsd,
	dnsdomainname, dos2unix, dpkg, dpkg-deb, du, dumpkmap, dumpleases,
	echo, ed, egrep, eject, env, envdir, envuidgid, ether-wake, expand,
	expr, factor, fakeidentd, fallocate, false, fatattr, fbset, fbsplash,
	fdflush, fdformat, fdisk, fgconsole, fgrep, find, findfs, flock, fold,
	free, freeramdisk, fsck, fsck.minix, fsfreeze, fstrim, fsync, ftpd,
	ftpget, ftpput, fuser, getopt, getty, grep, groups, gunzip, gzip, halt,
	hd, hdparm, head, hexdump, hexedit, hostid, hostname, httpd, hush,
	hwclock, i2cdetect, i2cdump, i2cget, i2cset, i2ctransfer, id, ifconfig,
	ifdown, ifenslave, ifplugd, ifup, inetd, init, insmod, install, ionice,
	iostat, ip, ipaddr, ipcalc, ipcrm, ipcs, iplink, ipneigh, iproute,
	iprule, iptunnel, kbd_mode, kill, killall, killall5, klogd, last, less,
	link, linux32, linux64, linuxrc, ln, loadfont, loadkmap, logger, login,
	logname, logread, losetup, lpd, lpq, lpr, ls, lsattr, lsmod, lsof,
	lspci, lsscsi, lsusb, lzcat, lzma, lzop, makedevs, makemime, man,
	md5sum, mdev, mesg, microcom, mim, mkdir, mkdosfs, mke2fs, mkfifo,
	mkfs.ext2, mkfs.minix, mkfs.vfat, mknod, mkpasswd, mkswap, mktemp,
	modinfo, modprobe, more, mount, mountpoint, mpstat, mt, mv, nameif,
	nanddump, nandwrite, nbd-client, nc, netstat, nice, nl, nmeter, nohup,
	nologin, nproc, nsenter, nslookup, ntpd, od, openvt, partprobe, passwd,
	paste, patch, pgrep, pidof, ping, ping6, pipe_progress, pivot_root,
	pkill, pmap, popmaildir, poweroff, powertop, printenv, printf, ps,
	pscan, pstree, pwd, pwdx, raidautorun, rdate, rdev, readahead,
	readlink, readprofile, realpath, reboot, reformime, remove-shell,
	renice, reset, resize, resume, rev, rm, rmdir, rmmod, route, rpm,
	rpm2cpio, rtcwake, run-init, run-parts, runlevel, runsv, runsvdir, rx,
	script, scriptreplay, sed, seedrng, sendmail, seq, setarch, setconsole,
	setfattr, setfont, setkeycodes, setlogcons, setpriv, setserial, setsid,
	setuidgid, sh, sha1sum, sha256sum, sha3sum, sha512sum, showkey, shred,
	shuf, slattach, sleep, smemcap, softlimit, sort, split, ssl_client,
	start-stop-daemon, stat, strings, stty, su, sulogin, sum, sv, svc,
	svlogd, svok, swapoff, swapon, switch_root, sync, sysctl, syslogd, tac,
	tail, tar, taskset, tc, tcpsvd, tee, telnet, telnetd, test, tftp,
	tftpd, time, timeout, top, touch, tr, traceroute, traceroute6, tree,
	true, truncate, ts, tsort, tty, ttysize, tunctl, ubiattach, ubidetach,
	ubimkvol, ubirename, ubirmvol, ubirsvol, ubiupdatevol, udhcpc, udhcpc6,
	udhcpd, udpsvd, uevent, umount, uname, unexpand, uniq, unix2dos,
	unlink, unlzma, unshare, unxz, unzip, uptime, users, usleep, uudecode,
	uuencode, vconfig, vi, vlock, volname, w, wall, watch, watchdog, wc,
	wget, which, who, whoami, whois, xargs, xxd, xz, xzcat, yes, zcat,
	zcip
```
