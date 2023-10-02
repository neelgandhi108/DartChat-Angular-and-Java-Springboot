
This project combines the power of Spring Boot and Angular to create a multiuser chat application with WebSocket, STOMP, and RabbitMQ integration. Below, you'll find a brief overview of the project's features, the components used, and instructions on how to get started.

### Key Features:

1.  Text-based multiple user chat
2.  Unique user login
3.  New user login notifications
4.  Online users list
5.  Multiple users can send messages to a common chat
6.  Log out notifications are displayed when users leave the chat

### Components Utilized:

This application leverages the following technologies and components:

-   Angular with Bootstrap 4 and Stomp library for the user interface.
-   Spring Boot with WebSocket (STOMP) for the backend.
-   RabbitMQ, integrated with the STOMP plugin using a Docker image.

### How to Use:

To get the multiuser chat application up and running, follow these steps:

1.  Start a Docker instance. The project uses a RabbitMQ image with the STOMP plugin. Use the following commands:
    
    bashCopy code
    
    `docker pull activiti/rabbitmq-stomp
    docker run -d --hostname my-rabbit --name rabbit-stomp -p 61613:61613 activiti/rabbitmq-stomp` 
    
2.  Navigate to the [backend folder](https://github.com/neelgandhi108/DartChat-Angular-and-Java-Springboot/backend) and open the `pom.xml` file. Run the following command to download all backend dependencies and start the backend server on port 8080:
    
    bashCopy code
    
    `mvn install` 
    
3.  Navigate to the `package.json` file in the UI folder and execute the command below to install all the required frontend libraries. To start the Node server and launch the UI on the default port 4200, use the following commands:
    
    bashCopy code
    
    `npm install
    ng serve -o` 
    

You can also customize the configuration in the [WebSocket service file](https://github.com/neelgandhi108/DartChat-Angular-and-Java-Springboot/blob/master/ui/src/app/services/websocket-service.service.ts) to suit your needs.

With these steps, you'll have the multiuser chat application running, enabling text-based communication among multiple users. Enjoy using this application for collaborative conversations!