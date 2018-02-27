Proyecto creado para poder ejecutar procesos de larga duración y enviar mensajes de su proceso a la vista. 

Tecnologías usadas:
    .net core 
    RabbitMQ
    Angular.js
    SignalR
    Docker
    
1. Correr el contenedor de rabbitmq 

    $ docker run -d --hostname my-rabbit --name some-rabbit -p 8080:15672 -p 5672:5672  rabbitmq:3-management

2. En la carpeta recibe ejecutar
    $ dotner run 

    La aplicación de consola comenzará a escuchar la cola del rabbitmq

3. correr el Api del backend e invocar la URL 
    http://localhost:5000/api/values


TODO: Hacer una aplicación en Angular que suba un archivo a S3, 
TODO: Poner una cola con esa URL del archivo subido, 
TODO: En el servicio, ejecutar el proceso de descargar la base y enviar mensajes a una cola de proceso. 
TODO: Enviar esos mensajes por medio de SignalR a la vista.