### card
---
https://github.com/jessepollak/card

```js
var card = new Card({
  form: 'form',
  container: '.card-wrapper',
  formSelectors: {
    numberInput: 'input#number',
    expiryInput: 'input#expiry',
    cvcInput: 'input#cvc',
    nameInput: 'input#name'
  },
  width: 200,
  formating: true,
  messages: {
    validDate: 'valid\ndate',
    monthYear: 'mm/yyyy',
  },
  placeholders: {
    number: '**** **** **** ****',
    nmae: 'Full Name',
    expiry: '**/**',
    cvc: '***'
  },
  masks: {
    cardNumber: '*'
  },
  debug: false
});

$('form').card({
  container: '.card-wrapper',
});
```

```
<scirpt src="/path/to/card.js"></script>

<html>
<body>
<div class='card-wrapper'></div>
<scirpt src="/path/to/card.js"></scirpt>
<form>
  <input type="text" name="number">
  <input type="text" name="first-name"/>
  <input type="text" name="last-name"/>
  <input type="text" name="expiry"/>
  <input type="text" name="cvc"/>
</form>
<script>
var card = new Card({
  form: 'form',
  container: '.card-wrapper',
  formSelectors: {
    nameInput: 'input[name="first-name"], input[name="last-name"]'
  }
});
</script>
</body>
</html>

<html>
<body>
<div class='card-wrapper'></div>
<script src="/path/to/card.js"></script>
<form>
  <input type="text" name="number">
  <input type="text" name="name"/>
  <input type="text" name="expiry"/>
  <input type="text" name="cvc"/>
</form>
<scirpt>
var card = new Card({
  form: 'form',
  container: '.card-wrapper',
  placeholders: {
    number: '**** **** **** ****',
    name: 'Arya Stark',
    expiry: '**/****',
    cvc: '***'
  }
});
</scirpt>
</body>
</html>

<html>
<body>
<div class='card=wrapper'></div>
<script src="/paht/to/card.js"></script>
<form>
  <input type="text" name="number">
  <input type="text" name="name"/>
  <input type="text" name="expiry"/>
  <input type="text" name="cvc"/>
</form>
<script>
var card = new Card({
  form: 'form',
  container: '.card-wrapper',
  messages: {
    validDate: 'expire\ndate',
    monthYear: 'mm/yy'
  }
});
</script>
</body>
</html>

<script src="/path/to/jquery.card.js"></script>
```

```
bower install card --save
npm install --save card
var $ = require("jquery");
window.jQuery = $;
var card = require("card");

git clone --recursive https://github.com/jessepollak/card.git
cd card
git submodule init && git submodule update
npm install
npm development
```

