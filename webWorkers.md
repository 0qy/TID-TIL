# Workers
They are scripts that run on a thread seperate to the browser's main thread. It can boost React apps because javascirpt async actions still only follows one thread at a time. Whereas with workers there could be a background task that is created via script. 

### Service Worker
`serviceWorker.unregister()` that is automatically there in index.js
It is a proxy between the browser and the network/cache.
It can intercept any network requets from the main document. It decides whether going to cache or going to the network. User would still gets something if there's no network . Great for PWA. 

This is different from Web Workers. 

### Web Workers 
For any background task that needs to be done. 
Dedicated workers vs Shared workers 
Didicated worker is for dedicated page, and when the page closes it terminates. Shared is shared between pages. 
Common use cases include spell checking, code analysing, image processing. 

### Creating a worker 
```
let mathWorker = new Worker('mathWorker.js') 

mathWorker.postMessage({firstNumber:20,secondNUmber:10})

mathWorker.addEventListener("message", (event) => {
  // Do some logic here with event data
})

```

```
//in mathWorker..js
self.addEventListener("message", (event) => {
  postMessage(doMathCalculation(event.data))
})

function doMathCalculation(first, sevond){
  return first + sevond
}

```

Eventlistner listens to the work for when it does its job. 
The post message is a event based communication which sends data between the two files. 
- Even-based communication 
- postMessage, data is cloned not shared between the two 
- Main thread can also terminate the worker with `mathWorker.terminate()` 
