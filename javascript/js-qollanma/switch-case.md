# Switch case

`switch` steytmenti turli shartlarga asoslangan turli vazifalarni bajarish uchun ishlatiladi.

### Switch steytmenti

Bir necha kod bloklaridan bajariladigan birini tanlash uchun `switch` steytmentidan foydalaning.

#### Sintaksis

```
switch(expression) {
  case x:
    // code block
    break;
  case y:
    // code block
    break;
  default:
    // code block
}
```

Bu shunday ishlaydi:

* Switch steytmenti bir marta e'lon qilinadi.
* Ifodaning qiymati har bir holatning qiymati bilan taqqoslanadi.
* Agar mos keladigan bo'lsa, berilgan kod bloki bajariladi.
* Agar mos kelmasa, standart kod bloki bajariladi.

```
// getDay() metodi hafta kunini 0 dan 6 gacha bo'lgan raqam sifatida qaytaradi.
// (Yakshanba = 0, dushanba = 1, seshanba = 2 ..)
// Ushbu misolda hafta kunlarining nomini aniqlash uchun hafta kunining raqamidan foydalaniladi:

switch (new Date().getDay()) {
  case 0:
    day = "Sunday";
    break;
  case 1:
    day = "Monday";
    break;
  case 2:
     day = "Tuesday";
    break;
  case 3:
    day = "Wednesday";
    break;
  case 4:
    day = "Thursday";
    break;
  case 5:
    day = "Friday";
    break;
  case 6:
    day = "Saturday";
}

// Kunning natijasi quyidagicha bo'ladi:
Monday
```

### Break kalit so'zi

Kod `break` kalit so'ziga kelganda, u `switch` blokidan chiqib ketadi.

Bu `swtich` blokining ichidagi kodni to'xtatadi.

Switch blokidagi oxirgi caseni to'xtatish shart emas. Blok baribir u yerda tugaydi.

{% hint style="warning" %}
**Eslatma:** Agar siz `break` kiritmasangiz, taqqoslash case bilan mos kelmasa ham, keyingi case bajariladi.
{% endhint %}

### Default kalit so'z

`default` kalit so'zi, agar shart hech qaysi case-ga mos kelmasa, ishlashi kerak bo'ladigan kodni o'z ichiga oladi:

```
Usul getDay()ish kunini 0 dan 6 gacha bo'lgan raqam sifatida qaytaradi.
Agar bugun shanba (6) yoki yakshanba (0) bo'lmasa, standart xabarni yozing:

switch (new Date().getDay()) {
  case 6:
    text = "Today is Saturday";
    break;
  case 0:
    text = "Today is Sunday";
    break;
  default:
    text = "Looking forward to the Weekend";
}

// Matnning natijasi quyidagicha bo'ladi:
Looking forward to the Weekend
```

`default` case switch blokidagi oxirgi holat bo'lishi shart emas:

```
switch (new Date().getDay()) {
  default:
    text = "Looking forward to the Weekend";
    break;
  case 6:
    text = "Today is Saturday";
    break;
  case 0:
    text = "Today is Sunday";
}
```

{% hint style="warning" %}
Agar `default` switch blokidagi oxirgi holat bo'lmasa, standart caseni `break` bilan tugatishni unutmang.
{% endhint %}

### Takrorlanuvchi kod bloklari

Ba'zan turli xil switch case-larda bir xil koddan foydalanishni xohlaysiz.

Bu misolda case 4 va case 5 bitta kod blokni, 0 va 6 esa boshqa kod blokini ulashadi:

```
switch (new Date().getDay()) {
  case 4:
  case 5:
    text = "Soon it is Weekend";
    break;
  case 0:
  case 6:
    text = "It is Weekend";
    break;
  default:
    text = "Looking forward to the Weekend";
}
```

### Tafsilotlarni almashtirish

Agar bir nechta case-lar switch qiymatiga mos kelsa, birinchi case tanlanadi.

Agar mos keladigan caselar topilmasa, dastur **default** qismdagi kodni bajaradi.

Agar `default` topilmasa, dastur bayonot(lar)ni switchdan keyin davom ettiradi.

### Qatiy taqqoslash

Switch case **qat'iy** taqqoslashdan foydalanadi (===).

Qiymatlar mos kelishi uchun uning turi bir xil bo'lishi kerak.

Qatiy taqqoslash operandlar turi bir xil bo'lsagina true bo'lishi mumkin.

Bu misolda hech qaysi holat x ga mos kelmaydi:

```
let x = "0";
switch (x) {
  case 0:
    text = "Off";
    break;
  case 1:
    text = "On";
    break;
  default:
    text = "No value found";
}
```
