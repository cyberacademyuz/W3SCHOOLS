# CSS Ranglar

CSS [140 dan ortiq rang nomlarini, HEX qiymatlarini, RGB qiymatlarini](../css-qollanma/css-ranglar/), RGBA qiymatlarini, HSL qiymatlarini, HSLA qiymatlarini va opacity larni qo'llab quvvatlaydi.

### RGBA Ranglar <a href="#rgba-ranglar" id="rgba-ranglar"></a>

RGBA rang qiymatlari RGB rang qiymatlarini kengaytirilgan varianti bo'lib, unda rangning shaffofligini bildiruvchi alpha kanali ham mavjud.

RGBA rang qiymati quyidagicha qilib belgilanadi: rgba (qizil, yashil, ko'k, alfa). Alpha parametri 0.0 (To'liq shaffof) va 1.0 (umuman shaffof bo'lmagan) orasidagi qiymat hisoblanadi.

<figure><img src="../../.gitbook/assets/image (849).png" alt=""><figcaption></figcaption></figure>

Quyidagi misolda turli RGBA ranglar ifodalangan:

```
#p1 {background-color: rgba(255, 0, 0, 0.3);}  /* red with opacity */
#p2 {background-color: rgba(0, 255, 0, 0.3);}  /* green with opacity */
#p3 {background-color: rgba(0, 0, 255, 0.3);}  /* blue with opacity */
```

### HSL Ranglar <a href="#hsl-ranglar" id="hsl-ranglar"></a>

Hue -- rangning 0 dan 360 gacha bo'lgan daraja. 0 bu qizil, 120 yashil va 240 esa ko'k.

Saturation bu qiymatning foizi. 0% bu kulrang degani va 100% esa rangning to'liq o'zi.

Lightness ham foiz hisobalanadi. 0% qora, 50% na qora, na oq, 100% esa oq.



HSL qisqartmasi Hue, Saturation va Lightness degan ma'noni anglatadi.

HSL rang qiymati quyidagicha belgilanadi: hsl (rang, to'yinganlik, yorug'lik).

1. Hue - rang doirasidagi darajasidir (0 dan 360 gacha)
   * 0 (yoki 360) qizil
   * 120 yashil
   * 240 ko'k
2. To'yinganlik - bu foizli qiymat: 100% - to'liq rang.
3. Yorug'lik ham foizda hisoblanadi; 0% qorng'u (qora) va 100% oq.

<figure><img src="../../.gitbook/assets/image (786).png" alt=""><figcaption></figcaption></figure>

Quyidagi misolda turli HSL ranglari ifodalangan:

```
#p1 {background-color: hsl(120, 100%, 50%);}  /* green */
#p2 {background-color: hsl(120, 100%, 75%);}  /* light green */
#p3 {background-color: hsl(120, 100%, 25%);}  /* dark green */
#p4 {background-color: hsl(120, 60%, 70%);}   /* pastel green */
```

### HSLA Ranglar <a href="#hsla-ranglar" id="hsla-ranglar"></a>

HSLA rang qiymatlari HSL ning alpha kanali qo'shilgan va kengaytirilgan varianti hisoblanib, u rang uchun shaffoflikni ham belgilaydi.

HSLA rang qiymati quyidagicha belgilanadi: hsla(_hue,_ _saturation_, _lightness, alpha_). bu yerda alfa parametri shaffoflikni ifodalayapti. Alpha parametri 0.0 (butunlay shaffof) va 1.0 (umuman shaffof emas) orasidagi raqamda beriladi.

<figure><img src="../../.gitbook/assets/image (836).png" alt=""><figcaption></figcaption></figure>

Quyidagi misolda turli HSLA ranglari ifodalangan:

```
#p1 {background-color: hsla(120, 100%, 50%, 0.3);}  /* green with opacity */
#p2 {background-color: hsla(120, 100%, 75%, 0.3);}  /* light green with opacity */
#p3 {background-color: hsla(120, 100%, 25%, 0.3);}  /* dark green with opacity */
#p4 {background-color: hsla(120, 60%, 70%, 0.3);}   /* pastel green with opacity */
```

### Opacity <a href="#opacity" id="opacity"></a>

CSSning `opacity` xususiyati butun elementga shaffoflik qo'shadi (orqafon rangi ham, matn ham shaffof bo'ladi).

`opacity` xususiyatining qiymati 0,0 (to'liq shaffof) va 1,0 (to'liq shaffof) orasidagi raqamli qiymat bo'lishi kerak.

<figure><img src="../../.gitbook/assets/image (782).png" alt=""><figcaption></figcaption></figure>

E'tibor bering, yuqoridagi matn ham shaffof!

Quyidagi misolda shaffoflikka ega bo'lgan turli elementlar ifodalangan:

```
#p1 {background-color:rgb(255,0,0);opacity:0.6;}  /* red with opacity */
#p2 {background-color:rgb(0,255,0);opacity:0.6;}  /* green with opacity */
#p3 {background-color:rgb(0,0,255);opacity:0.6;}  /* blue with opacity */
```
