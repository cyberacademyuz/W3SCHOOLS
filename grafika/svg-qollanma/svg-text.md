# SVG Text

### SVG matni - \<matn>

\<matn> elementi matnni aniqlash uchun ishlatiladi.

***

### 1-misol

Matn yozing:

I love SVG! Sorry, your browser does not support inline SVG.

Mana SVG kodi:

#### Misol

\<svg height="30" width="200">\
&#x20; \<text x="0" y="15" fill="red">I love SVG!\</text>\
\</svg>

***

### 2-misol

Matnni aylantiring:

I love SVG Sorry, your browser does not support inline SVG.

Mana SVG kodi:

#### Misol

\<svg height="60" width="200">\
&#x20; \<text x="0" y="15" fill="red" transform="rotate(30 20,40)">I love SVG\</text>\
\</svg>

***

***

### 3-misol

\<matn> elementi \<tspan> elementi bilan har qanday miqdordagi kichik guruhlarga joylashtirilishi mumkin. Har bir \<tspan> elementi turli formatlash va joylashuvni o'z ichiga olishi mumkin.

Bir necha qatorli matn (\<tspan> elementi bilan):

Several lines: First line. Second line. Sorry, your browser does not support inline SVG.

Mana SVG kodi:

#### Misol

\<svg height="90" width="200">\
&#x20; \<text x="10" y="20" style="fill:red;">Several lines:\
&#x20;   \<tspan x="10" y="45">First line.\</tspan>\
&#x20;   \<tspan x="10" y="70">Second line.\</tspan>\
&#x20; \</text>\
\</svg>

***

### 4-misol

Matn havola sifatida (\<a> elementi bilan):

I love SVG! Sorry, your browser does not support inline SVG.

Mana SVG kodi:

#### Misol

\<svg height="30" width="200" xmlns:xlink="http://www.w3.org/1999/xlink">\
&#x20; \<a xlink:href="https://www.w3schools.com/graphics/" target="\_blank">\
&#x20;   \<text x="0" y="15" fill="red">I love SVG!\</text>\
&#x20; \</a>\
\</svg>
