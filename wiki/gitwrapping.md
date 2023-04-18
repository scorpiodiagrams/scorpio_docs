!!Polyglot
## Gitwrapping

You can host markdown documents and their diagram specs using a method called 'gitwrapping'.  You place your specs at GitHub.  You then use [this link](gitwrapped.html) to view them, wrapped with the Scorpio JavaScript.  

> In some ways this is similar to having GitHub run Jekyll for you to deploy a website.  You can build multiple connected pages with text formatted from markdown and multiple diagrams this way.

< One difference to Jekyll is in when the processing is done.  The formatting and interaction with info cards relies on JavaScript, and is done client side rather than server side.

The gitwrapping feature is one way to get a Scorpio based website.  You save your specs and markdown files at GitHub and the gitwrapping will display them. Updates to the 'website' are immediate on pushing to GitHub. 

For something more durable, use the [snippet](snippet) method and use external JavaScript, e.g. from a CDN, or host the Scorpio JavaScript files as well as your content on your own website.