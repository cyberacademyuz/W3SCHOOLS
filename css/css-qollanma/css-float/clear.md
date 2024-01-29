# Clear

### `clear` xususiyati <a href="#clear-xususiyati" id="clear-xususiyati"></a>

`float` xususiyatidan foydalanganimizda va keyingi elementni pastda turishini (o‘ngda yoki chapda emas) xohlasak, “clear” xususiyatidan foydalanishimiz kerak bo‘ladi.

`clear` xususiyati suzuvchi element yonida joylashgan element bilan nima sodir bo'lishi kerakligini belgilaydi.

`clear` xususiyati quyidagi qiymatlardan birini o'z ichiga oladi:

* `none` - Element chap yoki o'ngdagi suzuvchi elementlarning tagiga surilmaydi. Bu default qiymat
* `left` - Element chapdagi suzuvchi elementlarning tagiga suriladi
* `right` - Element o'ngdagi suzuvchi elementlarning tagiga suriladi
* `both` - Element chap va o'ngdagi suzuvchi elementlarning tagiga suriladi
* `inherit` - Element o'zining ota elementidan `clear` xususiyatini meros qilib oladi

Floatlarni tozalashda clearni floatga moslashingiz kerak bo'ladi: agar element chapga suzib chiqqan bo'lsa, chap tomonni tozalashingiz kerak bo'ladi. Float  berilgan element float holatda turaveradi, lekin clear berilgan element veb-sahifada uning tagiga joylashadi.

{% code title="Ushbu misolda chap tomondagi float tozalangan. Bu degani <div2> element suzilgan <div1> elementning tagiga tushirilgan" %}
```
div1 {
float: left;
}
div2 {
clear: left;
}
```
{% endcode %}

### clearfix hiylasi <a href="#clearfix-hack" id="clearfix-hack"></a>

Agar `float` berilgan (suzuvchi) element uni o'rab turgan elementdan balandroq bo'lsa, u konteynerdan tashqariga "chiqib ketadi". Keyin bu muammoni hal qilish uchun **clearfix**ni qo'shishimiz mumkin:

<figure><img src="../../../.gitbook/assets/image (348).png" alt=""><figcaption></figcaption></figure>

```
.clearfix {
overflow: auto;
}
```

Agar margin va paddinglarni boshqara olsangiz, `overflow: hidden;` **clearfix**-i yaxshi ishlaydi (aks holda scrollbar paydo bo'lganini ko'rishingiz mumkin).  Biroq, yangi va zamonaviy bo'lgan clearfix hiylasidan foydalanish xavfsizroq va ko'p vebsaytlarda quyidagi koddan foydalaniladi:

```
.clearfix::after {
content: "";
clear: both;
display: table;
}
```

{% hint style="warning" %}
`::after` pseudo classi haqida keyingi bo'limlarda o'rganasiz
{% endhint %}
