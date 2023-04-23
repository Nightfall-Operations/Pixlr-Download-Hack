# Pixlr-Download-Hack
Download your image from Pixlr.com without using any daily saves using this easy Bookmarklet.

**HOW TO INSTALL**
1. Copy the code below and make a new bookmarks page with the code as the url.
```javascript
javascript:(function() {  var previewSection = document.getElementById("workspace");  var menu = document.getElementById("download-menu");  if (menu) {    document.body.removeChild(menu);    return;  }  if (previewSection) {    var canvas = previewSection.getElementsByTagName("canvas")[0];    if (canvas) {      var img = canvas.toDataURL("image/png");      menu = document.createElement("div");      menu.id = "download-menu";      menu.style.position = "fixed";      menu.style.top = "5px";      menu.style.left = "50%";      menu.style.transform = "translateX(-50%)";      menu.style.padding = "10px";      menu.style.fontSize = "18px";      menu.style.color = "white";      menu.style.backgroundColor = "red";      menu.style.borderRadius = "5px";      menu.style.zIndex = "9999";      menu.innerHTML = `        <div>Choose image type:</div>        <div>          <button onclick="downloadImage('${img}', 'png')">PNG</button>          <button onclick="downloadImage('${img}', 'jpg')">JPG</button>          <button onclick="downloadImage('${img}', 'webp')">WEBP</button>          <button onclick="downloadImage('${img}', 'svg')">SVG</button>        </div>        <button id="close-menu" style="position: absolute; top: 5px; right: 5px; font-size: 18px; color: white; background-color: transparent; border: none; cursor: pointer;">X</button>`;      document.body.appendChild(menu);      var closeButton = document.getElementById("close-menu");      closeButton.addEventListener("click", function() {        document.body.removeChild(menu);      });    } else {      alert('Failed to fetch image data.');    }  } else {    alert('Failed to fetch image data.');  }})();function downloadImage(img, type) {  var markElements = document.querySelectorAll("li.mark");  markElements[1].click();  markElements[1].click();  setTimeout(function() {    var link = document.createElement("a");    var filename = 'pixlr' + Math.floor(Math.random() * 9999) + '.' + type;    link.setAttribute("download", filename);    link.setAttribute("href", img.replace("image/png", "image/" + type));    link.click();    document.body.removeChild(menu);  }, 200);}
```

2. Go to the page where you edit your pixlr image.

3. Click the bookmarklet to download the image.

> NOTE: At the moment this only works in Pixlr X
