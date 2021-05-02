# https://mechd.opensutd.org
## The mechD page guide

Hello there. Firstly, thank you for taking the time to come and update this website, really appreciate your effort:> Don't worry if you haven't touched coding past that python course in freshmore cos page is really (hopefully) pretty easy to maintain. If you feel like revamping the website, just go ahead and let your creative juice run #nohardfeelings

### Installations
Firstly, you gotta somehow get all this code onto your computer right. Download your favourite text editor that supports html/css (I used visual studio code so most of the tips will be related to that). So if you are using visual studios, I recommend that you also download the Live Server (for seeing live updates to the site) and Github Pull Request and Issues (this one should be downloaded by default).

Link your visual studio to your github. You can follow the tutorial here: https://code.visualstudio.com/docs/editor/github, or if you want to use other stuff go ahead too!

Request to be a collaborator for the repo on git or just log in with the MechD github account. Then pull the repo onto your on laptop and tada you're all set to go!

### Crash course on HTML
You'll be dealing with this mostly for the content stuff so you need to know the syntax of it (don't worry its easier than python imho). Since the CSS part is mostly fixed and done (thank you templates), you probably won't need to edit it much so I won't be going into it. But do read up more if you are interested! 

The most important things you'll probably need to use is the basic tags, text tags, lists and formatting. This is a pretty good link if you want a quick reference: https://web.stanford.edu/group/csp/cs21/htmlcheatsheet.pdf. But you should be able to get the hang of it pretty quickly once you start!
##### Basic tags
<> is a start tag and </> is an end tag. You must always have the end tag, think of it as a bracket, you must always close your bracket!
`<head></head>`: anything between these two tags will be considered the title of the webpage and it isn't displayed in the webpage itself but whatever you type between `<title></title>` is the name that you'll see on your tab! In this case, you should see SUTD MechD.
`<body></body>`: Everything in between this two tags can be see in the main webpage
`<p></p>`: Creates a new paragraph
`<br>`: Inserts a line break (this one is special! it doesn't have an end tag)
`<div> </div>`: Used to divide blocks for formatting with css

##### Text tags
`<h1></h1> to <h6></h6>`: Creates text of different sizes. h1 is the biggest and h6 is the smallest. The size is set with CSS and is mostly prefixed for this website (its in the `main.css` file if you are interested).
`<b> </b>`: Creates bold text
`<em> </em>`: Creates italicized text
`<a href="URL">clickable text</a>`: Create link to specific url with text

##### Lists
`<ul> </ul>`: Creates an unordered list (ie bullet points)
`<ol start=?> </ol>`: Creates an ordered list (ie numbered lists)
`<li> </li>`: Encompasses each list item

#### Brief overview
There are four main sections of the website but you probably will only need to touch two. 

**Home**: `index.html`
The home page has the banner picture (which you can update when you have a better one :x this one was made in a pretty big rush so oops), description of what we do and upcoming events. The upcoming events is probably the most important section to edit!

**About**: `About.html`
Brief intro the the club, you probably can update this as the constituition changes or when there is new activities/events/focus for the club.

**Events**: `\Events`
!! This is probably the most of interest and complicated section. It is split into ongoing events and past events. To change the ongoing/past events that appear in the list find the part of the code that looks like this (should be at the start of each page file!):
```
<li><a href="/Events/Past Events/Past_Events.html">Events</a>
```

Add more list items within `<ul>` and `</ul>`: 
```
<a href="#">Ongoing Events</a>
	<ul>
		<li><a href="/Events/Past Events/Fusion360 Modelling.html">Fusion360 Modelling Competition</a></li>
	</ul>
```
Past events would work the same way. **Remember to do this for all the pages if not it won't update properly!** --> Note that you can't just copy and paste into all the files, you have to move the `<li class="current">` tag to the correct place for each page.

You can create new pages for events and then link the pages accordingly. The href link is usually the file path of the page that you want to link to. Templates for new pages can be found in the `/Templates` folder, just copy the one that you want and rename.

**Contact**: `Contact.html`
This page just contains our email and (very outdated) facebook. 