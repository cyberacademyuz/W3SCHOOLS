# Vue Build

{% hint style="success" %}
Vue loyihasi tugagach, u "ishlab chiqish rejimi"dan "qurilish" rejimiga o'tishi kerak.

Qurilish buyrug'i bizning Vue loyihamizni to'g'ridan-to'g'ri brauzerda ishlash uchun optimallashtirilgan .html, .js va .css fayllariga kompilyatsiya qiladi **.**

Biz Vue loyihamizni boshqalar kirishi uchun serverda fayllar yaratish uchun quramiz.
{% endhint %}

### Veb-sahifani "Yaratish" uchun

Hozirgacha ushbu qo'llanmada loyihalarimiz ishlab chiqish rejimida ishladi, ya'ni Vite qurish vositasi ishlab chiqish serverida ishlaydi. Rivojlanish jarayonida o'zgartirishlar kiritib, ularni saqlaganingizda, Vite sahifani darhol yangilaydi. Bu kompyuterdan juda ko'p resurslarni talab qiladi.

Qurilish bosqichi rivojlanish bosqichidan so'ng, sahifa ommaviy foydalanishga tayyor bo'lganda amalga oshiriladi. Keyin loyihamizni Vite-ni ishlab chiqish rejimida ishga tushirmasdan brauzer tushunadigan fayllarga qurishimiz kerak. Qurilish bosqichi server resurslaridan foydalanishni minimallashtirish va ish faoliyatini yaxshilash uchun amalga oshiriladi.

Vue ilovangizni yaratish uchun, agar u ishlayotgan bo‘lsa, “Q” yoki “ctrl”+‘C” tugmalarini bosib ishlab chiqish serverini to‘xtating, so‘ngra quyidagini yozing:

```
npm run build
```

Loyihangiz qurilganda, Vite `dist`loyihangizni umumiy serverda ishga tushirish uchun zarur bo'lgan barcha fayllar, brauzer tushunadigan fayllar va `*.html`biz ishlab chiqish jarayonida foydalanadigan fayllar o'rniga papka yaratadi.`*.css*.js*.vue`

![](https://www.w3schools.com/vue/img\_project\_built.png)

Brauzerda qurilgan loyihangizni ko'rish uchun buyruqdan foydalaning:

```
npm run preview
```

Ushbu buyruq jilddan qurilgan loyihani ko'rsatadigan brauzer oynasini ochishi kerak `dist`.
