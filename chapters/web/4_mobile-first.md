## Mobile First – but why?

When we are talking about the mobile first approach, it is necessary to know why it is so important nowadays to design for the mobile web. It is important to get the latest or future information about digital transformations – the shift, that not even private people trying to conquer the mobile field, even governments or big companies seek to settle this area. They are evaluating the benefits of mobile devices in kind of agility and flexibility. But with this shift, there is a tremendous effort and duty shipped by, that developers have to concern. The targeting devices are flooding the market, and every device has own screen resolutions or operating systems and therefore different browsers. This aspect was crucial for the Altwiener Christkindlmarkt, instead of the fact that a lot of people were visiting the homepage through a mobile device in the city of Vienna. The fact that these people were often foreigns with a cheap data plan was important to improve their browser experience.
> cf. World Bank Group: Digital Dividends – world development report 2016 – 1818 H Street NW, Washington DC 20433, International Bank for Reconstruction and Development / The World Bank, 2016, p. 2 – 37

## Web is not a western invention

> "There are more things in heaven and earth, Horatio, Than are dreamt of in your philosophy."
> Shakespeare, William: Hamlet – The Tragedy of Hamlet. Edited by Edward Dowden: Methuen and Co. 36 Essex Street: Strand London, 1899, p.52

With this words, Hamlet is speaking to his friend Horatio, in the famous tragedy of Shakespeare. But these words have not lost any actuality itself. Moreover, it is as important as a developer, to keep this words in mind. We are having the latest technologies like the new MacBook Pro and the latest iPhone 7+ and are used to the thought that everyone has this unlimited data plan and the fastest and most reliable network. Obviously, that is not the web experience most people are having. That is the reason why it is such important to keep in mind that a website should work for everyone as good as possible and not even for the western countries. According to the world bank report of 2016 1.1 billion people across the world are surfing the web with a high-speed internet. That is pretty less in comparison with the world's population, if you think about the fact, that 3.2 billion people are having access to the web. 
> cf. Lawson, Bruce: World Wide Web, Not Wealthy Western Web – https://www.smashingmagazine.com/2017/03/world-wide-web-not-wealthy-western-web-part-1/, 20.03.2017

The way of thinking that a website does not have to be optimised for countries in the middle east outside is ridiculous. However, if a closer look is taken to the world map from the world bank report where the countries are sized according to the internet population, circumstances are shifting. If someone thinks that a product is only bought by companies or customers of the west, then probably it is the reason, because the site is not optimised for the middle east. The dating app Ignighter was developed by three Jewish guys from the US. They were targeting people from the middle class of New York and the western countries. They struggled a lot with reaching the critical mass, so the founders noticed that they were getting many sing-ups from the middle east, especially from India. Because of this they rebranded the whole app and became India`s biggest dating site. Even though nothing is predictable, new websites should be considered with the middle east.
> cf. Lawson, Bruce: World Wide Web, Not Wealthy Western Web – https://www.smashingmagazine.com/2017/03/world-wide-web-not-wealthy-western-web-part-1/, 20.03.2017


### Progressive web apps

### The problem with images

The problem in responsive design is not always the size of the pictures on the screen, measured in px. Furthermore, it should be considered the file size, measured in kb, that is needed to provide this content. Let us assume that a picture is provided for a desktop with a width of 1440px. The image needs the width of 1400px to be served in an optimal quality. Assume this page is now viewed on a mobile device, with a ratio of 375x667px like an iPhone 6. Of course, it is not necessary to be as much of a genius as Steven Hawking, to recognise that 1.025px are not used of this image. That was the point where the HTML5 picture tag came across and all the polyfills for the `srcset` attribute. In particular, the problem with the `<img>` tag was solved then because it was possible to send multiple sources for multiple devices and we do not have to deliver big Retina images to non-Retina devices. But saving bandwidth is not the only benefit of providing the correct size. Accordingly, an enormous amount of battery is saved during the load of the page – it required a lot of CPU-cycles to render the image in the correct size. Maybe in the western part of the world that does not matter but there are many areas of the world, where battery life is as important as saving costs on bandwidth.
> cf. Lawson, Bruce: World Wide Web, Not Wealthy Western Web – https://www.smashingmagazine.com/2017/03/world-wide-web-not-wealthy-western-web-part-1/, 20.03.2017

### Solving the problem with the images

Previously, before the picture tag came across there was only one method to provide different images – the background-image property with CSS, which could detect the screen size of the device. But concerning the Search Engine Optimisation, background images are outright horrible for performance. So Google is not able to detect them. The second option was to load the right images with JavaScript, but what is with pages, which are blocking JavaScript or during the time the DOM is built up. Nothing is visible. So that was the point where we were facing the HTML5 feature of the picture tag. This tag was able to provide some source tags with different medias like `network-speed` or `min-width`. Furthermore, it was able to provide a fallback for old browser, without the support of the picture tag. 
> cf. Lawson, Bruce: Notes on Adaptive Images – http://www.brucelawson.co.uk/2011/notes-on-adaptive-images-yet-again/, 20.03.2017

| IE   |  Firefox | Safari | Chrome | Opera | iPhone | Android |
| ---- | -------- | ------ | ------ | ----- | ------ | ------- |
| 13+  |  38+     | 9.1+   | 38+    | 25+   | 9.3+   | 53+     |
Can I use: Picture element – http://caniuse.com/#search=picture, 20.02.2017

``` html

<picture alt="Alternative Text">
    <source src="images/high.jpg" media="min-width: 1200px">
    <source src="images/medium.jpg" media="networ-speed: 3g">
    <source src="images/low.jpg">

    <!-- Fallback if not supported -->
    <img src="images/medium.jpg" alt="Alternative Text">
</picture>

```  
