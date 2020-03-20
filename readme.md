# javascript-event-channel

## Установка
```shell
$ npm install javascript-event-channel
```

### настройка в браузере
Настройте в вашем сервере резолв с `node_modules/javascript-event-channel` в `/javascript-event-channel`

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

### Дополнительно
Если вы используете vscode, можно настроить резолв для корректной работы самого редактора с помощью файла `jsconfig.json`
```json
{
  "compilerOptions": {
    "baseUrl": "../node_modules/",
    "paths": {
      "javascript-event-channel/*": ["./javascript-event-channel/*"]
    }
  }
}
```
