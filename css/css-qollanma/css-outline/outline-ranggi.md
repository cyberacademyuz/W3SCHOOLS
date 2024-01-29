# Outline ranggi

### CSS Outline color <a href="#css-kontur-rangi" id="css-kontur-rangi"></a>

`outline-color` xususiyati outline-ga rang berish uchun ishlatiladi.

Ranglar quyidagi qiymatlar asosida berilishi mumkin:

* name (nom) - ma'lum rang nomi asosida, masalan, "red"
* HEX - ma'lum bir hex qiymat asosida, masalan, "#ff0000"
* RGB - ma'lum bir RGB qiymat asosida, masalan, "rgb(255,0,0)"
* HSL - ma'lum bir HSL qiymat asosida, masalan, "hsl(0, 100%, 50%)"
* invert - rangni o'zgartirishni amalga oshiradi (rang backgroundidan qat'iy nazar outline-ning ko'rinishini ta'minlaydi)

Quyidagi misolda turli xil ranglarga ega har xil outlinelar ko'rsatilgan. Shuningdek, ushbu elementlarning outline ichida ingichka qora chegarasi borligiga e'tibor bering:

<figure><img src="../../../.gitbook/assets/image (494).png" alt=""><figcaption></figcaption></figure>

```
p.ex1 {
  border: 2px solid black;
  outline-style: solid;
  outline-color: red;
}

p.ex2 {
  border: 2px solid black;
  outline-style: dotted;
  outline-color: blue;
}

p.ex3 {
  border: 2px solid black;
  outline-style: outset;
  outline-color: grey;
}
```

### HEX qiymatlari <a href="#hex-qiymatlari" id="hex-qiymatlari"></a>

Outline ranglari HEX qiymatlari asosida ham belgilanishi mumkin:

```
p.ex1 {
  outline-style: solid;
  outline-color: #ff0000; /* red */
}
```

### RGB qiymatlari <a href="#rgb-qiymatlari" id="rgb-qiymatlari"></a>

yoki RGB qiymatlari asosida ham belgilanishi mumkin:

```
p.ex1 {
  outline-style: solid;
  outline-color: rgb(255, 0, 0); /* red */
}
```

### HSL qiymatlari <a href="#hsl-qiymatlari" id="hsl-qiymatlari"></a>

HSL qiymatlardan ham foydalanishingiz mumkin:

```
p.ex1 {
  outline-style: solid;
  outline-color: hsl(0, 100%, 50%); /* red */
}
```

{% hint style="warning" %}
HEX, HSL va RGB qiymatlar haqida <mark style="color:green;">CSS Ranglar</mark> bo'limida ko'proq ma'lumot olishingiz mumkin.
{% endhint %}
