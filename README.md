# Pixlr Download Hack
Download your image from Pixlr.com without using any daily saves using this easy Bookmarklet.

**HOW TO INSTALL**
1. Copy the code below and make a new bookmarks page with the code as the url.
```javascript
javascript:(function(){if(typeof(Storage)!=="undefined"){if(window.location.href.indexOf("https://pixlr.com")!==-1){localStorage.clear();alert("Local storage cleared for https://pixlr.com");}else{alert("This bookmarklet is intended for https://pixlr.com only.");}}else{alert("Local storage is not supported in your browser.");}})();
```

2. Click the bookmarklet anywhere on the pixlr website
  
3. Reload your page
