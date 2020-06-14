### Name: Microsooft
Value: 100<br>
Description: We have to use Microsoft Word at the office!? Oof... <br><br>Download the file below.
<br>

![alt text](https://github.com/PrathmeshPure/CTF-Writeups/blob/master/NahamCon%20CTF/Forensics/Microsooft/chall.png "Challenge")

<br>

Running `binwalk` on given [<a href=https://github.com/PrathmeshPure/CTF-Writeups/blob/master/NahamCon%20CTF/Forensics/Microsooft/microsooft.docx>file</a>, `src/oof.txt` is in the `docx` file.<br>

![alt text](https://github.com/PrathmeshPure/CTF-Writeups/blob/master/NahamCon%20CTF/Forensics/Microsooft/1st.png "Output")

<br>

![alt text](https://github.com/PrathmeshPure/CTF-Writeups/blob/master/NahamCon%20CTF/Forensics/Microsooft/2nd.png "Output")

<br>

Opening `txt` file, flag can be seen in plain text.
<br>

![alt text](https://github.com/PrathmeshPure/CTF-Writeups/blob/master/NahamCon%20CTF/Forensics/Microsooft/flag.png "Output")
<br>

`flag{oof_is_right_why_gfxdata_though}`
