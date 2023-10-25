# Comandos para levantar el servicio de telefonia

## Router

```pkt
Router(config)#int fa0/0.vlanTelefonia
Router(config-subif)#encapsulation dot1Q vlanTelefonia
Router(config-subif)#ip address gatewayTelefonia 255.255.255.0
Router(config-subif)#no shut
```

```pkt
1. Router(config)#telephony-service
2. Router(config-telephony)#max-ephones cantidadDispositivos #en este caso solo necesitamos 2 telefonos
3. Router(config-telephony)#max-dn cantidadDispositivos
4. Router(config-telephony)#ip source-address gatewayTelefonia port numeroPuerto(generalmente 2000) #el puerto puede variar
5. Router(config-telephony)#auto assign 1 to cantidadDispositivos
```
