# jquery.imageready
A jquery plugin to check if images have loaded.

Usage:

```
$("selector").imageready(callback, options);
```

Example: 
```
$("selector").imageready(function($notLoadedImages) {

  if ($notLoadedImages.length > 0) {
    console.log("Some images haven't loaded");
  } else {
    console.log("All images and background images have loaded");
  }
  
}, {
  allowTimeout: true,
  timeoutDuration: 2000
});
```
