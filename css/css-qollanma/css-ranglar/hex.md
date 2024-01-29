# HEX

Hexadecimal rangi RR (qizil), GG (yashil) va BB (ko'k) hexadecimal raqamlari rang komponentlarini belgilaydi.

### HEX Value <a href="#hex-value" id="hex-value"></a>

CSS-da rangni quyidagi shaklda hexadecimal qiymatdan foydalanib berish mumkin:

**#**_**rrggbb**_

Bu yerdagi rr (qizil), gg (yashil) va bb (ko'k) larning qiymatlari 00 va ff o'rtasidagi o'n oltilik sanoq tizimidagi qiymatlardir

Masalan, #ff0000 qizil bo'ladi, sababi qizil eng baland qiymatda (ff) va qolganlari eng past qiymatda (00) turibdi. (decimal 0-255 sifatida bir xil)

Qora rangni ko'rsatish uchun barcha qiymatlarni 00 ga tenglashtirish kerak: #000000.

Oq rangni ko'rsatish uchun barcha qiymatlarni ff ga tenglashtirish kerak: #ffffff.

<figure><img src="../../../.gitbook/assets/image (449).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (118).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (266).png" alt=""><figcaption></figcaption></figure>

Kulrang ranglar asosan uchchala rang qiymatlari bir xil bo'lganda xosil bo'ladi:

<figure><img src="../../../.gitbook/assets/image (143).png" alt=""><figcaption></figcaption></figure>

### 3 ta raqamdan iborat HEX qiymat <a href="#id-3-ta-raqamdan-iborat-hex-qiymat" id="id-3-ta-raqamdan-iborat-hex-qiymat"></a>

Ba'zida siz 3 ta raqamdan iborat HEX qiymatdagi ranglarni ko'rishingiz mumkin.

3 ta raqamdan iborat HEX qiymatdagi ranglar ba'zi 6 ta raqamli HEX ranglarni qisqartmasi hisoblanadi.

3 ta raqamdan iborat HEX qiymati quyidagi ko'rinishda bo'ladi:

**#**_**rgb**_

Bu yerda r,g va b - qizil, yashil va ko'k komponentlarni 0 va f orasidagi qiymatlar asosida belgilaydi.

3 ta raqamdan iborat HEX qiymat qachonki barcha 6 ta qiymatdan iborat HEX kodlar bir xil bo'lganda ishlatiladi. Masalan #ff00cc, #f0c qilib yozilishi mumkin.

Mana masalan:

```
body  {
background-color:  #fc9;  /* same as #ffcc99 */
}
h1  {
color:  #f0f;  /* same as #ff00ff */
}
p  {
color:  #b58;  /* same as #bb5588 */
}
```
