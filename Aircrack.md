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
kill [PID
```

## airodump-ng
<dl>
  <dt> Escanear el espectro </dt>
  <dd> airodump-ng < interfaces > </dd>

  <dt>Escanear una encriptacion especifico y que tenga WPS durante 10 segundos "1.0 WPS"</dt>
  <dd>timeout 10 airodump-ng --wps --encrypt WEP/WAP/OPN < interfaces > </dd>

  <dt>Escanear un CANAL, AP en un archivo de un cliente/s WAP</dt>
  <dd>airodump-ng --bssid < macAP >_ -c < canal > -w < archivo > -a <macHost>,<macHost>  < interfaces> </dd>

  <dt>Escanear un CANAL, AP en un archivo con IVS  WEP</dt>
  <dd>airodump-ng --bssid < macAP > -c < canal > -w < archivo > --ivs < interfaces > </dd>

  <dt>Leer un archivo escrito </dt>
  <dd>airodump-ng -r < file-001.cap > </dd>
</dl>

## aireplay-ng



aireplay-ng --fakeauth [0/1] -a < macAP > -h < macHost > < interfaces >
airodump-ng -w < Archivo > --bssid < macAP >
iwconfig < interfacesmon0 > channel < canal >
iwconfig < interfaces > channel < canal >
aireplay-ng --arpreplay  -b < macAP > -h < macHost > < interfaces >


airodump-ng -w < Archivo > --bssid < macAP >
aireplay-ng --deauth [n/0] -a < macAP > < interfaces >
aireplay-ng --deauth [n/0] -a < macAP > -c < macHost > < interfaces >


airodump-ng -w < Archivo > --bssid < macAP >
aireplay-ng --interactive -b <macAP> -h <macHost> < interfaces >
aireplay-ng --interactive -b <macAP> -h <macHost> -r < Archivo > < interfaces >


aireplay-ng --test < interfaces >




## reaver
airodump-ng --wps < interfaces >
wash -i < interfaces >
reaver -i < interfaces > -b < macAP > -d 30 -S -N -vv 
