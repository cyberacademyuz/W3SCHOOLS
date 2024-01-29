# JS Window

**B**rauzer **O**byekti **M**odeli (BOM) JavaScript-ga brauzer bilan “suhbatlashish” imkonini beradi.

### Brauzer obekt modeli (BOM)

BOM uchun rasmiy standartlar mavjud emas.

Zamonaviy brauzerlar interaktivlik uchun bir xil metodlar va xususiyatlarni amalga oshirganligi sababli, u ko'pincha BOMning metodlari va xususiyatlari deb ataladi.

### window obyekti

`window` obyekti barcha brauzerlar tomonidan qo'llab-quvvatlanadi. U brauzer oynasini ifodalaydi.

Barcha global obyektlar, funktsiyalar va o'zgaruvchilar avtomatik tarzda window obyektining a'zolariga aylanadi.

Global o'zgaruvchilar window obyektining xususiyatlari hisoblanadi.

Global funksiyalar window obyektining metodlari hisoblanadi.

Hatto `document` obyekti ham (HTML DOM ning) window obyektining xususiyati hisoblanadi:

```
window.document.getElementById("header");
```

bir xil bo'ladi:

```
document.getElementById("header");
```

### window o'lchami

Brauzer oynasining o'lchamini aniqlash uchun ikkita xususiyatdan foydalanish mumkin.

Ikkala xususiyat ham o'lchamlarni piksellarda qaytaradi:

* `window.innerHeight`- brauzer oynasining ichki balandligi (piksellarda) ko'rsatadi
* `window.innerWidth`- brauzer oynasining ichki kengligi (piksellarda) ko'rsatadi

{% hint style="warning" %}
Brauzer oynasi toolbars va scroolbarni o'z ichiga olmaydi.
{% endhint %}

```
let w = window.innerWidth;
let h = window.innerHeight;
```

### windowning boshqa metodlari

Boshqa ba'zi metodlar:

* `window.open()`- yangi oyna ochish
* `window.close()`- joriy oynani yopish
* `window.moveTo()`- joriy oynani surish
* `window.resizeTo()`- joriy oyna o'lchamini o'zgartirish
