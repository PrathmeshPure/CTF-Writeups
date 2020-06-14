Name: Ooo-la-la
Value: 100
Description: Uwu, wow! Those numbers are fine! <br><br>Download the file below.

flag{ooo_la_la_those_are_sexy_primes}

```python
#rsa algorithm
#formulae required
#p,q large random prime numbers
#n=p*q
#phi=(p-1)*(q-q)
#e=3
#to encrypt cipher=data^e mod n
#consider k=2
#d= (k*phi+1)/e
#to decrypt
#plain = cipher^d mod n
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
plain = pow(cipher, d, n)# % n
print("plain > ",plain)

print(long_to_bytes(plain))

```
