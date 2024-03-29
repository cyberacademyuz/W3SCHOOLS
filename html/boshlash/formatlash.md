# Formatlash

HTMLda, o'ziga xos ma'noga ega matnni ifodalash uchun bir nechta elementlarga mavjud.

## <mark style="color:green;">HTMLning formatlash elementlari</mark>

Formatlash elementlari o'ziga xos turdagi matnlarni ko'rsatish uchun mo'ljallangan:

* <mark style="color:red;">`<b>`</mark> - Qalin matn
* <mark style="color:red;">`<strong>`</mark> - Muhim matn
* <mark style="color:red;">`<i>`</mark> - Kursiv (_Italic_) matn
* <mark style="color:red;">`<em>`</mark> - Urg'u berilgan matn
* <mark style="color:red;">`<mark>`</mark> - Belgilangan matn
* <mark style="color:red;">`<small>`</mark> - kichik matn
* <mark style="color:red;">`<del>`</mark> - O'chirilgan matn
* <mark style="color:red;">`<ins>`</mark> - Kiritilgan matn
* <mark style="color:red;">`<sub>`</mark> - Subscript (ostki) matn
* <mark style="color:red;">`<sup>`</mark> - Superscript (ustki) matn

### <mark style="color:green;">HTMLdagi</mark> <mark style="color:green;">`<b>`</mark> <mark style="color:green;">va</mark> <mark style="color:green;">`<strong>`</mark> <mark style="color:green;">elementlari</mark>

HTMLning <mark style="color:red;">`<b>`</mark> elementi muhim ahamiyatga ega bo'lmagan qalin matnni ifodalaydi.

{% tabs %}
{% tab title="HTML" %}
```html
<b>Bu qalin matn</b>
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_formatting_b" %}
{% endtab %}
{% endtabs %}

HTMLning <mark style="color:red;">`<strong>`</mark> elementi muhim ahamiyatga ega bo'lgan matnni ifodalaydi. Undagi matn ham odatda qalin qilib ko'rsatiladi.

{% tabs %}
{% tab title="HTML" %}
```html
<strong>Bu muhim matn!</strong>
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_formatting_strong" %}
{% endtab %}
{% endtabs %}

## <mark style="color:green;">HTMLning</mark> <mark style="color:green;">`<i>`</mark> <mark style="color:green;">va</mark> <mark style="color:green;">`<em>`</mark> <mark style="color:green;">elementlari</mark>

HTMLning <mark style="color:red;">`<i>`</mark> elementi matnning bir qismini kursiv holatda ko'rsatadi.

**Maslahat:** <mark style="color:red;">`<i>`</mark> elementidan ko'pincha texnik atama, boshqa tildagi ibora, biror fikrni ko'rsatish uchun foydalaniladi.

{% tabs %}
{% tab title="HTML" %}
```html
<i>Bu matn kursiz</i>
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_formatting_i" %}
{% endtab %}
{% endtabs %}

HTMLning <mark style="color:red;">`<em>`</mark> elementi urg'u berilgan matnni ifodalaydi. Undagi matn odatda kursiv ko'rinishda bo'ladi.

**Maslahat:** Ekranni o'qib beruvchi dasturlar <mark style="color:red;">`<em>`</mark> bilan berilgan matnlarni urg'u bilan talaffuz qiladi.

{% tabs %}
{% tab title="HTML" %}
```html
<em> Bu urg'u berilgan matn </em>
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_formatting_em" %}
{% endtab %}
{% endtabs %}

## <mark style="color:green;">HTMLning</mark> <mark style="color:green;">`<small>`</mark> <mark style="color:green;">elementi</mark>

HTMLning <mark style="color:red;">`<small>`</mark> elementi kichik matnlarni ifodalaydi.

{% tabs %}
{% tab title="HTML" %}
```html
<small> Bu bir kichikroq matn <small>
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_formatting_small" %}
{% endtab %}
{% endtabs %}

## <mark style="color:green;">HTMLning</mark> <mark style="color:green;">`<mark>`</mark> <mark style="color:green;">elementi</mark>

HTMLning <mark style="color:red;">`<mark>`</mark> elementi belgilanishi yoki takidlanishi kerak bo'lgan matnni ifodalaydi.

{% tabs %}
{% tab title="HTML" %}
```html
<p>Bugun <mark> sut </mark> sotib olishni unutma</p>
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_formatting_mark" %}
{% endtab %}
{% endtabs %}

## <mark style="color:green;">HTMLning</mark> <mark style="color:green;">`<del>`</mark> <mark style="color:green;">elementi</mark>

HTMLning <mark style="color:red;">`<del>`</mark> elementi sahifadan o'chirilgan matnni ifodalaydi. Brauzerlar avtomatik tarzda o'chirilgan matnning o'rtasiga chiziq chizadi.

{% tabs %}
{% tab title="HTML" %}
```html
<p> Mening sevimli rangim <del> ko'k </del> qizil. <p>
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_formatting_del" %}
{% endtab %}
{% endtabs %}

## <mark style="color:green;">HTMLning</mark> <mark style="color:green;">`<ins>`</mark> <mark style="color:green;">elementi</mark>

HTMLning <mark style="color:red;">`<ins>`</mark> elementi sahifaga kiritilgan matnni ifodalaydi. Brauzerlar odatda bu matnning tagiga chiziq chizishadi.

{% tabs %}
{% tab title="HTML" %}
```html
<p> Mening sevimli rangim <del> ko'k </del> <ins> qizil </ins>. <p>
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_formatting_del_ins" %}
{% endtab %}
{% endtabs %}

## <mark style="color:green;">HTMLning</mark> <mark style="color:green;">`<sub>`</mark> <mark style="color:green;">elementi</mark>

HTMLning <mark style="color:red;">`<sub>`</mark> elementi ostki (ₛᵤₛ꜀ᵣᵢₚₜ) mattni ifodalaydi. Subscript matn, oddiy qatorning yarim baravar pastida ko'rinadi va ba'zan kichikroq shriftda bo'ladi. Subscript matnlar H₂O kabi kimyoviy formulalarni yozishda foydalaniladi.

{% tabs %}
{% tab title="HTML" %}
```html
<p>Bu <sub>ostki</sub> matn.</p>
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_formatting_sub" %}
{% endtab %}
{% endtabs %}

## <mark style="color:green;">HTMLdagi</mark> <mark style="color:green;">`<sup>`</mark> <mark style="color:green;">elementi</mark>

HTMLning <mark style="color:red;">`<sup>`</mark> elementi ustki (ˢᵘᵖᵉʳˢᶜʳᶦᵖᵗ) matnni ifodalaydi. Superscript matn, oddiy matnning yarim baravar tepasida ko'rinadi va ba'zan kichikroq shriftda bo'ladi. Superscript matn odatda 2² kabi yozilishi kerak bo'lgan matnlarda ishlatiladi.

{% tabs %}
{% tab title="HTML" %}
```html
<p>Bu <sup>ustki</sup> matn.</p>
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_formatting_sup" %}
{% endtab %}
{% endtabs %}

| Teg       | Tavsif                                        |
| --------- | --------------------------------------------- |
| \<b>      | Qalin matnni ifodalash                        |
| \<em>     | Urg'u berilgan matnni ifodalash               |
| \<i>      | Matnning bir qismini kursiv qilish            |
| \<small>  | Kichikroq matnni ifodalash                    |
| \<strong> | Muhim matnni ifodalash                        |
| \<sub>    | Subscript matnni ifodalash                    |
| \<sup>    | Superscript matnni ifodalash                  |
| \<ins>    | Kiritilgan matnni ifodalash                   |
| \<del>    | O'chirilgan matnni ifodalash                  |
| \<mark>   | Belgilangan yoki takidlangan matnni ifodalash |
