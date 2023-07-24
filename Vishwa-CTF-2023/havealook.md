Hello everyone, here I will describe my first CTF challenge that I ever passed. This task is not difficult, but interesting: two specific ways of information hiding are used, and to get the encrypted information you have to use two different tools.

![VishwaCTF](https://i.imgur.com/aQBD7oO.png "VishwaCTF")

<br>
<br>

In the folder containing this walkthrough you will find an image file in jpeg format. At first glance it looks like a normal image, but the category of this challenge is steganography, which means that this file contains an encrypted message.

![havealook](https://i.imgur.com/CnRxyDO.png "havealook")

------------

<br>
<br>
Let's go straight to the solution. There are several technologies that allow you to hide a file inside another. One of them is RARJPG, which allows you to hide a RAR archive inside a JPG image. By opening the image with the WinRar, we get access to the contents of the archive.

![RAR](https://i.imgur.com/SSHlmCc.png "RAR")
<br><br>
What do we see here? A sound file in WAV format. Playing it does not give us any useful information. We could assume that the flag is encoded with some kind of Morse code, but in fact to extract the flag we need to know what a spectrogram is.
<br>


------------

<br>

Any audio signal can be visualised in a number of ways. A waveform shows how the amplitude of a sound wave changes over time.

![Waveform](https://i.imgur.com/aiJlYqj.png "Waveform")

------------
<br>

Spectrum analysers show what frequency range the audio is in at any given time.

![Spectrum ](https://i.imgur.com/dijEok1.png "Spectrum ")

------------

<br>
When we combine these two types of visualisation, we can literally see three aspects of audio: duration over time, frequency range and loudness of a particular frequency. This is what the spectrogram was invented for. Look at the image below: it's a fragment of a human voice.

![](https://i.imgur.com/w9jlG44.png)

On the horizontal axis is a timeline. On the vertical axis is the frequency range, from 0 Hertz at the bottom to 22000 Hertz at the top. The colour represents the volume: from absolute silence in black to maximum volume in white.

<br>

A spectrogram turns an audio file into a canvas on which you can literally draw in specialised audio editors. When we open the same audio file in the spectrogram editor, we see a flag.

![](https://i.imgur.com/MDWVjsi.png)

<br>

I used the Izotope RX 10 audio editor to solve this task, but you can easily find services on the internet to display the spectrogram.

![](https://i.imgur.com/31jjHl3.png)

------------


<br>
Thanks for reading, I hope you found this walkthrough interesting, useful and learned something new!

<br>

### Useful links

<br>

 * [Simple Help: How to Hide a .rar File Within an Image File](https://www.simplehelp.net/2008/12/04/how-to-hide-rar-files-within-picture-files/ " Simple Help: How to Hide a .rar File Within an Image File")
 * [Hacktrix: How To Hide Your Files And Folders Inside Images](https://www.hacktrix.com/how-to-hide-your-files-and-folders-inside-images "How To Hide Your Files And Folders Inside Images")
 * [Spectral analyzer of Signals](https://www.dcode.fr/spectral-analysis "Spectral analyzer of Signals")
 * [Izotope: Understanding Spectrograms](https://www.izotope.com/en/learn/understanding-spectrograms.html "Izotope: Understanding Spectrograms")
 * [Christian Espinosa on Youtube: Hide a Message in an Audio File](https://www.youtube.com/watch?v=1EqCQrVEEVs " Steganography: Hide a Message in an Audio File Christian Espinosa")
 * [Another cool writeup from VishwaCTF](https://dev.to/lambdamamba/ctf-writeup-vishwactf-2022-3me5)
