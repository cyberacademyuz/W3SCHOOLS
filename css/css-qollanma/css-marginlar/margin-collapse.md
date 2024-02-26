# Margin collapse

Ba'zida ikkita marginlar bitta marginga collapse mumkin

## <mark style="color:green;">Margin Collapse</mark> <a href="#margin-collapse" id="margin-collapse"></a>

Elementlarning yuqori va pastki marginlari ba'zan ikkita marginning kattaroq marginiga birikib ketadi.

Chap va o'ng marginlarda bunday bo'lmaydi! Faqat tepa va pastki qismlardagi marginlarda sodir bo'ladi!

Quyidagi misolga qarang:

{% tabs %}
{% tab title="CSS" %}
Margin collapse qanday bo'ladi:

```css
h1 {
  margin: 0 0 50px 0;
}

h2 {
  margin: 20px 0 0 0;
}
```

{% embed url="https://www.w3schools.com/css/tryit.asp?filename=trycss_margin_collapse" %}
{% endtab %}
{% endtabs %}

Yuqoridagi misolda <mark style="color:red;">`<h1>`</mark> elementining pastki margini 50px qilingan va <mark style="color:red;">`<h2>`</mark> elementning tepa qismidagi margini 20px qilingan.

Mantiqan olganda <mark style="color:red;">`<h1>`</mark> va <mark style="color:red;">`<h2>`</mark> orasidagi vertikal marginlar jami 70px (50px + 20px) bo'lishi kerak. Ammo margin collapse tufayli margin 50px ni tashkil qiladi.
