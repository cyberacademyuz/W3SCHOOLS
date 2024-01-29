# CSS !important

### !important nima ? <a href="#important-ozi-nima" id="important-ozi-nima"></a>

`!important` qoidasi CSS dagi xususiyat yoki qiymat uchun ko'proq o'ziga xoslik berish uchun ishlatiladi.

Haqiqatan ham, agar `!important` qoidasidan foydalansangiz, u ushbu elementdagi barcha eski css qoidalarini bekor qiladi!

Keling, bir misolni ko'rib chiqaylik:

```
#myid {
  background-color: blue;
}

.myclass {
  background-color: gray;
}

p {
  background-color: red !important;
}
```

#### Misolni tushuntirish: <a href="#misolni-tushuntirsak" id="misolni-tushuntirsak"></a>

Yuqoridagi misolda. ID selektori va class selektori yuqori o'ziga xoslikka ega bo'lsa ham, uchchala paragrafning orqa fon ranggiz qizil bo'ladi, chunki `!important` qoidasi ikkala holatdagi `background-color` xususiyatini bekor qiladi.

### !important haqida muhim <a href="#important-haqida-muhim" id="important-haqida-muhim"></a>

`!important` qoidasini bekor qilishning yagona yo'li bu deklaratsiyaga bir xil (yoki undan yuqori) o'ziga xoslikdagi boshqa `!important` qoidani manba kodiga kiritishdir - va shu yerdan bir muammo boshlanadi! Bu CSS kodini chalkashtirib yuboradi va debugging qiyin bo'ladi, ayniqsa  css kodlaringiz katta bo'lsa!

Bu yerda oddiy misol yaratdik. CSS kodiga qaraganingizda, qaysi rang eng muhim deb hisoblanishi unchalik aniq emas:

```
#myid {
  background-color: blue !important;
}

.myclass {
  background-color: gray !important;
}

p {
  background-color: red !important;
}
```

**Maslahat**: `!important` qoidasi haqida bilish yaxshi. Sababi buni ba'zi CSS kodlarda uchratishingiz mumkin. Biroq, agar kerak bo'lmasa, undan foydalanmang.

### Bitta yoki ikkita ishlatish bu yaxshi <a href="#balki-bitta-yoki-ikkita-ishlatish-bu-yaxshi" id="balki-bitta-yoki-ikkita-ishlatish-bu-yaxshi"></a>

Agar boshqa yo'l bilan bekor qilib bo'lmaydigan stillni bekor qilishingiz kerak bo'lsa unda `!important` dan foydalansangiz bo'ladi. Bu CMS da ishlayotganingizda as qotishi mumkin.

`!important`dan foydalanishda yana bir holat: Sahifadagi barcha tugmalar uchun maxsus dizayn bermoqchisiz deb hisoblaylik. Bunda tugmalar kulrang background rangli, oq matnli va bir nechta padding va xoshiya bilan bezatilgan:

```
.button {
  background-color: #8c8c8c;
  color: white;
  padding: 5px;
  border: 1px solid black;
}
```

Ba'zan tugma dizayni o'zgarishi mumkin, agar uni yuqori o'ziga xoslikka ega bo'lgan boshqa element ichiga qo'ysak, unda xususiyatlar o'rtasida ziddiyat paydo bo'ladi. Bunga misol keltiramiz:

```
.button {
  background-color: #8c8c8c;
  color: white;
  padding: 5px;
  border: 1px solid black;
}

#myDiv a {
  color: red;
  background-color: yellow;
}
```

Nima bo'lishidan qat'iy nazar, barcha tugmalarni bir xil ko'rinishga "majburlash" uchun tugmaning xususiyatlariga `!important` qoidasini qo'shishimiz mumkin, masalan:

```
.button {
  background-color: #8c8c8c !important;
  color: white !important;
  padding: 5px !important;
  border: 1px solid black !important;
}

#myDiv a {
  color: red;
  background-color: yellow;
}
```
