# Performance-in-JavaScript
A Collection of articles and notes on Performance.

## General Principles
#### Make your website lighter (-Duh)
This is a very obvious thing to do since you need to process and show less information and content, consume less bandwith in the network etc.

This becomes all the more important when you are dealing with users who are using old computers, mobiles, 2G, 3G speeds etc
How to achieve this?
1. Remove unnecessary libraries
 - you don't need jQuery, React, Angular etc for small animation or basic event handling
 - you don't need Bootstrap, just for one widget or style one button.

These libraries and frameworks are there for complex websites and web applications. Apps which are going to scale in future and requires a collabrative approach of many people.

2. Use different size images and resources for different devices
3. Compress Images
4. Use SVG for simple shapes and icons.
5. Make a sprite sheet instead of multiple images.