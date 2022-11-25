
## **Contexto**

El Centro Médico Galenos es una empresa familiar la cual facilitaba módulos totalmente implementados a médicos generales y especialistas, con el tiempo han ido implementado otros servicios tales como kinesiología, oftalmología y otorrinolaringología con salas que necesitan implementación especial.
Se agregó un servicio a los médicos el cual consta de una secretaria que organizaba toda la documentación relativa a atenciones y pagos.
Debido al crecimiento del centro han aparecido problemáticas tales como cálculos de las comisiones que difieren entre lo calculado por la secretaria y lo calculado por los médicos. Gasto excesivo de tiempo en organizar agendas de los médicos, recepción de pagos y cálculos de comisiones.
Para solucionar esto se ha propuesto la automatización de todos estos procesos, brindando tiempo a la secretaria para no descuidar sus otras funciones y agilizando todos los procesos del centro médico.

1. Se hace el supuesto de que el centro médico tiene apróximadamente 8 boxs por planta y 4 plantas por sucursal, haciendo un tal de 32 médicos, atendiendo el promedio de 4 pacientes por hora. Trabajando un promedio entre 5 y 7 horas, se estima que se atienden entre 600 y 900 pacientes por día. Esto da un total de aproximadamente 28.000 pacientes por mes como máximo.
2. Se hace el supuesto de que los pacientes acuden al centro médico cada 2 meses en promedio, por lo tanto se estima un total de 50.000 fichas médicas a digitalizar.

## **Objetivos**

Los objetivos del proyecto son:

1. Automatizar el sistema de cobros, cálculo de comisiones y agendado de horarios de los centros médicos.
2. Lograr mediante una aplicación web el registro efectivo de usuarios con el fin de que puedan agendar hora con los médicos del centro.
3. Evitar errores en los cobros de comisiones.
4. Brindar tiempo a las secretarias para enfocarse en sus otras tareas.


## **Stakeholders**

<html>
<body>
<!--StartFragment-->

Stakeholders | Preocupaciones | Requerimientos | Valor aportado
-- | -- | -- | --
Dueños del Centro Médico | Eficiencia del sistema | El sistema debe cumplir con todos los requerimientos mínimos para poder automatizar los procesos actuales. |  El centro médico al automatizar sus procesos verá incrementado su potencial para atender a más personas y su eficiencia, esto se traduce en mayor cantidad de clientes que a su vez significa mayor cantidad de ingresos para el centro médico. |   |   |  
Médicos | Que las comisiones se calculen de manera correcta | Sistema de cálculo efectivo de las comisiones para cada médico |  Automatización del proceso de cálculo de las comisiones |   |   |  
Secretarias | Que el sistema sea amigable | Interfaz creada bajo ciertos estándares para lograr que sea amigable con el usuario | Aprendizaje veloz de las funcionalidades del software por parte del usuario
Pacientes | Disponibilidad de horas médicas | Mostrar al usuario la disponibilidad de horas para el médico especialista que requieran | Brindar información necesaria al usuario, creando una satisfacción y confianza en el mismo.
Cajeros | Saber cómo se ingresarán los pagos en el sistema | Sistema intuitivo y veloz para ingresar pagos y generar boletas | Automatización del pago y generación de boleta |   |   |  



<!--EndFragment-->
</body>
</html>

## **Requisitos funcionales**

1. La interfaces deben contener el logo y nombre del centro médico.


## **Requisitos no funcionales**

1. El tiempo de respuesta en del sistema debe estar entre 1 y 3 segundos.
2. El sistema será capaz de seguir funcionando en caso de corte del suministro eléctrico por un periodo de 6 horas gracias a la disposición de un generador.
3. El sistema será capaz de seguir funcionando sin conexión a Internet, exceptuando las interfaces web para los usuarios, quienes no podrán comunicarse con el sistema.
4. El sistema debe contar con escalabilidad en la capacidad ya que aumenta con el tiempo su cantidad de pacientes, médicos y sucursales.
5. Los datos deben estar protegidos de acuerdo a la ley 19.628.

## **Restricciones**
1. El desarrollo está limitado por el presupuesto dispuesto a gastar por parte de los dueños de los centros médicos.
2. El proyecto debe implementarse en un tiempo breve y de manera efectiva para evitar interrupciones del servicio a los usuarios.
3. El sistema debe ser simple de utilizar para los usuarios, independiente de su rol dentro del sistema.
4. El proyecto está sujeto a la protección y privacidad de los datos de los usuarios conforme a lo dispuesto en el artículo 19 Nº 4 de la Constitución Política de la República  y a las normas pertinentes de la ley 19.628.


## **Diagrama de motivaciones**

![](https://github.com/Halan07/Caso-3-Obtenci-n-Horas-M-dicas-y-Control-de-Comisiones/blob/main/Diagrama%20de%20movitaciones.png?raw=true)

## **Modelo Lógico**

![](https://github.com/Halan07/Caso-3-Obtenci-n-Horas-M-dicas-y-Control-de-Comisiones/blob/main/Modelo%20L%C3%B3gico%20con%20fondo%20azul%20Corregido.png)

## **Documentado**

(*) - OBLIGATORIO<br/>
(°) - OPCIONAL<br/>
(#) - CLAVE PRIMARIA<br/>
(U) - ÚNICO<br/>

### **Persona:**
Entidad que contiene 4 subtipos, estos definen las funciones de cada usuario en el sistema.

**Atributos:**<br/>
* Identificador (STRING)(#*U)<br/>
* RUT (STRING)(*)<br/>
* Nombre (STRING)(*)<br/>
* Apellido (STRING)(*)<br/>
* Apellido2 (STRING)(°)<br/>
* Nombre social (STRING)(*)<br/>
* Teléfono (ENTERO)(*)<br/>
* Correo (STRING)(°)<br/>
* Contraseña (STRING)(*)<br/>

### **Cita:** 
Está asociada a un paciente y una agenda.

**Atributos:**<br/>
* Identificador (STRING)(#*U)<br/>
* Hora_Cita(TIME)(*)<br/>
* Fecha_Cita(DATE)(*)<br/>


### **Comisión:**
Está asociada a un médico.

**Atributos:**<br/>
* Identificador (STRING)(#*U)<br/>
* Monto (ENTERO)(*)<br/>



## **Configuración**

* Datos que se guardarán y son relevantes para el correcto funcionamiento del sistema.

* Almacenamiento de la cantidad de intentos de ingresos erróneos, bloqueando luego del tercer intento por una hora.

* Credenciales de autenticación para la correcta vista del sitio y funcionalidades disponibles según quién ingresa.

* Control de la cantidad de veces que un usuario cancela las horas, notificando un abuso en caso de cancelar 5 horas seguidas.

* Permitir sólo solicitudes de usuarios que se conectan desde Chile.

## **Servicios**

* **Servicio de gestión de pagos automático.**<br/>
Servicio que permite la realización de pagos con distintos métodos de manera automática<br/>
**Entrada:**<br/>
Método de pago, escáneo de tarjeta si requiere, claves si aplica.<br/>
**Salida:**<br/>
Resultado de la transacción.<br/>
* **Servicio de gestión de usuario.**<br/>
Servicio que permite el registro e inicio de sesión de usuarios a la plataforma.<br/>
**Entrada:** <br/>
Registro: Datos obligatorios de la entidad persona (RUT, Nombre, Apellido, Nombre social, Teléfono, Contraseña, confirmación contraseña).<br/>
Inicio: RUT, Contraseña.<br/>
**Salida:** <br/>
Vista de la plataforma como usuario.<br/>
Mensaje de error en los datos ingresados.<br/>
* **Servicio de gestión de agenda.**<br/>
Servicio que permite la creación y modificación de agendas ligadas a un usuario.<br/>
**Entrada:**<br/>
UUID usuario al que se le creará la agenda.<br/>
**Salida:**<br/>
Asignación correcta de agenda al usuario.<br/>
* **Servicio de gestión de citas**<br/>
Servicio que permite realizar solicitudes de citas a los usuarios, las cuales se vincularán a una agenda disponible.<br/>
**Entrada:**<br/>
1- Hora y fecha de la cita.<br/>
2- Solicitud de borrado.<br/>
**Salida:**<br/>
1- Mensaje de confirmación de agendado de la cita.<br/>
2- Mensaje de confirmación de cita borrada correctamente. <br/>
* **Servicio de creación de boleta.**<br/>
Servicio que recopila los datos importantes para la boleta y los convierte en un documento sencillo el que se imprimirá para su posterior entrega al cliente.<br/>
**Entrada:**<br/>
Nombre cajero, nombre paciente, nombre médico, fecha y hora cita.<br/>
**Salida:** <br/>
Documento listo para impresión.<br/>
Impresión del documento.<br/>
* **Servicio de cálculo de comisiones.**<br/>
Servicio que calcula comisiones de las boletas.<br/>
**Entrada:**<br/>
Monto boleta, uuid médico.<br/>
**Salida:**<br/>
Monto comisión que se asocia al médico.<br/>

## **Arquitectura Cloud**
Se ha optado por una arquitectura serverless, esta será descrita junto a cada una de sus capas y componentes a continuación.
![](https://github.com/Halan07/Caso-3-Obtenci-n-Horas-M-dicas-y-Control-de-Comisiones/blob/main/Arquitectura%20Cloud.png)
### **Capa de Host**<br/>
Se utilizará Amazon S3 para ejecutar el sitio web estático, contiene todos los archivos HTML, CSS Y JS.
### **Capa de Operabilidad**<br/>
Se utilizará Amazon API Gateway para poder publicar y mantener las API.<br/>
Se utilizará Amazon Cognito para toda la autenticación de los usuarios.<br/>
Se utilizará AWS Lambda para poder ejecutar el código de manera remota, se definen permisos a un rol creado, este rol lo utilizará lambda para ejecutar las funciones.
### **Capa de Data**<br/>
Se utilizará Amazon RDS como base de datos para la arquitectura cloud.

### **Buenas prácticas**<br/>
**Principio de mínimo privilegio** > Se utiliza al hacer la base de datos privada, se crean reglas en el Security Group de la base de datos, haciendo que sólo pueda ser accedida mediante lambda, esto límite el acceso a los recursos, permitiendo a las partes acceder sólo a la información necesaria para su correcto funcionamiento.
Ejemplo:
![](https://github.com/Halan07/Caso-3-Obtenci-n-Horas-M-dicas-y-Control-de-Comisiones/blob/main/Security%20Group.png)
**Seguridad a nivel de cuenta MFA** > Proteger la cuenta utilizada de AWS con Autenticación Multifactor, agregando una capa de seguridad.