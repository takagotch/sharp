### sharp
---
https://github.com/lovell/sharp

https://sharp.dimens.io/en/stable/

#### aquos
https://github.com/takagotch/aquos

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
.png()
.toBuffer()
.then( ... );

console.log(sharp.format);

console.log(sharp.versions);

sharp.queue.on('change', funciton(queueLength){
  console.log('Queue contains ' + queueLength + ' task(s)');
});

const pipeline = sharp().rotate();
pipeline.clone().resize(800, 600).pipe(firstWritableStram);
pipeline.clone().extract({ left: 20, top: 20, width: 100, height: 100}).pipe(secondWritableStream);
readableStream.pipe(pipeline);

const image = sharp(inputJpg);
image
  .metadata()
  .then(function(metadata) {
    .resize(Math.round(metadata.width / 2))
    .webp()
    .toBuffer();
  })
  .then(function(data) {
  });

const image = sharp(inputJpg);
image
  .stats()
  .then(function(stats) {
  });

sharp(input)
  .toFile('output.png', (err, info) => { ... });
  
sharp(input)
  .toFile('output.png')
  .then(info => { ... });
  .catch(err => { ... });

sharp('input.tiff')
  .png()
  .tile({
    size: 512
  })
  .toFile('output.dz', function(err, info) {
  });

sharp(input)
  .resize({ width: 100 })
  .toBuffer()
  .then(data => {
  });

sharp(input)
  .resize({ height: 100 })
  .toBuffer()
  .then(data => {
  });

sharp(input)
  .resize(200, 300, {
    kernel: sharp.kernel.nearest,
    fit: 'contain',
    position: 'right top',
    background: { r: 255, g: 255, b: 255, alpha: 0.5 }
  })
  .toFile('output.png')
  .then(() => {
  });
  
const transformer = sharp()
  .resize({
    width: 200,
    height: 200,
    fit: sharp.fit.cover,
    position: sharp.strategy.entropy
  });
readableStream
  .pipe(transformer)
  .pipe(writableStream);

sharp(input)
  .resize(200, 200, {
    fit: sharp.fit.inside,
    withoutEnlargement: true
  })
  .toFormat('jpeg')
  .toBuffer()
  .then(function(outputBuffer) {
  });

sharp(input)
  .resize(140)
  .extend({
    top: 10,
    bottom: 20,
    left: 10,
    right: 10
    background: { r: 0, g: 0, b: 0, alpha: 0 }
  })

sharp(input)
  .extract({ left: left, top: top, width: width, height: height })
  .toFile(output, function(err) {
  });
})
```


