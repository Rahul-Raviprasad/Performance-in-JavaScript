###Positioning the Scripts

#### 1. Always add the scripts at the very end of the body tags.

Browsers generally don't start downloading anything until they encounter <body> tag.
So if script files are kept to the top then, there will be a considerable delay where a blank screen will be present until the page is shown.

Internet Explorer 8, Firefox 3.5, Safari 4, and Chrome 2 all allow parallel downloads of JavaScript files.
Today newer browsers support the ability to download scripts in parallel. The scripts are still executed in order they are declared.

See below the browser comparision:

![Image of browserscope comparison](https://github.com/Rahul-Raviprasad/Performance-in-JavaScript/blob/master/images/browserscope.org%7C%7Cscripts.png)

And their comment on || script script:

![Image of parallel scripts loading](https://github.com/Rahul-Raviprasad/Performance-in-JavaScript/blob/master/images/parallelScriptsComment.png)

```html
<html>
  <head>
  </head>
  </body>
    <!--all the elements defn-->
    ...
    ...
    ...

    <!--Add Scripts here-->
    <script src='abc.js'></script>
  </body>
</html>
```

#### 2. Minify the Scripts

Needless to say the smaller the size of the file, less time it will take to transfer online.
You can use build tools like Grunt or Gulp for this. You can also explore different minifiers.

In my case, I copy all the scripts to a build folder, and then just run uglify on them.

I configured uglify like this in Grunt.

```javascript

uglify: {
  compile: {
    options: {
      banner: '<%= meta.banner %>',
    },
    files: [{
      expand: true,
      cwd: '<%= build_dir %>',
      src: ['*.js'],
      dest: '<%= build_dir %>'
    }]
  }
}
```

#### 3. Combine the Scripts

It will take more time to load 10 scripts, say of size 10kb, than 1 script of 100kb size.

The concatenation can happen offline using a build tool or in real-time using a tool such as the Yahoo! combo handler.

Yahoo! created the combo handler for use in distributing the Yahoo! User Interface (YUI) library files through their Content Delivery Network (CDN). Any website can pull in any number of YUI files by using a combo-handled URL and specifying the files to include. For example, this URL includes two files: http://yui.yahooapis.com/combo?2.7.0/build/yahoo/yahoo-min.js&2.7.0/build/event/event-min.js.
This URL loads the 2.7.0 versions of the yahoo-min.js and event-min.js files. These files exist separately on the server but are combined when this URL is requested. Instead of using two script tags (one to load each file), a single script tag can be used to load both.

I personally prefer using a build tool like Gulp or Grunt to do this.
Again with example of grunt task

```javascript
concat: {
  build_css: {
    src: [
      '<%= vendor_files.css %>',
      'src/**/*.css'
    ],
    dest: '<%= build_dir %>/<%= cssdestinaion %>'
  },
  build_js: {
    options: {
      banner: '<%= meta.banner %>'
    },
    src: [
      '<%= vendor_files.js %>',
      'src/**/*.js'
    ],
    dest: '<%= build_dir %>/<%= jsdestination %>.js'
  }
}
```
