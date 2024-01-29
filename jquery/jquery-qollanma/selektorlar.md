---
description: jQuery selektorlari kutubxonaning o'ta muhim bo'lgan qismlaridan biri.
---

# Selektorlar

jQuery selektorlari, HTMLdagi element(lar)ni tanlashga va manipulatsiya qilishga imkon beradi.

jQuery selektorlari HTML elementlarining nomiga, id-siga, klasslariga, turiga, attributlariga, attribut qiymatlariga va yana hokazolarga qarab qidiradi (tanlaydi). U mavjud CSS selektorlariga asoslangan va qo'shimcha ravishda u o'ziga xos selektorlarga ega.

jQuerydagi barcha selektorlar dollar belgisi va qavslar bilan boshlanadi: $()

#### Element selectori <a href="#element-selector" id="element-selector"></a>

jQuery element selektori elementning nomiga qarab tanlaydi.

Sahifadagi barcha `<p>` elementlarini quyidagi tarzda tanlashingiz mumkin:

```
$("p") 
```

**Masalan**

Foydalanuvchi tugmani bosganida barcha `<p>` elementlari yashiriladi:

```
$(document).ready(function(){
  $("button").click(function(){
    $("p").hide();
  });
});
```

#### #id selectori <a href="#id-selector" id="id-selector"></a>

jQuery `#id` selektori HTML dagi tegni qidirishda id attributidan foydalanadi.

id attributiga ega element ko'pincha bitta bo'lishi kerak, shunday ekan o'sha yagona elementni topish uchun biz #id selektoridan foydalanamiz.

Elementni topish uchun birinchi hash belgisini yozamiz va HTML elementning id attributidagi qiymatni kiritamiz:

```
$("#test") 
```

**Masalan**

Foydalanuvchi tugmani bosganida `id="test"` attributiga ega barcha elementlar yashiriladi:

```
$(document).ready(function(){
  $("button").click(function(){
    $("#test").hide();
  });
});
```

#### .class selektori <a href="#class-selektori" id="class-selektori"></a>

jQuery `.class` selektori HTML elementini qidirishda class attributidan foydalanadi.

Elementni topish uchun birinchi nuqta belgisini yozamiz va HTML elementning class attributidagi qiymatni kiritamiz:

```
$(".test") 
```

**Masalan**

Foydalanuvchi tugmani bosganida barcha `class="test"` attributiga ega elementlar yashiriladi:

```
$(document).ready(function(){
  $("button").click(function(){
    $(".test").hide();
  });
});
```

#### jQuery selektorlariga ko'plab misollar <a href="#jquery-selektorlariga-koplab-misollar" id="jquery-selektorlariga-koplab-misollar"></a>

| Sintaksis                  | Ta'rif                                                                               |
| -------------------------- | ------------------------------------------------------------------------------------ |
| $("\*")                    | Barcha elementlarni tanlaydi                                                         |
| $(this)                    | Aynan shu HTML elementini tanlaydi                                                   |
| $("p.intro")               | class="intro" bo'lgan barcha elementlarni tanlaydi                                   |
| $("p:first")               | Birinchi `<p>` elementni tanlaydi                                                    |
| $("ul li:first")           | Birinchi `<ul>` elementidagi birinchi `<li>` ni tanlaydi                             |
| $("ul li:first-child")     | Har bir `<ul>` dagi birinchi `<li>` ni tanlaydi                                      |
| $("\[href]")               | href attributiga ega barcha elementlarni tanlaydi                                    |
| $("a\[target='\_blank']")  | Barcha `<a>` elementlarining target attributida "\_blank" qiymati borlarni tanlaydi  |
| $("a\[target!='\_blank']") | Barcha `<a>` elementlarining target attributida "\_blank" qiymati yo'qlarni tanlaydi |
| $(":button")               | Barcha `<button>` elementlarini va `<input>` type="button" elementlarini tanlaydi    |
| $("tr:even")               | Barcha juft `<tr>` elementlarini tanlaydi                                            |
| $("tr:odd")                | Barcha toq `<tr>` elementlarini tanlaydi                                             |

Turli selektorlarning ko'rish uchun bizning <mark style="color:green;">jQuery Selector tester</mark> imizdan foydalaning.

jQuery selektorlari haqida to'liq ma'lumot olish uchun iltimos, bizning <mark style="color:green;">jQuery Selektor qo'llanmasi</mark> sahifamizga o'ting.

### Alohida fayllardagi funksiyalar <a href="#alohida-alohida-fayllardagi-funksiyalar" id="alohida-alohida-fayllardagi-funksiyalar"></a>

Agar web saytingiz ko'plab sahifalarga ega bo'lsa va jQuery funksiyalaringizni saqlashni osonlashtirmoqchi bo'lsangiz, jQuery funksiyalaringizni alohida .js faylida saqlashingiz  mumkin.

Ushbu qo'llanmada jQuery-ni namoyish qilganimizda, funktsiyalar to'g'ridan-to'g'ri `<head>` bo'limiga qo'shiladi. Biroq, ba'zida ularni alohida faylga joylashtirish afzalroq, masalan (.js fayliga murojaat qilish uchun src atributidan foydalaning):

```
<head>
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.6.0/jquery.min.js"></script>
<script src="my_jquery_functions.js"></script>
</head> 
```
