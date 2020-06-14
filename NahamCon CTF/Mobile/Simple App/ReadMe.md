### Name: Simple App
Value: 50<br>
Description: Here's a simple Android app. Can you get the flag? <br><br>Download the file below.
<br>

![alt text](https://github.com/PrathmeshPure/CTF-Writeups/blob/master/NahamCon%20CTF/Mobile/Simple%20App/chall.png "Challenge")

Decompile the apk file using below command<br>

`jadx /path/Simple\ App/simple-app.apk`

After checking the source, flag can be seen at <br>

`/path/simple_app/MainActivity.java`

<br>

`flag{3asY_4ndr0id_r3vers1ng}`
