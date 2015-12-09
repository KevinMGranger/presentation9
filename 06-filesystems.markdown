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

# WORM

- Write Once Read Many


# Synthetic Filesystems

- Examples:
	- /proc
	- /acme

# FHS (from a 9front install)
