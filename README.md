# Performance-in-JavaScript
A Collection of articles and notes on Performance.

## General Principles
#### Make your website lighter (-Duh)
This is a very obvious thing to do since you need to process and show less information and content, consume less bandwidth in the network etc.

This becomes all the more important when you are dealing with users who are using old computers, mobiles, 2G, 3G speeds etc
How to achieve this?
1. Remove unnecessary libraries
 - You don't need jQuery, React, Angular etc for small animation or basic event handling
 - You don't need Bootstrap, just for one widget or style one button. These libraries and frameworks are there for complex websites and web applications. Apps which are going to scale in future and requires a collaborative approach of many people.

2. Use different size images and resources for different devices
3. Compress Images
4. Use SVG for simple shapes and icons.
5. Make a sprite sheet instead of multiple images.
    you can use Stitches An HTML5 sprite sheet generator - https://draeton.github.io/stitches/

#### Use CDNs

#### Hosting service and server speed

#### Don't use redirects

#### Remove the tap delay
Mobile browsers often use a 300-350ms delay between the triggering of the touchend and click events. This delay was added so the browser could determine if there was going to be a double-tap triggered or not, since double-tap is a common gesture used to zoom into text. This delay can have the side effect of making interactions feel laggy, and therefore giving the user the impression that the site is slow, even if it’s their own browser causing the problem.

Fortunately there’s a way to remove the delay. Add following in the <head> of your page, and the delay no longer takes effect:

<meta name="viewport" content="width=device-width">


### Icon systems
problem
lets say your site requires 20 icons, you really don't want to make 20 seperate HTTP calls to fetch them. That would be slow.

Solution
An Icon system does 2 things
1. All icons are in one request
2. makes icons easy to use.

### Reducing image size, without loosing quality.
www.smushit.com/ysmush.it/
imageoptimizer.net
pmt.sourceforge.net/pngcrush/

### Image sprite
flowermind.com/sprite-creator
spriteme.org
spritegen.website-performance.org/

css optimizer for inline styles

### concatenation
zbugs.com

### JSON
Just because we use JSON, doesn't automatically mean its good.
Many times there is repetitive data in calls. Maybe because of how the backend is organized.
So say on a social media site, your profile fetches some data, then a timeline items gets another data but also contains data already present and on and on.

### AJAX vs Web Sockets
For the same stuff generally AJAX is a little bit more heavier.

### Resource loading
1. Preloading.
There are pitfall, you are loading something assuming you will need it in future. If you did, great but What if you don't?

one way is to use the follwoing

<link rel="prefetch" href="something.jpg">
2.  Lazy Loading /on demand/Post loading.

Stuff that is not immediately needed.

```js
function scriptLoaded() {
  // do something here
}

var myScript = document.createElement("script");
myScript.src = "xyz.js";
document.head.appendChild(myScript);

// onload doesn't only mean loading the file, but means loaded, executed and done.
myScript.onload = scriptLoaded;

myScript.onreadystatechange = function () {
  if(myScript.readyState === "loaded" || myScript.readyState === "complete") {
    scriptLoaded();
  }
}

```

Try dynamic loading of stuff, you can tools like lab.js and avoid document.write

document.write is considered a bad practice.(EVIL)
https://stackoverflow.com/questions/802854/why-is-document-write-considered-a-bad-practice

## Tools to analyze performance

1. https://developers.google.com/speed/

2. https://www.keycdn.com/support/pinpoint-website-performance-issues/

3. http://whichloadsfaster.co/
You can check and compare with your competitor imstantly. for example amazon.in vs flipkart

4. https://www.webpagetest.org/
