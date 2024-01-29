# Canvas Reference

HTML5 \<canvas> tegi skriptlar (odatda JavaScript) orqali tezda grafiklarni chizish uchun ishlatiladi.

Biroq, \<canvas> elementining o'ziga xos rasm chizish qobiliyati yo'q (bu faqat grafiklar uchun konteyner) - grafikani haqiqiy chizish uchun skriptdan foydalanishingiz kerak.

getContext() usuli tuvalga chizish usullari va xususiyatlarini ta'minlovchi ob'ektni qaytaradi.

Ushbu ma'lumotnoma getContext("2d") ob'ektining xususiyatlari va usullarini o'z ichiga oladi, undan matn, chiziqlar, qutilar, doiralar va boshqalarni tuvalga chizish uchun foydalanish mumkin.

***

### Brauzerni qo'llab-quvvatlash

Jadvaldagi raqamlar elementni to'liq qo'llab-quvvatlaydigan birinchi brauzer versiyasini ko'rsatadi.

| Element   |     |     |     |     |     |
| --------- | --- | --- | --- | --- | --- |
| \<canvas> | 4.0 | 9.0 | 2.0 | 3.1 | 9.0 |

Internet Explorer 9, Firefox, Opera, Chrome va Safari \<canva> va uning xususiyatlari va usullarini qo'llab-quvvatlaydi.

Eslatma: Internet Explorer 8 va undan oldingi versiyalari \<canvas> elementini qo'llab-quvvatlamaydi.

***

### Ranglar, uslublar va soyalar

| Property                                                                                                                                                  | Description                                                              |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------ |
| [fillStyle](https://www-w3schools-com.translate.goog/tags/canvas\_fillstyle.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)         | Sets or returns the color, gradient, or pattern used to fill the drawing |
| [strokeStyle](https://www-w3schools-com.translate.goog/tags/canvas\_strokestyle.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)     | Sets or returns the color, gradient, or pattern used for strokes         |
| [shadowColor](https://www-w3schools-com.translate.goog/tags/canvas\_shadowcolor.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)     | Sets or returns the color to use for shadows                             |
| [shadowBlur](https://www-w3schools-com.translate.goog/tags/canvas\_shadowblur.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)       | Sets or returns the blur level for shadows                               |
| [shadowOffsetX](https://www-w3schools-com.translate.goog/tags/canvas\_shadowoffsetx.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp) | Sets or returns the horizontal distance of the shadow from the shape     |
| [shadowOffsetY](https://www-w3schools-com.translate.goog/tags/canvas\_shadowoffsety.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp) | Sets or returns the vertical distance of the shadow from the shape       |

\


| Method                                                                                                                                                                    | Description                                                   |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------- |
| [createLinearGradient()](https://www-w3schools-com.translate.goog/tags/canvas\_createlineargradient.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp) | Creates a linear gradient (to use on canvas content)          |
| [createPattern()](https://www-w3schools-com.translate.goog/tags/canvas\_createpattern.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)               | Repeats a specified element in the specified direction        |
| [createRadialGradient()](https://www-w3schools-com.translate.goog/tags/canvas\_createradialgradient.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp) | Creates a radial/circular gradient (to use on canvas content) |
| [addColorStop()](https://www-w3schools-com.translate.goog/tags/canvas\_addcolorstop.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)                 | Specifies the colors and stop positions in a gradient object  |

***

***

### Chiziq uslublari

| Property                                                                                                                                            | Description                                                     |
| --------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------- |
| [lineCap](https://www-w3schools-com.translate.goog/tags/canvas\_linecap.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)       | Sets or returns the style of the end caps for a line            |
| [lineJoin](https://www-w3schools-com.translate.goog/tags/canvas\_linejoin.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)     | Sets or returns the type of corner created, when two lines meet |
| [lineWidth](https://www-w3schools-com.translate.goog/tags/canvas\_linewidth.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)   | Sets or returns the current line width                          |
| [miterLimit](https://www-w3schools-com.translate.goog/tags/canvas\_miterlimit.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp) | Sets or returns the maximum miter length                        |

### To'rtburchaklar

| Method                                                                                                                                                | Description                                          |
| ----------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------- |
| [rect()](https://www-w3schools-com.translate.goog/tags/canvas\_rect.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)             | Creates a rectangle                                  |
| [fillRect()](https://www-w3schools-com.translate.goog/tags/canvas\_fillrect.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)     | Draws a "filled" rectangle                           |
| [strokeRect()](https://www-w3schools-com.translate.goog/tags/canvas\_strokerect.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp) | Draws a rectangle (no fill)                          |
| [clearRect()](https://www-w3schools-com.translate.goog/tags/canvas\_clearrect.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)   | Clears the specified pixels within a given rectangle |

### Yo'llar

| Method                                                                                                                                                            | Description                                                                                   |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| [fill()](https://www-w3schools-com.translate.goog/tags/canvas\_fill.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)                         | Fills the current drawing (path)                                                              |
| [stroke()](https://www-w3schools-com.translate.goog/tags/canvas\_stroke.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)                     | Actually draws the path you have defined                                                      |
| [beginPath()](https://www-w3schools-com.translate.goog/tags/canvas\_beginpath.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)               | Begins a path, or resets the current path                                                     |
| [moveTo()](https://www-w3schools-com.translate.goog/tags/canvas\_moveto.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)                     | Moves the path to the specified point in the canvas, without creating a line                  |
| [closePath()](https://www-w3schools-com.translate.goog/tags/canvas\_closepath.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)               | Creates a path from the current point back to the starting point                              |
| [lineTo()](https://www-w3schools-com.translate.goog/tags/canvas\_lineto.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)                     | Adds a new point and creates a line to that point from the last specified point in the canvas |
| [clip()](https://www-w3schools-com.translate.goog/tags/canvas\_clip.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)                         | Clips a region of any shape and size from the original canvas                                 |
| [quadraticCurveTo()](https://www-w3schools-com.translate.goog/tags/canvas\_quadraticcurveto.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp) | Creates a quadratic Bézier curve                                                              |
| [bezierCurveTo()](https://www-w3schools-com.translate.goog/tags/canvas\_beziercurveto.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)       | Creates a cubic Bézier curve                                                                  |
| [arc()](https://www-w3schools-com.translate.goog/tags/canvas\_arc.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)                           | Creates an arc/curve (used to create circles, or parts of circles)                            |
| [arcTo()](https://www-w3schools-com.translate.goog/tags/canvas\_arcto.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)                       | Creates an arc/curve between two tangents                                                     |
| [isPointInPath()](https://www-w3schools-com.translate.goog/tags/canvas\_ispointinpath.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)       | Returns true if the specified point is in the current path, otherwise false                   |

### Transformatsiyalar

| Method                                                                                                                                                    | Description                                                                                                                                                                                                        |
| --------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [scale()](https://www-w3schools-com.translate.goog/tags/canvas\_scale.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)               | Scales the current drawing bigger or smaller                                                                                                                                                                       |
| [rotate()](https://www-w3schools-com.translate.goog/tags/canvas\_rotate.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)             | Rotates the current drawing                                                                                                                                                                                        |
| [translate()](https://www-w3schools-com.translate.goog/tags/canvas\_translate.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)       | Remaps the (0,0) position on the canvas                                                                                                                                                                            |
| [transform()](https://www-w3schools-com.translate.goog/tags/canvas\_transform.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)       | Replaces the current transformation matrix for the drawing                                                                                                                                                         |
| [setTransform()](https://www-w3schools-com.translate.goog/tags/canvas\_settransform.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp) | Resets the current transform to the identity matrix. Then runs [transform()](https://www-w3schools-com.translate.goog/tags/canvas\_transform.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp) |

### Matn

| Property                                                                                                                                                | Description                                                      |
| ------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------- |
| [font](https://www-w3schools-com.translate.goog/tags/canvas\_font.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)                 | Sets or returns the current font properties for text content     |
| [textAlign](https://www-w3schools-com.translate.goog/tags/canvas\_textalign.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)       | Sets or returns the current alignment for text content           |
| [textBaseline](https://www-w3schools-com.translate.goog/tags/canvas\_textbaseline.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp) | Sets or returns the current text baseline used when drawing text |

\


| Method                                                                                                                                                  | Description                                                     |
| ------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------- |
| [fillText()](https://www-w3schools-com.translate.goog/tags/canvas\_filltext.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)       | Draws "filled" text on the canvas                               |
| [strokeText()](https://www-w3schools-com.translate.goog/tags/canvas\_stroketext.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)   | Draws text on the canvas (no fill)                              |
| [measureText()](https://www-w3schools-com.translate.goog/tags/canvas\_measuretext.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp) | Returns an object that contains the width of the specified text |

### Rasm chizish

| Method                                                                                                                                              | Description                                      |
| --------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------ |
| [drawImage()](https://www-w3schools-com.translate.goog/tags/canvas\_drawimage.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp) | Draws an image, canvas, or video onto the canvas |

### Piksel manipulyatsiyasi

| Property                                                                                                                                               | Description                                                                |
| ------------------------------------------------------------------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------- |
| [width](https://www-w3schools-com.translate.goog/tags/canvas\_imagedata\_width.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)   | Returns the width of an ImageData object                                   |
| [height](https://www-w3schools-com.translate.goog/tags/canvas\_imagedata\_height.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp) | Returns the height of an ImageData object                                  |
| [data](https://www-w3schools-com.translate.goog/tags/canvas\_imagedata\_data.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)     | Returns an object that contains image data of a specified ImageData object |

\


| Method                                                                                                                                                          | Description                                                                                    |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- |
| [createImageData()](https://www-w3schools-com.translate.goog/tags/canvas\_createimagedata.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp) | Creates a new, blank ImageData object                                                          |
| [getImageData()](https://www-w3schools-com.translate.goog/tags/canvas\_getimagedata.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)       | Returns an ImageData object that copies the pixel data for the specified rectangle on a canvas |
| [putImageData()](https://www-w3schools-com.translate.goog/tags/canvas\_putimagedata.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)       | Puts the image data (from a specified ImageData object) back onto the canvas                   |

### Kompozitsiyalash

| Property                                                                                                                                                                        | Description                                                            |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| [globalAlpha](https://www-w3schools-com.translate.goog/tags/canvas\_globalalpha.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)                           | Sets or returns the current alpha or transparency value of the drawing |
| [globalCompositeOperation](https://www-w3schools-com.translate.goog/tags/canvas\_globalcompositeoperation.asp?\_x\_tr\_sl=auto&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp) | Sets or returns how a new image are drawn onto an existing image       |

### Boshqa

| Method        | Description                                        |
| ------------- | -------------------------------------------------- |
| save()        | Saves the state of the current context             |
| restore()     | Returns previously saved path state and attributes |
| createEvent() |                                                    |
| getContext()  |                                                    |
| toDataURL()   |                                                    |
