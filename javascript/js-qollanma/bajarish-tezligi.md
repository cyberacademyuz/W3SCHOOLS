# Bajarish tezligi

JavaScript kodining ishlash tezligini qanday oshirish mumkin.

### Loop jarayonlarini yengillashtiring

Dasturlashda looplardan keng foydalaniladi.

Sikldagi har bir steytment, jumladan `for` operatori siklning har bir iteratsiyasi uchun bajariladi.

Loopdan tashqarida ham yozilishi mumkin bo'lgan steytmentlar yoki tayinlashlar tsiklning tezroq ishlashini ta'minlaydi.

{% code title="Yomon:" %}
```
for (let i = 0; i < arr.length; i++) {
```
{% endcode %}

{% code title="Yaxshi:" %}
```
let l = arr.length;
for (let i = 0; i < l; i++) {
```
{% endcode %}

Ortiqcha kod har safar tsikl takrorlanganda massivning `length` xususiyatiga murojaat qilaveradi.

Arrayning length xususiyatiga sikldan tashqarida murojaat qilinsa sikl tezroq ishlaydi.

### DOMga murojaat qilishni kamaytiring

DOM ga murojaat qilish boshqa steytmentlarga qaraganda juda sekin ishlaydi.

Agar DOM elementlariga bir necha marta murojaat qilish kerak bo'lsa, unga bir marta murojaat qilib uni lokal oʻzgaruvchiga tayinlang va o'sha o'zgaruvchidan foydalaning:

{% code title="" %}
```
const obj = document.getElementById("demo");
obj.innerHTML = "Hello";
```
{% endcode %}

### DOM elementlarini kamaytiring

DOM dagi elementlar sonini kamaytiring.

Bu sahifa yuklanishini yaxshilaydi va ma'lumotlarning ekranda ko'rinishini tezlashtiradi, ayniqsa kichikroq qurilmalarda bu yaxshi samara beradi.

DOM elementlarini qidirish (masalan, getElementsByTagName) DOM elementlarining kamligi sabab tezlashadi.

### Keraksiz o'zgaruvchilardan saqlaning

Agar qiymatni saqlash kerak bo'lmasa, yangi o'zgaruvchi yaratmang.

Masalan mana bu kabi kodingizni:

```
let fullName = firstName + " " + lastName;
document.getElementById("demo").innerHTML = fullName;
```

Mana bunday o'zgartirishingiz mumkin:

```
document.getElementById("demo").innerHTML = firstName + " " + lastName;
```

### JavaScript fayl yuklanishini kechiktirish

Skriptlaringizni sahifaning pastki qismiga qo'yish brauzerga avval sahifani yuklash imkonini beradi.

Agar birinchi javascript fayl yuklanishi uchun uni yuqoriga qo'ygan bo'lsangiz skript yuklab olinayotganda brauzer boshqa kodlarni o'qimaydi.&#x20;

{% hint style="warning" %}
HTTP spetsifikatsiyasi brauzerlar parallel ravishda ikkitadan ortiq komponentni yuklab ololmasligini belgilaydi.
{% endhint %}

Yuqoridagiga muqobil tarzda skript tegida `defer="true"` atributidan foydalanish mumkin. Defer atributi sahifa yuklanganidan keyingina script faylni o'qish kerakligini bildiradi, lekin u faqat tashqi ulangan skriptlar fayllar uchun ishlaydi.

Iloji bo'lsa, sahifa to'liq yuklanganidan keyin, script faylni yuklash kerakligini ifodalovchi kod blokidan foydalaning:

```
<script>
window.onload = function() {
  const element = document.createElement("script");
  element.src = "myScript.js";
  document.body.appendChild(element);
};
</script>
```

### `with`-dan foydalanishdan saqlaning

`with` kalit so'zini ishlatishdan saqlaning. Bu tezlikka salbiy ta'sir ko'rsatadi. Bundan tashqari, u scopelarni chalkashtirib yuboradi.

Qatiy rejim (strict mode)da `with`  kalit so'ziga ruxsat berilmaydi.
