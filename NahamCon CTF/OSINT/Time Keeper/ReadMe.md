### Name: Time Keeper
Value: 50 <br>
Description: There is some interesting stuff on this website. Or at least, I thought there was... <br><br>Connect here:<br><a href="https://apporima.com/">https://apporima.com/</a><br><br>
<b>Note, this flag is not in the usual format.</b>
<br>

![alt text](https://github.com/PrathmeshPure/CTF-Writeups/blob/master/NahamCon%20CTF/OSINT/Time%20Keeper/chall.png "Challenge")

**Or at least, I thought there was** is giving hint to look for history or cached pages.
<br>
It can be done at https://web.archive.org/web/*/https://apporima.com/

<br>
It has some archieved pages from April
<br>

![alt text](https://github.com/PrathmeshPure/CTF-Writeups/blob/master/NahamCon%20CTF/OSINT/Time%20Keeper/1st.png "Output")

Checking cached page from April, It is saying flag is at /flag.txt

https://web.archive.org/web/20200418214642/https://apporima.com/
<br>

![alt text](https://github.com/PrathmeshPure/CTF-Writeups/blob/master/NahamCon%20CTF/OSINT/Time%20Keeper/2nd.png "Output")

On checking cached page /flag.txt at https://web.archive.org/web/*/https://apporima.com/flag.txt

<br>

![alt text](https://github.com/PrathmeshPure/CTF-Writeups/blob/master/NahamCon%20CTF/OSINT/Time%20Keeper/3rd.png "Output")

Finally going to history page of flag.txt, flag can be seen

https://web.archive.org/web/20200418213337/https://apporima.com/flag.txt
<br>

![alt text](https://github.com/PrathmeshPure/CTF-Writeups/blob/master/NahamCon%20CTF/OSINT/Time%20Keeper/flag.png "Flag")

`JCTF{the_wayback_machine}`