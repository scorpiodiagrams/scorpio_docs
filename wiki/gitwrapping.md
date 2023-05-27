!!Polyglot
## Gitwrapping

If you want to make documents with Scorpio diagrams and Scorpio's markdown, and share them on the web, you can copy the Scorpio software and add your own documents and diagrams.

There is another way. It's called 'GitWrapping'. You use GitHub to store the documents and diagrams, and Scorpio to present the pages 'GitWrapped'.

You place your specs at GitHub.  You then use [this link](gitwrapped.html#scorpio_dev;dev_docs?git=scorpiodiagrams) to view them, wrapped with the Scorpio JavaScript. Change 'scorpiodiagrams' in the url to your github user or organisation name and change 'scorpio_dev;dev_docs' to the repo and document you want to serve first.
----
Since GitHub supports markdown, you see at least an approximation to the eventual documents through the GitHub user interface.

> In some ways this is similar to having GitHub run Jekyll for you to deploy a website.  You can build multiple connected pages with text formatted from markdown and multiple diagrams this way.

< One difference to Jekyll is in when the processing is done.  The formatting and interaction with info cards relies on JavaScript, and is done client side rather than server side.

The gitwrapping feature is one way to get a Scorpio based website.  Updates to the 'website' are immediate on pushing to GitHub. 

If you just want diagrams, another approach is to use the [snippet](snippet) method and use external JavaScript, e.g. from a CDN.