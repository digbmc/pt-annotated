---
title: "Tempo and Shot Length in PTA's Filmography"
author: Lucia Engelhardt
layout: data-essay
featured_image: punc-04151
tags:
    - data-essay
    - pta
---

### Intro

The term tempo is often associated with music as a way to measure the pace of a song. However, within the context of film, tempo is used to describe the pacing of a film and how viewers experience the narrative speed (i.e., did the film feel long, short, etc). All films have varying degrees of temporality, with certain moments feeling slower or faster as a way to stand out from the rest of the film. For this reason, tempo is one of the key tools used by filmmakers to construct the narrative of their film. Examples of filmmakers manipulating tempo could be for battle scenes, the moment before someone gets murdered in a thriller, or a training montage. 
Bordwell describes varying techniques filmmakers employ to change the tempo of their film: shots with lots of fast movement captured (actors running, objects moving fast, disco strobe), intense and dynamic camera movement (whiplash pans, jerky reframings, rack focusing), or quick cutting (making the length of each shot super short). However, the main way Bordwell discusses tempo in film is through the lens of average shot length (ASL). [^1]

###Who is David Bordwell?

Bordwell is a prominent film theorist whose work is often used in film analysis course curricula. In his book *The Way Hollywood Sees It: Story and Style in Modern Movies*, he follows the changing techniques of filmmakers over time. One of Bordwell's chapters argues that filmmakers have less creative freedom in terms of the tools they use for filmmaking due to pressure to use new dominant technologies. Bordwell cites the increase in quicker cutting (having more shots per film and shorter ASL) over time as an example of this phenomenon. I based my study of PTA’s film tempo on Bordwell’s breakdown of quick cutting. My goal is to bridge technical aspects of filmmaking/film theory to the experience of viewing one of PTA’s films in an effort to discuss and understand film in a holistic way. 
The visualizations I made are ultimately to encourage viewers to compare their own experiences of watching PTA’s films to the filmmaking tools he’s employed. Some questions to think about when using these visualizations could be: what moments feel faster and slower in PTA’s films? Why do they feel different than the flow of the rest of the film? What was PTA trying to convey to viewers with these changes? And ultimately, is PTA successful with his application of tempo?[^2]

### Methods

**Gathering the Data**

For Figure I, I sorted through the PT-Annotated metadata for the process of capturing screenshots and cleaned it up. I only kept the necessary data for my visualization, which included: the screenshot IIIF manifests, the timestamp of screenshot/scene #, and the screenshot name in the PT-Annotated database. I then had to convert all of the screenshot timestamps to seconds to make it easier to graph them as data points.

For Figure II, I used the application [MakeMKV](https://www.makemkv.com/) to decrypt all ten of PTA's films and then produce MKV files. The DVDs for this process were acquired through Bryn Mawr's library system and are all owned by Bryn Mawr College. After procuring the MKV files of each DVD, I then converted the MKV files to MP4 files because MKV files are not compatible with [Distant Viewing Explorer's](https://distantviewing.org/dvexplorer/) open-source code. To convert MKV files to MP4, I used [FFmpeg](https://www.ffmpeg.org/). Once I had the MP4 files, I ran each one (one at a time) through [Distnat Viewing Explorer's open-source code](https://distantviewing.org/dvscripts/shot.html) in JupyterLab. This process takes a very long time (around forty to seventy minutes per file). Distant Viewing Explorer detects shot boundaries (when one shot is cut/transitions to another shot) of videos. Once the code finished running, the end result was a data table with the start and end times (in seconds) of every shot within the file, which I then converted to shot lengths. 

#### Figure I: PT-Annotated Screenshots

Figure I was a means to represent one of Bordwell’s offered ways of measuring film tempo (through changes in shots/movement on camera). The guidelines for taking screenshots of PTA’s films are as follows:
    1. Capture a screenshot any time the focus of the frame changes (shows something new) 
    2. Screenshot title cards/title screens at start of film (even when it’s a blank screen) 
    3. Don’t take a screenshot every time the camera switches for shot-reverse-shots during conversations, only when something new             occurs within the shot-reverse-shot scene (i.e., change in angle, new character, etc.) 
    4. Too many screenshots are better than not enough 
These screenshot guidelines essentially demonstrate what was deemed as important information while watching each film from the perspective of whoever took the screenshots. This visualization represents qualitative data and a viewer’s experience while watching PTA’s films.

#### Figure II: Shot Lengths and ASL of PTA’s Films

Figure II’s visualization includes a scatter plot with shot lengths and a bar chart with the ASL of each film. This data is quantitative and represents Bordwell’s main method of explaining the tempo of films through ASL. 

### Figure I

<div class="mb-4">
<div class="embed-responsive ratio ratio-4x3">
<iframe src="https://lucia-engelhardt.github.io/data-essays/graph/finished-ss-graph(5).html" width="100%" ></iframe></div></div>

How to use the graph: if you hover your mouse over a tick, the thumbnail for the tick's screenshot appears. The x-axis is the timestamp at which the screenshot was taken during the film (all in sequential order), while the y-axis is each of PTA’s films. The bottom chart works as a slider. You can click and slide your mouse to examine specific moments in the films at a closer look. 

### Figure II

<div class="mb-4">
<div class="embed-responsive ratio ratio-4x3">
<iframe src="https://lucia-engelhardt.github.io/data-essays/graph/asl-final-scatterplot(5).html" width="100%" ></iframe></div></div>
 
How to use the graph: if you click on one of the films in the legend, you can examine one film at a time. You can also move around the graph and zoom in or out. If you hover your mouse over a point, you can see the point’s metadata. The x-axis shows the shot number in the order of the film (from the first to the last), while the y-axis shows the length of each shot in seconds. 

### Analysis

As an example of the potential ways these graphs can be used for analysis, I will examine *Punch-Drunk Love*. Looking at the first half of the film, Figure I displays more breaks (pockets of no screenshots) occurring, while Figure II shows the shot lengths are consistently longer (which is an indicator of slow tempo based on Bordwell’s theory). This makes sense since the tempo of *Punch-Drunk Love*–like most films–begins on the slower end. The tempo increases throughout the film and being the quickest at the film’s climax. The film begins by following the inner workings of Barry Egan’s life before meeting Lena Leonard. As Barry's relationship with Lena grows, so does the speed of the film. 

An example of when PTA manipulates tempo to display shifting dynamics between Barry and Lena is during their date at the 43 minute (2,608 second) mark. Shot #129 is one of the longest shots during their date. Barry tells Lena his pudding scam secret, and the longer the shot continues, the more Barry opens up to Lena. Then, just as Barry finishes his story, Lena brings up an embarrassing story Barry’s sister told her about one of Barry’s outbursts. The viewer can immediately feel Barry close up. The shot feels quicker as Barry fidgets, and the tempo of the scene shifts and increases. Ultimately, reaching a crescendo in shot #132 after Barry abruptly announces he must go to the bathroom and then destroys the restaurant’s bathroom within the span of fourteen seconds (a relatively quick shot compared to the ASL of this film). 

The rest of the film feels increasingly fast. After Barry and Lena’s date, there is a rapid succession of quick shots (and lots of screenshots were captured during this time). The viewer can feel Barry get punched by his sudden and rapidly growing love for Lena through this change in tempo. 

Something interesting to note is that at some points Figures I and II oppose each other. Based on Bordwell’s theory of tempo, the quicker a film’s relative shot length, the faster the tempo should feel. When sequences involve many shot-reverse shots (typically during conversations) and no new information is being provided to the viewer (characters, angles, etc), fewer screenshots are taken. This makes sense based on the [screenshotting guidelines](#figure-i-pt-annotated-Screenshots) given to the screenshotters.  

An example of this is at the timestamp 1:28:49 (5,329 second mark) in *Magnolia*. During this scene, the reporter Gwenovier is confronting Frank Mackey about his family history. In Figure II, around shot # 366, there is no indication that the scene is slowing down, and rather, the shots following shot #366 are all much shorter than *Magnolia*’s ASL. However, the scene itself feels painfully slow as Mackey’s past slowly comes to light. The rhythm of the film stalls as the viewer awaits Mackey’s secret to be revealed, similar to waiting for a response with bated breath. 

This is why, although shot length can be useful to look at for understanding filmmaking techniques, quantitative data isn’t enough to understand the tempo of a film. Instances such as this are why it’s useful to have access to both visualizations when measuring tempo. Neither quantitative nor qualitative data alone is enough to understand tempo in a nuanced way. 

### Other Applications
Beyond examining one of PTA’s films, these visualizations could lend themselves to be useful for cross-examining PTA’s work with other famous directors, with films being produced now, or further temporal examination within film. Other research that explores tempo within film is:

Broberg and Panagiotidis' research which aims to explain the role of tempo in film and also conducts its own study of action films. The conclusion the essay reaches is that when shot lengths are shorter, the viewer will perceive the film as having a higher tempo.[^3] 

Adams et al. conducted a study to demonstrate how tempo is used by filmmakers. The study tests the ability of machine learning to see if it is able to gain important information about the film. The study was successful, and thus the authors conclude that shot length and motion can be used not only to change a film’s tempo but also to convey meaningful information to viewers. [^4]

### Bibliography
- Adams, Brett, Chitra Dorai, and Svetha Venkatesh. "Role of shot length in characterizing tempo 
    and dramatic story sections in motion pictures." (2000).
- Bordwell, David. *The Way Hollywood Tells It: Story and Style In Modern Movies*. E-book, 
    Berkeley: University of California Press, 2006, 
    https://hdl.handle.net/2027/heb08199.0001.001. 
- Broberg, Felix and Panagiotidis, Andreas. “Impact of shot length and motion on cinematic 
    tempo.” KTH Royal Institute of Technology, 2022, 
    https://kth.diva-portal.org/smash/get/diva2:1704346/FULLTEXT01.pdf.
- Costa, D. "tempo." *Encyclopedia Britannica*, April 9, 2026. 
    https://www.britannica.com/art/tempo-music. 
- Taylor Arnold and Lauren Tilon, *Distant Viewing Explorer* (2025). 
    https://distantviewing.org/dvexplorer 


[^1]:Bordwell, “Intensified Continuity: Four Dimensions.”
[^2]:Bordwell, “Intensified Continuity: Four Dimensions.”
[^3]:Broberg and Panagiotidis, “Impact of shot length and motion on cinematic 
    tempo.”
[^4]:Adams et al., "Role of shot length in characterizing tempo 
    and dramatic story sections in motion pictures."
