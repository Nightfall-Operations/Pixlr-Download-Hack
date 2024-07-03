# Pixlr-Download-Hack
Download your image from Pixlr.com without using any daily saves using this easy Bookmarklet.

**HOW TO INSTALL**
1. Copy the code below and make a new bookmarks page with the code as the url.
```javascript
javascript:(function(){if(typeof(Storage)!=="undefined"){if(window.location.href.indexOf("https://pixlr.com")!==-1){localStorage.clear();alert("Local storage cleared for https://pixlr.com");}else{alert("This bookmarklet is intended for https://pixlr.com only.");}}else{alert("Local storage is not supported in your browser.");}})();
```

2. Go to the page where you edit your pixlr image.

3. Click the bookmarklet to download the image.

> NOTE: At the moment this only works in Pixlr X
