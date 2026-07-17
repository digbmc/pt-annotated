---
title: Paul Thomas Visualized
author: Grace Muller
layout: data-essay
featured_image: supp-72001
tags: 
    - PTA
    - data essay
---

### Table of Contents
{: .no_toc}

- list 
{:toc} 

### Introduction
What is meaning? Well, it's a complicated question. The quest to ascribe meaning to an object or text often requires one to unearth readings and subtext that lie far beneath the surface. “Deformative” methods of interpretation take this unearthing to the extreme, calling for “responsive works of imagination, not reflexive works of analysis."[^1] This effort seeks to pry open a work, to reimagine it in novel and equally valuable ways to highlight new avenues of meaning and interpretation. These deformed works—such as reading a poem backwards—deconstruct the original text to allow us to see what is not immediately accessible upon first viewing.  

The main goal of the present project is to deform the feature film corpus of director Paul Thomas Anderson via the use of image processing technology. I use three main types of data visualizations in this project: summed z-projections, montages, and median hue and saturation graphs. In creating this piece, I’ve been heavily inspired by the deformative, digital surrealist work of <a href="https://drodz11.github.io/colors-of-ozu/">Dave Rodriguez</a> and <a href="https://dhq.digitalhumanities.org/vol/11/1/000276/000276.html">Kevin Ferguson</a>. The latter coined the term “digital surrealism” to describe works that are created “by means of an automatic process which reveals otherwise unconscious information about film texts."[^2] This computer-driven, automatic process that Ferguson refers to involves taking a film, splitting it into thousands of parts using a computer program, then smushing and stitching it back together via image processing software to create a static image that, while unmoving, also serves as a representation of an entire film as the sum of its individual parts. Surely, this is an avenue of deformative criticism; by summing entire films into single images, we’re able to tap into a method of viewing that is inaccessible and unimaginable when simply watching the film.  

Anderson makes use of color and composition as vehicles to communicate themes, foreshadowing, and various other aspects of a film. *Punch-Drunk Love*, for example, uses blue and red to represent the film’s protagonist Barry and Lena, respectively. As Barry makes his way onto the <a href="https://ptannotated.com/items/punc-10209.html">Hawaii-bound airplane,</a> the two airline employees on the jet bridge are dressed in red, representing the fact that Lena is the final destination of Barry’s journey.[^3] Throughout *There Will Be Blood*, Anderson uses high and low camera angles to show the audience who has authority in any given shot. It’s clear that Anderson’s use of color, composition, camera angles, and so on has analyzable intentionality. By utilizing image processing technology, we can illuminate these directorial choices, providing a new foundation to analyze each film.  

This analysis can also be extended to comparisons between directors. The z-projections created for Dave Rodriguez’s <a href="https://drodz11.github.io/colors-of-ozu/">*Colors of Ozu*,<a> for example, are strikingly different from the ones I created for this project. All of those z-projections contain a very clear image of one central figure, with light skin and dark hair; the z-projections I created using Anderson’s work are very different. Beyond that, however, these visualizations exist in a category of deformed work made up of images that, while originating from an external text, have been transformed into a new, individual work. They’re complex, multifaceted tools, providing a basis of analysis while also existing as an entirely new, transformative work.  

### Method

All the images presented in this project were made using a public domain image processing software called ImageJ (specifically a version called <a href="https://imagej.net/software/fiji/downloads">Fiji</a>), which was originally developed by the National Institute of Health, but has since become a rich source of data collection for digital humanities projects.[^4] My z-projections, montages, and graphs are created first by using the “stack” feature of ImageJ. A stack is a series of images that ImageJ places in a single window. To create a stack, I imported a folder that contained a series of stills from each film as an “image sequence.” What the feature does, essentially, is stack each image fed into the program to create a three-dimensional object that can be measured and visualized. In these stacks, the pixels that make up each image become voxels (volumetric pixels) in a 3D space.[^5] These stacks can then be manipulated using different features of ImageJ to produce the desired image (in my case, these are the z-projections, montages, and graphs). 

The z-projection images were made using the “sum slices” setting for z-projections on ImageJ. To understand that process, it’s important to grasp that each pixel in each image in a stack has RGB values. RGB stands for red, green, blue, each of which has a different numerical value that produces the desired color of the pixel. It’s almost as if you’re mixing paint; you need a certain amount of red, green, and blue paint to get the color you want. Instead of mixing paint, however, computers mix light. This is why the RGB values use red, green, and blue specifically; the human eye processes colored light as differing amounts of red, green, and blue. Thus, the “amount” of light is translated into different RGB values for the computer to read and produce. A higher red value adds more red into the image, a higher green value adds more green into the image, and so on. When I ask ImageJ to sum the slices in a stack, ImageJ adds together all of the numerical voxel values to produce the voxel that appears in the summed image. It measures values along the z-axis of the stack, hence the name “z-projection.” In order to actually see the image, ImageJ has to do some processing behind the scenes for us (RGB 255, 255, 255 is just white). The ImageJ user manual doesn’t explain this at all—it only describes the sum-slices setting as creating “the sum of the slices in a stack."[^6] It can be presumed, then, that ImageJ is adjusting and resizing these values so that the ratios between them stay the same while still providing a viewable image.   

The process for making montages and graphs is much simpler in comparison. The montage feature places each image in a stack side-by-side sequence. To make the graphs, I used an open-source add-on for ImageJ called <a href="https://github.com/culturevis/imageplot">ImagePlot</a> which, as its name suggests, is able to measure data for each image in a set (creating numerical values for hue, saturation, etc.) and plot those images according to specified x and y values.  

These stacks are created using folders full of stills from each film. I began my research for this project using the screenshots taken for *Paul Thomas Annotated: In the Margins*, but they weren’t producing the desired results. Our screenshot capture guidelines instruct one to “capture a screenshot any time the focus of the frame shifts and highlights something new (character, background detail, etc.).” For something like a shot-reverse-shot sequence, for example, only a few shots may be captured. This is a qualitative method that doesn’t account for the unique temporality that these digital surrealist works are meant to provide. The smaller dataset led to many of my original z-projections looking nearly identical. This method also doesn’t accurately communicate how long an object is on screen, and doesn't account for every shot; it favors moments in which more events and cuts are happening, creating a dataset that can be skewed towards more eventful sequences of a film. That process works for our larger project, but it was clear that I needed a different dataset and a different approach for my essay to most accurately reflect the films in their totality.  

I ended up utilizing an open-source tool called <a href="https://www.ffmpeg.org">FFmpeg</a> to gather my stills. It has no graphic user interface and instead requires users to interact with the command line, a text-based tool that allows you to issue commands directly to your computer’s operating system. The advantage FFmpeg provides is that while other programs may require it to run for the entire duration of the film, FFmpeg can extract stills in a fraction of that time. The command I used (the same one that was used by Dave Rodriguez, which can be found <a href="https://drodz11.github.io/colors-of-ozu/methods.html">here</a>) was set to create a still of one frame for every two seconds of video, taking around 4,000 shots (or “slices”) for each film. This quantitative method allowed me to create much more robust datasets; the data visualizations created from them more accurately portray the particular temporality that comes with aggregating an entire film, and each had much more striking visuals. 

<a href="https://github.com/digbmc/pta-features-data/tree/main/deformance-gm"><svg class="bi icon-sprite" aria-hidden="true"><use xlink:href="{{ 'assets/lib/icons/github.svg' | relative_url }}"/></svg>View more information about methods</a>

### Z-Projections

All the data visualizations have a distinct temporal quality; these processes compress an entire film into one image. It’s not the entire film, of course, as it is but a still frame. However, it is not a single still either. A still would be a single moment from the film, but that’s not what this image represents. It contains an entire film layered within itself, exposing that film’s visual core. Rodriguez refers to it as “a kind of ‘impression’ or aggregation of the visual experience of the film itself distilled from its duration."[^7] Ferguson notes that “this process magnifies a cinematic experience that is otherwise entirely unnoticeable: the pure, cumulative effect of duration on our eyes and brains without the distraction of narrative or image."[^8] In aggregating an entire film, we draw out its most important and visually distinctive parts, leaving us with a “trace of the filmmaker’s intentions” that is impossible to imagine while only watching the film.[^9] This distinct temporality can be applied not just to the z-projections, but to the montages and graphs as well.  

The first striking thing about this collection of z-projections is just how different they are from one another. As I look at the summed z-projection for *Punch-Drunk Love*, I feel as though I’m viewing multiple scenes playing out at once. I see various figures performing various actions: sitting down for <a href="https://ptannotated.com/items/punc-04422.html">dinner</a>, <a href="https://ptannotated.com/items/punc-00634.html">peeking</a> out from behind a wall, standing, walking, etc. However, looking at the summed z-projection of *The Master*, I feel as though I’m looking at the shape of <a href="https://ptannotated.com/items/mast-20751.html">Lancaster Dodd</a> himself through a fogged-up window. *Hard Eight* looks like an open doorway, with lights of a <a href="https://ptannotated.com/items/hard-04108.html">dressing room mirror</a> over on the right side. This reflects the varied types of shots and compositions that Anderson uses; the longer a figure, shot, object, or color is onscreen, the more it imprints itself on the final image.

There’s a small shape towards the bottom of *Punch-Drunk Love* that ends up being the back of one of the chairs in Barry’s house, for example: 

<div class="row justify-content-center align-items-center">
  <div class="col-md-5 text-center">
    {% include feature/image.html objectid="supp-72001" caption="A summed z-projection of <i>Punch-Drunk Love</i>" %}
  </div>
  <div class="col-md-5 text-center">
    {% include feature/image.html objectid="punc-02940" caption="A screenshot taken from <i>Punch-Drunk Love</i> at 29:40" %}
  </div>
</div>

This is a unique <a href="https://ptannotated.com/items/punc-02940.html">shot</a>; the camera stays stationary as Barry moves around the room while “Georgia” from the phone sex line begs him to send her some money. The camera is in the shadows, as if spying on Barry, reflecting how much Barry doesn’t want anyone to know that he’s called a phone sex line. Because of the stationary camera, that chair stays in the same spot on screen for an extended period of time and thus is visible in the final image.  

Another scene that really shines through in this image is Barry and Lena’s <a href="https://ptannotated.com/items/punc-04609.html">dinner date</a>—you can clearly see their silhouettes on either side of the projection. The presence of the two central figures indicates to us that this film isn’t just about Barry and his individual journey, but the story of a relationship blossoming between two people. The image’s overall color also demonstrates this new relationship. Its purple color is a <a href="https://ptannotated.com/items/punc-04151.html">combination</a> of blue and red, the two colors commonly used to represent Barry and Lena. The z-projection then becomes a metaphor for the film itself: just as red and blue come together via the z-projection to form a purple hue, Barry and Lena come together over the course of the film to form a relationship that brings new meaning to both of their lives.  

{% include feature/juxtapose.html width="75" figure1="punc-04422" figure2="supp-72001" label1="A screenshot taken from Punch-Drunk Love at 42:22" label2="A summed z-projection of Punch-Drunk Love"%}

Conversely, the z-projection for *There Will Be Blood* doesn’t appear to contain any figures, but instead reflects the long, sweeping shots of <a href="https://ptannotated.com/items/twbb-03150.html">Little Boston’s landscape.</a>

<div class="row justify-content-center align-items-center">
  <div class="col-md-5 text-center">
    {% include feature/image.html objectid="supp-72019" caption="A summed z-projection of <i>There Will Be Blood</i>" %}
  </div>
  <div class="col-md-5 text-center">
    {% include feature/image.html objectid="twbb-03736" caption="A screenshot taken from <i>There Will Be Blood</i> at 37:36" %}
  </div>
</div>

The landscape composition of the z-projection places emphasis on the land itself, from which Daniel—like a vampire—will suck up all the oil. It draws our attention to the subject of his exploitation. Daniel tries to suck the life out of everything. He treats the land of Little Boston the same way he treats people, such as the Sundays or, as he claims, H.W. The z-projection, then, has by extension placed emphasis on Daniel’s character and the way he treats others, molding them into objects of his extraction.

If we turn to *The Master*, we can once again see a human figure; the shady outline of a person looks remarkably similar to the shots of Dodd during his final interaction with Freddie towards the end of the film.

<div class="row justify-content-center align-items-center">
  <div class="col-md-5 text-center">
    {% include feature/image.html objectid="mast-20402" caption="A screenshot taken from <i>The Master</i> at 2:04:02" %}
  </div>
  <div class="col-md-5 text-center">
    {% include feature/image.html objectid="supp-72004" caption="A summed z-projection of <i>The Master</i>" %}
  </div>
</div>

This scene is one of extreme emotional tension. By centering Dodd in the frame and <a href="https://ptannotated.com/items/mast-20751.html">zooming</a> in so closely, Anderson achieves an almost suffocating atmosphere, forcing the viewer to focus on his farewell song to Freddie and the visceral relationship that between these two men. 

There is a major difference between some of these z-projections—some of them utilize differing aspect ratios. An aspect ratio is the ratio between an image’s width and height. If an aspect ratio for an image is 2:1, for example, that means the image is twice as wide as it is tall. Out of Anderon’s ten current feature films, six (his first five and *Licorice Pizza*) use a 2.39:1 widescreen aspect ratio, while four use a 1.85:1 aspect ratio.[^10] This widescreen format allows for better image quality, along with a more immersive viewing experience for the audience. For films such as *There Will Be Blood*, the wide aspect ratio lends itself well to <a href="https://ptannotated.com/items/twbb-13902.html">wide desert shots</a>; for more <a href="https://ptannotated.com/items/phan-02446.html">intimate scenes</a>, it allows for a higher level of visual detail. By using different aspect ratios, Anderson achieves different tonal and emotional effects, as displayed by the z-projections.  

These very simple analyses have been facilitated by the use of the z-projection; they highlight some of the most relevant and important images in the film by showing, through their temporal aggregation of the entire film, which objects have been shown and emphasized the most. This places the z-projection not only in a place of analysis, but also of discovery—it is not only an analyzable piece in itself, as you can examine it for shapes, colors, and other aspects relevant to the film, but it can serve as a springboard for further interrogation and analysis of the original film by displaying the importance of certain objects, which may not be apparent while simply viewing it. 

{% include feature/custom-carousel.html title="Summed-Slice Z-Projections" carousel-items="supp-72010, supp-72022, supp-72007, supp-72001, supp-72019, supp-72004, supp-72028, supp-72016, supp-72025, supp-72013" %}


### Median Hue and Median Saturation Graphs 

When it comes to film, hue and saturation play a large part. When I say hue, I’m referring to “the section of light that color comes from."[^11] It’s what people normally think of when they think of color—red, green, and blue all have different hues. However, the “brightness” of a color doesn’t affect its hue; a light blue has the same hue as a dark blue. Saturation, on the other hand, describes the intensity of a color, or how much of the color there is.[^12] A very light pink is less saturated than firetruck red. There is a third variable at play here, value, which refers to the “lightness or darkness of a color”; value is the same thing as brightness. These three variables are crucial to creating any given color.  

{% include feature/image.html objectid="supp-72034" width="50" height="50" caption="A diagram of the Munsell Color System that explains hue, saturation (chroma), and brightness (value)" %}

Color provides ample opportunity for filmmakers to visually communicate tone and meaning in their films. Warm tones (yellows, oranges, reds) may be used to communicate happiness or safety, while cooler tones (blues, purples) may be used to communicate sadness, loneliness, and isolation. These meanings are all subjective and culturally coded, of course; individual films can ascribe their own meanings to any and all colors, and the connotations a certain color carries will vary depending on who is making or viewing a film. Changing the colors in a scene can change that scene’s entire tone and mood, making it a valuable stylistic element for filmmakers to utilize. 

With this in mind, I have created graphs that map median hue on the x-axis and median saturation on the y-axis. When I refer to the median, I am referring to the “middle” value of every hue and saturation value in a still; I obtained this data by using the ‘ImageMeasure’ add-on to ImagePlot, which can be found in the ‘extras’ folder within ImagePlot when downloaded. The higher the hue value, the further the color is on a model like a color wheel (the lower values are towards red, and the higher values towards blue and purple). The higher the saturation value, the more intense the color is. I chose to plot hue because of how important it is to communicating tone, mood, and other elements, while I chose to map saturation in order to determine the intensity of that important color. This is useful when examining films such as *Punch-Drunk Love*, which use desaturated color to convey its story.  

To apply this method, we can look at the graph for *Punch-Drunk Love*.

{% include feature/image.html objectid="supp-72003" width="50" height="50" caption="A graph mapping the median hue and median saturation for each slice of <i>Punch-Drunk Love</i>" %}


Most of the frames taken from the film appear in the bottom right section of the graph, indicating that much of the film uses cool-toned, desaturated lighting. Barry’s <a href="https://ptannotated.com/items/punc-00144.html">office</a> is his safe space, but it is bathed in uncomfortable fluorescent light. It’s lonely, devoid of the vibrancy and color that comes with human connection, reflecting the lonely state that Barry finds himself in at the beginning of the film. The graph displays the heavy focus that *Punch-Drunk Love* places on that loneliness, along with Barry’s journey towards breaking free from it. It illuminates the emphasis the film places on certain hues, and the saturation of those hues, indicating what the filmmaker is trying his hardest to communicate via the film. In the case of *Punch-Drunk Love*, we can see just how much the film centers around Barry’s loneliness and his quest for human connection.  

Similarly to *Punch-Drunk Love*, *Phantom Thread* applies color to its central characters. Reynolds and Cyril, as members of the House of Woodcock, commonly dress in <a href="https://ptannotated.com/items/phan-00642.html">darker colors</a> and <a href="https://ptannotated.com/items/phan-02726.html">cooler tones</a>; cool tones seem to embody the <a href="https://ptannotated.com/items/phan-03849.html">house</a> itself. Alma, on the other hand, frequently dresses in warm shades of <a href="https://ptannotated.com/items/phan-10241.html">red</a> and <a href="https://ptannotated.com/items/phan-01300.html">burgundy</a>, which symbolizes how her presence alone disrupts the House of Woodcock and Reynolds’s way of life. In graphing the median hue and median saturation of the stills gathered from *Phantom Thread*, these points become clear.

{% include feature/image.html objectid="supp-72018" width="75" caption="A graph mapping the median hue and median saturation for each slice of <i>Phantom Thread</i>" %}

According to this graph, the slices from the film can pretty neatly be categorized as either red or blue, highlighting the tension in the dynamics between Alma and the other characters throughout the film.

Conversely to these blues and reds, looking at the graph for *Licorice Pizza*, I was immediately struck by how <a href="https://ptannotated.com/items/lico-15358.html">yellow</a> the film was.

{% include feature/image.html objectid="supp-72027" width="75" caption="A graph mapping the median hue and median saturation for each slice of <i>Licorice Pizza</i>" %}

This yellowish tint that defines the film is a reflection of its depiction of the 70s, but it’s thematically relevant as well; *Licorice Pizza* is a coming-of-age film in which one of the central protagonists, Gary Valentine, is constantly balancing the tension between wanting to be perceived as an adult and wanting to retreat into the warm, carefree fantasies of childhood. It makes sense, then, why the film would bathe itself in a warm, <a href="https://ptannotated.com/items/lico-02514.html">yellow</a> light; through it, Anderson captures the innocence and fun of childhood, which aligns with the loose, episodic structure of the film itself. Just as with the z-projections, these graphs allow us to highlight certain aspects of each film as a means for analysis. 

{% include feature/custom-carousel.html title="Median Hue/Saturation Graphs" carousel-items="supp-72012, supp-72024, supp-72009, supp-72003, supp-72021, supp-72006, supp-72030, supp-72018, supp-72027, supp-72015" %}

### Montages

Like the z-projections and graphs, the montages also aggregate an entire film into a single image, but there is an element of chronology that the other two cannot convey. A montage retains the chronological order of the film, while also presenting that chronology as a static image that can be analyzed in ways unachievable through an orthodox viewing of a film. Seeing the montage as a whole object allows the viewer to examine each frame in the context of the entire film, illuminating their relationships to each other and “glean[ing] a strong chromatic impression from having the visual palette of the film laid out in a single image."[^13] We can view chronological developments of color as a film progresses through its runtime, and gain an overview of the film’s colors as a whole. 

Let’s examine the montage for *Punch-Drunk Love*, for example. 

{% include feature/image.html objectid="supp-72002" width="75" caption="A montage of <i>Punch Drunk Love</i>" %}

Many segments of the film are bathed in a bright, almost uncomfortable fluorescent light that shines in through desaturated whites and grays. In the beginning of the film, Barry is closed off, stagnant, and lonely. The warehouse in which his <a href="https://ptannotated.com/items/punc-00039.html">office</a> is housed is reflective of this; despite being his area of comfort (one might expect a comforting place to be full of soft, warm tones), Barry’s office is drowned in desaturated color. However, there are pops of color throughout. As the film progresses chronologically, those strips of fluorescent light become shorter and fewer until the credits scene bursts onscreen with its beautiful, saturated colors. The credits scene is an example of some of the particularly colorful moments of the film, which occur when Barry actively allows that color to flow into his life. The two dreamlike <a href="https://ptannotated.com/items/punc-01009.html">color sequences</a> of the film, created by artist Jeremy Blake, come after these particular moments; the first occurs directly after Barry brings the <a href="https://ptannotated.com/items/punc-00942.html">harmonium</a> into his office, and the second—the <a href="https://ptannotated.com/items/punc-12737.html">credits</a> sequence—appears after Barry <a href="https://ptannotated.com/items/punc-12620.html">resolves</a> to stay in Lena’s life and follow her wherever she goes. Through these actions, Barry actively chooses to allow love and spontaneity to enter his personal sphere, hence the bursts of color. More saturated colors also appear throughout the film naturally as a result of a changed setting, such as Barry’s spontaneous visit to Hawaii, or his date with Lena, but the element of Barry’s agency and choice is still present. The shift from washed out, fluorescent whites and blues to bursting, saturated colors develops chronologically, signaling Barry’s emergence from his lonely shell that becomes illuminated via examination of the montage.   

{% include feature/image.html objectid="supp-72005" width="75" caption="A montage of <i>The Master</i>" %}

This analysis extends to Anderson's other films as well. *The Master* is a film about contrasts, flashing between extreme moments of light and darkness. “In particular,” writes Philip Bagnall,  “it’s all about people looking for the light, being bathed in glows and beams, only to wind up darkened and despairing before another light source rejuvenates them anew."[^14] Characters are suffocated and pulled in by literal darkness in their moments of mental darkness, while they are drawn to hope made manifest in the light like moths to a cloth-covered flame. For example, after Freddie is accused of poisoning a fellow farm worker and forced to <a href="https://ptannotated.com/items/mast-01854.html">flee</a>, he wanders hopelessly through the darkness of a San Francisco night, only to become captivated by the bright, warm light of a <a href="https://ptannotated.com/items/mast-01950.html">yacht.</a> The Cause and the people he finds there become a new source of hope and purpose for Freddie, illustrated in the lighting of this scene. If we examine the temporal relationship between light and darkness throughout the film, we can see a steady climb from darkness to light that begins during Freddie’s “<a href="https://ptannotated.com/items/mast-03720.html">processing</a>” (illustrated by a dark black strip of stills towards the top of the image) and culminates in Freddie’s <a href="https://ptannotated.com/items/mast-14958.html">motorcycle ride</a> under a bright desert sky (illustrated via the montage in the long, bright strip of stills towards the bottom of the image). The chronological shifts in light and darkness throughout *The Master* are now illuminated to us and are able to support our analysis.  

As these short analyses of both *Punch-Drunk Love* and *The Master* illustrate, we are able to gain insight into that “chromatic impression” of a film that Rodriguez describes via the montage, while its chronological nature helps to show the intentional shifts in color and brightness within these films which would be unavailable during a regular viewing experience. 

{% include feature/custom-carousel.html title="Montages" carousel-items="supp-72011, supp-72023, supp-72008, supp-72002, supp-72020, supp-72005, supp-72029, supp-72017, supp-72026, supp-72014" %}

### Genre

These images are also quite reflective of the genre of their original films. Anderson’s films span across many genres; he’s directed romances, dramas, period pieces, and comedies, to name a few. The visible features of these genres can provide points of comparison for films across his entire oeuvre. I utilize the montages specifically because they provide a visually intuitive, accurate sense of a film’s overall palette, especially when its shots utilize extreme contrast; sometimes, with visualizations like z-projections, that contrast gets lost. It’s also important to note here that genre is extremely subjective. It’s a group of human-made, flexible categories that hinge on how people perceive certain trends in media—and, of course, different people consume and perceive different pieces of media in very different ways. However, despite being a subjective characteristic, genre is still useful when performing film analysis, since it allows us to examine the genre-based context a film is placed in, or conventions it may utilize. If we examine *Licorice Pizza* and *Punch-Drunk Love*, for example, which are classified by many as romantic comedies, we can see this classification reflected in both films’ use of bright, colorful compositions. 

<div class="row justify-content-center align-items-center">
  <div class="col-md-5 text-center">
    {% include feature/image.html objectid="supp-72002" caption="A montage of <i>*Punch-Drunk Love*</i>" %}
  </div>
  <div class="col-md-5 text-center">
    {% include feature/image.html objectid="supp-72026" caption="A montage of <i>*Licorice Pizza*</i>" %}
  </div>
</div>


Romantic comedies commonly use vivid colors to evoke the fuzzy feelings of being in love; joy, love, and happy endings are all common throughout the genre. *Punch-Drunk Love* in particular was inspired by <a href="https://ptannotated.com/items/punc-05951.html">classic musicals</a>, and their influence can be felt in oversaturated colors used throughout the film.[^15] *Punch-Drunk Love*, then, is calling on genre conventions not only from modern rom-coms, but mid-twentieth-century theatre. If we take a look at some of Anderson’s dramas, however, it’s a very different story.

<div class="row justify-content-center align-items-center">
  <div class="col-md-5 text-center">
    {% include feature/image.html objectid="supp-72008" caption="A montage of <i>Magnolia</i>" %}
  </div>
  <div class="col-md-5 text-center">
    {% include feature/image.html objectid="supp-72011" caption="A montage of <i>Hard Eight</i>" %}
  </div>
</div>

*Hard Eight* and *Magnolia* are two of Paul Thomas Anderson’s earlier films; while *Hard Eight* is a neo-noir crime drama, and *Magnolia* is a sprawling collection of interpersonal storylines, they both fall into the dramatic genre. Unlike the rom-coms, these montages are almost entirely dark. As dramas usually deal with serious, emotionally-charged plotlines, this darkness is reflective of a sort of emotional darkness, juxtaposed with the warmth and happiness that rom-coms usually bring to mind. This pattern is also consistent with his other films, with the exception of *One Battle After Another.*  

While I recognize that these films also commonly utilize brightness to demonstrate contrast, they’re also all characterized by frequent stretches of darkness. Predictably, many of the stills from these films are also on the desaturated side. Compared to the rom-coms, they’re far less colorful, reflecting their more serious emotional tone. 

Despite *One Battle After Another's* dramatic features, it’s a very colorful and brightly lit film. This is a reflection of the other genre conventions that *One Battle After Another* employs; beyond being a drama, it also has many qualities of an action film, especially compared to Anderson’s other films (you won’t find a climactic car chase in *Phantom Thread*, that’s for sure). A trend for action movies over the past few decades has been a distinctive color-grading style that primarily utilizes shades of orange and teal.[^16] This orange and teal color palette indicative of the action genre is very visible in the montage for *One Battle After Another*.  

{% include feature/image.html objectid="supp-72014" width="50" caption="A montage of <i>One Battle After Another</i>" %}
{% include feature/image.html objectid="supp-72015" width="75" caption="A median hue/saturation graph of <i>One Battle After Another</i>, which furthur illustrates the use of orange/blue" %}


By analyzing these images in accordance with the genres of their respective films, we can see how the conventions of that genre manifest visually. Generally speaking, the genre of the film correlates with its visual style: the rom-coms are bright and colorful; the dramas include extreme points of darkness and brightness, making use of contrasting, dramatic lighting; and the modern action film uses blues and oranges that are commonly seen in action films today. It's worth noting, however, that Anderson has the tendency to merge genres, bending their conventions as he sees fit. Many of his films contain scenes reminiscent of <a href="https://ptannotated.com/items/punc-12212.html">western standoffs</a>, for instance, and comedic beats are present in every one of his films. Through the use of different genres and genre conventions, Anderson achieves different emotional results, from the tension of a cowboy <a href="https://ptannotated.com/items/twbb-11319.html">confrontation</a> to the tenderness of a <a href="https://ptannotated.com/items/punc-10655.html">kiss</a>. By using this method, especially as Anderson continues to direct new films, we can further investigate the meaning of genre and how it applies to his work. 

### Deformation as Art

These images have provided us both with their own analyses and with a springboard for further interrogation, but we haven’t yet allowed ourselves to stand back and appreciate them as their own artistic bodies. Part of the goal of this project has been to let these images speak for themselves, after all. That goal begs the question: what can we learn from these images when they are removed from the contexts of their films? Can they contain something within themselves more than just an aesthetically pleasing image? Jason Mittel, another scholar exploring digital surrealism, “fully admit[s] that these resulting works are difficult to categorize. Are they acts of scholarship? Do they contain or provoke arguments? Or are they creative works, more akin to experimental films?”[^17]

There’s actually a branch of deformative criticism that explores this, pushing back on deformation performed solely for the sake of analysis. Mark Sample muses on the idea that most deformative work fails to embrace the deformance at the last possible moment, always circling back to the text as a means to provide analysis for the original work. Via the evocation of Humpty Dumpty, Sample writes that, after Humpty’s fall, instead of putting him back together, Sample would rather “let him lie there, a cracked shell oozing yolk. He is broken. And he is beautiful. The smell, the colors, the flow, the texture, the mess. All of it, it is unavailable until we break things…”[^18] Just as with the surrealist work of the twentieth century, we’ve drawn out something new and unexpected. Why, then, should we not take the time to appreciate these images as art objects in their own right? Rather than using our deformative work simply as a means to an analytical end, we should appreciate the beauty of these deformed works as art in their own right. In referring to these images as works of art, however, I believe it’s important to note that credit for this work is not entirely my own. I am not the sole contributor. While I am responsible for using image processing software as a tool to create these images, and they exist as transformative works, they were still created using art that is not my own. If anything, I have facilitated a collaboration between Anderson and the software used for this project.   

Just by using the term “digital surrealism,” Ferguson already places his work in a traditionally artistic context. His digital surrealism reflects the goal of twentieth-century surrealist visual art and literature, which sought to use a new artistic form—“automatic writing,” which involved suppressing conscious artistic control—in order to tap into one’s unconscious mind.[^19] These artists built upon psychologists such as Sigmund Freud and political theorists such as Karl Marx in order to reach into the recesses of the mind limited by social convention to produce unexpected imagery that they would not otherwise not create.[^20] With this context in mind, Ferguson’s “digital surrealism” makes more sense: we’re literally using an automatic process—a computer program—in order to unlock something about the film that is inconceivable while watching normally. It’s as if we are reaching into the “mind” of the film (or perhaps the filmmaker) to procure these images.  

A point can perhaps be made against this piece regarding the use of computational methods to reduce an entire artistic work to a single image. However, it is not my intent to use this methodology to remove any human quality from these films; in fact, it is my human mind that has allowed me to analyze these images using knowledge of where they came from. These analyses would not be possible without having viewed the films, or without having access to them in some capacity. It is not my goal to reduce or replace Anderson’s art with my own work but rather to serve as a companion to it via a new perspective. If someone views these images without having seen his work, it is my hope that they would go on to watch it and draw conclusions for themselves. I chose this methodology not out of a desire for reductionism, but out of a desire to innovate and shed new light on the corpus of a director I deeply admire.      

Ferguson also compares his own z-projections to the “color field” style of Mark Rothko. Rothko’s “multiforms,” colorful paintings of blobbed and layered shapes, were created as an attempt “to purge from his work myth, symbol, landscape, figure, drawing of any kind, in order to paint in patches of hazy, luminous color."[^21] From this effort to break the cycle of dazed, half-alive weeks born out of a love/hate relationship with his vocation as an artist, come warm, intense works that “suggest a man who… is working in a state of infatuation with his media, as if he has just discovered it."[^22] As his style matured into the “color fields” that Ferguson draws on, Rothko’s nonfigurative painting became efforts to overcome loneliness and vitalize the very activity of painting.[^23]  

{% include feature/image.html objectid="supp-72033" caption="An exhibition of Rothko's Seagram Murals, an example of his 'color field' style" %}

As I recall my time working on this project, I relate to these sentiments very deeply. When I found Rodriguez’s project, and later Ferguson’s, it was as if something switched on in my brain. I have since become overwhelmed with an interest in Digital Humanities, and this interest has facilitated the writing of what is one of the longest academic pieces I’ve ever written (and it’s felt like it’s taken almost no effort at all). It’s even facilitated my speaking at an academic conference, something that I thought I would’ve been much more afraid about doing (and that’s ignoring the fact that I decided to sign up only a few hours before). I have approached this project with so much joy and excitement at the feeling that I’m actually doing something to contribute to my field; I have found infatuation with my medium upon discovering it for the first time. I felt as if I were revitalizing my joy for writing just as Rothko was revitalizing his joy for painting. 

In this way, these images serve as testaments and love letters to the joy of creation and discovery. Mittell writes that “deformative criticism is a reminder of the joys of discovery, finding something distinct and refreshing even within the most familiar film, breaking apart our critical preconceptions to point us toward new, strange pathways."[^24] I’ve already had the chance to enjoy Anderson’s films, but this project has given me the opportunity to enjoy them all over again in a fresh medium. I hesitate to ascribe a purpose to these works when viewing them as their own body—I personally don’t think an object needs a purpose to be meaningful, and I don’t want to risk taking away from our appreciation of these works as art on their own— but if they did have a purpose, I believe it would be to bring the viewer this sense joy and discovery. I believe this project has succeeded in doing just that. It’s certainly given me that joy, and I can only hope I have succeeded in conveying it to you, the reader, as well.  

### Conclusion

To continue our conversation with Mittell on deformative criticism, he suggests that to be successful, a piece must allow one to see the original text through completely new eyes. By utilizing ImageJ to create these visualizations, we’ve definitely achieved a new perspective; they’re a completely new way to view the film, aggregated together and able to be seen in a single, unmoving picture. While I feel as though I have accomplished this on a very technical level, whether I’ve truly accomplished something here, I believe, lies with you, my reader. This all means very little in an isolated file on my laptop. Anderson, Ferguson, Rodriguez, and many others shared their own ideas, allowing me to create this work; it is through the sharing of my own ramblings that others can ascribe meaning to them, and the cycle continues.[^25] I can try to give this piece my own meaning as much as I’d like, but that doesn’t change the subjectivity of the very concept. Sample says—and I wholeheartedly agree—digital humanities is about sharing. I hope that, in sharing this, you have been able to find new meaning in these films as I certainly have. The question of meaning is answered by you.  

### Bibliography

- Bagnall, Philip. “Walking in the Light: Illuminating religion in Paul Thomas Anderson’s THE 
MASTER.” *Scannain.* <a href="https://www.scannain.com/featured/opinion-piece/walking-sunshine-light-religion-paul-thomas-andersons-master/">https://www.scannain.com/featured/opinion-piece/walking-sunshine-light-religion-paul-thomas-andersons-master/</a>.

- Breslin, James E. B. *Mark Rothko: A Biography.* Chicago: University of Chicago Press, 1993.

- Cima, Rosie. “Why Every Movie Looks Sort of Orange and Blue.” *Priceonomics*. January 28, 2015. 
<a href="https://priceonomics.com/why-every-movie-looks-sort-of-orange-and-blue/">https://priceonomics.com/why-every-movie-looks-sort-of-orange-and-blue/</a>.

- “Color In Film: Color Basics.” *Cinegrading.*
<a href="https://cinegrading.com/blogs/all/color-in-film-color-basics?srsltid=AfmBOorgnuI4LZElLyS24yxMExXm7MrxYiVrxAkXB9tDwIUqIm2wRLtA">https://cinegrading.com/blogs/all/color-in-film-color-basics?srsltid=AfmBOorgnuI4LZElLyS24yxMExXm7MrxYiVrxAkXB9tDwIUqIm2wRLtA</a>.

- Ferguson, Kyle L. “Digital Surrealism: Visualizing Walt Disney Animation Studios.” *Digital 
Humanities Quarterly* 11, no. 1 (2017). <a href="https://dhq.digitalhumanities.org/vol/11/1/000276/000276.html">https://dhq.digitalhumanities.org/vol/11/1/000276/000276.html</a>.

- Ferreira, Tiago and Wayne Rasband. *ImageJ User Guide: IJ 1.46r*. October 2, 2012. 
<a href="https://imagej.net/ij/docs/guide/user-guide.pdf">https://imagej.net/ij/docs/guide/user-guide.pdf</a>.

- “The Imperfect Cinematography of Paul Thomas Anderson.” *Indepthcine*. December 7, 2025. 
<a href="https://www.indepthcine.com/videos/pta-cinematography">https://www.indepthcine.com/videos/pta-cinematography</a>.

- Kuhn, Annette, and Guy Westwell. *A Dictionary of Film Studies.* 1st edition. Oxford: Oxford University Press, 2012. <a href=" https://doi.org/10.1093/acref/9780199587261.001.0001">https://doi.org/10.1093/acref/9780199587261.001.0001</a>.

- Mittell, Jason. “Deformin' in the Rain: How (and Why) to Break a Classic Film.” *Digital 
Humanities Quarterly* 15, no. 1 (2021). <a href="https://dhq.digitalhumanities.org/vol/15/1/000521/000521.html">https://dhq.digitalhumanities.org/vol/15/1/000521/000521.html.</a>

- “Orange and Blue Movies are Common.” *Under the Moonlight*. March 31, 2018.
<a href="https://underthemoonlight.ca/2018/03/31/orange-and-blue-movies-are-common/">https://underthemoonlight.ca/2018/03/31/orange-and-blue-movies-are-common/</a>.

- *Paul Thomas Annotated: In the Margins*. <a href="https://ptannotated.com">https://ptannotated.com</a>.

- Richie, Donald. *Ozu: His Life and Films*. Berkeley: University of California Press, 1974.

- Rodriguez, Dave. *Colors of Ozu*. 2022. <a href="https://drodz11.github.io/colors-of-ozu/">https://drodz11.github.io/colors-of-ozu/</a>.

- Sample, Mark. “Notes towards a Deformed Humanities.” @samplereality. May 2, 2012. 
<a href="https://samplereality.com/2012/05/02/notes-towards-a-deformed-humanities/">https://samplereality.com/2012/05/02/notes-towards-a-deformed-humanities/</a>.

- Samuels, Lisa and McGann, Jerome. “Deformance and Interpretation.” *New Literary History* 30, no. 1 (Winter 1999): 25-56. <a href="https://raley.english.ucsb.edu/wp-content/.Engl800/Deformance.pdf">https://raley.english.ucsb.edu/wp-content/.Engl800/Deformance.pdf</a>.

- Voorhies, James. “Surrealism.” The Metropolitan Museum of Art. October 1, 2004. 
<a href="https://www.metmuseum.org/essays/surrealism">https://www.metmuseum.org/essays/surrealism</a>.

### Notes

[^1]: Lisa Samuels and Jerome McGann, "Deformance and Interpretation," *New Literary History* 30, no. 1 (Winter 1999), 29.
[^2]: Kyle L. Ferguson, “Digital Surrealism: Visualizing Walt Disney Animation Studios," *Digital Humanities Quarterly* 11, no. 1 (2017). 
[^3]: *Paul Thomas Annotated: In the Margins.*
[^4]: Ferguson, “Digital Surrealism: Visualizing Walt Disney Animation Studios.”
[^5]: Tiago Ferreira and Wayne Rasband, *ImageJ User Guide: IJ 1.46r*, October 12, 2012, 12, https://imagej.net/ij/docs/guide/user-guide.pdf. 
[^6]: Ibid., 90
[^7]: David Rodriguez, *Colors of Ozu*, 2022, https://drodz11.github.io/colors-of-ozu/. 
[^8]: Ferguson, “Digital Surrealism: Visualizing Walt Disney Animation Studios.”
[^9]: Ibid.
[^10]: "The Imperfect Cinematography of Paul Thomas Anderson."
[^11]: "Color in Film: Color Basics."
[^12]: Ibid.
[^13]: Rodriguez, *Colors of Ozu*.
[^14]: Philip Bagnall, “Walking in the Light: Illuminating religion in Paul Thomas Anderson’s THE MASTER," *Scannain*, https://www.scannain.com/featured/opinion-piece/walking-sunshine-light-religion-paul-thomas-andersons-master/.
[^15]: *Paul Thomas Annotated: In the Margins.*
[^16]: Rosie Cima, “Why Every Movie Looks Sort of Orange and Blue,” *Priceonomics*, January 28, 2015, https://priceonomics.com/why-every-movie-looks-sort-of-orange-and-blue/.
[^17]: Jason Mittell, “Deformin' in the Rain: How (and Why) to Break a Classic Film,” *Digital Humanities Quarterly* 15, no. 1 (2021), https://dhq.digitalhumanities.org/vol/15/1/000521/000521.html. 
[^18]: Sample, "Notes Towards a Deformed Humanities," @samplereality. May 2, 2012, https://samplereality.com/2012/05/02/notes-towards-a-deformed-humanities/. 
[^19]: James Voorhies, "Surrealism," The Metropolitan Museum of Art. October 1, 2004, https://www.metmuseum.org/essays/surrealism. 
[^20]: Ibid. 
[^21]: James E. B. Breslin, *Mark Rothko: A Biography* (Chicago: University of Chicago Press, 1993), 232. 
[^22]: Ibid., 235. 
[^23]: Ibid., 237. 
[^24]: Mittell, “Deformin' in the Rain: How (and Why) to Break a Classic Film.”
[^25]: Special thanks to Dave for his help on this project!
