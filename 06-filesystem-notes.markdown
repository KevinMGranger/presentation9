# Filesystems

- Why no symlinks or . or ..?
	- " Symbolic links make the Unix file system non-hierarchical, resulting in multiple valid path names for a given file. This ambiguity is a source of confusion, especially since some shells work overtime to present a consistent view from programs such as pwd, while other programs and the kernel itself do nothing about the problem." - Rob Pike [2]
	- A canonical path is kept for every FD. ".." is simply resolved by removing the path element preceeding it.


# Storage Itself

- Original Setup: [1]
	- RAM Cache
	- 600 MB Magnetic Spinner
	- 300 GB "jukebox" WORM
		- Optical Drive
	- "With the high-speed links, it is unnecessary for clients to cache data; the file server centralizes the caching for all its clients, avoiding the problems of distributed caches."

- Venti: hash-identified block storage
	- a-la git or swift or s3
	- merkle trees!

- Fossil: meant to eventually replace parts of the file server code and kernel-level code
	- Uses same system representation as venti (Vac) but on-disk format facilitates snapshots
	- keeps local stuff up to date, sends old stuff to venti

- came about in 2002, zfs was announced in 2004 (theoretically started in 2001)

# Synthetic Filesystems

- /proc
	- ctl and note instead of signals


# Sources

[1]: http://doc.cat-v.org/plan_9/1st_edition/designing_plan_9
[2]: http://doc.cat-v.org/plan_9/4th_edition/papers/lexnames