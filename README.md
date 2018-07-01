Versão Traduzida para o Português-BR / Translated Version to Brazilian Portuguese.

Osciloscópio / Oscilloscope
============

Ferramenta para analisar níveis de voltagem em função do tempo, usando 
[Arduino](http://www.arduino.cc) na Porta Seral / 

Tool for analyzing voltage levels over time using
[Arduino](http://www.arduino.cc) on USB serial port.

Consiste de uma ferramenta de linha de Comando escrita em [Python](http://www.python.org) e 
código para Arduino /
Consists of command line tool written in [Python](http://www.python.org) and
code for Arduino.

Projeto / Project
-------
O projeto original também está hospedado no GitHub - [Oscilloscope project](https://github.com/beli-sk/oscilloscope)
[Oscilloscope project](https://github.com/beli-sk/oscilloscope) is hosted on Github.

O que é preciso / Requirements
------------

### hardware

 * Arduino Duemilanove c/ ATmega328 ou plataforma compatível / Arduino Duemilanove w/ ATmega328 or compatible platform
 * Cabo USB / USB cable
 * PC

### software

 * Python 2 (testado with 2.7) / (tested with 2.7)
 * [PySerial module](http://pyserial.sourceforge.net/)
 * (opcional) / (optional) [gnuplot](http://gnuplot.info/)

Como utilizar / Usage
-----

**Aviso**: Nunca exceda a voltagem máxima dos pinos de entrada do seu Arduino, 
que podem ser entre 3,3V ou 5V. Sempre tenha certeza que a voltagem que você 
está medindo não está acima da voltagem permitida nos pinos de entrada analógica!
Também tenha certeza de que os dois circuitos (Arduino e o circuito medido) têm 
um terra comum.

**Warning**: Never exceed maximal input voltage of your Arduino's input pins
which could be either 3.3V or 5V. Always make sure the voltage you are
measuring is not above the allowed voltage on the analog input pins! Also
make sure the two circuits (Arduino and the measured circuit) have a common
ground.

 * conecte o Arduino ao PC com um cabo serial / connect Arduino to PC with serial cable
 * (apenas na primeira vez) grave o sketch do diretório _Oscilloscope_ / 
 (only first time) flash the sketch from _Oscilloscope_ directory
 * conecte a ponta de prova ao pino analógico 0 do Arduinno / 
 connect probed signal to analog pin 0 on Arduino
 * rode o arquivo oscilloscope.py com a linha de comando (use -h para ajuda), ex.:
 run oscilloscope.py with command line arguments (use -h for help), e.g.:

        ./oscilloscope.py -d /dev/ttyUSB0

 *ou* rode `gnuplot_scope.sh` com os mesmos argumentos para encaminhar
 diretamente ao gnuplot
 
 *or* run `gnuplot_scope.sh` with the same arguments to pipe the data
   directly to gnuplot

License
-------

Copyright 2013 Michal Belica < *devel* at *beli* *sk* >

```
This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see http://www.gnu.org/licenses/ .
```

You find a copy of the GNU General Public License in file LICENSE distributed
with the software.

