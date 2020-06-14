### Name: Candroid
Value: 50<br>
Description: I think I can, I think I can! <br><br>Download the file below.
<br>

![alt text](https://github.com/PrathmeshPure/CTF-Writeups/blob/master/NahamCon%20CTF/Mobile/Candroid/chall.png "Challenge")


Decompile the apk file using below command<br>

`jadx /path/Candroid/candroid.apk`

After checking the source, flag can be seen at <br>

`/path/candroid/resources/res/values/strings.xml`

<br>

`flag{4ndr0id_1s_3asy}`
