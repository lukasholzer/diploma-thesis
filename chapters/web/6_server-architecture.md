# The technological Stack

Technology is one of the most important parts when it comes to the point of development and production. It is a combat between using a bullet proof solutions, that might be outdated, and using the fanciest and latest technologies, which are often poorly tested or not production ready. The problem is the speed, technologies are changing and updating. It is like a competition against the time. Every week there is a new major version releasing and things are going even faster now. Maybe when writing these lines a new framework is now in production somewhere out in the world.
But what is the single and only solution? Short hint, there is no only solution. Think about all problems out there, but every problem might need a different solution. So there are no laws and rules how to tackle a specific problem it is more looking for the needs of the customer and combining them with the habits and preferences of the developers. Finally the developer has to work and maintain these technologies. So in the ecosystem of the Altwiener Christkindlmarkt, the focus was on a modular CMS like Contentful and Storyblok. Instead of a static site generator or Wordpress. On the one hand Wordpress would be pretty simple to install and their is a bunch of plugins out their, but on the other hand a CMS like Storyblok which is API driven is plattform independent. The benefit of an API driven CMS is that you can choose your stack on your own. In case of Storyblok, a JSON *(JavaScript Object Notation)* based *Application Programming* Interface is easier to handle in JavaScript as in PHP.


* Frontend
  * HTML5
  * SCSS
  * Gulp for Compiling
  * Vorteile von Typescript und statical Typed Languages
* API Driven CMS
  * Vorteile
  * Unterschied zu static site generators
  * im Beispiel Marktführer Contentful
  * Modularität von Storyblok
* Server
  * Node.JS Backend mit Handlebars Templating
  * Vorteile von Nginx zu Apache
  * Load Balancing
  * Vorteile von HTTPS
  * Thumbor Image service
* Versionierung
  * Git + Git flow im Vorteil

## The Frontend

### What is HTML5

If you talk about HTML5, you talk about a Hyper Text Mark Language short HTML. In general it is like a structuring language for content. In other words you describe the content. You tell the interpreter so that this line of code is a headline of the first section or this area is a sidebar. The interpreter, in many cases a modern web browser can handle these markup and render it. HTML5 is a superseding of HTML4 and all previous versions of HTML. It is kind of the *next generation of HTML*, so it is the scaffolding for a new way of web application and websites. To conclude HTML5 takes advantage of new features which are shifting the way of browser experience. To sum some up HTML5 is cross platform compatible, so all you need is a modern web browser that can interpret these new tags and definitions. Despite the fact it is a new way of a formally documentation for unwritten standards in most browsers. So it was a shift for developers to rely on new features in a way that every browser interpret these features according to a standard. HTML5 brings some new features as well. Semantic elements like `<header>`, `<footer>` or `<article>`. Geolocation, a persistent local storage, offline web applications or even microdata to extend the vocabulary of HTML5 with custom semantics.
> cf. Pilgrim, Mark: HTML5 – Up and Running. (First Edition) – 1005 Gravenstein Highway North, Sebastopol, CA 95472: O’Reilly Media, Inc., 2010, p. 11 – 12.

Turning to the point that you want to use HTML5 features on the web application. The question, can I use HTML5 on my web page is misleading, probably HTML5 is not one big thing, it is a collection of features and some browsers only supporting a variety of features, like certain tags or video elements. Obviously it is possible to detect the support of thoses features. But getting familiar with the detection techniques it is necessary to get familiar with the Document Object Model short DOM.
> cf. Pilgrim, HTML5 – Up and Running, p.29

### What is the DOM

So what is the Document Object Model? It is not the source code you write in an .html file. Therefore the DOM is the result of your source code parsed by the browser, even though it is not the source code if you click in your browser on View Source. As can be expected View Source shows you exact the HTML that makes up the page. If you want to have a look at the DOM you need to inspect the site with the developer tools. There you get a brief overview of all document nodes. You can click on them and expand them. so it is like a box model where every box is wrapped in another box. So if you want to manipulate the DOM during runtime of a page – in case of user interaction – you have to take advantage of JavaScript. You can fetch some DOM-Nodes or Single Nodes with a simple `document.querySelector('container');` This would return the first Node of type container. Now you can store this node in a variable and manipulate it.
> COYIER, CHRIS: What is the DOM? – https://css-tricks.com/dom/, 10.03.2017

In other words JavaScript is a language the browser can understand and interpret. On the contrary there is the DOM – the place where the magic happens. So facing this two arguments you can say JavaScript is a DOM accessing and manipulation language where you can watch events, attached to some DOM nodes. In other words you can give a button a click event that executes a function when the button is pressed.
> COYIER, CHRIS: What is the DOM? – https://css-tricks.com/dom/, 10.03.2017

"The (…) DOM is an application programming interface (API) (…) It defines the logical structure of documents and the way a document is accessed and manipulated."
> W3C: What is the Document Object Model – https://www.w3.org/TR/DOM-Level-2-Core/introduction.html, 10.03.2017

In point of detection techniques for HTML5 features we are accessing the `window`or `navigator` Object and testing if the property for the particular feature is available in this context. For this kind of testing there is an HTML5 detection library called Modernizr. It is open source and under the MIT-licence and detects the support for HTML5 and CSS3 features. It is important that you include this script in the `<head>` Tag of the page. This is important because you need it before the DOM is built up, so that you can check the support of the features. This is possible because page rendering is blocked until the script is loaded and executed.
> cf. Pilgrim, HTML5 – Up and Running, p.30


### Using HTML5 tags and getting rid of the boxing hell


``` html

  <div class="header">
    <h1>My Header</h1>
  </div>

``` 

``` html

  <header>
    <h1>My Header</h1>
  </header>

``` 

### Why using a statical typed Language in the web


## The Sea