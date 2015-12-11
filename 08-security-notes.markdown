# Security

- Plan 9 takes multiple approaches to security.

- As was mentioned, every system resource in Plan 9 is represented as a file system.  Thus, all operations with these "files" are done by a single protocol, 9P.

- Each running process has its own private view of the system called a name space.
  - Because of this, resources (represented as files) can be added and removed from name spaces very simply.
  - Sandboxing applications is also possible and simple.

- In Plan 9, all group and user IDs are strings, as opposed to the numerical UIDs of UNIX.

- While in UNIX, there exists a user named "root", with special privileges and access to system resources, Plan 9 instad has a Host owner.  

- Host owner is a standard user account with no special privileges like root, but who owns all of the machine's resources.
  - The host owner is usually whoever booted the machine.

- For authentication and secret data, like keys, Plan 9 makes use of a program called Factotum.
  - Like everything else in Plan 9, factotum is accessed as a file system.
  - Factotum is responsible for handling the user's keys and managing authentication protocols.

- To quote a paper by the developers:

Concentrating security code in a single program offers several advantages including: ease of update or repair to broken security software and protocols; the ability to run secure services at a lower privilege level; uniform management of keys for all services; and an opportunity to provide single sign on, even to unchanged legacy applications.
