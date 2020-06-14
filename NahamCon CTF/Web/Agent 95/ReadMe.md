### Name: Agent 95
Value: 50<br>
Description: They've given you a number, and taken away your name~ <br><br>Connect here:<br><a href="http://jh2i.com:50000">http://jh2i.com:50000</a>
<br>
![alt text](https://github.com/PrathmeshPure/CTF-Writeups/tree/master/NahamCon%20CTF/Web/Agent%2095/chall.png "Challenge")

On loading given link,<br>

![alt text](https://github.com/PrathmeshPure/CTF-Writeups/tree/master/NahamCon%20CTF/Web/Agent%2095/1st.png "Challenge")

So simply changing user agent to `Mozilla/4.0 (compatible; MSIE 5.50; Windows 95; SiteKiosk 4.8)` for request, gives flag.<br>

![alt text](https://github.com/PrathmeshPure/CTF-Writeups/tree/master/NahamCon%20CTF/Web/Agent%2095/flag.png "Challenge")

`flag{user_agents_undercover}`

