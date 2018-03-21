# RAIL Model

RAIL is a user-centric performance model that breaks down the user's experience into key actions.

Aspects of RAIL
* Response
* Animation
* Idle
* Load

### Goals and guidelines
In the context of RAIL, the terms goals and guidelines have specific meanings:

Goals. Key performance metrics related to user experience. Since human perception is relatively constant, these goals are unlikely to change any time soon.
Guidelines. Recommendations that help you achieve goals. These may be specific to current hardware and network connection conditions, and therefore may change over time.
Focus on the user
Make users the focal point of your performance effort.

### metrics
User Perception Of Performance Delays
* 0 to 16ms:	Users are exceptionally good at tracking motion, and they dislike it when animations aren't smooth. They perceive animations as smooth so long as 60 new frames are rendered every second. That's 16ms per frame, including the time it takes for the browser to paint the new frame to the screen, leaving an app about 10ms to produce a frame.
* 0 to 100ms: Respond to user actions within this time window and users feel like the result is immediate. Any longer, and the connection between action and reaction is broken.
* 100 to 300ms:	Users experience a slight perceptible delay.
* 300 to 1000ms:	Within this window, things feel part of a natural and continuous progression of tasks. For most users on the web, loading pages or changing views represents a task.
* 1000ms or more:	Beyond 1000 milliseconds (1 second), users lose focus on the task they are performing.
* 10000ms or more	Beyond 10000 milliseconds (10 seconds), users are frustrated and are likely to abandon tasks. They may or may not come back later


### Tools for measuring RAIL
There are a few tools to help you automate your RAIL measurements. Which one you use depends on what type of information you need, and what type of workflow you prefer:

* Chrome DevTools. The developer tools built into Google Chrome. Provides in-depth analysis on everything that happens while your page loads or runs.
* Lighthouse. Available in Chrome DevTools, as a Chrome Extension, as a Node.js module, and within WebPageTest. You give it a URL, it simulates a mid-range device with a slow 3G connection, runs a series of audits on the page, and then gives you a report on load performance, as well as suggestions on how to improve. Also provides audits to improve accessibility, make the page easier to maintain, qualify as a Progressive Web App, and more.
* WebPageTest. Available at webpagetest.org/easy. You give it a URL, it loads the page on a real Moto G4 device with a slow 3G connection, and then gives you a detailed report on the page's load performance. You can also configure it to include a Lighthouse audit.

Sources:
https://developers.google.com/web/fundamentals/performance/rail
