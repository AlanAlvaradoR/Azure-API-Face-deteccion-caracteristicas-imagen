# Azure-API-Face-deteccion-caracteristicas-imagen
Consumo de la API de Face de los coginitive Services de Azure

![Logo de Face Cognitive](https://github.com/AlanAlvaradoR/Azure-API-Face-deteccion-caracteristicas-imagen/blob/main/imagenes/)

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

![API de Face](https://github.com/AlanAlvaradoR/Azure-API-Face-deteccion-caracteristicas-imagen/blob/main/imagenes/)


