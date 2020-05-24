# NuLL_Br3aker_2020 CTF Writeup
Hello Folks, I am Prathamesh, I have recently started with CTFs.
This is my very first writeup on CTF(So please bear with me) and will be sharing more from now.
### EXCLUSIVE by NuLL Br3aker 2020 (https://ctf.0xdeadbeef.games/)
#### Category- Forensic
#### Given Question-
#### Two soldiers are communicating through pictures. The war created lots of loss to both parties. You need to find out what is their last message.
![alt text](https://github.com/PrathmeshPure/CTF-Writeups/blob/master/Null%20Breaker/Forensic/Exclusive/challenge.png)
Below two images were given in this challenge. ( whereami.bmp and xor-gate-symbol.jpg)
![alt text](https://github.com/PrathmeshPure/CTF-Writeups/blob/master/Null%20Breaker/Forensic/Exclusive/whereami.bmp)
![alt text](https://github.com/PrathmeshPure/CTF-Writeups/blob/master/Null%20Breaker/Forensic/Exclusive/xor-gate-symbol.jpg)
`xor-gate-symbol.jpg` this name was giving me a hint of combining images in `StegSolve`, but doing so with given images was not giving any output.
So I tried binwalk on both images.
![alt text](https://github.com/PrathmeshPure/CTF-Writeups/blob/master/Null%20Breaker/Forensic/Exclusive/supporting/whereami_binwalk.png)
![alt text](https://github.com/PrathmeshPure/CTF-Writeups/blob/master/Null%20Breaker/Forensic/Exclusive/supporting/xor_binwalk.png)
OK, so I can see two JPEG files, let's try to extract it.
![alt text](https://github.com/PrathmeshPure/CTF-Writeups/blob/master/Null%20Breaker/Forensic/Exclusive/supporting/xor_binwalk-e.png)
So you can see that, there is this image
![alt text](https://github.com/PrathmeshPure/CTF-Writeups/blob/master/Null%20Breaker/Forensic/Exclusive/supporting/extracted.jpeg)
So simply rename this file with `jpeg` extension.
![alt text](https://github.com/PrathmeshPure/CTF-Writeups/blob/master/Null%20Breaker/Forensic/Exclusive/supporting/rename.png)
Now open `whereami.bmp` in `StegSolve` and select `exctracted.jpeg` using `Image combiner` option.
So you will see below output.
![alt text](https://github.com/PrathmeshPure/CTF-Writeups/blob/master/Null%20Breaker/Forensic/Exclusive/supporting/solved.bmp)
You can see the flag on the left side, but it's not readable.
I took a screenshot of it for better visibility.
![alt text](https://github.com/PrathmeshPure/CTF-Writeups/blob/master/Null%20Breaker/Forensic/Exclusive/supporting/screenshot.png)
`nbCTF{n0_on3_i5_saf3}` is the flag.