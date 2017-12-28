[qrCodejs]: https://github.com/vivialex/qrcodejs

# wx_program_QRCode
基于qrcodejs的微信小程序二维码生成库

原本的[qrCodejs]在小程序上运行不了，因此对其进行了修改，并且删去不适用的代码

## wxml
```HTML
<canvas canvas-id="canvas" style="width: 300px; height: 300px"></canvas>
```
## js
```Javascript
var qrcode = new QRCode('canvas', {
    text: 'http://jindo.dev.naver.com/collie',
    width: 300,
    height: 300,
    colorDark : '#000000',
    colorLight : '#ffffff',
    correctLevel : QRCode.correctLevel.H
});

qrcode.clear(); // clear the code.
qrcode.makeCode('http://naver.com'); // make another code.
```
