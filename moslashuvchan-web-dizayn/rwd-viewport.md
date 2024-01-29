# RWD Viewport

### Viewport nima ?

Viewport veb-sahifaning foydalanuvchiga ko'rinadigan qismidir.

Viewport qurilmaga qarab farq qiladi va mobil telefonda kompyuter ekraniga qaraganda kichikroq bo'ladi.

Planshetlar va mobil telefonlar paydo bo'lishidan oldin veb-sahifalar faqat kompyuter ekranlari uchun mo'ljallangan bo'lib, veb-sahifalar uchun statik dizayn va fixed o'lchamga ega bo'lish oddiy hol edi.

Keyin, planshetlar va mobil telefonlar orqali internetdagi saytlarga kirishni boshlaganimizda, fixed o'lchamdagi veb-sahifalar viewportga sig'mas edi. Qurilmalardagi brauzerlar buni to'g'irlash uchun butun veb-sahifani ekranga moslashtirib kichraytirishardi.

Bu mukammal yechim emas !! Lekin tez to'g'irlash yo'li edi.

### Viewportni sozlash

HTML5 veb-dizaynerlarga `<meta>` tegi orqali viewportni nazorat qilish imkonini beradigan usulni taqdim qildi.

Barcha veb-sahifalaringizga quyidagi viewport elementini kiritishingiz kerak:

```
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

Bu brauzerga sahifa o'lchamlari va masshtabini boshqarish bo'yicha ko'rsatmalar beradi.

`width=device-width` qismi sahifaning kengligini qurilmaning ekran kengligiga rioya qilishini belgilaydi (bu qurilmaga qarab o'zgaradi).

Ushbu `initial-scale=1.0` qismi esa sahifa brauzer tomonidan birinchi marta yuklanganda boshlang'ich masshtab darajasini o'rnatadi.

_Bu bir sahifaning viewport berilgan va berilmagan holatdagi ko'rinishiga misol:_

\
&#x20;                              [![](https://www.w3schools.com/css/img\_viewport1.png)](https://www-w3schools-com.translate.goog/css/example\_withoutviewport.htm?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)               ![](https://www.w3schools.com/css/img\_viewport2.png)

&#x20;                                   Viewport meta tegisiz                     Viewport meta tegi bilan

{% hint style="warning" %}
**Maslahat:** Agar ushbu sahifani telefon yoki planshet orqali ko'rayotgan bo'lsangiz, farqni ko'rish uchun yuqoridagi havollarga kirib tekshirishingiz mumkin.
{% endhint %}

## Viewport uchun kontent o'lchami

Foydalanuvchilar desktop va mobil qurilmalarda vebsaytlarni scroll qilish uchun undan gorizontal tarzda emas vertikal tarzda foydalanishadi.

Agar foydalanuvchi butun veb-sahifani ko'zdan kechirish uchun gorizontal tarzda scroll qilishga yoki sahifani kattalashtirishga majbur bo'lsa, bu yomon **user experience**ga sabab bo'ladi.

Ba'zi qo'shimcha qoidalarga rioya qilish kerak:

**1. Katta fixed kenglikdagi elementlardan foydalanmang -** Masalan, agar rasm viewportdan kattaroq width-da ko'rsatilsa, bu viewportni gorizontal tarzda scroll qilishga olib kelishi mumkin. Ushbu kontentni viewport kengligiga moslashtirishni unutmang.

**2. Kontentni yaxshi ko'rsatish uchun viewport kengligiga tayanishiga yo'l qo'ymang** - CSSda  piksell sifatida berilgan ekran o'lchamlari va kenglik, qurilmalarda turlicha bo'lgani sababli kontent to'g'ri ko'rsatilishi uchun viewport kengligiga tayanmasligi kerak.

**3. Katta va kichik ekranlar uchun turli stillar berishda CSSning media querielaridan foydalaning** - Sahifa elementlariga CSSdagi width-larini katta absolute qilib berish elementni kichik qurilmada viewport uchun juda keng boʻlishiga olib keladi. Buning o'rniga `width: 100%;` kabi relative kenglik qiymatlaridan foydalani. Bundan tashqari, katta absalyut positioning qiymatlaridan foydalanishda ehtiyot bo'ling. Bu elementni kichik qurilmalarda viewportdan tashqariga chiqib ketishiga olib kelishi mumkin.
