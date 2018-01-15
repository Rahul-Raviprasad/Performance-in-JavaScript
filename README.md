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

## Tools to analyze performance

1. https://developers.google.com/speed/

https://www.keycdn.com/support/pinpoint-website-performance-issues/
