# Margin collapse

Ba'zida ikkita marginlar bitta marginga collapse mumkin

### Margin Collapse <a href="#margin-collapse" id="margin-collapse"></a>

Elementlarning yuqori va pastki marginlari ba'zan ikkita marginning kattaroq marginiga birikib ketadi.

Chap va o'ng marginlarda bunday bo'lmaydi! Faqat tepa va pastki qismlardagi marginlarda sodir bo'ladi!

Quyidagi misolga qarang:

{% code title="Margin collapse qanday bo'ladi:" %}
```
h1 {
  margin: 0 0 50px 0;
}

h2 {
  margin: 20px 0 0 0;
}
```
{% endcode %}

Yuqoridagi misolda `<h1>` elementining pastki margini 50px qilingan va `<h2>` elementning tepa qismidagi margini 20px qilingan.

Mantiqan olganda `<h1>` va `<h2>` orasidagi vertikal marginlar jami 70px (50px + 20px) bo'lishi kerak. Ammo margin collapse tufayli margin 50px ni tashkil qiladi.
