### Name: Doh
Value: 50<br>
Description: Doh! Stupid steganography... <br><br><b>Note, this flag is not in the usual format.</b><br><br>Download the file below.
<br>

![alt text](https://github.com/PrathmeshPure/CTF-Writeups/blob/master/NahamCon%20CTF/Steganography/Doh/chall.png "Challenge")

Below is the given `jpg` image.<br>

![alt text](https://github.com/PrathmeshPure/CTF-Writeups/blob/master/NahamCon%20CTF/Steganography/Doh/doh.jpg "Given")

Using `stegoveritas` , extracts `steghide_8ea5d9160d217f0d7bee4eafeea52339.bin` file.<br>

![alt text](https://github.com/PrathmeshPure/CTF-Writeups/blob/master/NahamCon%20CTF/Steganography/Doh/1st.png "Output")

Applying `strings` command on `bin` file, gives flag.<br>

![alt text](https://github.com/PrathmeshPure/CTF-Writeups/blob/master/NahamCon%20CTF/Steganography/Doh/flag.png "Flag")


`JCTF{an_annoyed_grunt}`
