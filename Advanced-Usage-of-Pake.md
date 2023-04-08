#### 1. How do I rewrite the style, e.g. to remove ads from the original site, or even redesign it?

First, open devtools debug mode with `npm run dev`. After that, find the name of the style you want to change and verify the effect in devtools, and find the location of the style in `inject/pake.css` with `style.innerHTML`. Finally, add the style you need to override, there are some examples you can copy.

#### 2. How to inject js code, e.g. to implement event listeners, e.g. keyboard shortcuts?

Refer to the event listener in `inject/index.js` with `document.addEventListener`, and write it directly, it's more of a basic front-end technique here.

#### 3. How to communicate with Pake about events in containers, such as dragging and dropping, scrolling, special clicks on the Web, etc.?

Refer to the communication code in `index.js` with `invoke`, write the event listener and then use `invoke` to pass the event and its parameters, then refer to the container to receive events `invoke_handler` and handle them yourself.