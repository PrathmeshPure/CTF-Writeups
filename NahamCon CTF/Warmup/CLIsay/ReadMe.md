### Name: CLIsay
Value: 20<br>
Description: cowsay is hiding something from us!
<br>

![alt text](https://github.com/PrathmeshPure/CTF-Writeups/blob/master/NahamCon%20CTF/Warmup/CLIsay/chall.png "Challenge")

<br>
For this challenge `ELF` library was given.
<br>

```
clisay: ELF 64-bit LSB pie executable, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, BuildID[sha1]=70e60678f1c0b75ea3aae2a4e8e1e8978e3c6fc0, for GNU/Linux 3.2.0, not stripped
```

![Given File](https://github.com/PrathmeshPure/CTF-Writeups/blob/master/NahamCon%20CTF/Warmup/CLIsay/clisay)

<br>
For analysis the file, I used https://cloud.binary.ninja and could see the flag in plain text.

![alt text](https://github.com/PrathmeshPure/CTF-Writeups/blob/master/NahamCon%20CTF/Warmup/CLIsay/flag.png "Flag")


`flag{Y0u_c4n_r3Ad_M1nd5}`