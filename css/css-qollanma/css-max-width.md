# CSS Max-width

### Width, max-width va margin: auto; dan foydalanish <a href="#width-max-width-va-margin-auto-dan-foydalanish" id="width-max-width-va-margin-auto-dan-foydalanish"></a>

Avvalgi bo'limda aytilganidek blok elementlar butun kenglikni egallaydi (imkon qadar chapga va o'ngga cho'ziladi)

Blok elementga `width` berish konteynerining ohirigacha cho'zilishini oldini oladi. Keyin elementni konteynerning ichida gorizontal tarzda o'rtaga olib kelish uchun marginlarini auto qilishingiz mumkin. Shunda element berilgan kenglikni egallaydi va qolgan bo'sh joylar ikki margin o'rtasida teng taqsimlanadi.

<figure><img src="../../.gitbook/assets/image (500).png" alt=""><figcaption></figcaption></figure>

**Note:** Yuqoridagi vaziyatda muammo brauzer ekrani kichrayganda yuzaga keladi va brauzer skroller qo'shadi.

O'rniga max-width ishlatilsa brauzerning bu holatni ushlashi ancha yaxshilanadi. Bu kichkina ekranli qurilmalarga sayt yaratayotganda ancha asqotadi.

<figure><img src="../../.gitbook/assets/image (402).png" alt=""><figcaption></figcaption></figure>

**Tip:** Yuqoridagi ikkita div oʻrtasidagi farqni koʻrish uchun brauzer oynasining oʻlchamini 500px dan kamroq qilib oʻzgartiring!

Mana bu kodda yuqoridagi ikkita divni misoli keltiriladi:

```
div.ex1 {
  width: 500px;
  margin: auto;
  border: 3px solid #73AD21;
}

div.ex2 {
  max-width: 500px;
  margin: auto;
  border: 3px solid #73AD21;
}
```
