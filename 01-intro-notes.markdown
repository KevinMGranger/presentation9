# What is Plan 9?

- Multi-processing, multi-tasking, general purpose OS.
- Had features typically reserved for other "types" of OSes:
	- aside from what's necessary to boot, FS drivers ran in user space-- see criticisms of Tanenbaum [4]
	- "Plan 9's kernel is a fraction of the size of any microkernel
          we know and offers more functionality and comparable
          or often better performance."
	-18,000 in Plan 9, "about 5000 lines perform memory management, process management, hardware interface, and system calls. The rest are for the 17 different file systems implementing devices, networks, process control, etc. Since most of the file systems are completely self contained, the complexity of the kernel code is even lower than its 18,000 lines would imply. A working, albeit not very useful, kernel can be configured containing only the file systems implementing pipes, a local root, and a console. This totals 5899 lines of commented C code (counted using wc *.[ch] ). As a compari-son, Mach’s micro-kernel without device drivers has 25,530 lines of C code (calculated, we’re told, by counting semi-colons). By the same metric our minimal kernel is only 4,622 lines long, less than 1/5 the size. In fact, our kernel with every file system included is still less than half the size of their micro-kernel."[5]
	- Realtime features, touch upon those in scheduling

- Distributed
	- In order to take advantage of advancements in technology in separate areas
	- "efficiency, security, simplicity, and reliability" / "cost-effectiveness, maintenance, performance, reliability, and security" [1]
	- In a standard Plan 9 setup, one computer handles storage, one handles computing, and you sit at a graphical terminal [1]

- Unix, but unix-y-er.
	- Radical Simplicity
		- GNU cat:  782 lines, 22,684 chars
		- plan 9 cat.c: 35 lines, 531 chars
	- "The foundations of the system are built on two ideas: a per-process name space and a simple message-oriented file system protocol." [2]
		- everything... no, EVERYTHING is a file(system).

# Who made plan9?

- KT: protocol begun, C compiler
- RP: naming, window systems
- DP: networking
- PW: simplified NS management, reengineerd, Alef
- TK JM HT: drivers
- TD: shell & raster
- Trickey Duff and Andrew Hume: APE
- BF: ports
- the rest listed as "others"
[3]

# What were plan9's defining features?

- Language Support:
	- C (Dennis Ritchie)
		- "Different"
	- Alef
		- GoC
		- recieve.l
		- Later replaced with c threading lib
	- rc
		- awk, sed, sam (ssam)

- UTF-8 everything
	- Invented for Plan 9

- Distributed
- Filesystems / Namespaces

More on that later.

# When?

Press Notes+ and see!


# References
[1]: http://doc.cat-v.org/plan_9/1st_edition/designing_plan_9
[2]: http://doc.cat-v.org/plan_9/4th_edition/papers/names
[3]: http://cm.bell-labs.com/sys/man/preface.html
[4]: http://harmful.cat-v.org/software/andy_tanenbaum
[5]: http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.41.9192