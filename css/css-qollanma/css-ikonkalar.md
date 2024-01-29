# CSS Ikonkalar

icon kutubxonalardan foydalanish orqali Iconlarni HTML sahifaga osongina qo'shish mumkin.

<figure><img src="../../.gitbook/assets/image (172).png" alt=""><figcaption></figcaption></figure>

### Iconlar qanday qo'shiladi ? <a href="#qanday-qilib-ikonkalarni-qoshish-mumkin" id="qanday-qilib-ikonkalarni-qoshish-mumkin"></a>

Iconlardan oson foydalanish usullaridan biri [FontAwesome](https://fontawesome.com/icons) kabi kutubxonalardan foydalanishdir.

Iconning maxsus class nomini istalgan HTML elementiga qo'shing, masalan: (`<i>` yoki `<span>`)

Kutubxonada ko'rsatilgan barcha iconlar o'zgaruvchan vektorda bo'lib, ularni CSS orqali o'zgartirish mumkin (rangini, soyasini, o'lchamini va hokazo).

### Font Awesome iconlari <a href="#font-awesome-ikonkalari" id="font-awesome-ikonkalari"></a>

FontAwesome iconlaridan foydalanish uchun, [<mark style="color:green;">fontawesome.com</mark>](https://fontawesome.com/)ga o'tib, tizimga kiring va HTML ning `<head>` bo'limiga qo'shiladigan codeni oling:

<mark style="color:red;">`<script src="https://kit.fontawesome.com/yourcode.js" crossorigin="anonymous"></script>`</mark>

**FontAwesome**dan foydalanishni chuqurroq o'rganish uchun bizning [<mark style="color:green;">fontawesome 5 qo'llanmasi</mark>](https://www.w3schools.com/icons/fontawesome5\_intro.asp) sahifamizga o'ting.

**Note:** Hech qanday yuklab olish yoki o'rnatib olish shart emas!

```
<!DOCTYPE html>
<html>
<head>
<script src="https://kit.fontawesome.com/a076d05399.js" crossorigin="anonymous"></script>
</head>
<body>

<i class="fas fa-cloud"></i>
<i class="fas fa-heart"></i>
<i class="fas fa-car"></i>
<i class="fas fa-file"></i>
<i class="fas fa-bars"></i>

</body>
</html>
```

<figure><img src="../../.gitbook/assets/image (344).png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
**Font Awesome**ning barcha iconlari haqida toʻliq maʼlumot olish uchun <mark style="color:green;">Icon Reference</mark> sahifasiga tashrif buyuring.
{% endhint %}

### Bootstrap Iconlari <a href="#bootstrap-icons" id="bootstrap-icons"></a>

Bootstrap ning **glyphicon**laridan foydalanish uchun quyidagi kodni HTML ning `<head>` bo'limiga kiriting:

<mark style="color:red;">`<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css">`</mark>

**Note:** Hech qanday yuklab olish yoki o'rnatib olish shart emas!

```
<!DOCTYPE html>
<html>
<head>
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css">
</head>
<body>

<i class="glyphicon glyphicon-cloud"></i>
<i class="glyphicon glyphicon-remove"></i>
<i class="glyphicon glyphicon-user"></i>
<i class="glyphicon glyphicon-envelope"></i>
<i class="glyphicon glyphicon-thumbs-up"></i>

</body>
</html>
```

<figure><img src="../../.gitbook/assets/image (327).png" alt=""><figcaption></figcaption></figure>

### Google Iconlari <a href="#google-icons" id="google-icons"></a>

Google ning Icon laridan foydalanish uchun quyidagi kodni HTMLning `<head>` bo'limiga kiriting:

<mark style="color:red;">`<link rel="stylesheet" href="https://fonts.googleapis.com/icon?family=Material+Icons">`</mark>

**Note:** Hech qanday yuklab olish yoki o'rnatib olish shart emas!

```
<!DOCTYPE html>
<html>
<head>
<link rel="stylesheet" href="https://fonts.googleapis.com/icon?family=Material+Icons">
</head>
<body>

<i class="material-icons">cloud</i>
<i class="material-icons">favorite</i>
<i class="material-icons">attachment</i>
<i class="material-icons">computer</i>
<i class="material-icons">traffic</i>

</body>
</html>
```

<figure><img src="../../.gitbook/assets/image (470).png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
Barcha iconlarning to'liq ro'yxatini olish uchun <mark style="color:green;">Icon qo'llanmasi</mark>ga o'ting.
{% endhint %}
