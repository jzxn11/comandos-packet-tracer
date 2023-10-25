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
