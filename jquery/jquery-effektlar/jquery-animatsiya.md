# jQuery Animatsiya

jQuery bilan siz maxsus animatsiyalar ham qila olasiz.

![](<../../.gitbook/assets/image (287).png>)

### jQuery Animatsiyalari - Animate() metodi <a href="#jquery-animatsiyalari-animate-metodi" id="jquery-animatsiyalari-animate-metodi"></a>

jQueryning `animate()` metodi maxsus animatsiyalar yasash uchun ishlatiladi.

**Sintaksis**

```
$(selector).animate({params},speed,callback);
```

Talab qilinadigan params parametri animatsiya qilinadigan CSS xususiyatlarini belgilaydi.

IIxtiyoriy speed parametri effektning davomiyligini belgilaydi. U quyidagi qiymatlarni qabul qiladi: "slow", "fast", millisekundlar.

Ixtiyoriy callback parametri slide effekti bajarilgandan keyin ishga tushadigan funksiya hisoblanadi.

Quyidagi misol `animate()` metodidan oddiy foydalanishni ko'rsatadi; u `<div>` elementini 250px left xususiyatiga yetguncha o'ngga suradi:

```
$("button").click(function(){
  $("div").animate({left: '250px'});
}); 
```

{% hint style="warning" %}
Standrat tarzda, barcha HTML elementlarining position xususiyati static bo'ladi va ularni surib bo'lmaydi.\
Positionni boshqarish uchun avval elementning CSS position xususiyatini relative, fixed qat'iy yoki absolute qilib belgilashni unutmang!
{% endhint %}

### jQuery animate() - Bir nechta xususiyatlarni birlashtirish

Bir vaqtning o'zida bir nechta xususiyatlarni aminatsiya qilish mumkinligiga e'tibor qiling:

```
$("button").click(function(){
  $("div").animate({
    left: '250px',
    opacity: '0.5',
    height: '150px',
    width: '150px'
  });
});
```

{% hint style="info" %}
BARCHA CSS xususiyatlarini `animate()` metodi bilan manipulyatsiya qilish mumkinmi?\
\
Ha, deyarli! Shu bilan birga, bir muhim narsani yodda tutish kerak: `animate()` metodi bilan foydalanilganda barcha xususiyat nomlari camel caseda bo‘lishi kerak: **padding-left** o‘rniga **paddingLeft,** **margin-right** o‘rniga **marginRight** va hokazo ko'rinishida yozish kerak bo‘ladi.\
\
Bundan tashqari, rangli animatsiya jQuery kutubxonasiga kiritilmagan. Agar rangni animatsiya qilmoqchi bo'lsangiz, jQuery.com saytidan [<mark style="color:green;">Color Animations plagin</mark>](http://plugins.jquery.com/)ini\
yuklab olishingiz kerak .
{% endhint %}

### jQuery animate() - Relative qiymatlardan foydalanish

Bundan tashqari, relative qiymatlarni berish mumkin. Bu qiymat oldiga += yoki -= qo'yish orqali amalga oshiriladi:

```
$("button").click(function(){
  $("div").animate({
    left: '250px',
    height: '+=150px',
    width: '+=150px'
  });
}); 
```

### jQuery animate() - Pre-defined qiymatlardan foydalanish

Xususiyatning animatsiya qiymatini `"show"`, `"hide"` yoki `"toggle"` sifatida belgilashingiz mumkin:

```
$("button").click(function(){
  $("div").animate({
    height: 'toggle'
  });
}); 
```

### jQuery animate() - Navbat funksiyasidan foydalanadi

By default, jQuery animatsiyalar uchun navbat funksiyasi bilan birga keladi.

Bu shuni anglatadiki, agar bir nechta `animate()` chaqiruvlarini ketma ket yozsangiz, jQuery ushbu metod chaqiruvlari bilan "ichki" navbat yaratadi. Keyin u animatsiya chaqiruvlari birma bir ishlaydi.

Shunday qilib, turli xil animatsiyalarni ketma ket bajarishni istasangiz, navbat funksiyasidan foydalanamiz:

{% code title="1-misol" %}
```
$("button").click(function(){
  var div = $("div");
  div.animate({height: '300px', opacity: '0.4'}, "slow");
  div.animate({width: '300px', opacity: '0.8'}, "slow");
  div.animate({height: '100px', opacity: '0.4'}, "slow");
  div.animate({width: '100px', opacity: '0.8'}, "slow");
}); 
```
{% endcode %}

Ushbu misoldagi kod birinchi `<div>` elementni o'ng tomonga suradi va keyin matnning o'lchamini kattalashtiradi:

{% code title="2-misol" %}
```
$("button").click(function(){
  var div = $("div");
  div.animate({left: '100px'}, "slow");
  div.animate({fontSize: '3em'}, "slow");
});
```
{% endcode %}
