Emoticons-js
============

A jquery plugin to insert emojis, font smileys, embed videos (youtube/vimeo), media files,pdf and highlight code syntax.

Features
--------

* Converts emoticon text codes into emoticons :smile: , :heart:
* Finds links in text input and turns them into html links.
* Youtube and Vimeo video embedding
* HTML5 player supported media embedding (mp3,mp4,ogg)
* PDF viewing with preview and then the actual pdf in a frame.
* Inline Code Syntax highlighting (uses highlight.js)

Dependencies
------------
* Jquery
* [Highlight.js](https://highlightjs.org/) (Optional if code syntax highlighting is needed)

Getting started
---------------

**bower**
```bower install --save emoticons-js```

**npm**
```npm install --save emoticons-js```

Load css file
```html
<link rel="stylesheet" href="path/to/jquery.emoticons.css"/>
```

Load Scripts
```html
<script src="path/to/jquery.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/highlight.js/8.4/highlight.min.js"></script> <!--==== Optional =====-->
<script src="path/to/jquery.emoticons.js"></script>
```

HTML Structure
--------------
```html
<div id="element">
  <div> Some content here </div>
  <div> Some content here </div>
  ...
  ...
</div>
```

Simple Usage
------------
```html
<script>
$('#element').emoticons({
    ytAuthKey : 'xxxxxxxx'
});
</script>
```
Advanced Usage
--------------

```html
<script>
$('#element').emoticons({
      //Instructs the library whether or not to embed urls
      link              : true,
      //same as the target attribute in html anchor tag . supports all html supported target values.
      linkTarget        : '_blank',
      //Array of extensions to be excluded from converting into links
      linkExclude       : ['jpg','pdf'],
      //set true to show a preview of pdf links
      pdfEmbed          : true,
      //set true to embed images
      imageEmbed        : true,
      //set true to embed audio
      audioEmbed        : false,
      //set true to show a preview of youtube/vimeo videos with details
      videoEmbed        : true,
      //set true to show basic video files like mp4 etc. (supported by html5 player)
      basicVideoEmbed   : true,
      //width of the video frame (in pixels)
      videoWidth        : 640,
      //height of the video frame (in pixels)
      videoHeight       : 390,
      //( Mandatory ) The authorization key obtained from google's developer console for using youtube data api
      ytAuthKey         : 'xxxxxxx',
      //Instructs the library whether or not to highlight code syntax.
      highlightCode     : true,
      //callback before pdf preview
      beforePdfPreview  : function(){},
      //callback after pdf preview
      afterPdfPreview   : function(){},
      // callback on video frame view
      onVideoShow:function(){},
      //callback on video load (youtube/vimeo)
      onVideoLoad:function(){}

});
</script>
```
If you specify either one of **videoWidth** or **videoHeight** , the other option will be automatically set in the aspected ratio.


Contributing
------------

Before sending a pull request remember to follow [jQuery Core Style Guide](http://contribute.jquery.org/style-guide/js/).

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Make your changes on the `src` folder, never on the `dist` folder.
4. Commit your changes: `git commit -m 'Add some feature'`
5. Push to the branch: `git push origin my-new-feature`
6. Submit a pull request :smile:

License
-------

```
The MIT License (MIT)
Copyright (c) 2014 Ritesh Kumar

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

