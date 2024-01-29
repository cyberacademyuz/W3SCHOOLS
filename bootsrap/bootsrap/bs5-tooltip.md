# BS5 Tooltip

### Tooltiplar

Tooltip komponenti foydalanuvchi sichqoncha koʻrsatkichini element ustida olib kelganda paydo boʻladigan kichik oyna:

![](<../../.gitbook/assets/image (725).png>)

### Tooltipni qanday yaratish kerak

Tooltip yaratish uchun elementga `data-bs-toggle="tooltip"` atributini qo'shing.

Tooltip ichida ko'rsatiladigan matnni belgilash uchun `title` atributidan foydalaning:

```
<button type="button" class="btn btn-primary" data-bs-toggle="tooltip" title="Hooray!">Hover over me!</button>
```

**Eslatma:** Tooltip ishlashi uchun JavaScript bilan ishga tushirilishi kerak.

Quyidagi kod hujjatdagi barcha tooltiplarni ishga tushiradi:

```
<script>
var tooltipTriggerList = [].slice.call(document.querySelectorAll('[data-bs-toggle="tooltip"]'))
var tooltipList = tooltipTriggerList.map(function (tooltipTriggerEl) {
  return new bootstrap.Tooltip(tooltipTriggerEl)
})
</script>
```

### Tooltip joylashuvi

Standart tarzda tooltip elementning tepasida paydo bo'ladi.

Tooltiplarni elementning yuqori, pastki, chap yoki o'ng tomonida ko'rsatish uchun `data-bs-placement` atributidan foydalaning:

```
<a href="#" data-bs-toggle="tooltip" data-bs-placement="top" title="Hooray!">Hover</a>
<a href="#" data-bs-toggle="tooltip" data-bs-placement="bottom" title="Hooray!">Hover</a>
<a href="#" data-bs-toggle="tooltip" data-bs-placement="left" title="Hooray!">Hover</a>
<a href="#" data-bs-toggle="tooltip" data-bs-placement="right" title="Hooray!">Hover</a>
```
