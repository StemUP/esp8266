1. install choco

win+x 选择管理员权限的powershell，输入：

```
Set-ExecutionPolicy Bypass -Scope Process -Force; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))
```

2. install python

```
choco install python3
```

3. install esptool

```
pip install esptool
```

4. erase_flash

```
esptool.py --chip esp8266 --port COM6 --baud 460800 erase_flash
```

5. flash micropython

```
esptool.py --chip esp8266 --port COM6 --baud 460800 write_flash -z 0x0000 micropython-esp8266-20190529-0x0000-v1.11.bin
```
