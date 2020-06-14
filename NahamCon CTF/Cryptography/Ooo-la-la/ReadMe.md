## Name: Ooo-la-la
Value: 100<br>
Description: Uwu, wow! Those numbers are fine! <br><br>Download the file below.
<br>

![alt text](https://github.com/PrathmeshPure/CTF-Writeups/blob/master/NahamCon%20CTF/Cryptography/Ooo-la-la/chall.png "Challenge")

<br>

Given information in txt file.<br>

```
N = 3349683240683303752040100187123245076775802838668125325785318315004398778586538866210198083573169673444543518654385038484177110828274648967185831623610409867689938609495858551308025785883804091
e = 65537
c = 87760575554266991015431110922576261532159376718765701749513766666239189012106797683148334771446801021047078003121816710825033894805743112580942399985961509685534309879621205633997976721084983
```
So its a RSA, we can factorise N online from http://factordb.com/
<br>

![alt text](https://github.com/PrathmeshPure/CTF-Writeups/blob/master/NahamCon%20CTF/Cryptography/Ooo-la-la/1st.png "Challenge")

<br>
Below is my solution to RSA decryption
<br>

```python
from Crypto.Util.number import *

p = 1830213987675567884451892843232991595746198390911664175679946063194531096037459873211879206428207
q = 1830213987675567884451892843232991595746198390911664175679946063194531096037459873211879206428213

n = p * q
phi = (p -1 ) * (q - 1)
e = 65537
print("e > ",e)

d = inverse(e, phi)
print("d > ",d)

cipher = 87760575554266991015431110922576261532159376718765701749513766666239189012106797683148334771446801021047078003121816710825033894805743112580942399985961509685534309879621205633997976721084983

plain = pow(cipher, d, n)

print(long_to_bytes(plain))

```

<br>
Running the program gives flag.
<br>

![alt text](https://github.com/PrathmeshPure/CTF-Writeups/blob/master/NahamCon%20CTF/Cryptography/Ooo-la-la/flag.png "Challenge")

<br>

`flag{ooo_la_la_those_are_sexy_primes}`