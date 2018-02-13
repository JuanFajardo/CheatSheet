# Suite Aircrack

## airmon-ng
#### Ver interfaces en modo monitor
```
airmon-ng
```
#### Comenzar Modo monitor
```
airmon-ng start <interface>
```
```
ifconfig <interface> down
ifconfig <interface> mode monitor
ifconfig <interface> up
```
#### Terminar Modo monitor
```
airmon-ng stop <interface>
```
```
ifconfig <interface> down
ifconfig <interface> mode manager
ifconfig <interface> up
```
#### Verificar demonios
```
airmon-ng check
```

#### Matar demonios
```
airmon-ng check kill
```

## airodump-ng
<dl>
  <dt> Escanear el espectro </dt>
  <dd> airodump-ng _< interfaces >_ </dd>

  <dt>Escanear una encriptacion especifico y que tenga WPS durante 10 segundos "1.0 WPS"</dt>
  <dd>timeout 10 airodump-ng --wps --encrypt WEP/WAP/OPN _< interfaces >_ </dd>

  <dt>Escanear un CANAL, AP en un archivo WAP</dt>
  <dd>airodump-ng --bssid _< macAP >_ -c _< canal >_ -w _< archivo >_ _< interfaces>_ </dd>

  <dt>Escanear un CANAL, AP en un archivo con IVS  WEP</dt>
  <dd>airodump-ng --bssid _< macAP >_ -c <canal> -w _< archivo >_ --ivs _< interfaces >_ </dd>

  <dt>Leer un archivo escrito </dt>
  <dd>airodump-ng -r _< file-001.cap >_ </dd>
</dl>
