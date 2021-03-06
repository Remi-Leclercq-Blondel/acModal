# acModal
A very simple lightweight responsive javascript library to make custom `confirm()` and `alert()`
acModal is very easy to use here is a basic example for an alert modal:

## Demo
[Alert modal](https://remi-leclercq-blondel.github.io/acModal/examples/alert.html)
[Confirm modal](https://remi-leclercq-blondel.github.io/acModal/examples/confirm.html)

## Install it

### With npm: 
Run this command in your project
```
npm install --save-dev ac-modal
```
And then: 
```javascript
const acModal = require('ac-modal');
```

### Inline
Or you can add it with a script tag, download the file `build/index.js` and then:
```html
<script src="https://yourwebsite.com/path/to/index.js"></script>
```

## Make an alert modal
``` javascript
//on element click show an alert modal
document.getElementById('button').addEventListener('click', function () {
    acModal.alert({
        message: 'This is an alert page', //the message to display
        buttonCallBack: function () { //the function on the click of the OK button
            console.log('You have clicked on OK');
        },
    });
});
```
#### Parameters
| Name          | type          | required |
| ------------- |-------------|--------|
| `title`      | `string` |false|
| `message`      | `string`      |true|
| `buttonCallBack` | `function`      |false|
| `buttonText` | `string`      |false default: OK|
| `appendTo` | `string`      |false (query selector)|

## Make a confirm modal
```javascript
//on element click show a confirm modal
document.getElementById('button').addEventListener('click', function () {
    acModal.confirm({
        title: 'Hi I am a title',
        message: 'Do you want to add some lorem ispum in page?',
        successCallBack: function () {
            console.log('You have clicked on the success button');
        },
        cancelCallBack: function () {
            console.log('You have clicked on the cancel button');
        },
    });
});
```
#### Parameters
| Name          | type          | required |
| ------------- |-------------|--------|
| `title`      | `string` |false|
| `message`      | `string`      |true|
| `successCallBack` | `function`      |false|
| `successText` | `string`      |false default: OK|
| `cancelCallBack` | `function`      |false|
| `cancelText` | `string`      |false default: Cancel|
| `appendTo` | `string`      |false (query selector)|

## For development
After you've clone the repository first run:
```shell
npm install
```
Then to run webpack:
```shell
npm run dev
```
