# Security

- Multiple approaches to security

- "Everything is a file(system)"
  - All files and file systems represented by 9P

- Each process has its own name space
  - Makes adding and removing resources from a process simple
  - Sandboxing

- Group and User IDs are strings

- Host owner
  - Standard user account, no special privileges
    - Not like UNIX's "root"
  - Usually whoever booted the terminal
  - Owns all of the machine's resources

- Factotum
  - Like the rest of Plan 9, implemented as a file server
    - Technically a program
  - Used for user authentication
  - Holds keys
