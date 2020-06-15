### Name: Localghost
Value: 75<br>
Description: BooOooOooOOoo! This spooOoOooky client-side cooOoOode sure is scary! What spoOoOoOoky secrets does he have in stooOoOoOore??<br><br>Connect here:<br><a href="http://jh2i.com:50003">http://jh2i.com:50003</a><br><br><b>Note, this flag is not in the usual format.</b>

<br>

![alt text](https://github.com/PrathmeshPure/CTF-Writeups/blob/master/NahamCon%20CTF/Web/Localghost/chall.png "Challenge")

On loading given link, pages seems ok.<br>
![alt text](https://github.com/PrathmeshPure/CTF-Writeups/blob/master/NahamCon%20CTF/Web/Localghost/ghost.png "Challenge")

view-source:http://jh2i.com:50003/jquery.jscroll2.js <br>
It shows Obfuscated Javascript</b>

![alt text](https://github.com/PrathmeshPure/CTF-Writeups/blob/master/NahamCon%20CTF/Web/Localghost/1st.png "Challenge")

Use Javascript Unobfuscator online

![alt text](https://github.com/PrathmeshPure/CTF-Writeups/blob/master/NahamCon%20CTF/Web/Localghost/2nd.png "Challenge")

From the output, below part can be seen,<br>

`"flag" = "SkNURntzcG9vb29va3lfZ2hvc3RzX2luX3N0b3JhZ2V9"`

Decoding it from `base64` gives plain flag.<br>

`JCTF{spoooooky_ghosts_in_storage}`