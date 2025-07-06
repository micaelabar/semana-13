
# Consumo Rest Microservicios
## Introducción:
La implementación y configuración de los microservicios fue realizada por el estudiante Pablo Sario, quien asumió la responsabilidad de resolver los problemas técnicos, gestionar adecuadamente las dependencias y ejecutar correctamente los servicios involucrados en el proyecto. Por su parte, la elaboración del presente informe y la sistematización del procedimiento técnico fueron llevadas a cabo por la estudiante Micaela Barbecho, quien estructuró la información de manera clara, precisa y formal.

Este trabajo conjunto evidencia la importancia de la colaboración entre los aspectos técnicos de la programación y la documentación técnica, permitiendo así una presentación integral y comprensible del proceso de desarrollo basado en una arquitectura moderna de microservicios.
## 1. Tiempo de duración:
La configuración, corrección de errores y ejecución exitosa de los microservicios tomó aproximadamente 2 horas, incluyendo identificación de errores, configuración del entorno y pruebas funcionales.
## 2. Fundamentos:
Los microservicios permiten dividir una aplicación monolítica en varios servicios pequeños, desplegables y escalables individualmente. Cada servicio se comunica entre sí a través de APIs REST. En este caso, se usó:
- Spring Boot: Para crear servicios rápidamente con configuración mínima.
- Eureka Server: Como servicio de descubrimiento para registrar y localizar los microservicios.
- Maven: Para la gestión de dependencias y construcción del proyecto.
## 3. Conocimientos previos
- Conocimientos básicos de Java y Spring Boot.
- Manejo de herramientas como Visual Studio Code o IntelliJ.
- Familiaridad con Maven.
- Comprensión general del concepto de microservicios.
## 4. Objetivo a alcanzar
- Configurar y ejecutar correctamente los tres microservicios.
- Solucionar errores de compilación y conflictos de puertos.
- Registrar exitosamente los servicios en el servidor Eureka.
- Demostrar la independencia y comunicación entre microservicios.
## 5. Equipo necesario
- Computadora con al menos 8 GB de RAM.
- Sistema operativo Windows 10 o superior.
- Conexión a internet.
- Editor de código (Visual Studio Code, IntelliJ, etc.).
## 6. Material de apoyo:
- Dependencias de Spring Boot.
- Documentación oficial de Spring Cloud.
- Comandos básicos de PowerShell y netstat.
- Repositorios de Maven:
https://repo.maven.apache.org
https://repo.spring.io
## 7. Procedimiento:
### Paso 1: Iniciar el servidor Eureka
Se ejecuta el comando `mvn spring-boot:run` desde el directorio del proyecto eureka-server para iniciar el servidor Eureka. Este paso compila el proyecto y descarga las dependencias necesarias.

### Evidencia:
<imag!![image](https://github.com/user-attachments/assets/37edee3f-10ac-4a9c-9349-3f32b044bf73)

### Paso 2:Crear directorio del API Gateway
Se crea el directorio del proyecto API Gateway dentro del directorio general del proyecto, utilizando los comandos `mkdir` y `cd` en PowerShell.
### Evidencia:
<imag!![image](https://github.com/user-attachments/assets/83e7d51d-8253-4aff-ac1f-fa04a622eed2)

### Paso 3: Generar proyecto desde Spring Initializr
Se configura el proyecto del API Gateway en Spring Initializr con las dependencias necesarias: Gateway, Eureka Discovery Client y Spring Reactive Web.
### Evidencia:
<imag!![image](https://github.com/user-attachments/assets/4f192d94-04ef-44b6-8062-e27272bb9a73)

### Paso 4:Configurar application.properties
Se definen los puertos y se especifica el nombre de los servicios y la zona del Eureka Server en el archivo `application.properties` de cada microservicio.
### Evidencia:
<imag!![image](https://github.com/user-attachments/assets/5d699145-e7f1-4481-9ce1-3b7af84d7e8a)

### Paso 5:Iniciar el API Gateway
Se inicia el servicio del API Gateway usando `mvn spring-boot:run`, y se observan los logs donde se cargan las configuraciones de rutas.
### Evidencia:
<imag!![image](https://github.com/user-attachments/assets/cada2693-35ef-4685-9991-9c91588dac33)

### Paso 6: Verificar registro en Eureka
Se accede a la consola web de Eureka (localhost:8761) para verificar que los servicios (API Gateway, Clientes y Pagos) estén registrados correctamente.
### Evidencia:
<imag!![image](https://github.com/user-attachments/assets/24675fde-7bc1-48bd-aa87-31e0e0972fa6)

### Paso 7:Verificar configuración de Maven y propiedades
Se revisan los archivos `pom.xml` y `application.properties` de los servicios para confirmar que las dependencias y configuraciones sean correctas.
### Evidencia:
<imag!![image](https://github.com/user-attachments/assets/6c608f07-ee26-41ee-a781-15e96006baaa)

### Paso 8: Vista previa del estado inicial del servidor Eureka
Cuando se inicia el servidor Eureka por primera vez, no hay servicios registrados. Esta es la vista inicial del panel de Eureka.
### Evidencia:
<imag!![image](https://github.com/user-attachments/assets/3b8d1f11-43fe-40de-b895-396b34a4ac88)

### Paso 9:Consola al iniciar Eureka Server
Se muestra la consola con los logs que indican que el servidor Eureka ha iniciado correctamente y está disponible en el puerto 8761.
### Evidencia:
<imag!![image](https://github.com/user-attachments/assets/509c3e19-3894-4b41-8eba-2c4cd8b6d4e7)

## 9. Conclusión:
El despliegue exitoso de una arquitectura de microservicios depende tanto de una correcta configuración de herramientas como de la capacidad para identificar y corregir errores en tiempo real. Utilizar Eureka como servidor de descubrimiento facilita el manejo de múltiples servicios, asegurando escalabilidad y flexibilidad en entornos distribuidos.
## 10. Bibliografía
- Spring Boot Reference Documentation – https://spring.io/projects/spring-boot
- Spring Cloud Netflix – https://cloud.spring.io/spring-cloud-netflix
- Documentación de Eureka Server – https://cloud.spring.io/spring-cloud-netflix/multi/multi_spring-cloud-eureka-server.html
- Maven Repository – https://mvnrepository.com
- Oracle Java Documentation – https://docs.oracle.com/javase/
