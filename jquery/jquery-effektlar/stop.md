# stop()

## jQuery da animatsiyalarni to'xtatish <a href="#jquery-da-animatsiyalarni-toxtatish" id="jquery-da-animatsiyalarni-toxtatish"></a>

jQuery stop() metodi animatsiyalarni yoki effektlarni tugashidan oldin to'xtatish uchun ishlatiladi.

![](<../../.gitbook/assets/image (192).png>)     ![](<../../.gitbook/assets/image (92).png>)

<figure><img src="../../.gitbook/assets/image (93).png" alt=""><figcaption></figcaption></figure>

### **Misollar**

[<mark style="color:green;">jQuery.stop()</mark>](https://www.w3schools.com/jquery/tryit.asp?filename=tryjquery\_stop\_slide) slaydi\
jQuery stop() metodini ko'rsatib berish.

[<mark style="color:green;">jQuery.stop() animatsiya (parametrlar bilan)</mark>](https://www.w3schools.com/jquery/tryit.asp?filename=tryjquery\_stop\_params)\
jQuery stop() metodini ko'rsatib berish.

### jQuery stop() metodi <a href="#jquery-stop-metodi" id="jquery-stop-metodi"></a>

jQueryning `stop()` metodi animatsiyalarni yoki effektlarini tugashidan avval to'xtatish uchun ishlatiladi.

`stop()` metodi barcha slide, fade va maxsus animatsiyalarni o'z ichiga olgan jQuery effekt funksiyalari uchun ishlaydi.

**Sintaksis**

```
$(selector).stop(stopAll,goToEnd);
```

Ixtiyor hisoblangan `stopAll` parametri animatsiya navbatini ham olib tashlash kerak yoki kerak emasligini belgilaydi. Bu parametr standart tarzda `false` bo'ladi, ya'ni faqat aktiv animatsiyalar to'xtatiladi, bu esa navbatdagi animatsiyalarni keyinchalik bajarishga imkon beradi.

Ixtiyoriy hisoblangan `goToEnd` parametri joriy animatsiyani tezda yakunlashni yoki yakunlamaslikni belgilaydi. Bu parametr standart tarzda `false` bo'ladi.

By default, `stop()` metodi tanlangan elementda bajarilayotgan joriy animatsiyani to'xtatadi.

Quyidagi misolda `stop()` metodi parametrlarsiz ko'rsatib berilgan:

```
$("#stop").click(function(){
  $("#panel").stop();
}); 
```
