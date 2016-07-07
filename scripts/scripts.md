Positioning the Scripts

1. Always add the scripts at the very end of the body tags.

Browsers generally don't start downloading anything until they encounter <body> tag.
So if script files are kept to the top then, there will be a considerable delay where a blank screen will be present until the page is shown.

Internet Explorer 8, Firefox 3.5, Safari 4, and Chrome 2 all allow parallel downloads of JavaScript files.
Today newer browsers support the ability to download scripts in parallel. The scripts are still executed in order they are declared.

See below the browser comparision:

![Image of browserscope comparison](https://github.com/Rahul-Raviprasad/Performance-in-JavaScript/images/browserscope.org || scripts.png)

And their comment on || script script:

![Image of parallel scripts loading](https://github.com/Rahul-Raviprasad/Performance-in-JavaScript/images/parallel scripts comment.png)
