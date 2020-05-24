# EXCLUSIVE
## Category- Forensic
### Given Question-
### Two soldiers are communicating through pictures. The war created lots of loss to both parties. You need to find out what is their last message.


![alt text](https://github.com/PrathmeshPure/CTF-Writeups/blob/master/Null%20Breaker/Forensic/Exclusive/challenge.png)

Below two images were given in this challenge.( whereami.bmp and xor-gate-symbol.jpg)

![alt text](https://github.com/PrathmeshPure/CTF-Writeups/blob/master/Null%20Breaker/Forensic/Exclusive/whereami.bmp)

![alt text](https://github.com/PrathmeshPure/CTF-Writeups/blob/master/Null%20Breaker/Forensic/Exclusive/xor-gate-symbol.jpg)

`xor-gate-symbol.jpg` this name was giving me hint of combining images in `StegSolve`, but doing so with given images was not giving any output.

So I tried binwalk on both images.

![alt text](https://github.com/PrathmeshPure/CTF-Writeups/blob/master/Null%20Breaker/Forensic/Exclusive/supporting/whereami_binwalk.png)

![alt text](https://github.com/PrathmeshPure/CTF-Writeups/blob/master/Null%20Breaker/Forensic/Exclusive/supporting/xor_binwalk.png)

OK, so I can see two JPEG files, lets try to extract it.

![alt text](https://github.com/PrathmeshPure/CTF-Writeups/blob/master/Null%20Breaker/Forensic/Exclusive/supporting/xor_binwalk-e.png)

So you can see that, there is this image

![alt text](https://github.com/PrathmeshPure/CTF-Writeups/blob/master/Null%20Breaker/Forensic/Exclusive/supporting/extracted.jpeg)

So simply rename this file with `jpeg` extention.

![alt text](https://github.com/PrathmeshPure/CTF-Writeups/blob/master/Null%20Breaker/Forensic/Exclusive/supporting/rename.png)

Now open `whereami.bmp` in `StegSolve` and select `exctracted.jpeg` using `Image combiner` option.

So you will see below output.

![alt text](https://github.com/PrathmeshPure/CTF-Writeups/blob/master/Null%20Breaker/Forensic/Exclusive/supporting/solved.bmp)

You can see flag on left side, but its not readable.

I took a screenshot of it for better visibility.

![alt text](https://github.com/PrathmeshPure/CTF-Writeups/blob/master/Null%20Breaker/Forensic/Exclusive/supporting/screenshot.png)

`nbCTF{n0_on3_i5_saf3}` is the flag.
