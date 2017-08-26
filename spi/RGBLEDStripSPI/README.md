## Neo Pixel (SPI Kaskadierung) 

![](../../images/actors/LedStrips.png)

[RGB LED Strip, siehe LadyAda Überguide](https://learn.adafruit.com/adafruit-neopixel-uberguide) 

- - -

LED Strips (RGB LED Streifen) eröffnen neue Möglichkeiten für die Dekorative Beleuchtungen von Gegenständen und Räumen.

LED Strips werden in den unterschiedlichsten Formen angeboten.

Es gibt unterschiedliche Arten der Ansteuerung, alle LED einer Farbe, jedes RGB LED einzeln.

Im aktuellen Beispiel verwenden wird ein LED Strip mit einen IC pro RGB LED, d.h. jedes RGB LED kann einzeln via SPI Bus angesprochen werden.

Die LED Strip wird an GND, 5V (!) und an die Datenpins CI - D13 (SLK), DI - D11 (MOSI) angeschlossen.

Auf dem Strip kommen [WS2801](http://www.adafruit.com/datasheets/WS2801.pdf) IC&#039;s zum Einsatz. Das Gegenstück zum WS2801 ist der [WS2811](https://www.adafruit.com/datasheets/WS2811.pdf) IC welcher aber nur mit ein paar mbed Boards funktioniert.

### Anwendungen 

*   Raumbeleuchtung
*   Dekorative Ausleuchtung von Gegenständen

