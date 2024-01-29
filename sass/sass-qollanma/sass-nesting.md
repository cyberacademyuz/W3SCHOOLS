# Sass nesting

### Sass Nesting qoidalari <a href="#sass-nesting-qoidalari" id="sass-nesting-qoidalari"></a>

Sass HTML kabi CSS selektorlarini joylashtirish imkonini beradi.

Sayt navigatsiyasi uchun Sass kodining ba'zi misollarini ko'zdan kechiring:

```
nav {
  ul {
    margin: 0;
    padding: 0;
    list-style: none;
  }
  li {
    display: inline-block;
  }
  a {
    display: block;
    padding: 6px 12px;
    text-decoration: none;
  }
}
```

E'tibor bering, Sassda `ul`, `li` va `a` selektorlari `nav` selektori ichiga joylashtirilgan.

CSS-da qoidalar birma-bir yoziladi (ichiga kiritilmagan holda):

```
nav ul {
  margin: 0;
  padding: 0;
  list-style: none;
}
nav li {
  display: inline-block;
}
nav a {
  display: block;
  padding: 6px 12px;
  text-decoration: none;
}
```

Sass-da xususiyatlarni bir birining ichiga joylashtirishingiz mumkinligi sababli, u standart CSS-ga qaraganda tartibliroq va o'qishga osonroq.

### Sass nesting xususiyatlari <a href="#sass-nesting-xususiyatlari" id="sass-nesting-xususiyatlari"></a>

Ko'pgina CSS xususiyatlari `font-family`, `font-size`, `font-weight` yoki `text-align`, `text-transform` va `text-overflow` kabi bir xil prefiksga ega.

Sass bilan ularni ichki xususiyatlar sifatida yozishingiz mumkin:

```
font: {
  family: Helvetica, sans-serif;
  size: 18px;
  weight: bold;
}

text: {
  align: center;
  transform: lowercase;
  overflow: hidden;
}
```

Sass transpileri yuqoridagi kodni oddiy CSS kodiga o'giradi:

```
font-family: Helvetica, sans-serif;
font-size: 18px;
font-weight: bold;

text-align: center;
text-transform: lowercase;
text-overflow: hidden;
```
