# BS5 Popover

### Popoverlar

Popover komponenti tooltiplarga o'xshaydi; bu foydalanuvchi elementni bosganida paydo bo'ladigan oyna. Farqi shundaki, popover ko'proq narsani o'z ichiga olishi mumkin.

![](<../../.gitbook/assets/image (718).png>)

### Popoverni qanday yaratish kerak

Popover yaratish uchun elementga `data-bs-toggle="popover"` atributini qo'shing.

Popoverning sarlavha matnini belgilash uchun `title` atributidan foydalaning va popover ichida ko'rsatilishi kerak bo'lgan matnni berish uchun `data-bs-content` atributidan foydalaning:

```
<button type="button" class="btn btn-primary" data-bs-toggle="popover" title="Popover Header" data-bs-content="Some content inside the popover">Toggle popover</button>
```

**Eslatma:** Popoverlar ishlashi uchun JavaScript bilan ishga tushirilishi kerak.

Quyidagi kod hujjatdagi barcha popoverlarni ishga tushiradi:

```
<script>
var popoverTriggerList = [].slice.call(document.querySelectorAll('[data-bs-toggle="popover"]'))
var popoverList = popoverTriggerList.map(function (popoverTriggerEl) {
  return new bootstrap.Popover(popoverTriggerEl)
})
</script>
```

### Popoverlar joylashuvi

Standrat tarzda popover elementning o'ng tomonida paydo bo'ladi.

Popoverni elementning yuqori, pastki, chap yoki o'ng tomonida ko'rsatish uchun `data-bs-placement` atributidan foydalaning:

```
<a href="#" title="Header" data-bs-toggle="popover" data-bs-placement="top" data-content="Content">Top</a>
<a href="#" title="Header" data-bs-toggle="popover" data-bs-placement="bottom" data-content="Content">Bottom</a>
<a href="#" title="Header" data-bs-toggle="popover" data-bs-placement="left" data-content="Content">Left</a>
<a href="#" title="Header" data-bs-toggle="popover" data-bs-placement="right" data-content="Content">Right</a>
```

{% hint style="warning" %}
**Eslatma:** Agar yetarlicha joy mavjud bo'lmasa joylashtirish atributlari to'g'ri ishlamaydi. Misol uchun: agar popoverni sahifaning yuqori qismida ko'rsatish uchun yuqoriga joylashuvidan foydalansangiz (ko'rsatish uchun joy bo'lmagan qismda), popover element yuqorisida emas uning ostida yoki o'ng tomonida (qayerda bo'sh joy bo'lsa) ko'rsatiladi.
{% endhint %}

### Popoverlarni yopish

Standart tarzda, elementni qayta bosganingizda popover yopiladi. Biroq, popoverni sahifaning istalgan qismini bosganda yopiladigan qilish uchun `data-bs-trigger="focus"` atributidan foydalanishingiz kerak:

```
<a href="#" title="Dismissible popover" data-bs-toggle="popover" data-bs-trigger="focus" data-bs-content="Click anywhere in the document to close this popover">Click me</a>
```

### Hoverli popover

**Maslahat**: Agar sichqoncha koʻrsatkichini element ustiga olib borganingizda popover oynasi koʻrsatilishini istasangiz,  `data-bs-trigger` atributida `hover` qiymatidan foydalaning:

```
<a href="#" title="Header" data-bs-toggle="popover" data-bs-trigger="hover" data-bs-content="Popover text">Hover over me</a>
```
