# Comandos para levantar el servicio de DHCP

## Caso 1:

### Router:

```pkt
Router(config)#ip dhcp pool nombreServicioDhcp
Router(dhcp-config)#network redServicioDhcp 255.255.255.0
Router(dhcp-config)#default-router gatewayServicioDhcp
Router(dhcp-config)#option 150 ip gatewayServicioDhcp
Router(dhcp-config)#exit
Router(config)#ip dhcp excluded-address inicioRangoIp finalRangoIp
```

## Caso 2: Desde un servidor

Click en el servidor -> Servicios -> DHCP:  
Pool Name: Nombre  
Default Gateway: IP DE LA INTERFAZ DEL ROUTER QUE ES GATEWAY DE LAS PCS  
DNS: 8.8.8.8  
Start IP Address: primer address permitido  
Maximum Number of Users: maximo numero de usuarios  
Click en Add para añadir  

### Router:
