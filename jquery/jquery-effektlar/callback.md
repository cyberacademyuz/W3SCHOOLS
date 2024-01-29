# Callback

Callback funksiya joriy effekt 100% tugagandan so'ng ishga tushadi.

### jQuery Callback funksiyalari <a href="#jquery-callback-funksiyalari-2" id="jquery-callback-funksiyalari-2"></a>

JavaScript statement lari qatorma-qator bajariladi. Biroq, effektlar bilan, keyingi qatordagi kod, birinchi qatordagi kod tugamasidan avval ham ishlashi mumkin. Bu hatoliklarni yuzaga keltiradi.

Buni oldini olish uchun Callback funksiya yaratiladi.

Callback funksiya joriy effekt tugagandan so'ng ishga tushadi.

Odatiy syntaksis: _**$(selector).hide(speed,callback);**_

#### Misollar <a href="#misollar" id="misollar"></a>

Quyidagi misolda, hide effekti bajarilib bo'lgandan keyin ishga tushadigan callback funksiyasi keltirilgan:

```
$("button").click(function(){
  $("p").hide("slow", function(){
    alert("The paragraph is now hidden");
  });
}); 
```

Quyidagi misolda, hide effekti bajarilib bo'lmasidanoq ishga tushadigan funksiya keltirilgan:

```
$("button").click(function(){
  $("p").hide(1000);
  alert("The paragraph is now hidden");
}); 
```
