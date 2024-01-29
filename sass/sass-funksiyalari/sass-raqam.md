# Sass Raqam

## Sass raqam funktsiyalari

Raqam funktsiyalari raqamli qiymatlarni boshqarish uchun ishlatiladi.

Quyidagi jadvalda Sass-dagi barcha raqam funksiyalarining ro'yxati keltirilgan:

| Funksiya                   | Ta'rif & Misol                                                                                                                                                                                                                                     |
| -------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| abs(_number_)              | <p><em>number</em> ning absalyut qiymatini qaytaradi.<br><strong>Misol:</strong><br>abs(15)<br>Natija: 15<br>abs(-15)<br>Natija: 15</p>                                                                                                            |
| ceil(_number_)             | <p><em>number</em> ni eng yaqin kattaroq butun songa yaxlitlaydi.<br><strong>Misol:</strong><br>ceil(15.20)<br>Natija: 16</p>                                                                                                                      |
| comparable(_num1_, _num2_) | <p><em>num1</em> va <em>num2</em> ni taqqoslash mumkin yoki mumkinmasligini qaytaradi.<br><strong>Misol:</strong><br>comparable(15px, 10px)<br>Natija: true<br>comparable(20mm, 1cm)<br>Natija: true<br>comparable(35px, 2em)<br>Result: false</p> |
| floor(_number_)            | <p><em>number</em> ni eng yaqin kichik butun songa yaxlitlaydi.<br><strong>Misol:</strong><br>floor(15.80)<br>Natija: 15</p>                                                                                                                       |
| max(_number..._)           | <p>Bir nechta raqamlardago eng katta qiymatni qaytaradi.<br><strong>Misol:</strong><br>max(5, 7, 9, 0, -3, -7)<br>Natija: 9</p>                                                                                                                    |
| min(_number..._)           | <p>Bir qancha raqamlardagi eng kichkinasini qaytaradi.<br><strong>Misol:</strong><br>min(5, 7, 9, 0, -3, -7)<br>Natija: -7</p>                                                                                                                     |
| percentage(_number_)       | <p><em>number</em> ni foizga aylantiradi (number ni 100 ga ko'paytirib).<br><strong>Misol:</strong><br>percentage(1.2)<br>Natija: 120</p>                                                                                                          |
| random()                   | <p>1 va 0 orasidagi random raqam qaytaradi.<br><strong>Misol:</strong><br>random()<br>Natija: 0.45673</p>                                                                                                                                          |
| random(_number_)           | <p>1 va <em>number</em> orasidagi random raqam qayytaradi.<br><strong>Misol:</strong><br>random(6)<br>Natija: 4</p>                                                                                                                                |
| round(_number_)            | <p><em>Raqamni</em> eng yaqin butun songa yaxlitlaydi.<br><strong>Misol:</strong><br>round(15.20)<br>Natija: 15<br>round(15.80)<br>Result: 16</p>                                                                                                  |
