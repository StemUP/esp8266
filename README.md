安装 choco 包管理工具

win+x 选择管理员权限的powershell，输入：

```
Set-ExecutionPolicy Bypass -Scope Process -Force; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))
```

安装 python

```
choco install python3
```

安装 esp8266 烧录工具 esptool

```
pip install esptool
```

擦除 esp8266

```
esptool.py --chip esp8266 --port COM6 --baud 460800 erase_flash
```

烧录 micropython

```
esptool.py --chip esp8266 --port COM6 --baud 460800 write_flash -z 0x0000 .\micropython-0x0000-esp8266-20190125-v1.10.bin
```

烧录 AP

```
esptool.py --chip esp8266 --port COM6 --baud 460800 write_flash -z 0x00 .\AP-0x00000.bin
esptool.py --chip esp8266 --port COM6 --baud 460800 write_flash -z 0x02 .\AP-0x02000.bin
```

connect MyAP

192.168.4.1

no automesh
