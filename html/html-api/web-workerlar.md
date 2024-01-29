# Web workerlar

Veb-ishchi - bu sahifaning ishlashiga ta'sir qilmasdan, fonda ishlaydigan JavaScript.

### Web worker nima?

HTML sahifasida skriptlarni bajarayotganda, skript tugaguniga qadar sahifa yuklanmay qoladi.

Veb-worker - bu sahifaning ishlashiga ta'sir qilmasdan, boshqa skriptlardan mustaqil tarzda orqafonda ishlaydigan JavaScriptdir. Web-worker orqafonda ishlayotgan paytda biror nimani bosish, narsalarni tanlash va boshqa o'zingiz istagan narsani qilishni davom ettirishingiz mumkin.

### Brauzerning qo'llab-quvvatlashi

Jadvaldagi raqamlar web-workerni to'liq qo'llab-quvvatlaydigan birinchi brauzer versiyasini bildiradi.

| API         | Chrome | Edge | Firefox | Safari | Opera |
| ----------- | ------ | ---- | ------- | ------ | ----- |
| Web Workers | 4.0    | 10.0 | 3.5     | 4.0    | 11.5  |

### Web  workerlarga misol

Quyidagi misolda raqamlarni orqafonda hisoblaydigan oddiy veb-worker yaratilgan:

![](<../../.gitbook/assets/image (785).png>)

### Veb worker qo'llab quvvatlanishini tekshiring

Veb-worker yaratishdan avval, foydalanuvchining brauzeri uni qo'llab-quvvatlashini tekshiring:

```
if (typeof(Worker) !== "undefined") {
  // Yes! Web worker support!
  // Some code.....
} else {
  // Sorry! No Web Worker support..
}
```

### Veb worker faylini yarating

Keling, JavaScript-faylda veb-workerimizni yaratamiz.

Bu yerda biz hisoblovchi skript yaratamiz. Skript "demo\_workers.js" faylida saqlanadi:

```
var i = 0;

function timedCount() {
  i = i + 1;
  postMessage(i);
  setTimeout("timedCount()",500);
}

timedCount();
```

Yuqoridagi kodning muhim qismi `postMessage()`- bu HTML sahifaga xabar yuborish uchun ishlatiladigan metod.

**Eslatma:** Odatda veb workerlar bunday oddiy skriptlar uchun emas, balki ko'proq CPU talab qiladigan intensiv vazifalar uchun ishlatiladi.

### Veb worker obyektini yaratish

Endi bizda veb worker fayli bor, biz uni HTML sahifadan chaqirishimiz kerak.

Quyidagi qatorlar worker allaqachon mavjud yoki mavjudmasligini tekshiradi, agar mavjud bo'lmasa - u yangi veb-worker obyektini yaratadi va kodni "demo\_workers.js" da ishga tushiradi:

```
if (typeof(w) == "undefined") {
  w = new Worker("demo_workers.js");
}
```

Keyin veb-workerdan xabarlarni yuborishimiz va qabul qilishimiz mumkin.

Veb-workerga "`onmessage`" hodisa tinglovchisini qo'shing.

```
w.onmessage = function(event){
  document.getElementById("result").innerHTML = event.data;
};
```

Veb-worker xabarni joylashtirganda, event listener ichidagi kod bajariladi. Veb-worker ma'lumotlari `event.data`da saqlanadi.

### Veb workerni to'xtatish

Veb-worker obyekti yaratilganda, u to'xtatilgunga qadar xabarlarni tinglashda davom etadi (tashqi skript fayldagi kod tugagandan keyin ham).

Veb-workerni va brauzer/kompyuter resurslarini to'xtatish uchun quyidagi `terminate()`metodidan foydalaning:

```
w.terminate();
```

### Veb workerni qayta ishlatish

Agar siz worker o'zgaruvchisini undefined qilib qo'ysangiz, u to'xtatilgandan keyin, kodni qayta ishlatishingiz mumkin:

```
w = undefined;
```

### Web-workerning to'liq kodi

Biz **.js** faylida allaqachon worker kodini ko'rdik. Quyida HTML sahifa uchun kod keltirilgan:

```html
<!DOCTYPE html>
<html>
<body>

<p>Count numbers: <output id="result"></output></p>
<button onclick="startWorker()">Start Worker</button>
<button onclick="stopWorker()">Stop Worker</button>

<script>
var w;

function startWorker() {
  if (typeof(Worker) !== "undefined") {
    if (typeof(w) == "undefined") {
      w = new Worker("demo_workers.js");
    }
    w.onmessage = function(event) {
      document.getElementById("result").innerHTML = event.data;
    };
  } else {
    document.getElementById("result").innerHTML = "Sorry! No Web Worker support.";
  }
}

function stopWorker() {
  w.terminate();
  w = undefined;
}
</script>

</body>
</html>O'zingiz sinab ko'ring »
```

### Veb workerlar va DOM

Veb-workerlar tashqi fayllarda bo'lganligi sababli, ular quyidagi JavaScript obyektlariga murojaat qilish huquqiga ega emaslar:

* window obyekti
* document ob'ekti
* Ota obyekt
