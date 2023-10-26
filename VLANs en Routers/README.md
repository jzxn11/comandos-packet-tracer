´´´pk  
Router(config)#inter fa0/0.10
Router(config-subif)#encapsulation dot1Q 10
Router(config-subif)#ip add 192.168.10.1 255.255.255.0
Router(config-subif)#no shutdown
Router(config-subif)#inter fa 0/0.20
Router(config-subif)#encapsulation dot1Q 20
Router(config-subif)#ip add 192.168.20.1 255.255.255.0
Router(config-subif)#no shutdown
Router(config-subif)#do copy run start
´´´  
