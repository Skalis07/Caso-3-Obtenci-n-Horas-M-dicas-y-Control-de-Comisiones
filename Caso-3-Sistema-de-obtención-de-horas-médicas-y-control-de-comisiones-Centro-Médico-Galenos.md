
## **Contexto**

El Centro Médico Galenos es una empresa familiar la cual facilitaba módulos totalmente implementados a médicos generales y especialistas, con el tiempo han ido implementado otros servicios tales como kinesiología, oftalmología y otorrinolaringología con salas que necesitan implementación especial.
Se agregó un servicio a los médicos el cual consta de una secretaria que organizaba toda la documentación relativa a atenciones y pagos.
Debido al crecimiento del centro han aparecido problemáticas tales como cálculos de las comisiones que difieren entre lo calculado por la secretaria y lo calculado por los médicos. Gasto excesivo de tiempo en organizar agendas de los médicos, recepción de pagos y cálculos de comisiones.
Para solucionar esto se ha propuesto la automatización de todos estos procesos, brindando tiempo a la secretaria para no descuidar sus otras funciones y agilizando todos los procesos del centro médico.

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

## **Supuestos**

1. Se hace el supuesto de que el centro médico posee un generador eléctrico que puede proporcionar energía por 6 horas luego de producido un corte del servicio.
2. Se hace el supuesto de que el centro médico tiene apróximadamente 8 box por planta y 4 plantas por sucursal, haciendo un tal de 32 médicos, atendiendo el promedio de 4 pacientes por hora. Trabajando un promedio entre 5 y 7 horas, se estima que se atienden entre 600 y 900 pacientes por día. Esto da un total de aproximadamente 28.000 pacientes por mes como máximo.
3. Se supone que los pacientes acuden al centro médico cada 2 meses, por lo tanto se estima un total de 50.000 fichas médicas a digitalizar.

## **Diagrama de motivaciones**

![](https://github.com/Halan07/Caso-3-Obtenci-n-Horas-M-dicas-y-Control-de-Comisiones/blob/main/Diagrama%20de%20movitaciones.png?raw=true)
