---
title: "Tempo as a Means of Understanding Time in PTA's Filmography"
author: Lucia Engelhardt
layout: data-essay
featured_image: punc-04151
tags:
    - Tempo
---
## What is Tempo?

Tempo is most often thought of as a characteristic of music. Tempo measures the pace of a song through beats per minute (BPM). However, tempo can also be used to understand a film's flow. But what does this look like? [^1]

## Tempo in Film
Within films, some moments feel noticeably faster or slower than the rest of the film. This variation in perceived time is a tool filmmakers use for a multitude of reasons. An example of these could be: action scenes with lots of dynamic movement and quick cutting to portray fighting; the moment before someone gets caught by a killer is slowed down by using slower movements and longer takes to draw out the audience’s anxiety making them feel more on edge; or a round of consecutive quick scenes to convey a passage of time to an audience (like in training montages). [^2]

Bordwell describes varying techniques filmmakers employ to change the tempo of their film: shots with lots of fast movement captured (actors running, objects moving fast, disco strobe), intense and dynamic camera movement (whiplash pans, jerky reframings, rack focusing), or quick cutting (making the length of each shot super short). 

The principal method Bordwell discusses to understand film tempo is through average shot length (ASL). This is one of the primary ways I explore tempo within PTA’s films.


## How To Measure Tempo in Film
Many techniques can be employed to help change the tempo of a film: shots with lots of fast movement captured (actors running, objects moving fast, disco strobe), intense and dynamic camera movement (whiplash pans, jerky reframings, rack focusing), or quick cutting (making the length of each shot super short). The data in this feature uses the average shot length (ASL) to measure the tempo of PTA’s films. [^3]

## David Bordwell’s The Way Hollywood Tells It: 
Bordwell is a prominent film theorist whose work is often used in film analysis courses. In his book The Way Hollywood Sees It: Story and Style in Modern Movies, he follows the changing techniques of filmmakers over time. He ultimately argues that filmmakers have less creative freedom in terms of the tools they use for filmmaking due to pressure to use new dominant technologies. 
Bordwell discusses the increase in quicker cutting (having more shots per film and shorter ASL) over time. I based my study of PTA’s film tempo on Bordwell’s breakdown of quick cutting. My goal is to bridge technical aspects of filmmaking/film theory to the experience of viewing one of PTA’s films. Hopefully, these insights will arise during your own viewing experience on whether or not certain moments feel slower/faster, why this happens, and if PTA is successful in using tempo as a means to convey meaning in his films. 


## Methods

**Figure I: PT-Annotated Screenshots**

Figure I was a means to represent one of Bordwell’s offered ways of measuring film tempo (through changes in shots/movement on camera). The guidelines for taking screenshots of PTA’s films were as follows:
    1. Capture a screenshot any time the focus of the frame changes (shows something new)
    2. Screenshot title cards/title screens at start of film (even when it’s a blank screen)
    3. Don’t take a screenshot every time the camera switches for shot-reverse-shots during conversations, only when                           something new occurs within the shot-reverse-shot scene (i.e., change in angle, new character, etc.). 
    4. Too many screenshots are better than not enough
These screenshot guidelines essentially demonstrate what was deemed as important information while watching each film from the perspective of whoever took the screenshots. 

After compiling all of the screenshots and necessary metadata (screenshot timestamp, scene, and film), I used JupyterLab and Vega-Altair to create a strip-plot graph displaying all ten of PTA’s films along with a thumbnail for each screenshot taken. 

**Figure II: ASL of PTA’s Films ** 
To capture the ASL of PTA’s films, I used open-source code from Distant Viewing Explorer to detect the shot boundaries (when one shot is cut/transitions to another shot) of each film. [^4] I then downloaded each film and converted the film files to mp4’s using ffmpeg. Next, I ran the converted MP4 through the Distant Viewing code, which produced a table with information about how many shot boundaries the film has, the timestamp (start and end of each shot), and the length of the shot. I compiled this information into a data sheet and, in JupyterLab, used Vega-Altair to make a scatter plot. The graph plots each sequential shot of every film (x-axis) and how long the shot is (y-axis). Thus, this graph displays the ASL of every one of PTA’s films. 


## The Rhythm of PTA through PT-Annotated Screenshots

<div class="mb-4">
<div class="embed-responsive ratio ratio-4x3">
<iframe src="https://lucia-engelhardt.github.io/data-essays/graph/finished-ss-graph(4).html" width="100%" ></iframe></div></div>

How to use the graph: if you hover your mouse over a tick, the thumbnail for the tick's screenshot appears. The x-axis is the timestamp at which the screenshot was taken during the film (all in sequential order), while the y-axis is each of PTA’s films. The bottom chart works as a slider. You can click and slide your mouse to examine specific moments in the films at a closer look. 

## ASL of PTA’s Films

<div class="mb-4">
<div class="embed-responsive ratio ratio-4x3">
<iframe src="https://lucia-engelhardt.github.io/data-essays/graph/asl-finished-scatterplot(2).html" width="100%" ></iframe></div></div>
 
How to use the graph: if you click on one of the films in the legend, you can examine one film at a time. You can also move around the graph and zoom in or out. If you hover your mouse over a point, you can see the point’s metadata. The x-axis is the number of the shot within the order of the film (the first shot all the way to the last shot in the film), while the y-axis displays the length of each shot in seconds. 

## Analysis


### Bibliography

[^1] Costa, Daniel. "tempo". Encyclopedia Britannica, 9 Apr. 2026, https://www.britannica.com/art/tempo-music. Accessed 6 July 2026.
[^2]     Bordwell, David. The Way Hollywood Tells It: Story and Style In Modern Movies. E-book, Berkeley: University of California Press, 2006, https://hdl.handle.net/2027/heb08199.0001.001.
[^3]    Bordwell, David. The Way Hollywood Tells It: Story and Style In Modern Movies. E-book, Berkeley: University of California Press, 2006, https://hdl.handle.net/2027/heb08199.0001.001.
[^4] Taylor Arnold and Lauren Tilon, Distant Viewing Explorer (2025). https://distantviewing.org/dvexplorer
