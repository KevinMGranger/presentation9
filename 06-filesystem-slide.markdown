# Filesystems

- Standard, Unix-y, but...
	- No . or ..
	- No symlinks


# 9p

-VFS-like interface, very predictable.
- Not just an interface, but a *protocol.*


# Namespaces

- Per-process-group (but exposable)
- Union
	- /bin:
		- /$cputype/bin
		- /rc/bin


# Storage Itself / Filesystems Themselves

- Original Setup
	- Only cached on file server!?
	- WORM
- Fossil & Venti

# Synthetic Filesystems

- Examples:
	- /proc
	- /acme
	- /irc
	- /upas/fs


# FHS (from a 9front install)

/386
/68000
/68020
/acme
/adm
/alpha
/amd64
/arm
/bin
/boot
/cfg
/cron
/dev
/dist
/env
/fd
/fd
/lib
/mail
/mips
/mnt
/mnt
/n
/net
/net.alt
/power
/power64
/proc
/rc
/root
/shr
/sparc
/sparc64
/srv
/sys
/tmp
/usr
