# BS5 Collapselar

### Oddiy collapse

Katta hajmdagi kontentni yashirish va ko'rsatishni xohlaganingizda collapselar yordam beradi:

![](<../../.gitbook/assets/image (556).png>)

```
<button data-bs-toggle="collapse" data-bs-target="#demo">Collapsible</button>

<div id="demo" class="collapse">
Lorem ipsum dolor text....
</div>
```

#### Misolni tushuntirish

`.collapse` classi collapse bo'ladigan elementni bildiradi; bu tugmani bosish orqali ko'rsatiladigan yoki yashiriladigan kontent hisoblanadi.

Colapseli tarkibni boshqarish (ko'rsatish/yashirish) uchun \<a> yoki \<tugma> elementiga `data-bs-toggle="collapse"` atributni  qo'shing. Keyin tugmani collapse tarkibiga ulash uchun `data-bs-target="#id"` atributini qo'shing.

**Eslatma:** \<a> elementlari uchun `href` atributi o‘rniga `data-bs-target` atributidan foydalanishingiz mumkin:

```
<a href="#demo" data-bs-toggle="collapse">Collapsible</a>

<div id="demo" class="collapse">
Lorem ipsum dolor text....
</div>
```

Collapseli kontent standart tarzda ko'rinmas holatda turadi. Biroq, uni standrat tarzda ko'rinadigan qilib qo'yish uchun `.show` classini qo'shishingiz mumkin:

```
<div id="demo" class="collapse show">
Lorem ipsum dolor text....
</div>
```

### Akkordion

<figure><img src="../../.gitbook/assets/image (682).png" alt=""><figcaption></figcaption></figure>

Quyidagi misolda card komponentini kengaytirish orqali oddiy akkordeon ko'rsatilgan.

**Eslatma:** Akkordion elementlardan biri ko'rsatilganda ota elementi ostidagi barcha akkordionli elementlarni yopiladigan qilish uchun `data-bs-parent` atributidan foydalaning.

```
<div id="accordion">

  <div class="card">
    <div class="card-header">
      <a class="btn" data-bs-toggle="collapse" href="#collapseOne">
        Collapsible Group Item #1
      </a>
    </div>
    <div id="collapseOne" class="collapse show" data-bs-parent="#accordion">
      <div class="card-body">
        Lorem ipsum..
      </div>
    </div>
  </div>

  <div class="card">
    <div class="card-header">
      <a class="collapsed btn" data-bs-toggle="collapse" href="#collapseTwo">
        Collapsible Group Item #2
      </a>
    </div>
    <div id="collapseTwo" class="collapse" data-bs-parent="#accordion">
      <div class="card-body">
        Lorem ipsum..
      </div>
    </div>
  </div>

  <div class="card">
    <div class="card-header">
      <a class="collapsed btn" data-bs-toggle="collapse" href="#collapseThree">
        Collapsible Group Item #3
      </a>
    </div>
    <div id="collapseThree" class="collapse" data-bs-parent="#accordion">
      <div class="card-body">
        Lorem ipsum..
      </div>
    </div>
  </div>

</div>
```
