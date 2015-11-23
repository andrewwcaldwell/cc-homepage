# HTML+CSS: building a homepage
The repository contains finished code from various HTML+CSS crash courses in Charlotte, NC. Note that this is finished code (not necessarily in the state where we finished in class), though we'll try to add comments to explain any important differences.

Links to specific sessions:
- [November 19, 2015 @ Packard Place](https://github.com/TIY-Charlotte-Frontend-Engineering/cc-homepage/tree/2015-11-19)
- [October 26, 2015 @ Packard Place](https://github.com/TIY-Charlotte-Frontend-Engineering/cc-homepage/tree/2015-10-26)
- [All](https://github.com/TIY-Charlotte-Frontend-Engineering/cc-homepage/branches/all)

To learn more about the Iron Yard in Charlotte, check out [our website](http://theironyard.com/locations/charlotte/) or [get in touch with us](mailto:wes@theironyard.com).

### Follow-ups
After attending a session, you may be interested in learning more about particular topics. Here are some links that can help you
find more about topics we covered in class; generally speaking there's a ton of stuff available online for everything related to HTML and CSS so feel free to dig around on your favorite search engine if these links don't do it for you. If there's anything you think would be good to add here, please let us know.

#### HTML tags
Mozilla's got a [great overview](https://developer.mozilla.org/en-US/docs/Web/HTML/Element) of all of the HTML tags and what they
mean. Remember that the purpose of HTML is to define the *structure and content* of your page, not the appearance. Choosing the
"right" tag is a matter of thinking through the structure that the information on your page has, and there will often be more than one
right answer.

HTML5 is the latest version of the HTML standard and is hot off the press from a standards perspective (it was finalized in 2014; it's precursor HTML4 was finalized in 1997). [IBM has a pretty good overview](http://www.ibm.com/developerworks/library/x-html5/) of some of the changes, both in concept and in practice, that HTML5 brings to the table. Many of them are related to semantics and how we describe the structure of information to a machine, though we also get some exciting new capabilities like [`<video>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/video), [`<audio>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/audio), and [`<canvas>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/canvas).

#### Semantic HTML
"Semantic" HTML describes the practice of using more descriptive tags to identify the content of particular parts of a document. `<div>`'s can be used to group any elements, but their great flexibility also means that they don't describe their contents very precisely. Tags like `<header>`, `<footer>`, `<figure>`, and `<nav>` are similar grouping mechanisms but better communicate the purpose of the content. The top answer on [this Stack Overflow post](http://stackoverflow.com/questions/1729447/what-are-the-benefits-of-using-semantic-html) nicely summarizes the value of semantic HTML.

#### CSS box model
This is a subject that requires some practice, but the best overview I've found is from [Mozilla's introduction to the CSS box model](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Box_Model/Introduction_to_the_CSS_box_model). There are also a bunch of different opinions on [this Stack Overflow post](http://stackoverflow.com/questions/2189452/when-to-use-margin-vs-padding-in-css) about when to use padding vs. margin though in some cases it simply won't matter.

[Learnlayout.com](http://learnlayout.com/) is another nice walkthrough of all things layout-related in HTML+CSS and covers box model-related topics.

#### Responsive web design
The best intro to responsive web design may be [the Wikipedia page](https://en.wikipedia.org/wiki/Responsive_web_design).

> Responsive web design (RWD) is an approach to web design aimed at crafting sites to provide an optimal viewing and interaction experience—easy reading and navigation with a minimum of resizing, panning, and scrolling—across a wide range of devices (from desktop computer monitors to mobile phones).

Responsive web design is an *approach* to designing websites, not a new technology; it was born from the need to design content that works well on a variety of different screen dimensions (phones, laptops, desktops, TV's, watches, etc). The canonical book on the subject is [this one](http://abookapart.com/products/responsive-web-design), and [this blog post](http://alistapart.com/article/responsive-web-design) from the author lays the foundation of why and how responsive-like design patterns are important in a multi-device world.

#### Browser support for HTML and CSS
"Viewing a webpage" is a surprisingly complex task with a number of dependencies that are out of the developer's hands. In order to see a web page as it's intended to be seen, the browser that a user is using has to be able to interpret the content of the page; in other words, the HTML and CSS that the developer uses has to be understood by the tool the user is using to view it. If all people used one version of one browser then this would be straightforward to guarantee, however the diversity of the modern browser landscape ensures that larger web sites can expect significant traffic from [at least five major browsers](http://gs.statcounter.com/) (not counting their mobile variants, which may or may not interpret websites the same way as their desktop equivalents). 

To make matters worse, browsers have an issue with "version fragmentation": the fact that many users will not update their browsers when new versions become available, meaning that not everyone who uses Browser X is going to see things the same way as others who use Browser X if the version of the two are different.

This is a difficult problem and it's unlikely to go away any time soon. The good news is that all of the major browsers are pushing harder than ever to support consistent HTML and CSS standards. The bad news is that older versions are likely to be used for years on a non-trivial chunk of your internet audience.

Here are a few best practices that can help ensure that your site works across browsers and browser versions.

1. Be aware of what HTML and CSS features are broadly supported vs niche. Sites like [caniuse.com](http://caniuse.com/) list breakdowns of major CSS, HTML, and Javascript features, which browsers + browser versions they work with, and the estimated percentage of internet users who use a given browser version. 
2. Use [polyfills](https://remysharp.com/2010/10/08/what-is-a-polyfill) or shims to detect and (ideally) provide support for newer features on older browsers. Many polyfills and shims already exist and are fairly easy to add once you know about them; [Modernizr](https://modernizr.com/) is a popular tool for detecting whether a browser supports a particular feature, and [HTML5please](http://html5please.com/) advises developers on whether to check for specific HTML / CSS feature compatibility before using them.
3. View your website in multiple browsers across multiple browser versions if possible. Tools like [Selenium](http://docs.seleniumhq.org/) and services like [Browserstack](https://www.browserstack.com/) exist to help automate this process, but even checking two or three major browsers manually will help catch the most egregious errors.

