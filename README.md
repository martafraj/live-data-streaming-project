# End to End - Proyecto de Subasta en Tiempo Real 
![kafka-live-stream](https://github.com/user-attachments/assets/538b6dfa-ad54-4678-a91c-886921547b85)

## Introducción al Proyecto: Sistema de Subastas en Tiempo Real
Este proyecto consiste en una plataforma web de subastas en tiempo real, donde los usuarios pueden participar en subastas de productos a través de una interfaz sencilla. Utiliza Flask como servidor web para generar los datos, Kafka para procesar los datos de manera paralela y escalable, y Azure MySQL para almacenar la información de las subastas. Además, Power BI se integra para ofrecer análisis visuales de los datos, permitiendo a los usuarios y administradores obtener informes detallados. Esta solución es eficiente, escalable y permite una experiencia de usuario fluida y dinámica.

## 1. Crear un entorno virtual

Para crear un entorno virtual en Python, primero navega a la carpeta de tu proyecto. Luego, crea un entorno virtual con el nombre que prefieras (por ejemplo, `venv`). El entorno virtual contendrá todos los paquetes necesarios para tu proyecto y se mantendrá aislado de otros proyectos.
```bash
python3 -m venv venv
```

## 2. Activar el entorno virtual

Una vez creado el entorno virtual, debes activarlo para empezar a usarlo. La activación varía dependiendo de tu sistema operativo:


- **En Windows**, debes ejecutar el comando de activación específico para este sistema.
```bash
venv\Scripts\activate
```
- **En macOS o Linux**, la activación también tiene un comando diferente.
```bash
source venv/bin/activate
```

Cuando el entorno esté activado, verás su nombre en la línea de comandos, indicando que todo lo que instales y ejecutes será dentro de este entorno aislado.

## 3. Instalar los requerimientos

Si tu proyecto tiene un archivo que lista las dependencias necesarias (como un archivo `requirements.txt`), puedes instalar todas las bibliotecas requeridas de manera automática. Esto asegura que tu proyecto tenga todas las herramientas necesarias para funcionar correctamente.
```bash
pip install -r requirements.txt
```

## 4. Ejecutar el proyecto

Ejecutar el proyecto Flask:  
```bash
flask run
```
Ejecutar los `writers` en diferentes terminales con:
```bash
python db_writer1.py
```

```bash
python db_writer2.py
```
Para escribir el archivo `csv` en otra terminal ejecuta:
```bash
python file_writer.py
```
## 5. PowerBI
- Probablemente no tengas el conector de MySQL para PowerBI, así que antes te hará falta instalarlo: [conector](dev.mysql.com/downloads/connector/net)
- Abre el archivo de powerbi: `dashboard-livestream.pbix`
- Te pedirá credenciales para la base de datos. Son las mismas de la conexión a MySQL definida en el archivo `config.py`
- Una vez conectado podrás visualizar los datos guardados en la base de datos
![mysql-powerbi](https://github.com/user-attachments/assets/ddffd57e-8ba1-408a-bd77-dc4fb8577330)


## 6. Desactivar el entorno virtual

Cuando termines de trabajar en el proyecto, puedes desactivar el entorno virtual para salir de él. Esto te devolverá a tu entorno de Python global.
```bash
deactivate
```

## Conlusion 
En conclusión, este proyecto de subastas en tiempo real ofrece una solución eficiente y escalable para gestionar grandes volúmenes de datos, garantizando una experiencia de usuario fluida y dinámica. La integración de tecnologías como Flask, Kafka, Azure MySQL y Power BI permite un procesamiento paralelo robusto, almacenamiento seguro de la información y análisis visual detallado. Con esta arquitectura, el sistema está preparado para adaptarse al crecimiento de usuarios y datos, asegurando su rendimiento y facilidad de mantenimiento a largo plazo.

## Contribuidores

¡Gracias a todos mis compañeros que han contribuido a este proyecto! 🚀


| Imagen                                       | Nombre del Colaborador                        | Descripción de la Contribución            |
|----------------------------------------------|----------------------------------------------|-------------------------------------------|
| <img src="https://github.com/leo-narvaez.png" width="40" height="40"> | [Leonardo Narváez](https://github.com/leo-narvaez) | Backend        |
| <img src="https://github.com/anaBorja.png" width="40" height="40"> | [Ana Borja](https://github.com/anaBorja) | Frontend           |
| <img src="https://github.com/martafraj.png" width="40" height="40"> | [Marta Fraile](https://github.com/martafraj) | Arquitectura           |
| <img src="https://github.com/Alvaro-diez.png" width="40" height="40"> | [Álvaro Diez](https://github.com/Alvaro-diez) | Arquitectura - Backend           |
| <img src="https://github.com/sbb23tajamar.png" width="40" height="40"> | [Samuel Barahona](https://github.com/sbb23tajamar) | Documentación        |

