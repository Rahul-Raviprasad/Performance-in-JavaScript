## JQuery Tips
There are few tricks to speed up performance in jQuery.

#### How to avoid the Flash of Unstyled content when the page loads first time?
This is more of a common technique and not particular to JQuery.

In your head element put this script on the top.
```html
<head>
  <script>
    document.documentElement.className = 'js';
  </script>
  <!---Some other stuff-->
</head>

```
Lets say the content bothering us has an id "flash"
A Simple Solution
Certainly we could add a rule to our stylesheet, such as #flash {display: none;}, and our problem would be solved. But it introduces another, people who woul have disabled js will not see this content at all. In some cases it might be ok, but in most cases it is not.

```js
$(document).ready(function() {
  // show the content now
});
```

Sources:
https://www.learningjquery.com/2008/10/1-way-to-avoid-the-flash-of-unstyled-content
