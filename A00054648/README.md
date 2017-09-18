# Taller 3

**Nombre:** Luis Alejandro Tróchez  

**Código:** A00054648

## Descripción  
Corta descripción de lo aprendido 

## Desarrollo
1. A continuación, se analizará el comando cat y de las llamadas al sistema que realiza.
Una breve descripción del comando:
![][1]
Y estos son algunos de las llamadas al sistema que realiza, gracias al comando strace
![][2]
Ahora encontrará la profundización de 5 de esas llamadas al sistema y por qué se usan en este comando.
•	mmap()  crea un nuevo puntero a la dirección virtual addr de largo length. Esto le permite al comando cat ubicar un buffer para leer. 
•	mprotect() modifica la protección que tiene las posiciones de memoria a las que el proceso quiere acceder. En el caso del comando cat, esta llamada le permite poder acceder a la lectura del archivo en cuestión.
•	fstat() lee las estadísticas del archivo como su estado y tamaño. Para el caso de cat, se utiliza para saber las condiciones del archivo a analizar, si este existe o no, si esta defectuoso o no.
•	brk() modifica la ubicación de la terminación del programa, por lo que le permite al comando cat determinar que el sistema tenga suficiente memoria.
•	execve() ejecuta el programa en binario o el script pasado por parámetro. Esto le permite al comando cat ejecutar el vi del que se vale pare leer.
2.
sendTo() es usado para transmitir un mensaje por medio de un socket. Dentro de sus parámetros están sockfd, msg, len, flags, to, tolen.
Recvfrom es usado, por el contrario, para recibir datos por medio de un socket. Dentro de los parámetros están sockfd, buf, len, flags, struct sockaddr from, fromlen.

[1]: 1.PNG
[2]: 2.PNG

