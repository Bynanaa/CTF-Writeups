>#     Imaginary CTF 2023: signpost.misc

<br>
Hi everyone, I'd like to share with you how I passed the CTF task. It turned out to be quite difficult for me, but in many ways I made it difficult for myself. The task is called Signpost, category misc (osint). Here I will describe not only the steps to pass, but also the wrong approaches, so that you can learn from them. I hope the content is not only interesting but also useful.

<br>

## Reverse image searching
<br>

In the description of the task we are asked to find the exact location of the place where the photo was taken.

![](https://i.imgur.com/dEjymaV.png)
<br>
<br>
Here it is

![](https://i.imgur.com/eM1xWoN.png)

The task may seem difficult because there are tens of thousands of these signs in every big city, but the fact that we can distinguish the names of places on the signs makes it easier. However, the first thing I did was to try to find this photo by searching for images in search engines.

Of course, it didn't lead to anything: a unique photo of the sign, taken at an unknown time, in a low resolution, only gives false positives in search engines. Bing, Yandex, TinEye, Google - nothing gave a clear result.

![enter image description here](https://i.imgur.com/92JtetA.png)

However, in the course of completing the task, I came across a website that claims to be able to help you find the approximate location where the photo was taken. It didn't work for me either, but the examples on the site are impressive. Give it a try, this site will probably work better for you:

https://labs.tib.eu/geoestimation/

## Сrop circles

No metadata, no hidden rarjpg: just signposts with the names of the landmarks. Here I started googling, and although the search vector turned out to be correct, the mistake was that I didn't start the search in google, but in google maps. 

Don't ask me why (because I don't know), but I started my search with Scottsdale Stadium. After going through all the possible results, I assumed that this stadium was in Phoenix, Arizona and drew a circle on the map with a radius of 761 miles. I did the same for the Polo Grounds, but with a radius of 2925 miles.

![enter image description here](https://i.imgur.com/Sz0Hbue.png)

Look how cool I narrowed down the area to find the pointer (I didn't). Apart from the fact that the whole idea of radii on the map turned out to be completely useless (mainly because the signs describe distances to landmarks by road, not in a straight line), and due to the language barrier, I had to wade through a bunch of invalid Google Maps results.

Such results did not bring me any closer to a clue. However, a Google search for the Seals Stadium led me to a Wikipedia article. Was it helpful? Stadium was demolished in 1958 and is now replaced by a shopping centre. What is so special about it that a sign still points to it 70 years later? It seemed to raise more questions than answers.

Instead of taking a closer look at the search results or the wikipedia article, I drew a 2-mile radius circle around Seals Stadium and started checking literally every intersection, hoping to find a signpost somewhere. And after recognising the utter failure of the idea, I went back to Google. And look at this:
![enter image description here](https://i.imgur.com/9JeXr0y.png)![enter image description here](https://i.imgur.com/6kTutTH.png)

<br>
<br>
A pinterest picture search brings up a few other pictures of this pointer too. There can be no doubt about it: this is the sign at AT&T Stadium in San Francisco.

![enter image description here](https://i.imgur.com/rWhQptU.png)
<br>
<br>

But how do you find the exact spot where the photo was taken? I've walked around the stadium three times, looked at all the photos I could find, and I still can't find the sign in the stadium.

I couldn't have been wrong, could I? My last hope was YouTube: I hoped to find videos with "reviews" of the stadium.

I watched a couple of videos, only to become even more demotivated. I opened another video without much hope, and just as I was about to give up, a signpost appeared around the corner.

<br>

Below is the video in which the pointer appears. Click on it to play.

![enter image description here](https://github.com/Bynanaa/CTF-Writeups/blob/main/Imaginary%20CTF%202023/firefox_4BB4MlI0Cr.gif)


<br>

I quickly find the exact location and enter the coordinates of the flag. I get a hundred points, earned with blood and sweat, and go to bed with a clear conscience.


![](https://i.imgur.com/JVOm22X.png)
<br>

What lessons can we learn from this task? Sometimes the simplest way is the one that works. 


![enter image description here](https://www.cwl.nsw.gov.au/wp-content/uploads/2012/09/thank-you014.gif)

