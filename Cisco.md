6sh7724504

# Comandos de IOS Cisco

> switch> Modo exec usuario
> switch# Modo exec privilegiado
> switch(config)#  configuracion global (modo de configuracion de terminal) 

### Modo Usuario (Modo Exec)

```bash
switch> 
```

## Modo Usuario Privelegiado (Modo Exec Privilegiado)

__(ingresar / salir / salir) a modo privilegiado__

```bash
switch> enable / disable / exit
switch# 
```

## Ver los detalles del switch

```bash
switch# show running-config
```

## Modo configuracion terminal

```bash
switch# configure terminal
switch(config)# 
```

## Configurar el Nombre
```bash
switch(config)# hostname
```

## Banner de ingreso
```bash
switch(config)# banner motd cSALGA INMEDIATAMENTE o SERA PERSEGUIDO POR LA LEYc
```

## Asignar constraseña a la linea de consola
```bash
switch(config)# line console 0
switch(config)# password PASSWORD123
switch(config)# login
```

## Asignar constraseña al terinal Privilegiado
```bash
switch(config)# enable secret PASSWORD123
```

## Encriptar las contraseñas
```bash
switch(config)# service password-encryption
```

## Ver el reloj y configurar 
```bash
switch# show clock
switch# clock set 10:02:01 10 oct 2020
```

## Ver versiona
```bash
switch# show version
```


## SEGURIDAD 
### PonerNombre a la configuracion
```bash
switch# copy running-config flash [ENTER]
		    ->nombre-config
```

### Copiar al sistema
```bash
switch# copy startp-config running-config
switch# copy running-config tftp
			 IP[]: 192.168.xx.xx
		[file-config]: enter
switch# write
```


### Confgiruar el dominio
```bash
switch(config)# ip domain-name potosi.bo
```
### Sincronizar el registro de ventos de la consola
```bash
switch(config)# line console 0
switch(config)# loggin synchronous
```

### Ver contenido del Flash 
```bash
# dir flash
```

### Ver o show
```bash
switch# show processes  (Muestra los procesos que se ejecutan en el router)
switch# show file system (Muestra el sistema de archivos
switch# show license all (Muestra la iinformacion relacionada con las licencias del dispositivo
switch# show startup-config (Muestra el archivo de configuracion iniciasl (en caso de que exista)
switch# show running-config (muentrs el archivo de configuracion de ejecucion actual
switch# show privilege (Muestra el nivel de privilegio
switch# show tcp (muestra el estado de las conexiones TCP
switch# show ip route (muestra la tabla de enrutamiento (informacion valiosa)
switch# show interfaces  (muestra las interfaces)
switch# show gigabiEthernet 0/0  (muestra una interface especifica)
switch# show interfaces f0/2
switch# show controllers  ( muestra las condiciones de hardware de las interfaces )
switch# show ip interface brief  ( Ver resumen de las interfaces )
switch# show mac-address-table (Ver la tabla de  direccion MacAddress
```

## Configuraciones de interfaces de un router
```bash
switch> enable
switch# configure terminal
switch(config)# interface s0/3/1 (Ingeras a una interface
switch(config)# clock rate 500000 (Asignacion manual de clock rate (se realizo ya que la interfaz s0/3/1 es DCE 
switch(config)# no shutdown
switch(config)# ip address 192.168.0.2 255.255.255.0 (Asignar Ip y MacAdress
```

## Observaciones

__Cantidad de host__

mascara de red  255.255.255.0
 
wilcard		0.0.0.255 


__Por si algun error__

ctrl+shift+6

__Minicom__

speed 9600

Data bits 7

stop bits 1

parity none

flowcontrel none

__Velocidades estadar serial__
115200
256000
921600


## Configuraciones VLAN de switch a maquinas
```bash
switch> enable
switch# configure terminal

switch(config)# hostanme SISTEMAS

switch(config)# vlan 116
switch(config)# int ra fa 0/10-13
switch(config)# swichtport mode access
switch(config)# swichtport access vlan 116

switch(config)# int ra fa 0/2-9
switch(config)# shutdown

switch(config)# int ra gi 0/1-0
switch(config)# shutdown

switch(config)# int ra fa 0/14-24
switch(config)# switchport mode access
switch(config)# switchport access vlan 13

switch(config)# do show vlan

switch(config)# do show running
```


## Configuraciones VLAN y TRUNK de switch a switch
```bash
switch> enable
switch# configure terminal

switch(config)# hostanme CORE
switch(config)# int ra fa 0/6-24
switch(config)# switchport mode access
switch(config)# switchport acces vlan 13
switch(config)# shutdown
switch(config)# 
switch(config)# int ra fa 0/1-3
switch(config)# switchport mode trunk
switch(config)# 
switch(config)# do show vlan
switch(config)# 
switch(config)# 
```

## Configurar Trunk con N vlans
```bash
switch> enable
switch# conf terminal
switch(config)# interface fastEthernet 0/25
switch(config)# switchport mode trunk
switch(config)# switchport trunk encapsulation dot1q
switch(config)# switchport trunk allowed vlan 4,5
switch(config)# exit
```

## Ruteo entre VLANS
```bash
switch(config)# interface fastEthernet 0/0
switch(config)# no shutdown
switch(config)# exit

switch(config)# interface fastEthernet 0/0.4
switch(config)# encapsulation dot1Q 4
switch(config)# ip address 192.168.4.1 255.255.255.0
switch(config)# exit

switch(config)# interface fastEthernet 0/0.5
switch(config)# encapsulation dot1Q 5
switch(config)# ip address 192.168.5.1 255.255.255.0
exit
```


## Configuraciones VLAN y TRUNK de switch a switch
```bash
switch> enable
switch# configure terminal

switch(config)# hostanme ROUTER
switch(config)# int fa 0/0.116
switch(config)# encapsulation dot1Q 116
switch(config)# ip address 192.168.116.1 255.2555.255.0
switch(config)# ip helper-address 192.168.116.1

ROUTER(confi)# 
```

## Creacion de Vlans y Asiganar IP
```bash
switch> enable
switch# configure terminal
switch(config)# vlan 50
switch(config)# name Vlan50
switch(config)# interface vlan 50
switch(config)# description Vlan50Red
switch(config)# ip address 192.168.50.250 255.255.255.0
switch(config)# no shutdown
switch(config)# exit
switch(config)# 
switch(config)# vlan 60
switch(config)# name VLAN60
switch(config)# interface vlan 60
switch(config)# description VLAN60Red2
switch(config)# ip address 192.168.60.250 255.255.255.0
switch(config)# no shutdown
switch(config)# exit
```
## Habilitar Telnet y poner password
```bash
switch(config)# line vty 0
switch(config)# password 192168691
switch(config)# login
switch(config)# logging synchronous 
switch(config)# exec-timeout 40
switch(config)# motd-banner
switch(config)# exit

switch(config)# hostname Cementerio

switch(config)# enable password 192168691
switch(config)# exit
```

## Comandos para detectar la red
```bash
switch# show vlans

switch# show ip interface brief

switch# show mac address-table address

switch# show cdp neighbor

switch# show cdp neighbor detail
```





