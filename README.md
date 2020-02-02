# A Guide to Using Web Components
I've put this guide together to help those new to web components learn more and to hopefully make it easier to assess whether web components are
a good fit for the problem they are trying to solve.

## Useful Resources
It's not like the resources available for React development but there is plenty of good documentation and videos out there on web
components. As always, start with the basics:
* I would start with this awesome video of Erin Zimmer talking about Web Components at the 2019 International Javascript Conference https://www.youtube.com/watch?v=zZ1YMJydqR0
* https://css-tricks.com/an-introduction-to-web-components/ This is an excellent 5 part introduction that covers the basics of working
with web components
* Some excellent documentation from the peeps at Google including best practices and browser issues to be aware of https://developers.google.com/web/fundamentals/web-components
* https://javascript.info/custom-elements This is quite a good walk through of the lifecycle of Custom Elements.

## SEO Considerations
Now that the Googlebot uses an evergreen version of Chromium it has built in support to deal with all the technologies used as part
of Web Components including Custom Elements and the Shadow DOM. The Googlebot flattens the shadow dom and light dom and is able see
the elements inside the Shadow DOM. For more details see https://developers.google.com/search/docs/guides/javascript-seo-basics.

## Web Analytics Considerations
How to handle click tracking of elements in shadow DOM? TBD.

## Using Web Components with Javascript Frameworks or Libraries
In general, web components will work with any existing front end framework or library. Have a look at this [quick reference](https://custom-elements-everywhere.com/) 
to see how they compare. React makes it a little more difficult than the others because it requires you to use a ref to call the functions of a 
web component and there are complications around event handling. Dan Abramov has said these issues will be addressed in a future release
of React but in the mean time read [here](https://reactjs.org/docs/web-components.html) for suggested approaches.

## Styling Options
https://blog.webf.zone/on-styling-web-components-b74b8c70c492 and https://javascript.info/shadow-dom-style are pretty good guides on what
you're available options are.

### Theming Web Components with Custom CSS Properties
If you only have colour changes from one theme to another then using Custom CSS Properties is a good option. You define your colours using
Custom CSS Properties on the parent page and these are then accessible from within your Custom Element and within the shadow DOM. See this


### Using SASS with Web Components
A lot of the guides out there for styling web components use inline CSS. But that's like going into the future to drive a flying car thats
powered by coal. No thanks! Thankfully its not that hard to set yourself up with using SASS with both Custom Elements in general and the
shadow DOM. This is an excellent guide on how to do it https://blog.webf.zone/on-styling-web-components-b74b8c70c492.

## Publishing Web Components
https://justinfagnani.com/2019/11/01/how-to-publish-web-components-to-npm/