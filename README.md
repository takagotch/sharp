### sharp
---
https://github.com/lovell/sharp

https://sharp.dimens.io/en/stable/

```js
const sharp = require('sharp');

sharp(inputBuffer)
  .resize(320, 240)
  .toFile('output.webp', (err, info) => ... );
  
sharp('input.jpg')
  .rotate()
  .resize(200)
  .toBuffer()
  .then( data => ... )
  .catch( err => ... );

const roundedCorners = Buffer.from(
  '<svg><rect x="0" y="0" width="200" height="200" rx="50" ry="50"></svg>';
);

const roundedCornerResizer = 
  sharp()
    .resize(200, 200)
    .overlayWith(roundedCorners, { cutout: true })
    .png();
    
readableStream
  .pipe(roundedConrnerResizer)
  .pipe(writableStream);
```

```
npm install sharp
yarn add sharp
```

```js
sharp('input.jpg')
  .resize(300, 200)
  .toFile('output.jpg', function(err) {
  });
  
var transformer = sharp()
  .resize(300)
  .on('info', function(info) {
    console.log('image height is ' + info.height);
  });
readablesStream.pipe(transformer).pipe(writableStream);

sharp({
  create: {
    width: 300,
    height: 200,
    channels: 4,
    background: { r: 255, g: 0, b: 0, alpah: 0.5 }
  }
})
























```


