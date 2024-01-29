# CSS Navigation bar

### Demo: Navigation Barlar <a href="#demo-navigation-barlar" id="demo-navigation-barlar"></a>

Vertikal                                           Gorizontal

<figure><img src="../../../.gitbook/assets/image (765).png" alt=""><figcaption></figcaption></figure>

### Navigation barlar <a href="#navigation-barlar" id="navigation-barlar"></a>

Har qanday veb-sayt uchun qulay navigatsiyaga ega bo'lish muhim ahamiyatga ega.

CSS yordamida HTML dagi zerikarli menyularni chiroyli navigation barlarixga aylantirsangiz bo’ladi.

### Navbar = Havolalar ro'yhati <a href="#navigation-bar-linklar-listi" id="navigation-bar-linklar-listi"></a>

Navigation barga asos sifatida standard HTML albatta kerak bo’ladi.

Biz o’z misollarimizda standard HTMLning ro'yhatlari asosida navbar yasaymiz.

Navbar asosan havolalar ro’yhati hisoblanadi, shunday ekan biz `<ul>` va `<li>` dan foydalana olamiz

```
<ul>
  <li><a href="default.asp">Home</a></li>
  <li><a href="news.asp">News</a></li>
  <li><a href="contact.asp">Contact</a></li>
  <li><a href="about.asp">About</a></li>
</ul>
```

Keling endi ro'yhatdagi dumaloqlarni, marginlar va paddinglarni olib tashlaymiz

```
ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
}
```

Misolni tushuntirish:

* `list-style-type: none;` ro'yhatdagi dumaloq belgilarni olib tashlaydi. Navbarda bunday belgilar kerak emas.
* `margin: 0;` va `padding: 0;` brauzerning default qiymatlarini olib tashlaydi

Yuqoridagi misoldagi kod vertikal va gorizontal navbarlarda ishlatiladigan standart kod bo'lib, keyingi bo'limlarda bu haqida ko'proq bilib olasiz.
