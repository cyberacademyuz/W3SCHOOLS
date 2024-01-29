# CSS Float

CSSning `float` xususiyati, element qanday suzib chiqishi kerakligini belgilaydi

CSSning `clear` xususiyati clear xususiyati berilgan elementning yonida qaysi elementlar suzib turishi va ular cleared elementning qaysi tomonida turishi mumkinligini belgilaydi.

![](<../../../.gitbook/assets/image (463).png>)                                         ![](<../../../.gitbook/assets/image (487).png>)

### float xususiyati <a href="#float-xususiyati" id="float-xususiyati"></a>

`float` xususiyati kontentni joylashtirish va formatlash uchun ishlatiladi, masalan. rasm konteynerdagi matnning chap tomoniga suzib chiqishi kerak bo'lganida.

`float` xususiyati quyidagi qiymatlardan birini o'z ichiga olishi mumkin:

* `left` - Element o'z konteynerining chap tomonida float bo'lib turadi
* `right` - Element o'z konteynerining o'ng tomonida float bo'lib turadi
* `none` - Element float bo'lmaydi. Standart holat hisoblanadi
* `inherit` - Element ota elementining float qiymatini meros qilib oladi

`float` xususiyatining eng oddiy holati bu rasm atrofini matn bilan to'ldirib uchun ishlatish.

### Misol - float: right; <a href="#misol-float-right" id="misol-float-right"></a>

Quyidagi misolda rasm matnning o'ng tomonida suzib turishi kerakligi aytilmoqda

<figure><img src="../../../.gitbook/assets/image (86).png" alt=""><figcaption></figcaption></figure>

```
img {
float: right;
}
```

### Misol - float: left; <a href="#misol-float-left" id="misol-float-left"></a>

Quyidagi misolda esa rasm matnning chap tomonida suzib turishi kerak

<figure><img src="../../../.gitbook/assets/image (502).png" alt=""><figcaption></figcaption></figure>

```
img {
float: left;
}
```

### Misol - No float <a href="#misol-no-float" id="misol-no-float"></a>

Quyidagi misolda esa rasm qayerga berilgan bo'lsa o'sha yerda turadi

<figure><img src="../../../.gitbook/assets/image (464).png" alt=""><figcaption></figcaption></figure>

```
img {
float: none;
}
```

### Misol - Bir-birining yonida suzishi <a href="#misol-bir-birining-yonida-suzishi" id="misol-bir-birining-yonida-suzishi"></a>

Normal holatda divlar bir birining ustida vertikal holda joylashadi. Biroq agar biz `float: left` dan foydalansak, elementlar chap tomondan bir birining yonida suzib chiqadi.

```
div {
float: left;
padding: 15px;
}
.div1 {
background: red;
}
.div2 {
background: yellow;
}
.div3 {
background: green;
}
```
