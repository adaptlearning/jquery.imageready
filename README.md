# jquery.imageready
A jquery plugin to check if images have loaded. Checks normal ``img`` tags and css ``background-image`` values, waits for images to load and triggers callback. Will timeout and trigger callback after 10000 milliseconds (or the specified amount if allowed). Returns image tags that weren't loaded as a jquery object.

Usage:

```
$("selector").imageready(callback, options);
```

Example: 
```
$("selector").imageready(function($notLoadedImages) {

  if ($notLoadedImages && $notLoadedImages.length > 0) {
    console.log("Some images haven't loaded");
  } else {
    console.log("All images and background images have loaded");
  }
  
}, {
  allowTimeout: true,
  timeoutDuration: 2000
});
```
