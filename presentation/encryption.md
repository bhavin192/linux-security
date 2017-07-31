### Disk Encryption


<span>Why disk encryption?</span>

<span>What is disk encryption?</span>

<span>Encrypting using dm-crypt/LUKS</span>

<span>Creating encrypted block in anaconda</span>

---

### Why disk <span style="color: #e49436">encryption</span>?


- one can easily view/copy disk contents using live boot
 
- Encryption provides
    - **Confidentiality**
	- **Availability**

---

### What is disk encryption?

- Protects the data and require passphrase/key as authentication to decrypt

- Additional security beyond existing OS security mechanisms

- Protects the data even if it has been physically removed from the system

---

### Encryption using <span style="color: #e49436">dm-crypt/LUKS</span>

**Linux Unified Key Setup(LUKS)** is a specification for device encryption

- LUKS uses kernel device mapper subsystem via dm-crypt module

- Creating and accessing encrypted device through ```cryptsetup``` utility

- LUKS also protecting mobile devices as
    - Removable storage media
	- Laptop disk drives

---

### Creating encrypted block in anaconda

- Create encrypted devices during system installation

    - Indivisual partition

	- software RAID array

	- logical volume

- **anaconda** offers option to set global passphrase for devices
