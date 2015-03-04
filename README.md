ESP8266 - Driver for the temperature and humidity sensor DHT11 and DHT22
========================================================================

<b>Схема подключения DHT22 к ESP-01:</b><br>
Вывод 1 DHT22 (Vcc) подключен к Vcc (3.3 Вольта) ESP-01<br>
Вывод 2 DHT22 (DATA_OUT) подключен к GPIO2 ESP-01<br>
Вывод 3 DHT22 (NC) не используется<br>
Вывод 4 DHT22 (GND) подключен к GND ESP-01<br>
Между выводом Vcc и DATA_OUT необходимо подключить подтягивающий резистор 5 кОм.<br>

<b>Таблица соответствия виртуальных выводов реальным:</b>

<a id="gpio_map"></a>
<table>
  <tr>
    <th scope="col">Индекс</th><th scope="col">Пин ESP8266</th><th scope="col">Индекс</th><th scope="col">Пин ESP8266</th>
  </tr>
  <tr>
    <td>0 [*]</td><td>GPIO16</td><td>8</td><td>GPIO15</td>
  </tr>
  <tr>
    <td>1</td><td>GPIO5</td><td>9</td><td>GPIO3</td>
   </tr>
   <tr>
    <td>2</td><td>GPIO4</td><td>10</td><td>GPIO1</td>
  </tr>
  <tr>
    <td>3</td><td>GPIO0</td><td>11</td><td>GPIO9</td>
   </tr>
   <tr>
    <td>4</td><td>GPIO2</td><td>12</td><td>GPIO10</td>
  </tr>
  <tr>
    <td>5</td><td>GPIO14</td><td></td><td></td>
   </tr>
   <tr>
    <td>6</td><td>GPIO12</td><td></td><td></td>
  </tr>
  <tr>
    <td>7</td><td>GPIO13</td><td></td><td></td>
   </tr>
</table>
<b>[*] Вывод D0 (GPIO16) можно использовать только на чтение и запись. Прерывания не поддерживаются, использование этого выводя для шин i2c, one-wire невозможно.</b>

<b>Сборка под Windows:</b><br>
1. <a href="http://programs74.ru/get.php?file=EspressifESP8266DevKitX86">Скачайте</a> и установите компилятор и SDK.<br>
2. <a href="http://sourceforge.net/projects/mingw/files/Installer/">Скачайте</a> и установите MinGW. Запускаем mingw-get-setup.exe, в процессе установки выберите режим без GUI, то есть уберите галочку "...also install support for the graphical user interface".<br>
3. <a href="http://programs74.ru/get.php?file=EspressifESP8266DevKitAddon">Скачайте</a> (84Mb) набор моих скриптов для автоматизации установки дополнительных модулей для MinGW.<br>
4. Запустите из моего набора файл install-mingw-package.bat. Он установит основные модули для MinGW, установка должна пройти без ошибок.<br>
5. Установите <a href="http://git-scm.com/download/win">Git for Windows</a> (после установки потребуется перезагрузить компьютер).<br>
6. Запускаем консоль C:\MinGW\msys\1.0\msys.bat<br>
7. В консоле выполните:<br>
```
cd /c/Espressif/examples
git clone https://github.com/CHERTS/esp8266-dht11_22
cd esp8266-dht11_22
make
make flash
```

--

<b>For a single device, connect as follows DHT22 to ESP-01:</b><br>
DHT22 1 (Vcc) to Vcc (3.3 Volts) ESP-01<br>
DHT22 2 (DATA_OUT) to GPIO2 ESP-01<br>
DHT22 3 (NC)<br>
DHT22 4 (GND) to GND ESP-01<br>
Between the terminal Vcc and DATA_OUT need to connect a pullup resistor of 5 Kohms.<br>

<b>GPIO table</b>

<a id="gpio_map"></a>
<table>
  <tr>
    <th scope="col">IO index</th><th scope="col">ESP8266 pin</th><th scope="col">IO index</th><th scope="col">ESP8266 pin</th>
  </tr>
  <tr>
    <td>0 [*]</td><td>GPIO16</td><td>8</td><td>GPIO15</td>
  </tr>
  <tr>
    <td>1</td><td>GPIO5</td><td>9</td><td>GPIO3</td>
   </tr>
   <tr>
    <td>2</td><td>GPIO4</td><td>10</td><td>GPIO1</td>
  </tr>
  <tr>
    <td>3</td><td>GPIO0</td><td>11</td><td>GPIO9</td>
   </tr>
   <tr>
    <td>4</td><td>GPIO2</td><td>12</td><td>GPIO10</td>
  </tr>
  <tr>
    <td>5</td><td>GPIO14</td><td></td><td></td>
   </tr>
   <tr>
    <td>6</td><td>GPIO12</td><td></td><td></td>
  </tr>
  <tr>
    <td>7</td><td>GPIO13</td><td></td><td></td>
   </tr>
</table>
<b>[*] D0(GPIO16) can only be used as gpio read/write. no interrupt supported. no pwm/i2c/ow supported.</b>

<b>Building on Windows:</b><br>
1. <a href="http://programs74.ru/get.php?file=EspressifESP8266DevKitX86">Download</a> and install compiler and SDK.<br>
2. <a href="http://sourceforge.net/projects/mingw/files/Installer/">Download</a> and install MinGW. Run mingw-get-setup.exe, the installation process to select without GUI, ie uncheck "... also install support for the graphical user interface".<br>
3. <a href="http://programs74.ru/get.php?file=EspressifESP8266DevKitAddon">Download</a> (84Mb) set my scripts to automate the installation of additional modules for MinGW.<br>
4. Run the file from my set of install-mingw-package.bat. He will establish the basic modules for MinGW, installation should proceed without error.<br>
5. Install <a href="http://git-scm.com/download/win">Git for Windows</a> (after installation to restart the computer).<br>
6. Run the console C:\MinGW\msys\1.0\msys.bat<br>
7. In the console, run:<br>
```
cd /c/Espressif/examples
git clone https://github.com/CHERTS/esp8266-dht11_22
cd esp8266-dht11_22
make
make flash
```
