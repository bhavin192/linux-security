### SELinux 

Security Enhanced Linux


- Linux Kernel security module 

- Mandatory access control (MAC) over resources 

- Project started by NSA 

---

#### Limitations of DAC

Discretionary access control


- Only two categories of users, administrator and non-administrator

- Process launched by user has same rights as user

- Process can alter security properties of files

- Example - ssh keys can be read by other software

---

#### The solution SELinux

non-discretionary access control or MAC 

- Adds new security properties to files, processes, sockets, ports

- Flexible security policies which can be changed

- Implemented in the Linux Kernel using Linux Security Module framework

---

#### SELinux Contexts 

SELinux policy rule

- Files and processes are labled with context
- It includes user, role, type which helps to decide the access

```sh
[fido@localhost ~]$ ls -Z /etc/passwd
system_u:object_r:passwd_file_t:s0 /etc/passwd


[fido@localhost ~]$ ls -Z /usr/bin/passwd
system_u:object_r:passwd_exec_t:s0 /usr/bin/passwd

```
---

#### SELinux policies 

SELinux has three modes 

- Enforcing

- Permissive

- Disabled 

---

#### Changing Policy 

```sh
[fido@localhost ~]$ getenforce
Enforcing
  

[fido@localhost ~]$ setenforce --help
usage:  setenforce [ Enforcing | Permissive | 1 | 0 ]


[fido@localhost ~]$ setenforce 0


[fido@localhost ~]$ getenforce
Permissive


```

@[1-2](Get the current policy)
@[5-6](setenforce help)
@[9-13](Changing the policy to Permissive)
@[14-15](To disable the SELinux, edit the configuration file `/etc/selinux/config` and change `SELINUX=disabled`)
