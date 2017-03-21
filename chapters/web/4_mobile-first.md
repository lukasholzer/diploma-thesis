# Mobile First – but why?

> "There are more things in heaven and earth, Horatio, Than are dreamt of in your philosophy."
> Shakespeare, William: Hamet – The Tragedy of Hamlet. Edited by Edward Dowden: Methuen and Co. 36 Essex Street: Strand London, 1899, p.52

Diese Worte spricht Hamlet zu seinem Freund Horatio, doch diese Worte haben nicht an Aktualität verloren – im Gegenteil. Denn der durchschnittliche User, der eine Website aufruft hat kein MacBook Pro der letzten Generation und das neueste iPhone und das schnellste iPad. Die Verantwortung nicht für sich selbst zu designen sondern den durchschnittlichen end-user im Kopf zu behalten ist ein durchgängige Thematik.



> cf. Lawson, Bruce: World Wide Web, Not Wealthy Western Web – https://www.smashingmagazine.com/2017/03/world-wide-web-not-wealthy-western-web-part-1/,  30.02.2017


Die „World Bank“ berichtet, dass mehr als 1.1 Milliarden Menschen auf der Welt zugang zu High Speed internet haben. 3.2 Milliarden Menschen haben Internetzugang mit mäßiger Geschwindigkeit und 5.2 Milliarden Menschen besitzen überhaupt ein Mobile Telefon. 7 Milliarden Menschen leben mit einem mobilen Internet Zugang.

> Enzenhofer, Klaus. (2017) UX reports from the trenches: Topconf Linz. 2017:

> [Smashing Mag Artikel](https://www.smashingmagazine.com/2017/03/world-wide-web-not-wealthy-western-web-part-1/)




> "There are more things in heaven and earth, Horatio, Than are dreamt of in your philosophy."
> Shakespeare, William: Hamlet – The Tragedy of Hamlet. Edited by Edward Dowden: Methuen and Co. 36 Essex Street: Strand London, 1899, p.52


### The problem with images

The problem in responsive design is not always the size of the images on the screen, measured in px. Furthermore, it should be considered the file size, measured in kb, that is needed to provide this content. Let us assume that a picture is provided for a desktop with a width of 1440px. The image needs the width of 1400px to be served in an optimal quality. Assume this page is now viewed on a mobile device, with a ratio of 375x667px like an iPhone 6. Of course, it is not necessary to be as much of a genius as Steven Hawking, to recognise that 1.025px are not used of this image. That was the point where the HTML5 picture tag came across and all the polyfills for the `srcset` attribute. In particular, the problem with the `<img>` tag was solved then because it was possible to send multiple sources for multiple devices and we do not have to deliver big Retina images to non-Retina devices. But saving bandwidth is not the only benefit of delivering the correct size. Accordingly, a huge amount of battery is saved during the load of the page – it required a lot of CPU-cycles to render the image in the correct size. Maybe in the western part of the world that does not matter but there are many parts of the world, where battery life is as important as saving costs on bandwidth. 
> cf. Lawson, Bruce: World Wide Web, Not Wealthy Western Web – https://www.smashingmagazine.com/2017/03/world-wide-web-not-wealthy-western-web-part-1/, 20.03.2017

### Solving the problem with the images

Previously, before the picture tag came across there was only one method to provide different images – the background-image property with CSS, that could detect the screen size of the device. But concerning the Search Engine Optimisation, background images are outright horrible for performance. So google is not able to detect them. The second option was to load the right images with JavaScript, but what is with pages, that are blocking JavaScript or during the time the DOM is built up. Nothing is visible. So that was the point where we were facing the HTML5 feature of the picture tag. This tag was able to provide some source tags with different medias like `network-speed` or `min-width`. Furthermore, it was able to provide a fallback for old browser, without the support of the picture tag. 
> cf. Lawson, Bruce: Notes on Adaptive Images – http://www.brucelawson.co.uk/2011/notes-on-adaptive-images-yet-again/, 20.03.2017

| IE   |  Firefox | Safari | Chrome | Opera | iPhone | Android |
| ---- | -------- | ------ | ------ | ----- | ------ | ------- |
| 13+  |  38+     | 9.1+   | 38+    | 25+   | 9.3+   | 53+     |
Can I use: Picture element – http://caniuse.com/#search=picture/, 20.02.2017

``` html

<picture alt="Alternative Text">
    <source src="images/high.jpg" media="min-width: 1200px">
    <source src="images/medium.jpg" media="networ-speed: 3g">
    <source src="images/low.jpg">

    <!-- Fallback if not supported -->
    <img src="images/medium.jpg" alt="Alternative Text">
</picture>

```  
