# BS5 Toast

### Tostlar

Tost komponenti alert oynasiga o'xshaydi, u biror narsa sodir bo'lganda (ya'ni, foydalanuvchi tugmani bosganda, forma yuborganida va hokazo) bir necha soniya davomida ko'rsatiladi.

![](<../../.gitbook/assets/image (670).png>)

### Tostni qanday yaratish kerak

Tost yaratish uchun `.toast` classidan foydalaning va uning ichkiga `.toast-header` va .toast-body ni qo'shing.

**Eslatma:** Tostlar standart tarzda ko'rinmay turadi. Agar uni ko'rsatishni istasangiz, `.show` classidan foydalaning . Uni yopish uchun `<button>` elementidan foydalaning va ushbu elementga `data-bs-dismiss="toast"`ni  qo'shing:

```
<div class="toast show">
  <div class="toast-header">
    Toast Header
    <button type="button" class="btn-close" data-bs-dismiss="toast"></button>
  </div>
  <div class="toast-body">
    Some text inside the toast body
  </div>
</div>
```

### Tostni ochish

Tugmani bosish orqali toastni ko'rsatish uchun uni JavaScript bilan ishga tushirishingiz kerak: kerakli elementni tanlang va `tost()` metodini chaqiring.

Tugmani bosganingizda quyidagi kod hujjatdagi barcha "tostlar" ni ko'rsatadi:

```
<script>
document.getElementById("toastbtn").onclick = function() {
  var toastElList = [].slice.call(document.querySelectorAll('.toast'))
  var toastList = toastElList.map(function(toastEl) {
    return new bootstrap.Toast(toastEl)
  })
  toastList.forEach(toast => toast.show())
}
</script>
```
