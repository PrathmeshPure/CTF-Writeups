### Name: Cow Pie
Value: 125<br>
Description: Ew. Some cow left this for us. It's gross... but something doesn't seem right... <br><br>Download the file below.
<br>
![alt text](https://github.com/PrathmeshPure/CTF-Writeups/blob/master/NahamCon%20CTF/Forensics/Cow%20Pie/chall.png "Challenge")


Using file command gives information<br>

`manure: QEMU QCOW2 Image (v3), 1153536 bytes`


So its a disk image.<br>

Simply using `strings` command gives output like-<br>

![alt text](https://github.com/PrathmeshPure/CTF-Writeups/blob/master/NahamCon%20CTF/Forensics/Cow%20Pie/flag.png "Challenge")

`flag{this_flag_says_mooo_what_say_you}`
