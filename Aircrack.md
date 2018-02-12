# Suite Aircrack

## airmon-ng
###Ver interfaces en modo monitor
airmon-ng

###Comenzar Modo monitor
airmon-ng start <interface>
ifconfig <interface> down
ifconfig <interface> mode monitor
ifconfig <interface> up

###Terminar Modo monitor
airmon-ng stop <interface>
ifconfig <interface> down
ifconfig <interface> mode manager
ifconfig <interface> up

###Verificar demonios
airmon-ng check
###Matar demonios
airmon-ng check kill

## airodump-ng
