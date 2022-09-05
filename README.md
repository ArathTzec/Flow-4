# Flow-4
Este repositorio contiene el flow 4 del curso de Node-Red visto en los contenidos de IoT 


## Material necesario
Para poder realizar necesario es necesario tener instalado:
- [Node.js](https://github.com/nodesource/distributions/blob/master/README.md) Usar la versión LTS v16x e instalar los build tools.
- [Node-Red](https://nodered.org/docs/getting-started/local)
- Instalar dashboard, puedes consultar el como mediante la siguiente guía: [dashboard CodigoIoT](https://edu.codigoiot.com/mod/page/view.php?id=1080)

## Notas

>Tambien ocuparas la siguiente linea de comando:  *mosquitto_pub -h localhost -t codigoIoT/Mor/mqtt/flow4 -m '{"ID":"Tu usuario/nombre","temp":18,"hum":78}'*

>No olvides primero abrir node red desde la terminal con node-red, de igual manera, abrir el **localhost:1880** en tu navegador de preferenecia

## Instrucciones

1. Agregar un mqtt in y colocar la siguiente dirección: codigoIoT/Mor/mqtt/flow4, tambien configurarlo en el servidor: localhost 1883

2. Agregar un json **es impoortante cambiar la configuracion a: Siempre convertir a objeto javaScript*

3. Posteriormente agregaras 2 function, uno con el nombre de temperartura y el otro con humedad. El codigo que pegaras ahi sera el siguiente (esto para los dos function pero con su variable correspondiente, en este caso hum y temp): 

*msg.payload = msg.payload.hum;
msg.topic= "Humedad";
return msg;*

4. Agregar un dashboard de gauge para las variables y un chart para las graficas

Aqui puedes ver los nodos de los flow :
![](https://github.com/ArathTzec/Flow-4/blob/main/Node-Red.png?raw=true)

## Resultados
Una vez completados los pasos anteriores te dirigirá al Dashboard, que es la interfaz donde ver la temperatura y humedad dependiendo del mensaje que envies, trata de enviar el codigo que se encuentra en notas 
![](https://github.com/ArathTzec/Flow-4/blob/main/Envio%20de%20datos%20de%20Manera-Local.png?raw=true)

Puedes encontrar el video explicativo en el siguiente enlace: [Youtube](https://www.youtube.com/watch?v=XLfiAwqAS1o)
