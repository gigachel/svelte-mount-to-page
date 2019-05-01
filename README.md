# Mount svelte component to html page

main.js
```js
mount('my-component', MyComponent); // mount svelte component (MyComponent) to html element (my-component)
```

index.html
```html
<html>
  <head>
    <title>Html from server</title>
  </head>
  <body>
    <script>
      var x = 10;
      var y = 5;
    </script>
    <my-component answer="{ x * 2 === 20 }"></my-component>
    <my-component answer="42"></my-component>  
    <my-component answer="42 + {x}"></my-component>
    <my-component answer="{ x + y }"></my-component>
    <my-component answer="{x} + {y}"></my-component>
    <my-component answer="{ [{a:1}, {b:2}] }"></my-component>
    <my-component answer="object: { JSON.stringify([{a:1}, {b:2}]) }"></my-component>

    <script src="main.js"></script>
  </body>
</html>
```
