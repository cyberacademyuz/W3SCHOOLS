# Debugging

{% hint style="warning" %}
Har safar yangi kompyuter kodini yozganingizda xatoliklar yuz berishi mumkin.
{% endhint %}

### Kodni debugging qilish

Kod sintaksis yoki mantiqiy xatolarni o'z ichiga olishi mumkin.

Bunday xatolarning ko'pchiligini ko'z bilan payqash qiyin.

Kodda xato bo'lsa ko'pincha, hech narsa bo'lmaydi. Ya'ni hech qanday xato xabarlari yo'q va siz xatolarni qayerdan qidirish kerakligi haqida hech qanday ko'rsatma olmaysiz.

Koddagi xatolarni qidirish (va tuzatish) debugging deb ataladi.

### JavaScript debuggerlari

Xatolarni tuzatish oson emas. Yaxshiyamki, barcha zamonaviy brauzerlarda maxsus JavaScript debuggeri bor.

Debuggerni yoqish va o'chirib qo'yish mumkin, bu esa xatolarni foydalanuvchiga majburan ko'rsatishga olib keladi.

Debugger yordamida siz to'xtash nuqtalarini (kod bajarilishi to'xtatilishi mumkin bo'lgan joylar) o'rnatishingiz va kod bajarilayotganda o'zgaruvchilarni tekshirishingiz mumkin.

Odatda, F12 tugmasini bosish orqali brauzeringizda debuggingni faollashtirasiz va  undan "Console" ni tanlang.

### console.log() metodi

Agar brauzeringiz debuggingni qo'llab-quvvatlasa, debugger oynasida JavaScript qiymatlarini ko'rsatish uchun `console.log()` dan foydalanishingiz mumkin:

```
<!DOCTYPE html>
<html>
<body>

<h1>My First Web Page</h1>

<script>
a = 5;
b = 6;
c = a + b;
console.log(c);
</script>

</body>
</html>
```

{% hint style="warning" %}
`console.log` metodi haqida to'liq ma'lumotnomani ko'rish uchun bizning Javascript console qo'llanmasi sahifamizga o'ting:
{% endhint %}

### Breakpointlarni o'rnatish

Debuger oynasida kodda to'xtash nuqtalarini o'rnatishingiz mumkin.

Har bir to'xtash nuqtasida JavaScript ishlashni to'xtatadi va sizga JavaScript qiymatlarini tekshirish imkonini beradi.

Qiymatlarni tekshirgandan so'ng, siz kodning bajarilishini davom ettirishingiz mumkin.

### debugger kalit so'zi

`debugger` kalit so'zi JavaScript-ning bajarilishini to'xtatadi va debuggingx\` funksiyasini chaqiradi.

Bu debuggerda breakpointni o'rnatish bilan bir xil funktsiyaga ega.

Agar debugging mavjud bo'lmasa, `debugger` steytmenti ta'sir qilmaydi.

Debugging yoqilgan bo'lsa, ushbu kod uchinchi qator ishlashidan oldin uni to'xtatadi.

```
let x = 15 * 5;
debugger;
document.getElementById("demo").innerHTML = x;
```

### Asosiy brauzerlarning debugging vositalari

Odatda, F12 yordamida brauzeringizda debuggingni faollashtirasiz va debugger menyusidan "Consolel" ni tanlang.

Aks holda, quyidagi amallarni bajaring:

### Chrome

* Brauzerni oching.
* Menyudan "Qo'shimcha vositalar" ni tanlang.
* Asboblardan "Dasturchi vositalari" ni tanlang.
* Nihoyat, Konsol-ni tanlang.

### Firefox

* Brauzerni oching.
* Menyudan "Veb dasturchi" ni tanlang.
* Nihoyat, "Veb konsol" ni tanlang.

### Edge

* Brauzerni oching.
* Menyudan "Tuzuvchi asboblari" ni tanlang.
* Nihoyat, "Console" ni tanlang.

### Opera

* Brauzerni oching.
* Menyudan "Debugger" ni tanlang.
* "Ishlab chiquvchi" bo'limida "Dasturchi vositalari" ni tanlang.
* Nihoyat, "Console" ni tanlang.

### Safari

* Asosiy menyuda Safari, Preferences, Advanced-ga o'ting.
* "Menyu satrida ishlab chiqish menyusini ko'rsatishni yoqish" belgisini belgilang.
* Menyuda yangi "Rivojlanish" opsiyasi paydo bo'lganda:\
  "Show error console" ni tanlang.

### Bilasizmi ?

{% hint style="warning" %}
Debugging - bu kompyuter dasturlaridagi buglarni(xatolarni) tekshirish, topish va kamaytirish jarayoni hisoblanadi.\
Aniqlangan birinchi kompyuter bugi elektronikada tiqilib qolgan haqiqiy qo'ng'iz (hasharot) edi.
{% endhint %}
