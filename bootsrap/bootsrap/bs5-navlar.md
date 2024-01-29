# BS5 Navlar

### Nav menyulari

![](<../../.gitbook/assets/image (732).png>)

Agar oddiy gorizontal menyu yaratmoqchi bo'lsangiz, `<ul>` elementiga `.nav` classini, keyin har bir `<li>` elementiga  `.nav-item` va ularning havolalariga `.nav-link` classini qo'shing:

```
<ul class="nav">
  <li class="nav-item">
    <a class="nav-link" href="#">Link</a>
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
```

### Surilgan nav

<figure><img src="../../.gitbook/assets/image (693).png" alt=""><figcaption></figcaption></figure>

Navni markazga olib kelish uchun `.justify-content-center` classini va navni o'ngga surish uchun `.justify-content-end` classini qo'shing.

```
<!-- Centered nav -->
<ul class="nav justify-content-center">

<!-- Right-aligned nav -->
<ul class="nav justify-content-end">
```

### Vertikal nav

![](<../../.gitbook/assets/image (663).png>)

Vertikal nav yaratish uchun `.flex-column` classini qo'shing:

```
<ul class="nav flex-column">
```

### Tablar

<figure><img src="../../.gitbook/assets/image (558).png" alt=""><figcaption></figcaption></figure>

Nav menyusini `.nav-tabs` classi yordamida navigatsiya tablariga aylantiring. `.active` classini aktiv/joriy havolaga qo'shing. Tablarni almashtirishni istasangiz, ushbu sahifadagi oxirgi misolga qarang.

```
<ul class="nav nav-tabs">
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
```

### Tabletkalar

![](<../../.gitbook/assets/image (671).png>)

Nav menyusini `.nav-pills` classi bilan navigatsiya tabletkalariga aylantiring. Agar tabletkalarni almashtirishni istasangiz, ushbu sahifadagi oxirgi misolga qarang.

```
<ul class="nav nav-pills">
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
```

### Asoslangan tablar / tabletkalar

Tablarni/tabletkalarni `.nav-justified` classi yordamida asoslang (teng kenglik):

<figure><img src="../../.gitbook/assets/image (542).png" alt=""><figcaption></figcaption></figure>

```
<ul class="nav nav-pills nav-justified">..</ul>
<ul class="nav nav-tabs nav-justified">..</ul>
```

### Dropdownli tabletkalar

![](<../../.gitbook/assets/image (727).png>)

```
<ul class="nav nav-pills">
  <li class="nav-item">
    <a class="nav-link active" href="#">Active</a>
  </li>
  <li class="nav-item dropdown">
    <a class="nav-link dropdown-toggle" data-bs-toggle="dropdown" href="#">Dropdown</a>
    <ul class="dropdown-menu">
      <li><a class="dropdown-item" href="#">Link 1</a></li>
      <li><a class="dropdown-item" href="#">Link 2</a></li>
      <li><a class="dropdown-item" href="#">Link 3</a></li>
    </ul>
  </li>
  <li class="nav-item">
    <a class="nav-link" href="#">Link</a>
  </li>
  <li class="nav-item">
    <a class="nav-link disabled" href="#">Disabled</a>
  </li>
</ul>
```

### Dropdownli tablar

<figure><img src="../../.gitbook/assets/image (668).png" alt=""><figcaption></figcaption></figure>

```
<ul class="nav nav-tabs">
  <li class="nav-item">
    <a class="nav-link active" href="#">Active</a>
  </li>
  <li class="nav-item dropdown">
    <a class="nav-link dropdown-toggle" data-bs-toggle="dropdown" href="#">Dropdown</a>
    <ul class="dropdown-menu">
      <li><a class="dropdown-item" href="#">Link 1</a></li>
      <li><a class="dropdown-item" href="#">Link 2</a></li>
      <li><a class="dropdown-item" href="#">Link 3</a></li>
    </ul>
  </li>
  <li class="nav-item">
    <a class="nav-link" href="#">Link</a>
  </li>
  <li class="nav-item">
    <a class="nav-link disabled" href="#">Disabled</a>
  </li>
</ul>
```

### Oʻzgaruvchan / Dinamik tablar

<figure><img src="../../.gitbook/assets/image (729).png" alt=""><figcaption></figcaption></figure>

Tablarni almashtirish imkoniyatini yaratish uchun har bir havolaga `data-toggle="tab"` atributini qo'shing. Keyin har bir tab uchun unikal identifikatorli `.tab-pane` classini qo'shing va ularni `.tab-content` classi bilan `<div>` elementiga oling.

Agar ularni bosganingizda tablarning sekin yo'q bo'lishini istasangiz,`.tab-pane`ga `.fade` classini  qoʻshing:

```
<!-- Nav tabs -->
<ul class="nav nav-tabs">
  <li class="nav-item">
    <a class="nav-link active" data-bs-toggle="tab" href="#home">Home</a>
  </li>
  <li class="nav-item">
    <a class="nav-link" data-bs-toggle="tab" href="#menu1">Menu 1</a>
  </li>
  <li class="nav-item">
    <a class="nav-link" data-bs-toggle="tab" href="#menu2">Menu 2</a>
  </li>
</ul>

<!-- Tab panes -->
<div class="tab-content">
  <div class="tab-pane container active" id="home">...</div>
  <div class="tab-pane container fade" id="menu1">...</div>
  <div class="tab-pane container fade" id="menu2">...</div>
</div>
```

### O'zgaruvchan/dinamik tabletkalar

<figure><img src="../../.gitbook/assets/image (546).png" alt=""><figcaption></figcaption></figure>

Xuddi shu kod tabletkalarga nisbatan qo'llaniladi; data-toggle atributini `data-toggle="pill"` ga o'zgartiring:

```
<!-- Nav pills -->
<ul class="nav nav-pills">
  <li class="nav-item">
    <a class="nav-link active" data-bs-toggle="pill" href="#home">Home</a>
  </li>
  <li class="nav-item">
    <a class="nav-link" data-bs-toggle="pill" href="#menu1">Menu 1</a>
  </li>
  <li class="nav-item">
    <a class="nav-link" data-bs-toggle="pill" href="#menu2">Menu 2</a>
  </li>
</ul>

<!-- Tab panes -->
<div class="tab-content">
  <div class="tab-pane container active" id="home">...</div>
  <div class="tab-pane container fade" id="menu1">...</div>
  <div class="tab-pane container fade" id="menu2">...</div>
</div>
```
