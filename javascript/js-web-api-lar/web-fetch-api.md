# WEB Fetch API

{% hint style="success" %}
Fetch API interfeysi veb-brauzerga veb-serverlarga HTTP so'rovlarini yuborish imkonini beradi.

😀 Endi `XMLHttpRequest` kerak emas.
{% endhint %}

### Brauzerning qo'llab-quvvatlashi

Jadvalda Fetch API-ni to'liq qo'llab-quvvatlaydigan brauzerlaring ilk versiyalari ko'rsatilgan:

| Chrome 42 | Edge 14  | Firefox 40 | Safari 10.1 | Opera 29 |
| --------- | -------- | ---------- | ----------- | -------- |
| Apr 2015  | Aug 2016 | Aug 2015   | Mar 2017    | Apr 2015 |

### Fetch API ga misol

Quyidagi misol faylni oladi va uning tarkibini ko'rsatadi:

```
fetch(file)
.then(x => x.text())
.then(y => myDisplay(y));
```

Fetch async va  awaitga asoslanganligi sababli, yuqoridagi misolni quyidagicha tushunish osonroq:

```
async function getText(file) {
  let x = await fetch(file);
  let y = await x.text();
  myDisplay(y);
}
```

Yoki undan ham yaxshirog'i: x va y o'rniga tushunarli nomlardan foydalaning:

```
async function getText(file) {
  let myObject = await fetch(file);
  let myText = await myObject.text();
  myDisplay(myText);
}
```
