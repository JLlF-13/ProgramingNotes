### `ontouchstart`, `ontouchend`

Touch events allow you to detect and respond to finger gestures on touchscreens. They are essential for building mobile-friendly interfaces.


---

### Main Touch Events

|Event|Description|
|---|---|
|`touchstart`|Fires when the user places a finger on the screen|
|`touchmove`|Fires when the finger moves across the screen|
|`touchend`|Fires when the finger is lifted off the screen|
|`touchcancel`|Fires when the touch is interrupted (e.g., by a system alert)

--- 

### Example: Detect Touch Start

```html
<div id="touchBox" style="width:100px; height:100px; background:orange;"></div>

<script>
  document.getElementById("touchBox").addEventListener("touchstart", function() {
    this.style.backgroundColor = "green";
    console.log("Touch started!");
  });
</script>
```

This changes the color of the box when the user touches it.


--- 

### Example: Tracking Finger Movement

```javascript
document.addEventListener("touchmove", function(event) {
  let touch = event.touches[0];
  console.log("Finger position:", touch.clientX, touch.clientY);
});
```

This logs the finger’s position as it moves across the screen.


---

### Prevent Default Behavior

Touch events can trigger scrolling or zooming. To disable that:

```javascript
element.addEventListener("touchmove", function(event) {
  event.preventDefault(); // Stops scrolling
}, { passive: false });
```

> Use_ `{ passive: false }` _to allow_ `preventDefault()` _to work on touch events._