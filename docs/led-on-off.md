# Led On Off

Run with:
```bash
node eg/led-on-off.js
```


```javascript
var five = require("johnny-five"),
  board, led;

board = new five.Board();

board.on("ready", function() {

  // Create a standard `led` hardware instance
  led = new five.Led({
    pin: 13
  });

  // "on" turns the led _on_
  led.on();

  // "off" turns the led _off_
  led.off();

  // Turn the led back on after 3 seconds (shown in ms)
  this.wait(3000, function() {

    led.on();

  });
});

```


## Breadboard/Illustration


![docs/breadboard/led-on-off.png](breadboard/led-on-off.png)
[docs/breadboard/led-on-off.fzz](breadboard/led-on-off.fzz)





## License
Copyright (c) 2012, 2013, 2014 Rick Waldron <waldron.rick@gmail.com>
Licensed under the MIT license.
Copyright (c) 2014, 2015 The Johnny-Five Contributors
Licensed under the MIT license.
