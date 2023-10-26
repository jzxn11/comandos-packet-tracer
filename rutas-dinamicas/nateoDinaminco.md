# Comandos para crear rutas dinamicas 

## Router 0
```
conf t
ip nat inside source static 172.5.5.5 200.0.0.10 (ip del cliente) (ip del router al otro router)
interface f0/0
ip address 172.5.5.1 255.255.255.0 (gateway del cliente y su mascara)
ip nat inside
no shutdown
exit

interface serial 0/3/0
ip address 200.0.0.1 255.255.255.0 (ip de la red entre routers y su mascara)
clock rate 64000
ip nat outside
no shutdown
exit

```

## Router 1
```
conf t
ip nat pool NAT-POOL 200.0.0.50 200.0.0.60 netmask 255.255.255.0 (rango de ips que tendran configurada la NAT y su mascara)
access-list 1 permit 10.10.10.0 0.0.0.255 (red de los paquetees que tienen permitido pasar)
ip nat inside source list 1 pool NAT-POOL

interface f0/0
ip address 10.10.10.1 255.255.255.0 (gateway del cliente y su mascara)
ip nat inside
no shutdown
exit

interface serial 0/3/0
ip address 200.0.0.2 255.255.255.0 (ip de la red entre routers y su mascara)
ip nat outside
no shutdown
exit
```
