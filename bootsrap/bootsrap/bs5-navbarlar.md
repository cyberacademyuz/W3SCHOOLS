# BS5 Navbarlar

### Navigatsiya barlari

Navigatsiya paneli sahifaning yuqori qismida joylashadi:

<figure><img src="../../.gitbook/assets/image (713).png" alt=""><figcaption></figcaption></figure>

### Boshlang'ich Navbar

Navbar bootstrap yordamida ekran o'lchamiga qarab kengayishi yoki kichrayishi mumkin.

Standart navbar `.navbar` classi bilan yaratiladi, undan keyin moslashuvchanlikni ta'minlovchi `.navbar-expand-xxl|xl|lg|md|sm` classi mavjud: (navbarni vertikal ravishda xxlarge, juda katta, katta, o'rta yoki kichik ekranlarga moslaydi).

Navbarga havolalar qo'shish uchun `class="navbar-nav"` bilan `<ul>` elementidan (yoki  `<div>`) foydalaning. Keyin `.nav-item` classiga ega `<li>` elementlarini va undan keyin `nav-link` classiga ega `<a>` elementini qo'shing:

<figure><img src="../../.gitbook/assets/image (658).png" alt=""><figcaption></figcaption></figure>

```
<!-- A grey horizontal navbar that becomes vertical on small screens -->
<nav class="navbar navbar-expand-sm bg-light">

  <div class="container-fluid">
    <!-- Links -->
    <ul class="navbar-nav">
      <li class="nav-item">
        <a class="nav-link" href="#">Link 1</a>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="#">Link 2</a>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="#">Link 3</a>
      </li>
    </ul>
  </div>

</nav>
```

### Vertikal navbar

<figure><img src="../../.gitbook/assets/image (687).png" alt=""><figcaption></figcaption></figure>

`.navbar-expand-*`Har doim vertikal bo'ladigan navigatsiya panelini yaratish uchun sinfni olib tashlang:

```
<!-- A grey vertical navbar -->
<nav class="navbar bg-light">
  ...
</nav>
```

### Markazda turuvchi navbar

Navbarni markazga joylashtirish uchun `.justify-content-center` classini qo'shing:

<figure><img src="../../.gitbook/assets/image (541).png" alt=""><figcaption></figcaption></figure>

```
<nav class="navbar navbar-expand-sm bg-light justify-content-center">
  ...
</nav>
```

### Rangli navbar

<figure><img src="../../.gitbook/assets/image (717).png" alt=""><figcaption></figcaption></figure>

Navbarning orqafon rangini oʻzgartirish uchun har qanday `.bg-color` classidan foydalaning: (`.bg-primary`, `.bg-success`, `.bg-info`, `.bg-warning`, `.bg-danger`, `.bg-secondary`, `.bg-dark` va `.bg-light`)

**Maslahat:** `.navbar-dark` klassi bilan navbardagi barcha havolalarga oq matn rangini qo'shing yoki qora rangli matn qo'shish uchun .navbar-light classidan foydalaning.

```
<!-- Grey with black text -->
<nav class="navbar navbar-expand-sm bg-light navbar-light">
  <div class="container-fluid">
    <ul class="navbar-nav">
      <li class="nav-item">
        <a class="nav-link active" href="#">Active</a>
      </li>
     <li class="nav-item">
        <a class="nav-link" href="#">Link</a>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="#">Link</a>
      </li>
      <li class="nav-item">
        <a class="nav-link disabled" href="#">Disabled</a>
      </li>
    </ul>
  </div>
</nav>

<!-- Black background with white text -->
<nav class="navbar navbar-expand-sm bg-dark navbar-dark">...</nav>

<!-- Blue background with white text -->
<nav class="navbar navbar-expand-sm bg-primary navbar-dark">...</nav>
```

{% hint style="warning" %}
**Aktiv/o‘chirilgan holat**: Joriy havolani ajratib ko‘rsatish uchun `<a>` elementiga `.active` classini qo‘shing yoki havolani bosish mumkin emasligini ko‘rsatish uchun `.disabled` classini qo‘shing. &#x20;
{% endhint %}

### Brend/Logo

`.navbar-brand` classi sahifangizning brend/logotip/loyiha nomini ta'kidlash uchun ishlatiladi:

<figure><img src="../../.gitbook/assets/image (695).png" alt=""><figcaption></figcaption></figure>

```
<nav class="navbar navbar-expand-sm bg-dark navbar-dark">
  <div class="container-fluid">
    <a class="navbar-brand" href="#">Logo</a>
  </div>
</nav>
```

Rasklar bilan `.navbar-brand` classidan foydalanilganda, Bootstrap 5 rasmni avtomatik tarzda navbarga vertikal ravishda moslash uchun still beradi.

<figure><img src="../../.gitbook/assets/image (733).png" alt=""><figcaption></figcaption></figure>

```
<nav class="navbar navbar-expand-sm bg-dark navbar-dark">
  <div class="container-fluid">
    <a class="navbar-brand" href="#">
      <img src="logo.png" alt="Avatar Logo" style="width:40px;" class="rounded-pill"> 
    </a>
  </div>
</nav>
```

### Navbar Matn

<figure><img src="../../.gitbook/assets/image (690).png" alt=""><figcaption></figcaption></figure>

Navbar ichidagi havola bo'lmagan elementlarni vertikal joylashtirish uchun `.navbar-text` classidan foydalaning (mos keladigan padding va matn rangi bilan ta'minlaydi).

```
<nav class="navbar navbar-expand-sm bg-dark navbar-dark">
  <div class="container-fluid">
    <span class="navbar-text">Navbar text</span>
  </div>
</nav>
```

<figure><img src="../../.gitbook/assets/image (705).png" alt=""><figcaption></figcaption></figure>

Ko'pincha, ayniqsa kichik ekranlarda navbar havolalarini berkitib qo'yish va ularni tugma bosilganidagina ko'rsatish kerak bo'ladi.

Collapse-li navbar yaratish uchun `class="navbar-toggler"`, `data-bs-toggle="collapse"` va data-bs-target="#_thetarget_" bilan tugmadan foydalaning. Keyin navbar tarkibini (havolalar va h.k.) `class="collapse navbar-collapse"` bilan `<div>` elementiga, so'ngra tugmaning `data-bs-target`iga mos keladigan identifikatorga o'rang. "thetarget"

```
<nav class="navbar navbar-expand-sm bg-dark navbar-dark">
  <div class="container-fluid">
    <a class="navbar-brand" href="#">Logo</a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#collapsibleNavbar">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="collapsibleNavbar">
      <ul class="navbar-nav">
        <li class="nav-item">
          <a class="nav-link" href="#">Link</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">Link</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">Link</a>
        </li>
      </ul>
    </div>
  </div>
</nav>
```

{% hint style="warning" %}
**Maslahat:** Shuningdek `.navbar-expand-md` classini doimo navbar havolalarini yashirish va toggler tugmachasini koʻrsatish uchun olib tashlashingiz mumkin.
{% endhint %}

### Dropdownli navbar

<figure><img src="../../.gitbook/assets/image (715).png" alt=""><figcaption></figcaption></figure>

Navbarlarda dropdown ham bo'lishi mumkin:

```
<li class="nav-item dropdown">
  <a class="nav-link dropdown-toggle" href="#" role="button" data-bs-toggle="dropdown">Dropdown</a>
  <ul class="dropdown-menu">
    <li><a class="dropdown-item" href="#">Link</a></li>
    <li><a class="dropdown-item" href="#">Another link</a></li>
    <li><a class="dropdown-item" href="#">A third link</a></li>
  </ul>
</li>
```

### Navbar formalari va tugmalar

<figure><img src="../../.gitbook/assets/image (674).png" alt=""><figcaption></figcaption></figure>

Shuningdek, navbarga forma qo'shishingiz mumkin:

```
<nav class="navbar navbar-expand-sm navbar-dark bg-dark">
  <div class="container-fluid">
    <a class="navbar-brand" href="javascript:void(0)">Logo</a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#mynavbar">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="mynavbar">
      <ul class="navbar-nav me-auto">
        <li class="nav-item">
          <a class="nav-link" href="javascript:void(0)">Link</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="javascript:void(0)">Link</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="javascript:void(0)">Link</a>
        </li>
      </ul>
      <form class="d-flex">
        <input class="form-control me-2" type="text" placeholder="Search">
        <button class="btn btn-primary" type="button">Search</button>
      </form>
    </div>
  </div>
</nav>
```

### Fixed navbar

<figure><img src="../../.gitbook/assets/image (730).png" alt=""><figcaption></figcaption></figure>

Navbar sahifaning yuqori yoki pastki qismida ham joylashtirilishi mumkin.

Fixed navbar sahifani tepaga va pastga harkatlantirishdan qat'iy nazar ko'rinib turadi.

`.fixed-top` classi navbarni **yuqori** qismga joylashtiradi:

```
<nav class="navbar navbar-expand-sm bg-dark navbar-dark fixed-top">
  ...
</nav>
```

Navbar sahifaning **pastki** qismida joylashishi uchun `.fixed-bottom` classidan foydalaning:

<figure><img src="../../.gitbook/assets/image (694).png" alt=""><figcaption></figcaption></figure>

```
<nav class="navbar navbar-expand-sm bg-dark navbar-dark fixed-bottom">
  ...
</nav>
```

Sahifa harakatlanganda navbar sahifaning yuqori qismidan qimirlamasligi uchun `.sticky-top` klassidan foydalaning. **Eslatma:** Bu clas **IE11** va undan kichik versiyalarda ishlamaydi.

<figure><img src="../../.gitbook/assets/image (832).png" alt=""><figcaption></figcaption></figure>

```
<nav class="navbar navbar-expand-sm bg-dark navbar-dark sticky-top">
  ...
</nav>
```
