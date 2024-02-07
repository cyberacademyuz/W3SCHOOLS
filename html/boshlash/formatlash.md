# Formatlash

HTML maxsus ma'noga ega matnni ifodalash uchun bir nechta elementlarni o'z ichiga oladi.

## HTMLdagi formatlash elementlari

Formatlash elementlari maxsus turdagi matnlarni ko'rsatish uchun mo'ljallangan:

* <mark style="color:red;">`<b>`</mark> -  Qalin matn
* <mark style="color:red;">`<strong>`</mark> - Muhim matn
* <mark style="color:red;">`<i>`</mark> - Kursiv (_Italic_) matn
* <mark style="color:red;">`<em>`</mark> - Urg'u berilgan matn
* <mark style="color:red;">`<mark>`</mark> - Belgilangan matn
* <mark style="color:red;">`<small>`</mark> - kichik matn
* <mark style="color:red;">`<del>`</mark> - O'chirilgan matn
* <mark style="color:red;">`<ins>`</mark> - Kiritilgan matn
* <mark style="color:red;">`<sub>`</mark> - Subscript (ostki) matn
* <mark style="color:red;">`<sup>`</mark> - Superscript (ustki) matn

### HTMLdagi \<b> va \<strong> elementlari

HTMLning `<b>` elementi qo'chimcha ahamiyatga ega bo'lmagan qalin matnni ifodalaydi.

```html
<b>Bu qalin matn</b>
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_formatting_b" %}

HTMLning <mark style="color:red;">`<strong>`</mark> elementi muhim ahamiyatga ega matnni ifodalaydi. Undagi matn odatda qalin qilib ko'rsatiladi.

```html
<strong>Bu muhim matn!</strong>
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_formatting_strong" %}

## <mark style="color:green;">HTMLdagi</mark> <mark style="color:green;"></mark><mark style="color:green;">`<i>`</mark> <mark style="color:green;"></mark><mark style="color:green;">va</mark> <mark style="color:green;"></mark><mark style="color:green;">`<em>`</mark> <mark style="color:green;"></mark><mark style="color:green;">elementlari</mark>

HTMLning <mark style="color:red;">`<i>`</mark> elementi matnning bir qismini kursiv holatda ko'rsatadi.

**Maslahat:** <mark style="color:red;">`<i>`</mark> elementidan ko'pincha texnik atama, boshqa tildagi ibora, biror fikrni ko'rsatish uchun foydalaniladi.

```html
<i>Bu matn kursiz</i>
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_formatting_i" %}

HTMLning <mark style="color:red;">`<em>`</mark> elementi urg'u berilgan matnni ifodalaydi. Undagi matn odatda kursiv ko'rinishda bo'ladi.&#x20;

**Maslahat:** Ekranni o'qin beruvchi dasturlar \<em> bilan berilgan matnlarni urg'u bilan talaffuz qiladi.

```html
<em> Bu urg'u berilgan matn </em>
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_formatting_em" %}

## <mark style="color:green;">HTMLning</mark> <mark style="color:green;"></mark><mark style="color:green;">`<small>`</mark> <mark style="color:green;"></mark><mark style="color:green;">elementi</mark>

HTMLning <mark style="color:red;">`<small>`</mark> elementi kichik matnlarni ifodalaydi.

```html
<small> Bu bir kichikroq matn <small>
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_formatting_small" %}

## <mark style="color:green;">HTMLning</mark> <mark style="color:green;"></mark><mark style="color:green;">`<mark>`</mark> <mark style="color:green;"></mark><mark style="color:green;">elementi</mark>

HTMLning <mark style="color:red;">`<mark>`</mark> elementi belgilanishi yoki takidlanishi kerak bo'lgan matnni ifodalaydi.

```html
<p>Bugun <mark> sut </mark> sotib olishni unutma</p>
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_formatting_mark" %}

## <mark style="color:green;">HTMLning \<del> elementi</mark>

HTMLning <mark style="color:red;">`<del>`</mark> elementi sahifadan o'chirilgan matnni ifodalaydi. Brauzerlar avtomatik tarzda o'chirilgan matnning o'rtasiga chiziq tortadi.

```html
<p> Mening sevimli rangim <del> ko'k </del> qizil. <p>
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_formatting_del" %}

## <mark style="color:green;">HTMLdagi</mark> <mark style="color:green;"></mark><mark style="color:green;">`<ins>`</mark> <mark style="color:green;"></mark><mark style="color:green;">elementi</mark>

HTMLning <mark style="color:red;">`<ins>`</mark> elementi sahifaga kiritilgan matnni ifodalaydi. Brauzerlar odatda bu matnning tagiga chiziq chizishadi.

```html
<p> Mening sevimli rangim <del> ko'k </del> <ins> qizil </ins>. <p>
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_formatting_del_ins" %}

## HTMLdagi \<sub> elementi

HTMLning <mark style="color:red;">`<sub>`</mark> elementi ostki (ₛᵤₛ꜀ᵣᵢₚₜ) mattni ifodalaydi. Subscript matn, oddiy qatorning yarim baravar pastida ko'rinadi va ba'zan kichikroq shriftda bo'ladi. Subscript matnlar H₂O kabi kimyoviy formulalarni yozishda foydalaniladi.

```html
<p>Bu <sub>ostki</sub> matn.</p>
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_formatting_sub" %}

## <mark style="color:green;">HTMLdagi</mark> <mark style="color:green;"></mark><mark style="color:green;">`<sup>`</mark> <mark style="color:green;"></mark><mark style="color:green;">elementi</mark>

HTMLning \<sup> elementi ustki (ˢᵘᵖᵉʳˢᶜʳᶦᵖᵗ)  matnni ifodalaydi. Superscript matn, oddiy matnning yarim baravar tepasida ko'rinadi va ba'zan kichikroq shriftda bo'ladi. Superscript matn odatda 2² kabi yozilishi kerak bo'lgan matnlarda ishlatiladi.

```html
<p>Bu <sup>ustki</sup> matn.</p>
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_formatting_sup" %}

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

