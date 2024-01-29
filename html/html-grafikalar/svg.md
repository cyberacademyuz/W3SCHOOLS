---
description: SVG vektorga asoslangan grafikalarni XML formatida yaratadi.
---

# SVG

SVG XML formatida vectorga asoslanga grafik tasvirlar yaratadi.

## SVG nima ?

* SVG - **S**calable **V**ector **G**raphics degan ma'noni bildiradi
* SVG - WEB uchun grafik tasvirlar yaratishda ishlatiladi
* SVG - bu W3C tavsiyasi

## HTMLning \<svg> elemanti

HTMLning \<svg> elementi SVG grafikalari uchun kontener hisoblanadi.

SVG-da yo'llar, qutilar, doiralar, matn va grafik tasvirlarni chizishning bir necha usullari mavjud.

## Browserning qo'llab quvvatlashi



| Element | Chrome | Edge | Firefox | Safari | Opera |
| ------- | ------ | ---- | ------- | ------ | ----- |
| \<svg>  | 4.0    | 9.0  | 3.0     | 3.2    | 10.1  |

### SVG Circle

![](<../../.gitbook/assets/image (6).png>)

```
<!DOCTYPE html>
<html>
<body>

<svg width="100" height="100">
  <circle cx="50" cy="50" r="40" stroke="green" stroke-width="4" fill="yellow" />
</svg>

</body>
</html>
```

### SVG Rectangle

![](<../../.gitbook/assets/image (56).png>)

```
<svg width="400" height="100">
  <rect width="400" height="100" style="fill:rgb(0,0,255);stroke-width:10;stroke:rgb(0,0,0)" />
</svg>
```

### SVG Rounded Rectangle

![](<../../.gitbook/assets/image (530).png>)

```
<svg width="400" height="180">
  <rect x="50" y="20" rx="20" ry="20" width="150" height="150"
  style="fill:red;stroke:black;stroke-width:5;opacity:0.5" />
</svg>
```

### SVG Star

![](<../../.gitbook/assets/image (1).png>)

```
<svg width="300" height="200">
  <polygon points="100,10 40,198 190,78 10,78 160,198"
  style="fill:lime;stroke:purple;stroke-width:5;fill-rule:evenodd;" />
</svg>
```

### SVG Logo

![](<../../.gitbook/assets/image (54).png>)

```
<svg height="130" width="500">
  <defs>
    <linearGradient id="grad1" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" style="stop-color:rgb(255,255,0);stop-opacity:1" />
      <stop offset="100%" style="stop-color:rgb(255,0,0);stop-opacity:1" />
    </linearGradient>
  </defs>
  <ellipse cx="100" cy="70" rx="85" ry="55" fill="url(#grad1)" />
  <text fill="#ffffff" font-size="45" font-family="Verdana" x="50" y="86">SVG</text>
  Sorry, your browser does not support inline SVG.
</svg>
```

### SVG va Canvas o'rtasidagi farqlar

SVG - bu XML-da 2D grafikalarni tavsiflash uchun til.

Canvas 2D grafik tasvirlarni tezda chizadi (JavaScript yordamida).

SVG XML-ga asoslangan, ya'ni har bir element SVG DOM ichida mavjud. Element uchun JavaScriptning eventga ishlov beruvchilarini biriktirishingiz mumkin.

SVG da har bir chizilgan shakl obyekt sifatida saqlanadi. Agar SVG obyektining atributlari o'zgartirilsa, brauzer shaklni avtomatik tarzda qayta ko'rsatishi mumkin.

Canvas pikselma piksel chiziladi. Canvasda, grafik tasvirchizilganidan keyin, u brauzer tomonidan unutiladi. Agar uning joylashuvini o'zgartirish kerak bo'lsa, butun ko'rinishni, shu jumladan grafik tasvir bilan qoplangan bo'lishi mumkin bo'lgan obyektlarni qayta chizish kerak.

### Canvas va SVG ni solishtirish

Quyidagi jadvalda Canvas va SVG o'rtasidagi ba'zi muhim farqlar ko'rsatilgan:

| Canvas                                                                                                                                                                                                                                | SVG                                                                                                                                                                                                                                                                                  |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| <ul><li>Ruxsatga bog'liq</li><li>event handlerlarni qo'llab-quvvatlamaydi</li><li>Poor text rendering capabilities</li><li>You can save the resulting image as .png or .jpg</li><li>Well suited for graphic-intensive games</li></ul> | <ul><li>Resolution independent</li><li>Support for event handlers</li><li>Best suited for applications with large rendering areas (Google Maps)</li><li>Slow rendering if complex (anything that uses the DOM a lot will be slow)</li><li>Not suited for game applications</li></ul> |

### SVG bo'yicha qo'llanma

SVG haqida batafsil ma'lumot olish uchun SVG qo'llanmamizni o'qing.
