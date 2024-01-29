# WEB Worker API

Web-worker - bu sahifaning ishlashiga ta'sir qilmasdan, orqafonda ishlaydigan JavaScript hisoblanadi.

### Veb worker nima ?

HTML sahifasida skriptlarni bajarayotganda, skript tugaguniga qadar sahifa javob bermay qoladi.

Web-worker - bu sahifaning ishlashiga ta'sir qilmasdan, boshqa skriptlardan mustaqil ravishda orqafonda ishlaydigan JavaScript. Siz istalgan kodni bajarishni davom ettirishingiz mumkin: web-worker orqafonda ishlayotgan paytda biror nimani bosish, turli narsalarni tanlash va hokazo.

### Brauzerning qo'llab-quvvatlashi

Jadvalda Web workerlarni to'liq qo'llab-quvvatlaydigan brauzerlarning ilk versiyalari ko'rsatadi:

| Chrome 4 | IE 10    | Firefox 3.5 | Safari 4 | Opera 11.5 |
| -------- | -------- | ----------- | -------- | ---------- |
| Jan 2010 | Sep 2012 | Jun 2009    | Jun 2009 | Jun 2011   |

### Web-workerlarga misol

Quyidagi misolda raqamlarni orqafonda hisoblaydigan oddiy web-workerni yaratadi:

<figure><img src="../../.gitbook/assets/image (67).png" alt=""><figcaption></figcaption></figure>

### Web-workerni qo'llab quvvatlanishini tekshirish

Web-worker yaratishdan oldin, foydalanuvchining brauzeri uni qo'llab-quvvatlashini tekshiring:

```
if (typeof(Worker) !== "undefined") {
  // Yes! Web worker support!
  // Some code.....
} else {
  // Sorry! No Web Worker support..
}
```

### Web-worker faylini yarating

Keling, tashqi JavaScript-faylida web-worker yarataylik.

Bu yerda biz counter skriptini yaratamiz. Skript "demo\_workers.js" faylida saqlanadi:

```
let i = 0;

function timedCount() {
  i ++;
  postMessage(i);
  setTimeout("timedCount()",500);
}

timedCount();
```

Yuqoridagi kodning muhim qismi `postMessage()`- bu HTML sahifaga xabar yuborish uchun ishlatiladigan metod.

Eslatma: Odatda web workerlar bunday oddiy skriptlar uchun ishlatilmaydi, balki ko'proq CPU bilan bo'gliq intensiv vazifalar uchun ishlatiladi.

### Web worker obyektini yaratish

Endi bizda web worker fayli bor, biz uni HTML sahifadan ko'rsatishimiz kerak.

Quyidagi qatorlar web worker allaqachon bor yoki yo'qligini tekshiradi, agar bor bo'lmasa - u yangi web worker obyektini yaratadi va kodni "demo\_workers.js" da ishga tushiradi:

```
if (typeof(w) == "undefined") {
  w = new Worker("demo_workers.js");
}
```

Endi web-workerdan xabarlar yuborishimiz va qabul qilishimiz mumkin.

Web-workerga "onmessage" hodisa tinglovchisini qo'shing.

```
w.onmessage = function(event){
  document.getElementById("result").innerHTML = event.data;
};
```

Web worker xabarni joylashtirganda, hodisa tinglovchisi ichidagi kod bajariladi. Web worker ma'lumotlari `event.data` da saqlanadi.

### Web workerni tugatish

Web worker obyekti yaratilganda, u to'xtatilgunga qadar xabarlarni tinglashda davom etadi (tashqi skript tugagandan keyin ham).

Web workerni va brauzer/kompyuter resurslarini ishlashini to'xtatish uchun `terminate()` metodidan foydalaning:

```
w.terminate();
```

### Web-workerni qayta ishlatish

Agar worker o'zgaruvchisini undefined qilib qo'ysangiz, u tugatilgandan so'ng, kodni qayta ishlatishingiz mumkin:

```
w = undefined;
```

### Web-workerning to'liq kodi

Biz allaqachon .js faylida web-worker kodini ko'rdik. Quyida HTML sahifa uchun kod keltirilgan:

```
<!DOCTYPE html>
<html>
<body>

<p>Count numbers: <output id="result"></output></p>
<button onclick="startWorker()">Start Worker</button>
<button onclick="stopWorker()">Stop Worker</button>

<script>
let w;

function startWorker() {
  if (typeof(w) == "undefined") {
    w = new Worker("demo_workers.js");
  }
  w.onmessage = function(event) {
    document.getElementById("result").innerHTML = event.data;
  };
}

function stopWorker() {
  w.terminate();
  w = undefined;
}
</script>

</body>
</html>
```

### Veb-workerlar va DOM

Veb-worker tashqi fayllarda bo'lganligi sababli, ular quyidagi JavaScript obyektlariga murojjat qilsh huquqiga ega emaslar:

* window obyekti
* document obyekti
* parent obyekt
