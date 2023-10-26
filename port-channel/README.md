# Comandos para levantar el servicio de Port-Channel

1. **Crear un Port Channel:**

   ```shell
   interface Port-channel 1

2. **Configurar el modo de agrupación (PAgP o LACP):**

* Para configurar PAgP (Port Aggregation Protocol):
   ```shell
   channel-group 1 mode desirable

* Para configurar LACP (Link Aggregation Control Protocol):
   ```shell
   channel-group 1 mode active

3. **Acceder a la configuración de los puertos físicos que deseas agregar al Port Channel:**

   ```shell
   interface range FastEthernet0/1 - 2

4. **Configurar los puertos físicos para usar el mismo número de grupo que el Port Channel (en este caso, 1):**

   ```shell
   channel-group 1 mode auto

 5. **Verificar la configuración::**

     ```shell
     show etherchannel summary
  
    show etherchannel detail

6. **Guardar la configuración**

   ```shell
   write memory

