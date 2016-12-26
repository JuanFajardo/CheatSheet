# SQLMAP

Sqlmap is an open source penetration testing tool that automates the process of detecting and exploiting SQL injection flaws and taking over of database servers.

## Wiki

[https://github.com/sqlmapproject/sqlmap/wiki/Usage](https://github.com/sqlmapproject/sqlmap/wiki/Usage)

## Comandos de reconocimiento

**Ver la version del sqlmap**

**`python sqlmap.py --version`**

**Ver informacion del SGBD**

**`python sqlmap.py -u "http://sqli.com/?id=1" -b`**

**Si encuentra un error dar un BEEP**

**`python sqlmap.py -u "http://sqli.com/?id=1&col=2&cod=2" --beep`**

**Verificar SQLI en metodo GET**

**`python sqlmap.py -u "http://sqli.com/?id=1" -b`**

**Verificar SQLI  en metodo POST**

**`python sqlmap.py -u "http://sqli.com/index.php" --data="?id=1&new=1" -b`**

**Verificar SQLI  en metodo POST de un parametro especifico**

**`python sqlmap.py -u "http://sqli.com/index.php" --data="?id=1&new=1" -p id -b`**

**Verificar SQLI  con GET usando la cookie de sesion**

**`python sqlmap.py -u "http://sqli.com/?id=1" --cookie="PHPSESSID=ghd8jkmb7e89iv42f2j9er7kd5" -b`**

**Verificar SQLI con GET usando un Agente especifico**

**Aleatorio**

**`python sqlmap.py -u "http://sqli.com/?id=1" --random-agent -b`**

**Especifico \(**[http://www.user-agents.org/\](http://www.user-agents.org/\)**\)**

**`python sqlmap.py -u "http://sqli.com/?id=1" --cookie="PHPSESSID=ghd8jkmb7e89iv42f2j9er7kd5" -b`**

**Verificar SQLI con GET usando un PROXY**

**`python sqlmap.py -u "http://sqli.com/?id=1" --proxy="127.0.0.1:8089" -b`**

## Comandos de explotacion

**Verificar SQLI con GET usando un PROXY**

**`python sqlmap.py -u "http://sqli.com/?id=1" --proxy="127.0.0.1:8089" -b`**

## 



