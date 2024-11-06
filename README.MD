# VISUALIZA 
## Modelo de mundo
#
<img src="https://cdn.prod.website-files.com/662fb92f905585b61b12afd8/666af67c534d424825188e46_loop_pcy%20saying%20hi%20crop.gif" style="display: block; margin: 0 auto;" width="300" height="300" border="100" />

#

## Descripción
Las personas con discapacidad visual enfrentan desafíos significativos para orientarse en entornos complejos, especialmente en espacios desconocidos o con muchos estímulos. Si bien los bastones y perros guía son herramientas valiosas, su capacidad para proporcionar información detallada sobre el entorno es limitada. Con el objetivo de mejorar la autonomía de las personas con discapacidad visual, se busca desarrollar una herramienta que les permita comprender mejor su entorno y que cuente con las siguientes características.

Al iniciar, el usuario será guiado por el programa en el proceso de registro durante este proceso, se solicitará al usuario que proporcione cierta información y también lo guiará en el proceso personalizar los ajustes según sus necesidades, una vez acabado el registro, el programa dará paso al apartado de personalización de los ajustes del programa.


## Funcionamiento
### Registro de usuario
 1. Se activa el programa mediante voz, y el programa saluda al usuario
 2. Se ingresa la información que el programa solicite 
 3. El sistema guarda los datos y este los confirma repitiendo los datos dichos por el usuario

##Registrar usuario
Nombre
R1 - Registrar usuario
Resumen 
El sistema debe permitir registrar el usuario y capturar información personal 
Entrada 
Nombre, Edad, Estado_civil


Resultado
El sistema en voz alta le pedirá le solicitará al usuario datos como nombre, edad, estado civil y  creará un diccionario con los datos del usuario. 
1.1 El sistema para comprobar que los datos sean correctos repite los datos tal como los entendió 
1.1.1 Si los datos dichos por el sistema son correctos, el programa continúa con el siguiente paso
1.1.2 Si los datos dichos por el sistema son incorrectos, el sistema le pedirá al usuario que vuelva a repetir los datos y volverá a hacer la comprobación.
1.1.3 Si el usuario responde que está acompañado se habilitará una opción para ingresar los datos de forma manual
1.1.4 Si el usuario responde que no está acompañado el programa se cierra y retorna que lo intente más tarde. 
El sistema guardará la información brindada por el usuario en un diccionario. 
El sistema le describe al usuario en voz alta las opciones para personalizar el programa.

##Personalización de ajustes


##Reconocimiento de objetos
Nombre
R2- Reconocimiento de objetos
Resumen
El sistema debe ser capaz de identificar y describir objetos en el entorno del usuario en tiempo real utilizando la cámara del dispositivo, proporcionando descripciones detalladas o generales de los objetos, según las preferencias del usuario.


Entrada


Resultado
El sistema analizará en tiempo real las imágenes capturadas por la cámara y buscará objetos en el entorno del usuario.
1.1 El sistema generará una lista con los objetos detectados.
1.2 El sistema describirá en voz alta las características de los objetos: tamaño, color, forma, ubicación y distancia aproximada.
El sistema ofrecerá descripciones generales o detalladas según la configuración personalizada del usuario:
2.1 Si el usuario seleccionó una descripción general, el sistema proporcionará detalles como el nombre del objeto y su ubicación.
2.2 Si el usuario seleccionó una descripción detallada, el sistema proporcionará más información, como la distancia, el tamaño y otros detalles específicos (ej. “El objeto es un teléfono móvil negro, rectangular, ubicado a 1 metro a la derecha”).
El sistema permitirá el reconocimiento de objetos personales importantes configurados previamente por el usuario:
3.1 Si el objeto es parte de la lista personalizada del usuario, el sistema lo destacará en la descripción.
3.2 Si un objeto no se encuentra en la lista de objetos personales, el sistema permitirá agregarlo mediante un comando de voz.
El sistema responderá a comandos de voz sencillos como "describe lo que hay delante de mí", "qué objetos tengo alrededor" o "cuál es el objeto más cercano".
4.1 Si el sistema no puede identificar un objeto, informará al usuario y sugerirá volver a intentar o ajustar el ángulo de la cámara.
4.2 El sistema proporcionará una opción para que el usuario consulte descripciones de objetos específicos, como "¿Qué es el objeto a mi izquierda?".
El sistema guardará las preferencias de configuración en un diccionario para futuros usos.

##Describir objeto
Nombre
R3 - Describir objeto 
Resumen
El sistema recibe la orden de identificar el objeto que el usuario desee
Entrada
Describir objeto (comando de voz)
Resultado 
Al mencionar la frase describir objeto se activa el reconocimiento de voz
Se abrirá la cámara del dispositivo y capturara el video de la cámara
Se llamará la función describir objeto que se utiliza para detectar el objeto que esté delante de la cámara
3.1 El sistema hace una comprobación donde le pregunta al usuario si quiere identificar el objeto que está más cerca a el
3.1.1 Si la respuesta es si el sistema empezará a identificar el objeto
3.1.2 Si la respuesta del usuario es no el programa detendrá la identificación de objetos    
     3.2  Se hará una comprobación para verificar que el             objeto si se halla detectado
     3.2.1 Si el objeto se detectó, el programa retorna una descripción en voz alta confirmando que se detectó el objeto y empieza a describirlo.
     3.2.2 Si el objeto no pudo ser detectado, el programa retorna una descripción en voz alta de que no ha podido detectar el objeto.


##Descripción de notificaciones
Nombre
R5- Descripción de notificaciones
Resumen
El sistema debe ser capaz de leer en voz alta cualquier notificación o mensaje recibido por el usuario preguntando primero si este desea que el contenido sea leido
Entrada
Notificacion, comando de voz del usuario 
resultado
1. El sistema detectará cuando el usuario recibe una notificación o mensaje. 
1.1 Antes de leer el contenido, el sistema preguntará al usuario si desea que el mensaje o notificación sea leído en voz alta. 1.2 Si el usuario confirma que desea escuchar el mensaje, el sistema procederá a leer el texto. 
1.3 Si el usuario indica que no desea escuchar el mensaje, el sistema ignorará la notificación.
2. El sistema ajustará la velocidad y el volumen de lectura de acuerdo con las preferencias del usuario previamente configuradas.




##Modificación de objetos importantes 
Nombre
R- Modificación de objetos importantes
resumen
El sistema permitira al usuario agregar eliminar y modificar objetos en su lista de objetos importantes a traves del comando de voz 
Entrada 


Resultado
1. El sistema debe reconocer los comandos de voz del usuario relacionados con la modificación de objetos importantes. 
1.1 El usuario podrá agregar un nuevo objeto diciendo "agregar [nombre del objeto] a la lista de objetos importantes". 
1.2 El usuario podrá eliminar un objeto diciendo "eliminar [nombre del objeto] de la lista de objetos importantes". 
1.3 El sistema confirmará la modificación en voz alta, indicando si el objeto fue agregado o eliminado correctamente.
2. El sistema actualizará la lista de objetos importantes en el diccionario de preferencias del usuario.




##Leer texto
Nombre
R7 - Leer texto
Resumen
El sistema recibe la orden de leer el documento digital o físico que le indique el usuario
Entrada
Comando de voz
Resultado
Al mencionar la frase, lee el documento se activa el reconocimiento de voz y se procesa el comando.
El sistema le indica 2 opciones (1 si es físico, 2 si es digital) 
2.1 Si el usuario responde 1, el sistema abrirá la cámara del dispositivo.
2.1.1 El sistema manda llamar el método capturar imagen
2.1.2 Si el sistema logra capturar el texto de la imagen le indicará al usuario mediante una descripción por voz que se pudo guardar el texto correctamente
2.1.3 El sistema le pedirá al usuario que responda si desea que el sistema lea el documento
2.1.3.1 Si la respuesta es si el sistema manda llamar el método leer texto
2.1.4 Si el sistema no logró capturar el texto de la imagen se le indicará al usuario que no pudo descifrar el texto de la imagen  
2.2 Si el usuario responde 2 el sistema le solicita al usuario que especifique el nombre o la dirección del archivo 
2.2.1 El sistema valida de que pueda abrir el formato del documento 
2.2.1.1 Si el formato se encuentra dentro de las librerías del sistema abrirá el documento
2.2.1.2 Si el formato no se encuentra dentro de las librerías del sistema se le informará al usuario mediante voz que no se pudo abrir el documento 
2.2.2 El sistema manda llamar el método capturar texto y extrae la información del documento y la guarda 
2.2.3 El sistema le pedirá al usuario que responda si desea que el sistema lea el documento
2.2.3.1 Si la respuesta es si el sistema manda llamar el método leer texto



##finalizar programa
##Interfaz






### Instrucciones
