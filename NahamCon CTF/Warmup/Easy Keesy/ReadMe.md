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

