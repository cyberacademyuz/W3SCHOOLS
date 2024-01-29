# Angular DOM

AngularJS ilova ma'lumotlarini HTML DOM elementlarining atributlari bilan bog'lash uchun direktivalarga ega.

### ng-disabled direktivasi

**ng-disabled** direktivasi AngularJS ilova maʼlumotlarini HTML elementlarining oʻchirilgan atributiga bogʻlaydi.

{% code title="AngularJSga misol:" %}
```
<div ng-app="" ng-init="mySwitch=true">

<p>
<button ng-disabled="mySwitch">Click Me!</button>
</p>

<p>
<input type="checkbox" ng-model="mySwitch">Button
</p>

<p>
{{ mySwitch }}
</p>

</div>
```
{% endcode %}

Ilovani tushuntirish:

**Ng-disabled** direktivasi **mySwitch** ilova maʼlumotlarini HTML tugmasining **disabled** atributiga bogʻlaydi.

**Ng-model** direktivasi HTML checkbox elementining qiymatini **mySwitch** qiymatiga bog'laydi.

Agar **mySwitch** qiymati **true** bo'lsa, tugma o'chiriladi:&#x20;

```
<p>
<button disabled>Click Me!</button>
</p>
```

Agar **mySwitch** qiymati **false** bo'lsa, tugma o'chirilmaydi:&#x20;

```
<p>
<button>Click Me!</button>
</p>
```

### Ng-show direktivasi

**Ng-show** direktivasi HTML elementini ko'rsatadi yoki berkitadi:

{% code title="AngularJSga misol:" %}
```
<div ng-app="">

<p ng-show="true">I am visible.</p>

<p ng-show="false">I am not visible.</p>

</div>
```
{% endcode %}

**Ng-show** direktivasi **ng-show** qiymatiga asoslangan HTML elementini ko'rsatadi (yoki yashiradi).

Siz true yoki false bo'ladigan har qanday expressiondan foydalanishingiz mumkin:

{% code title="AngularJSga misol:" %}
```
<div ng-app="" ng-init="hour=13">

<p ng-show="hour > 12">I am visible.</p>

</div>
```
{% endcode %}

{% hint style="warning" %}
Keyingi bo'limda HTML elementlarini yashirish uchun tugmani bosishdan foydalanishga ko'proq misollar keltirilgan.
{% endhint %}

### ng-hide direktivasi

**Ng-hide** direktivasi HTML elementini yashiradi yoki ko'rsatadi.

{% code title="AngularJSga misol:" %}
```
<div ng-app="">

<p ng-hide="true">I am not visible.</p>

<p ng-hide="false">I am visible.</p>

</div>
```
{% endcode %}
