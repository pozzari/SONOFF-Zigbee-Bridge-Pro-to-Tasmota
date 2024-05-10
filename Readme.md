Seguido do https://percy10442.pixnet.net/blog/post/570018748-sonoff-zigbee-bridge e https://notenoughtech.com/home-automation/tasmota-on-sonoff-zb-bridge-pro/#flash


1- Ligar a placa em modo Boot
<br><img width="308" alt="image" src="https://github.com/pozzari/SONOFF-Zigbee-Bridge-Pro-to-Tasmota/assets/39385337/bed3f59d-a8bb-469e-87d7-6d2af0099961">


2- Ir pro site https://tasmota.github.io/install/ e escolher "development->tasmota32-zigbeebridgegpro" como arquivo
![image](https://github.com/pozzari/SONOFF-Zigbee-Bridge-Pro-to-Tasmota/assets/39385337/c85a40c2-8a4f-442a-92c6-299bf57f741f)

3- Na interface Tasmota, ir para configuration->Auto-configuration->Sonoff ZBPro TCP->Apply configuration
![image](https://github.com/pozzari/SONOFF-Zigbee-Bridge-Pro-to-Tasmota/assets/39385337/d8d57ff8-829a-46e8-b54d-4da425908de2)

4- Queimar o Zigbee, indo em Consoles->Berry Scripting Console, nome do arquivo esta em 'Manage File System'

import sonoff_zb_pro_flasher as cc
cc.load("SonoffZBPro_coord_20220219.hex")
cc.check()
![image](https://github.com/pozzari/SONOFF-Zigbee-Bridge-Pro-to-Tasmota/assets/39385337/a58fee51-2f8e-4cbb-bbec-514d73603faa)


5- Executar cc.flash() e aguardar 5 a 8 minutos

<br>no terminal devemos ter: <img width="329" alt="image" src="https://github.com/pozzari/SONOFF-Zigbee-Bridge-Pro-to-Tasmota/assets/39385337/dab20cda-e930-469a-b5fb-409f97a14379">


6- No zigbee2mqtt adicionamos na parte serial: 
  port: tcp://[zbbridgePro_ip]:8888
  ![image](https://github.com/pozzari/SONOFF-Zigbee-Bridge-Pro-to-Tasmota/assets/39385337/0c649034-754f-49c2-9094-9b79dddf72b4)


