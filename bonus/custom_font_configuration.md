# Custom Font Configuration
By default webpack will not allow the import of custom font types. This allow this feature we will add a new fule to our configuration.

webpack.config.js:

```js
module: {
    rules: [

      //...

      // ADd new rule to allow import of custom fonts.
      {
        test: /\.(woff|woff2|eot|ttf|otf)$/i,
        type: 'asset/resource',
      },
    ],
  },
```

Now that our webpack is setup we can import and create custom font faces.

index.css/.scss:
```css
@font-face {
  font-family: 'Prototype Regular';
  src: url('./fonts/prototype.regular.ttf') format("truetype");
  font-weight: 400;
  font-style: normal;
}

body {
  margin: 0;
  padding: 0;
  background-color: #1f1f1f;
  color: #f1f1f1;
}

h1 {
  font-family: 'Prototype Regular';
}
```
