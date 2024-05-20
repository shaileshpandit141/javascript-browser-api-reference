# JavaScript Browser API Reference

JavaScript provides various Browser API Reference to interact with the browser environment, the document, and events. Here is a list of key objects and properties along with a brief explanation of each:

## Global Objects and Properties

### 1. window

- The global object representing the browser window or tab.
- Examples: 
  - **window.innerWidth**
  - **window.innerHeight**
  - **window.alert()**
  - **window.location**

### 2. document

- Represents the HTML document loaded in the window.
- Examples: 
  - **document.getElementById()**
  - **document.getElementById()**
  - **document.querySelector()**
  - **document.querySelectorAll()**
  - **document.title**
  - **document.URL**

### 3. navigator

- Provides information about the browser.
- Examples: 
  - **navigator.userAgent**
  - **navigator.language**
  - **navigator.onLine**
  - **navigator.geolocation**

### 4. screen

- Provides information about the user's screen.
- Examples: 
  - **screen.width**
  - **screen.height**
  - **screen.colorDepth** 
  - **screen.orientation**

### 5. location

- Provides information about the current URL.
- Examples: 
  - **location.href**
  - **location.hostname**
  - **location.pathname**
  - **location.searc**

### 6. history

- Allows manipulation of the browser session history.
- Examples: 
  - **history.back()**
  - **history.forward()**
  - **history.go()**
  - **history.length**

### 7. console

- Provides access to the browser's debugging console.
- Examples: 
  - **console.log()**
  - **console.error()**
  - **console.warn()**
  - **console.table()**

## Event Objects

### 1. Event

- The base event object from which all other event objects derive.
- Examples: 
  - **event.type**
  - **event.target**
  - **event.preventDefault()**
  - **event.stopPropagation()**

### 2. MouseEvent

- Represents events that occur due to the user interacting with a pointing device.
- Examples: 
  - **event.clientX**
  - **event.clientY**
  - **event.button**
  - **event.relatedTarget**

### 3. KeyboardEvent

- Represents events that occur due to the user interacting with a keyboard.
- Examples: 
  - **event.key**
  - **event.code**
  - **event.altKey**
  - **event.ctrlKey**

### 4. TouchEvent

- Represents events that occur due to the user interacting with a touch screen.
- Examples: 
  - **event.touches**
  - **event.targetTouches**
  - **event.changedTouches**

### 5. FocusEvent

- Represents events that occur when an element gains or loses focus.
- Examples: 
  - **event.relatedTarget**

### 6. InputEvent

- Represents events that occur when the value of an `<input>`, `<textarea>`, or `<select>` element changes.
- Examples: 
  - **event.inputType**
  - **event.data**

## Network and Storage Objects

### 1. XMLHttpRequest

- Allows for making HTTP requests to retrieve data from a URL without refreshing the page.
- Examples: 
  - **xhr.open()**
  - **xhr.send()**
  - **xhr.responseText**
  - **xhr.status**

### 2. fetch

- A modern interface for making HTTP requests.
- Examples: 
  ```javascript
  fetch(url).then(response => response.json())
  ```

### 3. localStorage

- Allows storage of key-value pairs in a web browser with no expiration time.
- Examples: 
  - **localStorage.setItem()**
  - **localStorage.getItem()**
  - **localStorage.removeItem()**

### 4. sessionStorage

- Allows storage of key-value pairs for the duration of the page session.
- Examples: 
  - **sessionStorage.setItem()**
  - **sessionStorage.getItem()**
  - **sessionStorage.removeItem()**

## Additional Objects

### 1. FormData

- Represents form data that can be sent using **XMLHttpRequest** or **fetch**.
- Examples: 
  - **formData.append()**
  - **formData.delete()**
  - **formData.entries()**

### 2. URL

- Provides utilities for working with URLs.
- Examples: 
  - **new URL()**
  - **url.searchParams**
  - **url.href**
  - **url.pathname**

### 3. Worker

- Represents a background task that can be run without interfering with the user interface.
- Examples: 
  - **new Worker()**
  - **worker.postMessage()**
  - **worker.terminate()**

### 4. WebSocket

- Provides a way to open a persistent connection between the client and server.
- Examples: 
  - **new WebSocket()**
  - **webSocket.send()**
  - **webSocket.onmessage**

## Timers and Intervals

### 1. setTimeout

- Calls a function or executes code after a specified delay.
- Examples: 
  ```javascript
  const timeoutID = setTimeout(() => { console.log('Hello!'); }, 1000);
  ```
  ```javascript
  clearTimeout(timeoutID);
  ```

### 2. setInterval

- Repeatedly calls a function or executes code at specified intervals.
- Examples: 
  ```javascript
  const intervalID = setInterval(() => { console.log('Hello again!'); }, 1000);
  ```
  ```javascript
  clearInterval(intervalID);
  ```

## Animation

### 1. requestAnimationFrame

- Tells the browser to execute a callback function to update an animation before the next repaint.
- Examples: 
  - **requestAnimationFrame(callback);**

## Geolocation

### 1. navigator.geolocation

- Provides access to the device’s geographic location.
- Examples: 
  - **navigator.geolocation.getCurrentPosition(successCallback, errorCallback);**

## Device and Sensors

### 1. DeviceOrientationEvent

- Provides information about the physical orientation of the device.
- Examples: 
  - **window.addEventListener('deviceorientation', handler);**

### 2. DeviceMotionEvent

- Provides information about the acceleration of the device.
- Examples: 
  - **window.addEventListener('devicemotion', handler);**

## Audio and Video

### 1. HTMLMediaElement

- Represents media elements, like `<audio>` and `<video>`.
- Examples: 
  - **video.play()**
  - **video.pause()**
  - **audio.volume**

### 2. MediaDevices

- Provides access to connected media input devices like cameras and microphones.
- Examples: 
  ```javascript 
  navigator.mediaDevices.getUserMedia(constraints).then(stream => { /* use stream */ });
  ```

## Canvas and Graphics

### 1. CanvasRenderingContext2D

- Provides a context for drawing on a `<canvas>` element.
- Examples: 
  - **canvas.getContext('2d')**
  - **ctx.fillRect()**
  - **ctx.drawImage()**

### 2. WebGLRenderingContext

- Provides a context for drawing 3D graphics on a `<canvas>` element using WebGL.
- Examples: 
  - **canvas.getContext('webgl')**
  - **gl.createShader()**
  - **gl.createProgram()**

## Clipboard

### 1. Clipboard

- Provides access to the clipboard for reading and writing text.
- Examples: 
    ```javascript
    navigator.clipboard.writeText('Text to copy');
    ```
    ```javascript
    navigator.clipboard.readText().then(text => { /* use text */ });.
    ```

## Notifications

### 1. Notification

- Provides a way to display system notifications to the user.
- Examples: 
    ```javascript
    new Notification('Hello!');
    ```
    ```javascript
    Notification.requestPermission().then(permission => { /* use permission */ });
    ```

## Drag and Drop

### 1. DataTransfer

- Represents the data being dragged during a drag-and-drop operation.
- Examples: 
    ```javascript
    event.dataTransfer.setData('text/plain', 'Hello, world!');
    ```
    ```javascript
    event.dataTransfer.getData('text/plain');
    ```

## Web Storage and IndexedDB

### 1. IndexedDB

- Provides a low-level API for storing large amounts of structured data.
- Examples: 
  - **indexedDB.open('myDatabase', 1);**

## Service Workers and Web Workers

### 1. ServiceWorker

- Provides a way to intercept and handle network requests, including programmatically managing a cache of responses.
- Examples: 
    ```javascript
    navigator.serviceWorker.register('/service-worker.js');
    ```

## Performance and Timing

### 1. Performance

- Provides access to performance-related information.
- Examples: 
  - **performance.now()**
  - **performance.mark()**
  - **performance.measure()**

## Push and Notifications

### 1. PushManager

- Provides a way to receive messages pushed from a server.
- Examples: 
    ```javascript
    registration.pushManager.subscribe(options);
    ```

## Others

### 1. MutationObserver

- Provides the ability to watch for changes being made to the DOM tree.
- Examples: 
    ```javascript
    new MutationObserver(callback).observe(targetNode, config);
    ```

### 2. IntersectionObserver

- Provides a way to asynchronously observe changes in the intersection of a target element with an ancestor element or the top-level document's viewport.
- Examples: 
    ```javascript
    new IntersectionObserver(callback).observe(targetElement);
    ```

### 3. ResizeObserver

- Provides a way to observe changes to the size of an element's content or border box.
- Examples: 
    ```javascript
    new ResizeObserver(callback).observe(targetElement);
    ```
