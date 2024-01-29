# Soya effekti

### ![](<../../../.gitbook/assets/image (576).png>)         ![](<../../../.gitbook/assets/image (290).png>) <a href="#css-soya-effektlari" id="css-soya-effektlari"></a>

### CSS Soyali effektlar <a href="#css-soya-effektlari" id="css-soya-effektlari"></a>

CSS yordamida element va matnlarga soya berishingiz mumkin.

Ushbu bo'limlarda quyidagi xususiyatlar haqida o'rganasiz:

* <mark style="color:red;">`text-shadow`</mark>
* <mark style="color:red;">`box-shadow`</mark>

### CSS Matn soyasi <a href="#css-matn-soyasi" id="css-matn-soyasi"></a>

CSS ning `text-shadow` xususiyati matnga soya beradi

Eng oddiy soya berishda 2 pikselli gorizontal va 2 pikselli vertikal soya berishingiz mumkin.

![](<../../../.gitbook/assets/image (237).png>)

```
h1 {
  text-shadow: 2px 2px;
}
```

Endi soyaga rang beramiz:

![](<../../../.gitbook/assets/image (540).png>)

```
h1 {
  text-shadow: 2px 2px red;
}
```

So'ngra blur effektini ham qo'shamiz:

![](<../../../.gitbook/assets/image (612).png>)

```
h1 {
  text-shadow: 2px 2px 5px red;
}
```

Quyidagi misolda qora soyaga ega oq rangli matn ko'rsatilgan.

![](<../../../.gitbook/assets/image (265).png>)

```
h1 {
  color: white;
  text-shadow: 2px 2px 4px #000000;
}
```

Quyidagi misolda esa qizil neon nurli soya ko'rsatilgan:

![](<../../../.gitbook/assets/image (247).png>)

```
h1 {
  text-shadow: 0 0 3px #FF0000;
}
```

### Bir nechta soyalar <a href="#bir-nechta-soyalar" id="bir-nechta-soyalar"></a>

Matnga bir nechta soya berish uchun bir nechta soyalarni vergul bilan ajratilgan holda yozing.

Quyidagi misolda qizil va ko'k neon nurli soya ko'rsatilgan:

![](<../../../.gitbook/assets/image (227).png>)

```
h1 {
  text-shadow: 0 0 3px #FF0000, 0 0 5px #0000FF;
}
```

Quyidagi misolda qora, ko'k va to'q ko'k soya berilgan oq rangli matn ko'rsatilgan:

![](<../../../.gitbook/assets/image (642).png>)

```
h1 {
  color: white;
  text-shadow: 1px 1px 2px black, 0 0 25px blue, 0 0 5px darkblue;
}
```

Ba'zi matnlar atrofida (soyasiz) tekis hoshiya yaratish uchun ham  `text-shadow` xususiyatidan foydalanishingiz mumkin:

![](<../../../.gitbook/assets/image (653).png>)

```
h1 {
  color: coral;
  text-shadow: -1px 0 black, 0 1px black, 1px 0 black, 0 -1px black;
}
```
