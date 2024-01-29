# CSS Inline-block

`display: inline;` bilan solishtirganda `display: inline-block;` ning asosiy farqi shundaki u elementdagi uzunlik va balandliklarni o'zgartirishga imkon beradi.

Bundan tashqari, `display: inline-block;` da tepa va pastki margin/paddinglar ishlaydi, lekin `display: inline;` da esa ishlamaydi.

`display: block;` bilan solishtirilganda, `display: inline-block` qilingan element butun qatorni egallamaydi, balki boshqa elementning yonida turadi.

Quyidagi misolda `display:inline`, `display:block` va `display: inline-block` lar o'rtasidagi farqni ko’rsatilgan

```
span.a {
  display: inline;  /* the default for span */
  width: 100px;
  height: 100px;
  padding: 5px;
  border: 1px solid blue; 
  background-color: yellow; 
}

span.b {
  display: inline-block;
  width: 100px;
  height: 100px;
  padding: 5px;
  border: 1px solid blue; 
  background-color: yellow; 
}

span.c {
  display: block;
  width: 100px;
  height: 100px;
  padding: 5px;
  border: 1px solid blue; 
  background-color: yellow; 
}
```

### Inline-block dan foydalangan holda navigatsiya menyusini yasash <a href="#inline-block-dan-foydalangan-holda-navigatsiya-menyusini-yasash" id="inline-block-dan-foydalangan-holda-navigatsiya-menyusini-yasash"></a>

`display: inline-block` ni yana bir eng ko’p ishlatiladigan holat bu elementlarni vertikal emas, balki gorizontal tarzda ko'rsatish. Quyidagi misolda navigatsiya menyusini `display: inline-block` asosida yaratganmiz:

```
.nav {
  background-color: yellow; 
  list-style-type: none;
  text-align: center; 
  padding: 0;
  margin: 0;
}

.nav li {
  display: inline-block;
  font-size: 20px;
  padding: 20px;
}
```
