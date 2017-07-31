### Filesystem Hierarchy Standards 

#### Partioning


- Limits impact of disk failure 

- Creating backups 

- Allow admin to add restrictions 

---

### File System Hierarchy


- read-only or read-write

- suid or nosuid

- exec or noexec

- auto or noauto

- default

---

### chroot

root# chroot /mnt/foo/

- to run daemons out
- Linux cgroups & FreeBSD jails
- Provide safe build of Environment

---

### File System Check

root# fsck -y /dev/sda8

- run on currupt file
- recovery purpose
- rebooting is healthy after fscking

---

### Permission commands

-  $ ls -la /etc/abc.conf -rw-r--r-- 1 root root 405
-  $ chmod 644 /path/to/file
-  $ chmod 4644 /path/to/file
-  $ chown user:group /path/to/file
-  $ chgrp group /path/to/file
-  $ umask 033

---

