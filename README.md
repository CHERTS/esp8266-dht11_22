ESP8266 - Driver for the temperature and humidity sensor DHT11 and DHT22
========================================================================

<b>����� ����������� DHT22 � ESP-01:</b><br>
����� 1 DHT22 (Vcc) ��������� � Vcc (3.3 ������) ESP-01<br>
����� 2 DHT22 (DATA_OUT) ��������� � GPIO2 ESP-01<br>
����� 3 DHT22 (NC) �� ������������<br>
����� 4 DHT22 (GND) ��������� � GND ESP-01<br>
����� ������� Vcc � DATA_OUT ���������� ���������� ������������� �������� 10 ���.<br>

<b>������ ��� Windows:</b><br>
1. <a href="http://programs74.ru/get.php?file=EspressifESP8266DevKitX86">��������</a> � ���������� ���������� � SDK.<br>
2. <a href="http://sourceforge.net/projects/mingw/files/Installer/">��������</a> � ���������� MinGW. ��������� mingw-get-setup.exe, � �������� ��������� �������� ����� ��� GUI, �� ���� ������� ������� "...also install support for the graphical user interface".<br>
3. <a href="http://programs74.ru/get.php?file=EspressifESP8266DevKitAddon">��������</a> (84Mb) ����� ���� �������� ��� ������������� ��������� �������������� ������� ��� MinGW.<br>
4. ��������� �� ����� ������ ���� install-mingw-package.bat. �� ��������� �������� ������ ��� MinGW, ��������� ������ ������ ��� ������.<br>
5. ���������� <a href="http://git-scm.com/download/win">Git for Windows</a> (����� ��������� ����������� ������������� ���������).<br>
6. ��������� ������� C:\MinGW\msys\1.0\msys.bat<br>
7. � ������� ���������:<br>
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
Between the terminal Vcc and DATA_OUT need to connect a pullup resistor of 10 ohms.

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
