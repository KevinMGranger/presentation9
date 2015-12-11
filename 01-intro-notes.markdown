# What is Plan 9?

- Multi-processing, multi-tasking, general purpose OS.
- Had features typically reserved for other "types" of OSes:
	- 

- Distributed
	- In order to take advantage of advancements in technology in separate areas
	- "efficiency, security, simplicity, and reliability" / "cost-effectiveness, maintenance, performance, reliability, and security" [1]
	- In a standard Plan 9 setup, one computer handles storage, one handles computing, and you sit at a graphical terminal [1]

- Unix, but unix-y-er.
	- Radical Simplicity
		- GNU cat:  782 lines, 22,684 chars
		- plan 9 cat.c: 35 lines, 531 chars
	- "The foundations of the system are built on two ideas: a per-process name space and a simple message-oriented file system protocol." [2]

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
	- rc
		- awk, sed, sam (ssam)

- UTF-8 everything
	- Invented for Plan 9

# When?

Press Notes+ and see!


# References
[1]: http://doc.cat-v.org/plan_9/1st_edition/designing_plan_9
[2]: http://doc.cat-v.org/plan_9/4th_edition/papers/names
[3]: http://cm.bell-labs.com/sys/man/preface.html