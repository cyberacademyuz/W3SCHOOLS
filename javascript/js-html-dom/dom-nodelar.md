# DOM Nodelar

Nodelar qo'shish va o'chirish (HTML elementlari)

### Yangi HTML elementlarini yaratish (nodelar)

HTML DOM-ga yangi element qo'shish uchun avval elementni (element node-ini) yaratishingiz va keyin uni mavjud elementga qo'shishingiz kerak.

```
<div id="div1">
  <p id="p1">This is a paragraph.</p>
  <p id="p2">This is another paragraph.</p>
</div>

<script>
const para = document.createElement("p");
const node = document.createTextNode("This is new.");
para.appendChild(node);

const element = document.getElementById("div1");
element.appendChild(para);
</script>
```

### Misolni tushuntirish&#x20;

Ushbu kod yangi `<p>` elementi yaratadi:

```
const para = document.createElement("p");
```

`<p>` elementiga matn qo'shish uchun avval matn node-ini yaratishingiz kerak. Ushbu kod matn node-ini yaratadi:

```
const node = document.createTextNode("This is a new paragraph.");
```

Keyin `<p>` elementiga matn node-ini qo'shishingiz kerak:

```
para.appendChild(node);
```

Vanihoyat, yangi elementni mavjud elementga qo'shishingiz kerak.

Ushbu kod mavjud elementni topadi:

```
const element = document.getElementById("div1");
```

Bu kod esa yangi elementni mavjud elementga qo'shadi:

```
element.appendChild(para);
```

### Yangi HTML elementlarini yaratish - insertBefore()

Oldingi misoldagi `appendChild()` metodi yangi elementni ota-ona elementining oxirgi farzandi sifatida qo'shdi.

Agar bunday qilishni xohlamasangiz,  `insertBefore()` metodidan foydalanishingiz mumkin:

```
<div id="div1">
  <p id="p1">This is a paragraph.</p>
  <p id="p2">This is another paragraph.</p>
</div>

<script>
const para = document.createElement("p");
const node = document.createTextNode("This is new.");
para.appendChild(node);

const element = document.getElementById("div1");
const child = document.getElementById("p1");
element.insertBefore(para, child);
</script>
```

### Mavjud HTML elementlarini olib tashlash

HTML elementini olib tashlash uchun  `remove()` metodidan foydalaning:

```
<div>
  <p id="p1">This is a paragraph.</p>
  <p id="p2">This is another paragraph.</p>
</div>

<script>
const elmnt = document.getElementById("p1"); elmnt.remove();
</script>
```

### Misolni tushuntirish&#x20;

HTML hujjatida ikkita asosiy node(ikkita `<p>` element)ga ega `<div>` elementi mavjud:

```
<div>
  <p id="p1">This is a paragraph.</p>
  <p id="p2">This is another paragraph.</p>
</div>
```

O'chiriladigan elementni toping:

```
const elmnt = document.getElementById("p1");
```

Keyin ushbu elementda `remove()` metodini ishlating:

```
elmnt.remove();
```

{% hint style="danger" %}
`remove()` metodi eski brauzerlarda ishlamaydi, uning o'rniga `removeChild()` dan qanday foydalanish kerakligi haqida quyidagi misolga qarang.
{% endhint %}

### Bola element node-ini olib tashlash

`remove()` metodini qo'llab-quvvatlamaydigan brauzerlarda elementni olib tashlash uchun asosiy nodeni topishingiz kerak:

```
<div id="div1">
  <p id="p1">This is a paragraph.</p>
  <p id="p2">This is another paragraph.</p>
</div>

<script>
const parent = document.getElementById("div1");
const child = document.getElementById("p1");
parent.removeChild(child);
</script>
```

### Misolni tushuntirish

Ushbu HTML hujjatida ikkita asosiy node(ikkita `<p>` element)ga ega  `<div>` elementi mavjud:

```
<div id="div1">
  <p id="p1">This is a paragraph.</p>
  <p id="p2">This is another paragraph.</p>
</div>
```

`id="div1"` atributiga ega elementni toping:

```
const parent = document.getElementById("div1");
```

`id="p1"` atributiga ega `<p>` elementini toping:

```
const child = document.getElementById("p1");
```

Bola elementni ota-ona elementidan olib tashlang:

```
parent.removeChild(child);
```

Ushbu kod buning vaqtinchalik yechimi: O'chirmoqchi bo'lgan bola elementini toping va ota-ona elementini topish uchun uning `parentNode` xususiyatidan foydalaning:

```
const child = document.getElementById("p1");
child.parentNode.removeChild(child);
```

### HTML elementlarini almashtiring&#x20;

Elementni HTML DOM ga almashtirish uchun quyidagi `replaceChild()` metodidan foydalaning:

```
<div id="div1">
  <p id="p1">This is a paragraph.</p>
  <p id="p2">This is another paragraph.</p>
</div>

<script>
const para = document.createElement("p");
const node = document.createTextNode("This is new.");
para.appendChild(node);

const parent = document.getElementById("div1");
const child = document.getElementById("p1");
parent.replaceChild(para, child);
</script>
```
