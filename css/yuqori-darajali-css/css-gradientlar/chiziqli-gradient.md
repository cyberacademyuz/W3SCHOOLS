# Chiziqli gradient

<figure><img src="../../../.gitbook/assets/image (764).png" alt=""><figcaption></figcaption></figure>

CSS gradientlari ikki yoki undan ko'p bo'lgan ranglar orasida o'tish (boshqa rangga) imkoniyatini beradi

CSS da uch xil gradientlar mavjud:

* Linear (chiziqli) gradientlar (pastga/yuqoriga/chapga/o‘ngga/diagonal tarzda yo'naladi)
* Radial gradientlar (ortasi orqali yaratiladi)
* Konusli gradientlar (markaziy nuqta atrofida aylantirilgan bo'ladi)

### CSS Linear gradientlar <a href="#css-chiziqli-gradientlar" id="css-chiziqli-gradientlar"></a>

Chiziqli gradient yaratish uchun kamida ikkita rangning to'xtash nuqtasini belgilashingiz kerak. Rangning to'xtash nuqtasi - bu ikki rang o'rtasida bir rangdan ikkinchisiga o'tadigan ranglardir. Bundan tashqari, gradient effekti orqali boshlang'ich nuqta va yo'nalishni ham berishingiz mumkin.

#### Sintaksis <a href="#sintaksisi" id="sintaksisi"></a>

```
background-image: linear-gradient(direction, color-stop1, color-stop2, ...);
```

Yo'nalish - yuqoridan pastga qarab (standart)

Quyidagi misol yuqoridan boshlanadigan chiziqli gradientni ko'rsatib bermoqda. U qizildan boshlanadi va sariq rangga o'tadi:

<figure><img src="../../../.gitbook/assets/image (776).png" alt=""><figcaption></figcaption></figure>

```
#grad {
  background-image: linear-gradient(red, yellow);
}
```

Yo'nalish - chapdan o'ngga

Quyidagi misolda chapdan boshlanadigan chiziqli gradient ko'rsatilgan. U qizildan boshlanib sariq rangga o'tadi:

<figure><img src="../../../.gitbook/assets/image (812).png" alt=""><figcaption></figcaption></figure>

```
#grad {
  background-image: linear-gradient(to right, red , yellow);
}
```

Yo'nalish - diagonal

Gorizontal va vertikal boshlang'ich nuqtani belgilash orqali diagonal tarzda gradient yaratishingiz mumkin.

Quyidagi misolda tepa tomon chapdan boshlanib pastki qismning o'ng tomonida tugaydigan chiziqli gradient ko'rsatilgan. U qizil rangdan boshlanib, sariq rangga o'tadi:

<figure><img src="../../../.gitbook/assets/image (767).png" alt=""><figcaption></figcaption></figure>

```
#grad {
  background-image: linear-gradient(to bottom right, red, yellow);
}
```

### Burchaklarni ishga solgan holda <a href="#burchaklarni-ishga-solgan-holda" id="burchaklarni-ishga-solgan-holda"></a>

Agar gradient yo'nalishini yaxshiroq boshqarmoqchi bo'lsangiz, oldindan belgilangan (to bottom, to top, to right, to left, to bottom right va hkz.) yo'nalishlar o'rniga burchakni belgilashingiz mumkin. **0deg** "_to top_" qiymatiga teng. 90deg qiymati esa "to right" ni bildiradi. 180deg esa "to botttom" ga teng.

#### Sintaksis <a href="#sintaksisi-2" id="sintaksisi-2"></a>

```
background-image: linear-gradient(angle, color-stop1, color-stop2);
```

Quyidagi misolda chiziqli gradientlarda burchaklardan qanday foydalanish ko'rsatilgan:

<figure><img src="../../../.gitbook/assets/image (823).png" alt=""><figcaption></figcaption></figure>

```
#grad {
  background-image: linear-gradient(180deg, red, yellow);
}
```

### Bir nechta rangli to'tash nuqtalaridan foydalanish <a href="#bir-nechta-rangli-toxtashlardan-foydalanish" id="bir-nechta-rangli-toxtashlardan-foydalanish"></a>

Quyidagi misolda bir nechta rangli to'xtash joylari orqali linear gradient yasash ko'rsatilgan:

<figure><img src="../../../.gitbook/assets/image (274).png" alt=""><figcaption></figcaption></figure>

```
#grad {
  background-image: linear-gradient(red, yellow, green);
}
```

Quyidagi misolda kamalak rangili va matnli linear gradient (chapdan o'ngga) yaratish ko'rsatilgan:

<figure><img src="../../../.gitbook/assets/image (780).png" alt=""><figcaption></figcaption></figure>

```
#grad {
  background-image: linear-gradient(to right, red,orange,yellow,green,blue,indigo,violet);
}
```

### Shaffoflikdan foydalanish <a href="#shaffoflikdan-foydalanish" id="shaffoflikdan-foydalanish"></a>

CSSning gradientlari shaffoflikni ham qo'llab-quvvatlaydi, bu esa xiraroq effektlar yaratish uchun ishlatilishi mumkin.

Rangni to'xtash joylarini berish va shaffoflikdan foydalanish uchun **rgba()** funksiyasini ishlatamiz. **Rgba()** funksiyasidagi oxirgi parametr **0** dan **1** gacha boʻlgan qiymatni o'z ichiga oladi va u rangning shaffofligini belgilaydi: 0 toʻliq shaffoflikni, 1 esa toʻliq rangni (shaffoflik yoʻqligini) bildiradi.

Quyidagi misolda chapdan boshlanadigan linear gradient ko'rsatilgan. U butunlay shaffof bo'lib, to'liq qizil rangga o'tadi:

<figure><img src="../../../.gitbook/assets/image (774).png" alt=""><figcaption></figcaption></figure>

```
#grad {
  background-image: linear-gradient(to right, rgba(255,0,0,0), rgba(255,0,0,1));
}
```

### Linear gradientni takrorlash <a href="#chiziqli-gradientni-takrorlash" id="chiziqli-gradientni-takrorlash"></a>

`repeating-linear-gradient()`  linear gradientlarni takrorlash uchun ishlatiladi:

<figure><img src="../../../.gitbook/assets/image (837).png" alt=""><figcaption></figcaption></figure>

```
#grad {
  background-image: repeating-linear-gradient(red, yellow 10%, green 20%);
}
```
