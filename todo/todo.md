1. caches pdf and tiffs[both single tiff with multiple pages & multiple tiff files for a task]. User once visited a page will cache and revisiting to the same page would fetch from javascript cache instead a call to server.
2.  https://github.com/leff/angular-pdf-viewer plugin earlier which doesn't support caching and asynchronous calls. how that can be improved?

//improve bitwise examples and go through these blog again.
http://michalbe.blogspot.in/2013/03/javascript-less-known-parts-bitwise.html
https://chrisrng.svbtle.com/bitwise-operators-in-javascript
https://www.safaribooksonline.com/library/view/supercharged-javascript-graphics/9781449311162/ch01s04.html
http://ncona.com/2016/07/bitwise-operations-in-javascript/


#### good read
 https://css-tricks.com/case-study-boosting-front-end-performance/?ref=webdesignernews.com
 https://blog.totaljs.com/blogs/tutorials/20161111-another-small-optimizations-in-javascript/

##### Tree shaking
http://www.syntaxsuccess.com/viewarticle/tree-shaking-in-javascript


##### explore


https://docs.google.com/presentation/d/1wiiZeRQp8-sXDB9xXBUAGbaQaWJC84M5RNxRyQuTmhk/edit#slide=id.p

https://medium.com/@addyosmani/javascript-start-up-performance-69200f43b201#.mazy92aol


## Single Threaded
Async vs Parallel

JS has asynchronous code but is not multi-threaded.

Intel's river trail.

Example of places where multi threading would help enormously
Map Reduce on an massively large binary array

JS is single threaded so, if CSS wants to repaint or if garbage collection happens just when your js function needs to run, you might experience jerkyness.


## WebWorkers
The thread actually runs completely separately and has its own context. The communication between your thread and the webworker thread can become a bottleneck
