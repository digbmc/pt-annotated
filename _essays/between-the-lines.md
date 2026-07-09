---
title: "Between the Lines: Graphing Paul Thomas Anderson's Network of Collaborators"
author: Clara Smith
layout: data-essay
featured_image: boog-05509
tags:
    - pta
    - network
    - data essay
---

<a href="/pt-annotated/network.html">Test Graph</a>

"*Want to know the common element for the entire group?... I'll tell you the answer.*" 

— Quiz Kid Donnie Smith, *Magnolia* (1999)

[Jump to Graph](#graphing-pta)

Who makes a movie? The simplest answer is: it’s complicated. Most often, films are cited to their director, who serves as the public face of the project and plays a central role in shaping its creative vision. It is no surprise, then, that the Paul Thomas Annotated website prioritizes the director as its focus. He is what binds together this corpus of films, bringing his unique style to each one across over twenty years of filmmaking. It is perhaps best to define Paul Thomas Anderson as the creator of these films, but he is not the sole maker. 

Building on the ideas of the French New Wave, Andrew Sarris introduced the *auteur* theory to American film theory, which posits that the director is the author of a film and has near complete creative control over their work.[^1] Not everyone who directs is an *auteur*, as a true *auteur* needs both talent and a distinctive personal style. Sarris visualizes the criteria as concentric circles, in which the outer ring is technical competence, then distinguishable personality, and the innermost circle is interior meaning. The *auteur* lies at the center of the diagram, having achieved all three levels in their work. Paul Thomas Anderson is widely considered one of the modern *auteurs*, but even without broad acclaim, the mere fact that we have created a site dedicated to the meaning and importance of his films indicates our thoughts on Anderson’s *auteur* status. 

However, *auteur* theory is not without its critics. Georges Sadoul argues instead that “a film is almost always a collective creation and each collaborator, from the least technician to the most famous star, in small part or large, is one of the authors.”[^2] Although this project focuses on Paul Thomas Anderson, his films are not a product of him alone, they take the work of a great number of people. This feature is not intended to deny Anderson as an *auteur*, nor declare him as the sole maker, but to understand how auteurship and collaborative work are not irreconcilable concepts. The graph does not seek to decenter Anderson, in fact, quite the opposite as he is the point through which everything intersects.

Let’s say a director proposes to use red and blue lighting in a scene to represent the romantic relationship between the two main characters. The director comes up with the idea, but it is the gaffer who implements it. It is up to them to use their expertise to choose which lights, what wattage, what shape and size, whether warm tone or cool tone works best. They must consider the set, the placement of the actors, the cameras that are being used. Once all these decisions are made, the director looks at the lighting, approves, and the production moves on. No one can deny that it is the director’s idea, but it is in collaboration with the rest of the crew. To skip from the director’s vision to their approval, is to miss out on the vital labor and the creative work of the crew. This graph seeks to bridge that gap, to draw the line between concept and execution of the films.
  
One way the film industry formally distinguishes different kinds of labor is through above-the-line and below-the-line workers.[^3] The distinction is based on the production budget and how the crew will be paid, although it also generally aligns with the type of work being done. Above-the-line are people in creative development, production, direction, and lead actors, who are typically paid a fixed rate for the project and may get residuals. Below-the-line are day-to-day crew members on hourly wages. Ostensibly, the separation is only about the budget and not relative importance of different figures, however the hierarchical nature of the terms implies a level of superiority. This visualization proposes another way of thinking about those lines. These lines are not separating people, they’re connecting them. 

A network graph was chosen for this visualization due to these connections. Weingart (2011) describes networks most simply as “stuff and relationships,” which is quite broad and could describe just about everything in the world. But, he continues, that does not mean that a network is a worthless endeavor, because “representing information as a network implicitly suggests not only that connections matter, but that they are required to understand whatever’s going on.”[^4] To truly deconstruct films, as we wish to do with Anderson’s filmography, we must pick apart the work that went into them. 

A social network graph of Hollywood is not an original idea. The idea of six degrees of separation is that everyone is at most six connections away from each other and has inspired the game “Six Degrees of Kevin Bacon” which is trying to link any given actor to Kevin Bacon.[^5] (PTA is connected to Kevin Bacon through multiple actors, for example Julianne Moore was in *Magnolia* (1999) and was also in *Crazy, Stupid, Love* (2011) with Kevin Bacon). While the concept of a Hollywood graph has been done many times, often these visualizations are focused on actors, and do not include connections between critical crew members, lacking the full picture of the creation of these films. 

Perhaps it is a coincidence that the graph ended up looking like a flower. But it is difficult not to think of *Magnolia* (1999), Anderson’s sprawling film about the invisible connections between strangers. Like the film itself, the graph highlights the meaning that emerges when we explore the relationships between individuals.

### Graphing PTA

<div class="mb-4">
<div class="embed-responsive ratio ratio-4x3">
<iframe src="https://claraeks.github.io/ptacollab/" width="100%" ></iframe></div></div>

*Note: This feature uses the TMDB API but is not endorsed or certified by TMDB.*

### Using the Graph

A network graph is divided into nodes (points) and edges (lines between points). In the case of this graph, people and films are nodes, and edges connect individuals to the films they have worked on. Nodes are color-coded by which department the crew member is most known for (e.g. acting, directing, etc.). You can click on any node and it will highlight the connections and pull up information about them, such as which films they have worked on and their specific department and role on set. Actors will additionally have their character name. If someone had multiple jobs on set, all positions will be listed. 

If you are searching for a particular collaborator, the search bar can be used to find them. The graph can be filtered through the group selector (Known For Department) in order to only see all the nodes of a particular category. 

#### Departments
- Art: In charge of the visual design of the film, positions include set designers, props, painters, etc.
- Crew: While a term for the overall workers on the film, here being used to categorize any role that does not fit into a specific department, positions include choreographers, drivers, catering, etc.
- Production: Administrative and logistical work, positions include casting, accounting, location coordinators, etc.
- Acting: Any performers, from leads, to extras, to voice actors
- Costume & Make-Up: In charge of the visual design of characters, positions include costume designers, hairstylists, make-up artists, etc.
- Sound: In charge of all auditory aspects of the film, positions include composers, sound mixers, ADR (dubbing), foley artists, etc.
- Camera: In charge of capturing the image of the film, positions include cinematographers, camera operators, grips (equipment technicians), etc.
- Directing: Managing the creative vision of the film, aside from the director, positions also include assistant directors (daily logistics) and script supervisors
- Visual Effects: In charge of the creation and manipulation of any digital imagery, positions include animators, CG artists, compositing artists, etc.
- Lighting: In charge of supplying light for every scene, positions include lighting designers, gaffers, electricians, etc.
- Editing: In charge of the post-production work of assembling shots into a film, aside from editors themselves positions include colorists, archival footage coordinators, etc.
- Writing: In charge of the creation of the screenplay, may also include the creators of the original concept (e.g. a book adaptation)

### Modes of Analysis

Aside from detailed information about collaborators, the structure of the graph can lend itself towards analysis. At initial glance, it is possible to tell the relative size of the film productions based on the number of connected nodes. Films with larger casts and crews appear denser, while the smaller productions occupy less space. 

The layout also highlights changes across Anderson’s career. His first four feature films cluster together on one side of the graph, while his later films are on the other. This division reflects a gradual shift in his creative partnerships. Some collaborators remain constant throughout his career and bridge these two periods. 

Position within the network is also meaningful. Because the graph uses a force-directed layout, collaborators who worked on many films tend to be pulled toward the center. Those who only worked on a single film are towards the outside.

### Methods

The data for this graph was gathered using [The Movie Database (TMDB) API](https://developer.themoviedb.org/docs/getting-started) based on the Credits page. This resource provided JSON files for each of the films that contained the name of every credited cast/crew member along with supplementary information about them. I used [OpenRefine](https://openrefine.org/) and Microsoft Excel in order to clean and transform the data into edges and nodes. I needed to combine any duplicates of individuals such that every person only appeared once but had all of their credited films listed. 

Each node is one row in a spreadsheet, which contains identifying information and additional attributes. For each node there is a unique ID based off of the existing IDs that TMDB uses as the API assigns every individual a number. The film’s IDs were based off of the existing four-letter notation used elsewhere in the PTAnnotated project (e.g. boog for Boogie Nights). Each node also had a label, in this case it was the name of the collaborator. In the case where someone goes by a different name than their given name, such as a stage name, the name that they are publicly known by was used for the sake of clarity. Additional attributes were their Known For department (from the TMDB API, which is based on their most credited role), and their specific departments and roles for each film. Films have attributes for release year and a link to the relevant PTAnnotated film page.

Edges are made by connecting a source and a target, so each collaborator was a source and the films they worked on were their targets. Functionally, this meant a spreadsheet with a column for the sources and a column for the target, if they are in the same row they are connected. A source can be connected to multiple targets. 

Once these spreadsheets were made, they were uploaded as [Gephi](https://gephi.org/) as CSV files. Gephi is an open source software for creating network graphs and was a key tool in this project. Gephi generated a graph based on the uploaded files. I then customized the layout, sizing, labels, etc. 

Once I was satisfied with my graph, I exported it as a graphml file, and then reuploaded it to Gephi Lite. Gephi Lite is the online browser-based version of Gephi, which allowed for even more customization, such as color organizing through specific hexcodes. Gephi Lite also can connect to GitHub as a way to publish public graph files. Since Gephi Lite cannot export interactive graphs, I re-imported my graph back into Gephi. Utilizing the [SigmaExport plugin](https://github.com/oxfordinternetinstitute/gephi-plugins/tree/sigmaexporter-plugin/modules/sigmaExporter), I exported as a [Sigma.js](https://www.sigmajs.org/) template. Sigma.js is a JavaScript library for creating interactive network graphs that can be viewed in a browser.  The plugin and template were created by the [Oxford Internet Institute’s InteractiveVis](https://github.com/oxfordinternetinstitute/InteractiveVis/) project. The export files, containing the data and the template for the site, were uploaded into GitHub.

At this point, I continued to make edits to the data and appearance in order for the graph to best suit my wishes, improving its accuracy and usability before its final publication.

### Limitations

This project faced a great number of hurdles and, as with any visualizations, there are drawbacks. TMDB was an enormous resource in this project, however using a preexisting data set that is community sourced at such a large quantity means that not every individual is able to be checked for accuracy and there may be discrepancies in name/involvement/title/etc. In addition, contributors have been grouped by what department they are “known for,” however this category is based on all of their works and not their specific involvement in PTA films. This has led to a few cases in which someone’s known for department does not align with their role. For example, Robert Downey Sr., who is listed for directing, had a cameo in two films and had no involvement in the direction. If one were to just look at the graph and the color coding this may be misleading, although the details are clarified in the information panel. 

The initial plan was to have an edge for every role a person has fulfilled, however, Gephi cannot support multiple edges between the same two nodes. So, even if someone had multiple jobs on the same film, they will only have one line between them and that film. Additionally, a person can only have one known for department, so they cannot be filtered by all of their roles (e.g. Anderson does not appear when filtered for writing, despite writing all of his films). 

### Supplementary Graph

Alongside the main network graph, I created a second visualization that approaches the same data from a more artistic perspective. Rather than connecting collaborators to the films they worked on, this graph connects every person directly to every other cast and crew member with whom they worked on a production. 

The color-coding of the nodes remains the same, based on the person’s job. But the color-coding of the edges is based on what film they worked together on. As thousands of overlapping relationships intersect, each production emerges through the density of color. This graph is less concerned with practical use than with revealing the immense scale and interconnectedness of filmmaking. Individual relationships are more difficult to distinguish, but they have a collective effect in creating an abstract portrait of creative labor.

<div class="mb-4">
<div class="embed-responsive ratio ratio-4x3">
<iframe src="https://clarasmith.digital.brynmawr.edu/ptacollab/#" width="100%" ></iframe></div></div>

*Note: This feature uses the TMDB API but is not endorsed or certified by TMDB.*

No one person makes a movie. By mapping the hundreds of artists, technicians, performers, and craftspeople who contribute to Anderson’s films, these graphs make visible the network of collaboration. Instead of condensing people in a list of credits, this project envisions an alternative, more interactive mode of attribution. In doing so, it offers another way of reading Anderson’s filmography through the relationships that make auteurship possible. Every connection reminds us that a creative vision only becomes a film through the expertise and work of countless others. To understand who makes a movie, sometimes you have to look between the lines. 

### Links and Downloads

- [GitHub gist of the main graph file](https://gist.github.com/claraeks/098cddacb0de6672ce2f4176e16bbb39), can be opened in [Gephi Lite](https://lite.gephi.org/v1.0.2/)
- [GitHub gist of the supplementary graph file](https://gist.github.com/claraeks/1f0aa905065c91e2d453716306ff1926), can be opened in [Gephi Lite](https://lite.gephi.org/v1.0.2/)


[^1]: Sarris, “Notes on the Auteur Theory in 1962.”
[^2]: Sadoul, Dictionary of Films, vi.
[^3]: Pruner, “Above-the-Line vs. Below-the-Line Crew.”
[^4]: Weingart, “Demystifying Networks, Parts I & II.”
[^5]: Fowler, “The Exact History of ‘Six Degrees of Kevin Bacon.’”

### Bibliography

- Bastian, Mathieu, Sebastien Heymann, and Mathieu Jacomy. “Gephi: An Open Source Software for Exploring and Manipulating Networks.” *Proceedings of the International AAAI Conference on Web and Social Media* 3, no. 1 (2009): 361–62.
- Fowler, Bella. “The Exact History of ‘Six Degrees of Kevin Bacon.’” *The New Zealand Herald*, August 31, 2019. https://www.nzherald.co.nz/entertainment/the-exact-history-of-six-degrees-of-kevin-bacon/NCVVAU73UZ4TNCZAK726ENOBBQ/.
- Huynh, David. *OpenRefine*. Version 3.10.1. Code for Science and Society, released 2026. https://openrefine.org/.
- Jacomy, Alexis, and Guillaume Plique. *Sigma.Js*. Version 1. Released 2014. www.sigmajs.org/.
- Oxford Internet Institute. *InteractiveVis*. Released 2012. https://github.com/oxfordinternetinstitute/InteractiveVis/.
- Pruner, Aaron. “Above-the-Line vs. Below-the-Line Jobs in Film.” *Backstage*, May 10, 2022. https://www.backstage.com/magazine/article/above-the-line-vs-below-the-line-crew-differences-74969/.
- Sadoul, Georges. *Dictionary of Films*. Edited by Peter Morris. Berkeley, University of California Press, 1972. http://archive.org/details/bub_gb_PvsZikRu-hAC.
- Sarris, Andrew. “Notes on the Auteur Theory in 1962.” *Film Culture* (New York), no. No. 27 (Winter 1962): 1–8. https://dn721605.ca.archive.org/0/items/film-culture-1962-no-27/film-culture-1962-no-27.pdf.
- The Movie Database. *The Movie Database API*. Version 3. Released 2026. https://developer.themoviedb.org/docs/getting-started.
- Weingart, Scott B. “Demystifying Networks, Parts I & II.” *Journal of Digital Humanities* 1, no. 1 (2011). https://journalofdigitalhumanities.org/1-1/demystifying-networks-by-scott-weingart/.

