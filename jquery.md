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

What this allows us to do is
