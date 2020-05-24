# EXCLUSIVE

![challenge.png](https://github.com/PrathmeshPure/CTF-Writeups/blob/master/Null%20Breaker/Forensic/Exclusive/challenge.png)

Below two images were given in this challenge.( whereami.bmp and xor-gate-symbol.jpg)

![whereami.bmp](https://github.com/PrathmeshPure/CTF-Writeups/blob/master/Null%20Breaker/Forensic/Exclusive/whereami.bmp)

![xor-gate-symbol.jpg](https://github.com/PrathmeshPure/CTF-Writeups/blob/master/Null%20Breaker/Forensic/Exclusive/xor-gate-symbol.jpg)

xor-gate-symbol.jpg this name was giving me hint of combining images in StegSolve, but doing so with given images was not giving any output.

So I tried binwalk on both images.

![whereami_binwalk](https://github.com/PrathmeshPure/CTF-Writeups/blob/master/Null%20Breaker/Forensic/Exclusive/supporting/whereami_binwalk.png)

![xor_binwalk](https://github.com/PrathmeshPure/CTF-Writeups/blob/master/Null%20Breaker/Forensic/Exclusive/supporting/xor_binwalk.png)

OK, so I can see two JPEG files, lets try to extract it.

![xor_binwalk-e](https://github.com/PrathmeshPure/CTF-Writeups/blob/master/Null%20Breaker/Forensic/Exclusive/supporting/xor_binwalk-e.png)

So you can see that, there is this image

![extracted](https://github.com/PrathmeshPure/CTF-Writeups/blob/master/Null%20Breaker/Forensic/Exclusive/supporting/extracted.jpeg)

```
So simply rename this file with <b>jpeg</b> extention.
```

![rename](https://github.com/PrathmeshPure/CTF-Writeups/blob/master/Null%20Breaker/Forensic/Exclusive/supporting/rename.png)
```
Now open whereami.bmp in <b>StegSolve</b> and select <b>exctracted.jpeg</b> using Image combiner option.
So you will see below output.
```
![solved](https://github.com/PrathmeshPure/CTF-Writeups/blob/master/Null%20Breaker/Forensic/Exclusive/supporting/solved.bmp)

You can see flag on left side, but its not readable.

I took a screenshot of it for better visibility.

![screenshot](https://github.com/PrathmeshPure/CTF-Writeups/blob/master/Null%20Breaker/Forensic/Exclusive/supporting/screenshot.png)

```
<b>nbCTF{n0_on3_i5_saf3}</b> is the flag.
```
