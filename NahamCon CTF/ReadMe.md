# NahamCon CTF Writeup
Hello Folks, I am Prathamesh, back again with another writeup.
This writeup is of NahamCon CTF (https://ctf.nahamcon.com) event.

![alt text](https://d24wuq6o951i2g.cloudfront.net/img/events/id/457/457748121/assets/5b11c1bdf53d63178f90d97d6dc2db87.NahamCon-Logo-Vertical-Main-.png "NahamCon Logo")

Hosted on 12 June, 20:30 IST — 14 June 2020, 03:30 IST Jeopardy On-line

## Category Warmup

### Name: CLIsay
Value: 20
Description: cowsay is hiding something from us!

![alt text](https://github.com/PrathmeshPure/CTF-Writeups/blob/master/NahamCon%20CTF/Warmup/CLIsay/chall.png "Challenge")

For this challenge `ELF` library was given.

```
clisay: ELF 64-bit LSB pie executable, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, BuildID[sha1]=70e60678f1c0b75ea3aae2a4e8e1e8978e3c6fc0, for GNU/Linux 3.2.0, not stripped
```

![Given File](https://github.com/PrathmeshPure/CTF-Writeups/blob/master/NahamCon%20CTF/Warmup/CLIsay/clisay)

For analysis the file, I used https://cloud.binary.ninja and could see the flag in plain text.

![alt text](https://github.com/PrathmeshPure/CTF-Writeups/blob/master/NahamCon%20CTF/Warmup/CLIsay/flag.png "Flag")

`flag{Y0u_c4n_r3Ad_M1nd5}`

### Name: Metameme
Value: 25
Description: Hacker memes. So meta.

![alt text](https://github.com/PrathmeshPure/CTF-Writeups/blob/master/NahamCon%20CTF/Warmup/Metameme/chall.png "Challenge")

Only `JPG` file was given, and name is suggesting `Meta`
![alt text](https://github.com/PrathmeshPure/CTF-Writeups/blob/master/NahamCon%20CTF/Warmup/Metameme/hackermeme.jpg "Given Image")
exiftool to the rescue.

`>> exiftool hackermeme.jpg `

![alt text](https://github.com/PrathmeshPure/CTF-Writeups/blob/master/NahamCon%20CTF/Warmup/Metameme/flag.png "Flag")

`flag{N0t_7h3_4cTuaL_Cr3At0r}`

### Name: Mr. Robot
Value: 25
Description: Elliot needs your help. You know what to do. Connect here:http://jh2i.com:50032

![alt text](https://github.com/PrathmeshPure/CTF-Writeups/blob/master/NahamCon%20CTF/Warmup/Mr%20Robot/chall.png "Challenge")

Name itself is a hint for this challenge.
Flag was present at http://jh2i.com:50032/robots.txt
`flag{welcome_to_robots.txt}`

### Name: Easy Keesy
Value: 30
Description: Dang it, not again...

![alt text](https://github.com/PrathmeshPure/CTF-Writeups/blob/master/NahamCon%20CTF/Warmup/Easy%20Keesy/chall.png "Challenge")

For this challenge `KDBX` file was given.
`Keepass password database 2.x KDBX`

Firstly rename the file, then generate its hash by `keepass2john` by below commands.
```
>> mv easy_keesy easy_keesy.kdbx
>> keepass2john easy_keesy.kdbx > easy_keesy.kdbx.hash
>> cat easy_keesy.kdbx.hash

easy_keesy:$keepass$*2*100000*0*d92288b1c51244a6b5adf65895aef924ddc083a819e0dbd387e7b842649c7974*af85267b1972de6c67cd4fa43d6b4d1b212516d4acd801643e8440f043332477*2d587ad4c839c1d2265525946215fb7e*215547d465bc6fb180a17abbd51625c4c3159b555d880d95400002355f7e2ab8*fbdc2c7d91a59d942e71d6b4d089e3ecbea5a2ab4d86094a6e777626b8779504
```
Save below part of the output to file.
```
$keepass$*2*100000*0*d92288b1c51244a6b5adf65895aef924ddc083a819e0dbd387e7b842649c7974*af85267b1972de6c67cd4fa43d6b4d1b212516d4acd801643e8440f043332477*2d587ad4c839c1d2265525946215fb7e*215547d465bc6fb180a17abbd51625c4c3159b555d880d95400002355f7e2ab8*fbdc2c7d91a59d942e71d6b4d089e3ecbea5a2ab4d86094a6e777626b8779504
```
Then crack the hash by below command.
`>> hashcat --force -a 0 -m 13400 easy_keesy.txt /usr/share/wordlists/rockyou.txt`

![alt text](https://github.com/PrathmeshPure/CTF-Writeups/blob/master/NahamCon%20CTF/Warmup/Easy%20Keesy/1st.png "Output")
![alt text](https://github.com/PrathmeshPure/CTF-Writeups/blob/master/NahamCon%20CTF/Warmup/Easy%20Keesy/2nd.png "Output")

From the output, password can be seen(monkey).

Just by opening the Keepass file in application and submitting the password, flag is waiting for you.
![alt text](https://github.com/PrathmeshPure/CTF-Writeups/blob/master/NahamCon%20CTF/Warmup/Easy%Keesy/flag.png "Flag")

`flag{jtr_found_the_keys_to_kingdom}`

### Name: Pang
Value: 40
Description: This file does not open!

![alt text](https://github.com/PrathmeshPure/CTF-Writeups/blob/master/NahamCon%20CTF/Warmup/Pang/chall.png "Challenge")

File named Pang was given.

![Given File](https://github.com/PrathmeshPure/CTF-Writeups/blob/master/NahamCon%20CTF/Warmup/Pang/pang)

Using file command, its confirm that its PNG image.

Tried renaming it to png, But it can't be opened.

![alt text](https://github.com/PrathmeshPure/CTF-Writeups/blob/master/NahamCon%20CTF/Warmup/Pang/1st.png "Output")

Again strings command to the rescue.
![alt text](https://github.com/PrathmeshPure/CTF-Writeups/blob/master/NahamCon%20CTF/Warmup/Pang/flag.png "Flag")

`flag{wham_bam_thank_you_for_the_flag_maam}`
