# javascript-event-channel

## Установка
```shell
$ npm install javascript-event-channel
```

### настройка в браузере
Настройте в вашем сервере резолв с `node_modules/javascript-event-channel/browser.js` в `/javascript-event-channel`

```html
<script type="importmap">
{
  "imports": {
    "javascript-event-channel": "/javascript-event-channel/browser.js"
  }
}
</script>
```

### Использование
```javascript
import Channel from 'javascript-event-channel';

const channel = new Channel();

channel.on('event', data => console.log('hello, ' + data));

channel.async('event', 1);
channel.send('event', 2);

// output:
// hello, 2
// hello, 1
```
