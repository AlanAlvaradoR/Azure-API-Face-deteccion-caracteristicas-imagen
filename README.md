# Azure-API-Face-deteccion-caracteristicas-imagen
Consumo de la API de Face de los coginitive Services de Azure

![Logo de Face Cognitive](https://github.com/AlanAlvaradoR/Azure-API-Face-deteccion-caracteristicas-imagen/blob/main/imagenes/FaceDetectionAzure.jpg)

## Requisitos

- Cuenta de [Azure](https://portal.azure.com/) con suscripción activa
- Computadora con Windows, Linux o MacOs

---------------------------------------------------------

## Pasos

1. Se inicia sesión en la página de [Machine Learning de Azure](https://ml.azure.com/home)

2. Se crea una nueva área de trabajo.

3. Se llenan los parámetros requeridos (Nombre, suscripción, grupo de recursos y región) y se da click en "crear"

*Nota: se puede crear un área de trabajo de ML desde el portal de Azure también, pero en este caso como no se requiere configurar la red ni ningún parámetro importante se crea más fácilmente y con menos requerimientos desde el machine learning studio*

4. Una vez creada el área de trabajo, se entra en la misma, se debe ver una pestaña como la siguiente

![Creació área de trabajo ML](https://github.com/AlanAlvaradoR/Azure-Machine-Learning/blob/main/imagenes/ML1.PNG)

5. En el menú lateral izquierdo se selecciona "proceso"

6. Se selecciona "Nuevo" en instancia de proceso (Para más fácil de entender es una nueva máquina virtual)

7. Se rellenan los campos requeridos: Nombre del proceso, región (bloqueada por el grupo de recursos), tipo de máquina virtual(GPU es más potente pero más cara) y tamaño. Al finalizar se da click en "crear".

8. En el menú lateral izquierdo se da click en "Notebooks".

9. Se da click en el símbolo de más (+) y luego en "crear nuevo archivo".

10. Se coloca un nombre (siempre conservando la terminación ".ipynb"), tipo de archivo "Notebook" y después se da click en "crear".

11. En otra pestaña del navegador se abre el siguiente [link](https://github.com/josejesusguzman/face-api-consumption-python/blob/main/face-consumption.py), se copia todo el código de Python y se vuelve a la página de Azure.

12. Se pega el código que se copió anteriormente dentro del Notebook que creamos, se debe algo parecido a esto:

![API de Face](https://github.com/AlanAlvaradoR/Azure-API-Face-deteccion-caracteristicas-imagen/blob/main/imagenes/API-Face.PNG)

13. Es necesario crear una API de Face de los Cognitive Services de Azure para poder usar sus servicios, por lo que se procede a crear uno desde el [Portal de Azure](https://portal.azure.com/#home)

*NOTA: Puede pedir iniciar sesión de nuevo

14. En el buscador superior se busca "API de Face" y se da enter. Debe de mostrar la página de API de Face del apartado de Coginitive Services

15. Se da click en "Crear".

16. Se completan los parámetros que se pidan:Nombre del grupo de recursos (el que creamos para la instancia de proceso), región, nombre y plan de tarifa (Free si no se va a usar demasiado el servicio). Se marca la casilla de la parte inferior y se da click en "revisar y crear".

17. Se espera a que se valide la implementación y se da click en "crear".

18. Una vez terminada la implementación se da click en "ir al recurso".

19. Se selecciona el apartado de "claves y puntos de conexión" en el menú izquierdo.

20. Se copia la clave1 y se pega en la parte que dice "AQUÍ_PONES_TU_CLAVE_DEL_RECURSO_DE_AZURE" en el código de la notebook

21. Se vuelve al menú de claves y puntos de conexión y se copia el link que dice "extremo".

22. Se pega el link en la parte que dice "AQUÍ_PONES_TU_URL_DESTINO_DEL_RECURSO_DE_AZURE" en el código de la notebook.

23. En el mismo código de la notebook se reemplaza la parte de 'AQUÍ_PONES_TU_IMAGEN' por el link de la imagen que se desea analizar

*Nota: La imagen debe poderse accesar directamente desde el link que se propociona y debe ser pública y no solicitar acceso ni nada parecido. Si no se cuenta con una, en el código viene un link con una imagen de ejemplo.

24. El código ya modificado dber verse parecido a este:

![Código Python Mod](https://github.com/AlanAlvaradoR/Azure-API-Face-deteccion-caracteristicas-imagen/blob/main/imagenes/CodigoPython.PNG)

24. Se da click en las flechitas dobles azules de la parte de arriba para ejecutar el código (o presionar Shift+Enter)

25. Se ejecutará el código y nos mostrará los resultados de la imagen al analizarla en la parte baja de la notebook:

- Edad
- Género
- Uso de lentes
- Emoción predominante


