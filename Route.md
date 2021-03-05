# Comandos de Route

__Agregar__

```# route add -net 192.168.10.10 netmask 255.255.255.0 gw 192.168.10.1 dev eth0```


__Eliminar__

```# route del -net 192.168.10.10 netmask 255.255.255.0 gw 192.168.10.1 dev eth0```


__Agregar Default gw__

```# route add default gw 192.168.10.1 dev eth0```


__Eliminar Default gw__

```# route del default gw 192.168.10.1 dev eth0```

__Ejemplos__

```
# route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.168.10.1 dev eth0
# route del -net 169.254.0.0 netmask 255.255.0.0 gw 0.0.0.0 dev eth0
```

>168.254.0.0	0.0.0.0	255.255.0.0	U 	1002 0	0	eth0
>0.0.0.0	192.168.1.1	0.0.0.0	UG	0	0	0	eth0
