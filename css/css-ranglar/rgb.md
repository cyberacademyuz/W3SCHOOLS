# RGB

<mark style="color:red;">**R**</mark><mark style="color:green;">**G**</mark><mark style="color:blue;">**B**</mark> - <mark style="color:red;">QIZIL</mark>, <mark style="color:green;">YASHIL</mark> VA <mark style="color:blue;">KO'K</mark> rang qiymatlarini ifodalaydi.

RGBA rang qiymati esa  Alfa (shaffofligi) ham mavjud bo'lgan RGB ning kengaytirilgan versiyasidir.

## <mark style="color:green;">RGB rang qiymatlari</mark>

HTMLda rang quyidagi formula yordamida RGB qiymati sifatida belgilanishi mumkin:

**rgb ( **_**qizil, yashil**_** , **_**ko'k**_** )**

Har bir parametr (qizil, yashil va ko'k) rangning intensivligini 0 dan 255 gacha bo'lgan qiymat bilan ifodalaydi.

Bu 256 x 256 x 256 = 16.777.216 ta rang mavjudl ekanligini anglatadi !

Masalan, rgb(<mark style="color:red;">255</mark>, 0, 0) qizil rang hisoblanadi, chunki qizil rang eng yuqori qiymat (255)ga ega, qolgan ikkitasi (yashil va ko'k) 0 deb belgilangan.

Yana bir misol, rgb(0, <mark style="color:green;">255</mark>, 0) yashil rang hisoblanadi, chunki yashil rang eng yuqori qiymat (255)ga ega, qolgan ikkitasi (qizil va ko'k) 0 deb belgilangan.

Qora rangni chiqarish uchun barcha parametrlarini 0 qiling, masalan: rgb(0, 0, 0).

Oq rangni chiqarish uchun barcha parametrlarni 255 qiling, masalan: rgb(255, 255, 255).

Quyidagi RGB qiymatlarini aralashtirish orqali tajriba qilib ko'ring:

<figure><img src="../../../.gitbook/assets/image (342).png" alt=""><figcaption></figcaption></figure>

### <mark style="color:green;">Misol</mark>

<figure><img src="../../../.gitbook/assets/image (852).png" alt=""><figcaption></figcaption></figure>

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_color_rgb" %}

### <mark style="color:green;">Kulrang soyalar</mark>

Kulrang soyalar odatda uchta parametrga bir xil qiymat berish orqali tuziladi:

<figure><img src="../../../.gitbook/assets/image (853).png" alt=""><figcaption></figcaption></figure>

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_color_rgb_gray" %}

### <mark style="color:green;">RGBA rang qiymatlari</mark>

RGBA rang qiymatlari rang uchun shaffoflikni belgilaydigan Alfa hamda RGB qiymatlarining kengaytmasidir.

RGBA rang qiymati quyidagicha belgilanadi:

rgba (qizil, yashil, ko'k, alfa)

Alfa parametri 0,0 (to'liq shaffof) va 1,0 (umuman shaffof emas) orasidagi raqam bo'ladi:

Quyidagi RGBA qiymatlarini aralashtirish orqali tajriba qilib ko'ring:

<figure><img src="../../../.gitbook/assets/image (854).png" alt=""><figcaption></figcaption></figure>

### <mark style="color:green;">Misol:</mark>

<figure><img src="../../../.gitbook/assets/image (855).png" alt=""><figcaption></figcaption></figure>

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_color_rgba" %}
