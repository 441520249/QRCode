# QRCode

## 安装
在项目文件夹中执行：
```
npm install --save qrcode
```
或者，全局安装以qrcode从命令行使用以保存qrcode图像或生成可在终端中查看的图像。
```
npm install -g qrcode
```

## demo
```html
<img class="code" :src="qrImg" alt="">
```
```js
import QRCode from 'qrcode'
watch: {
  'findByPageDetail.qrcodes' () {
    QRCode.toDataURL(this.findByPageDetail.qrcodes, {
      margin: 0
    }).then(res => {
      this.qrImg = res
    })
  }
}
```
```css
.QRcode{
  padding: 50px;
  display: flex;
  justify-content: center;
  align-items: center;
  background: #fff;
  border-radius: 0 0 20px 20px;
  .code{
    display: inline-block;
    width: 220px;
    height: 220px;
  }
  .codeword{
    margin-top: 20px;
    text-align: center;
  }
}
```
