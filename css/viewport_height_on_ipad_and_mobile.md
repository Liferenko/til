## 100vh and 100svh

Problem: iPad showed a whiteboard + membar ok, but Excalidraw's footer has been hidden 2-3 px behind a screen's bottom border. 

app.css file said:
```css
.active-session {
    width: 100vw;
    height: 100vh;
}
```

It was obvious that I need to find out why height is 99% accurate. 
It turns out it's been kinda popular issue in FE. 

Solution: The "s" letter.
```css
.active-session {
    width: 100vw;
    height: 100svh;
    /*it's possible to use 100dvh as well. "d" stands for "dynamic" */
}
```

[![More here](https://web.dev/static/blog/viewport-units/image/two-mobile-browser-visual-ca2bb505efaf1_1920.png)](https://web.dev/blog/viewport-units)

Nice explanation: https://www.youtube.com/watch?v=pOuE9sgK9jY

