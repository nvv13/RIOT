# About
This test application is made for verification of the WS2812B LED strip driver.

# Usage
Connect a WS2812B based LED strip to a board of your choice, build, and flash
this application. When run, you should see the strip changing its brightness
while lighting in red, then green, and then blue. After this sequence, you
should see a light moving up and down the strip, changing its color.


You might need to adjust the default parameters (number of LEDs on the strip and
pin configuration). You can do this simply by pre-setting the `CFLAGS`
environment variable, e.g.:
```
$ CFLAGS="-DWS2812B_PARAM_LED_NUMOF=78"" make all
```

To change the default pins, simply override the default parameters, e.g.:
```
$ CFLAGS="-DWS2812B_PARAM_DATA_PIN=GPIO_PIN\(2,3\) make all
```
