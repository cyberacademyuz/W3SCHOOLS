# AJAX ASP

AJAX ko'proq interaktiv ilovalar yaratish uchun ishlatiladi.

### AJAX ASPga misol

Quyidagi misolda foydalanuvchi input maydoniga belgilar kiritayotganda veb-sahifa veb-server bilan qanday bog‘lanishi mumkinligini ko‘rsatadi:

<figure><img src="../../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

### Misolni tushuntirish

Yuqoridagi misolda foydalanuvchi input maydoniga belgi yozganda, chaqirilgan `showHint()` funksiyasi bajariladi.

Funktsiya `onkeyup` hodisasi tomonidan ishga tushiriladi.

Mana uning kodi:

```
<p>Start typing a name in the input field below:</p>
<p>Suggestions: <span id="txtHint"></span></p>

<form>
First name: <input type="text" onkeyup="showHint(this.value)">
</form>

<script>
function showHint(str) {
  if (str.length == 0) {
    document.getElementById("txtHint").innerHTML = "";
    return;
  } else {
    const xmlhttp = new XMLHttpRequest();
    xmlhttp.onload = function() {
      document.getElementById("txtHint").innerHTML = this.responseText;
    }
  xmlhttp.open("GET", "gethint.asp?q=" + str);
  xmlhttp.send();
  }
}
</script>
```

Kod tushuntirish:

Birinchi, input maydonida hech narsa yo'qligini tekshiring (str.length == 0). Agar rostdan ham hech narsa bo'lmasa, `txtHint` tarkibini tozalang va funksiyadan chiqing.

Ammo input maydonida biror belgi bo'lsa, quyidagilarni bajaring:

* `XMLHttpRequest` obyektini yarating
* Server javobi tayyor bo'lganda bajariladigan funksiyani yarating
* So'rovni serverdagi ASP fayliga (gethint.asp) yuboring
* q parametri gethint.asp?q="+str kabi qo'shilganiga e'tibor qiling
* str o'zgaruvchisi input maydonining tarkibini saqlaydi

### ASP fayli - "gethint.asp"

ASP fayli bir qator ismlarni tekshiradi va brauzerga tegishli ism(lar)ni qaytaradi:

```
<%
response.expires=-1
dim a(30)
'Fill up array with names
a(1)="Anna"
a(2)="Brittany"
a(3)="Cinderella"
a(4)="Diana"
a(5)="Eva"
a(6)="Fiona"
a(7)="Gunda"
a(8)="Hege"
a(9)="Inga"
a(10)="Johanna"
a(11)="Kitty"
a(12)="Linda"
a(13)="Nina"
a(14)="Ophelia"
a(15)="Petunia"
a(16)="Amanda"
a(17)="Raquel"
a(18)="Cindy"
a(19)="Doris"
a(20)="Eve"
a(21)="Evita"
a(22)="Sunniva"
a(23)="Tove"
a(24)="Unni"
a(25)="Violet"
a(26)="Liza"
a(27)="Elizabeth"
a(28)="Ellen"
a(29)="Wenche"
a(30)="Vicky"

'get the q parameter from URL
q=ucase(request.querystring("q"))

'lookup all hints from array if length of q>0
if len(q)>0 then
  hint=""
  for i=1 to 30
    if q=ucase(mid(a(i),1,len(q))) then
      if hint="" then
        hint=a(i)
      else
        hint=hint & " , " & a(i)
      end if
    end if
  next
end if

'Output "no suggestion" if no hint were found
'or output the correct values
if hint="" then
  response.write("no suggestion")
else
  response.write(hint)
end if
%>
```
