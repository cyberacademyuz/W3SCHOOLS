# SVG Strocking

### SVG Stroke xususiyatlari

SVG insult xususiyatlarining keng doirasini taklif etadi. Ushbu bobda biz quyidagilarni ko'rib chiqamiz:

* insult
* zarba kengligi
* stroke-linecap
* zarba-dasharray

Barcha chiziq xususiyatlari har qanday turdagi chiziqlar, matn va elementlarning konturlariga qo'llanilishi mumkin.

***

### SVG zarbasi xususiyati

Strok xususiyati elementning chiziq, matn yoki kontur rangini belgilaydi:

&#x20;Sorry, your browser does not support inline SVG.

Mana SVG kodi:

#### Misol

\<svg height="80" width="300">\
&#x20; \<g fill="none">\
&#x20;   \<path stroke="red" d="M5 20 l215 0" />\
&#x20;   \<path stroke="black" d="M5 40 l215 0" />\
&#x20;   \<path stroke="blue" d="M5 60 l215 0" />\
&#x20; \</g>\
\</svg>

***

### SVG kontur kengligi xususiyati

Stroke-width xususiyati elementning chiziq, matn yoki kontur qalinligini belgilaydi:

&#x20;Sorry, your browser does not support inline SVG.

Mana SVG kodi:

#### Misol

\<svg height="80" width="300">\
&#x20; \<g fill="none" stroke="black">\
&#x20;   \<path stroke-width="2" d="M5 20 l215 0" />\
&#x20;   \<path stroke-width="4" d="M5 40 l215 0" />\
&#x20;   \<path stroke-width="6" d="M5 60 l215 0" />\
&#x20; \</g>\
\</svg>

***

***

### SVG stroke-linecap xususiyati

Stroke-linecap xossasi ochiq yo'lning har xil turlarini belgilaydi:

&#x20;Sorry, your browser does not support inline SVG.

Mana SVG kodi:

#### Misol

\<svg height="80" width="300">\
&#x20; \<g fill="none" stroke="black" stroke-width="6">\
&#x20;   \<path stroke-linecap="butt" d="M5 20 l215 0" />\
&#x20;   \<path stroke-linecap="round" d="M5 40 l215 0" />\
&#x20;   \<path stroke-linecap="square" d="M5 60 l215 0" />\
&#x20; \</g>\
\</svg>

***

### SVG stroke-dasharray xususiyati

Stroke-dasharray xususiyati chiziqli chiziqlar yaratish uchun ishlatiladi:

&#x20;Sorry, your browser does not support inline SVG.

Mana SVG kodi:

#### Misol

\<svg height="80" width="300">\
&#x20; \<g fill="none" stroke="black" stroke-width="4">\
&#x20;   \<path stroke-dasharray="5,5" d="M5 20 l215 0" />\
&#x20;   \<path stroke-dasharray="10,10" d="M5 40 l215 0" />\
&#x20;   \<path stroke-dasharray="20,10,5,5,5,10" d="M5 60 l215 0" />\
&#x20; \</g>\
\</svg>
