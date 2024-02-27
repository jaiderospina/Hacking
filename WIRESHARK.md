### WIRESHARK

**Wireshark** es una herramienta de análisis de protocolos de red de código abierto⁴. Originalmente conocido como Ethereal, ampliamente empleada para diversas tareas, incluyendo:

1. **Solución de problemas de red**: Wireshark permite a los usuarios capturar y examinar datos de tráfico en tiempo real, lo que ayuda a identificar y resolver problemas de red.

2. **Análisis de protocolos**: Wireshark puede ser utilizado para el desarrollo y depuración de protocolos, proporcionando una visibilidad detallada del tráfico de red.

3. **Auditoría de seguridad**: Wireshark es una herramienta valiosa para los profesionales de la seguridad informática, ya que puede ser utilizada para detectar anomalías de red y posibles amenazas de seguridad.
   
5.  **Hacking en cualquiera de sus "sombreros". 


# Fases de anális de paquetes en Wireshark. 

1. **Captura de Paquetes**: Esta es la fase inicial donde se capturan los paquetes de red. Wireshark ofrece la capacidad de seleccionar la interfaz de red de la cual se desea capturar el tráfico. Una vez que la captura está en marcha, Wireshark muestra en tiempo real todos los paquetes que pasan por esa interfaz.

2. **Filtrado de Paquetes**: Durante la captura, es común que se capture una gran cantidad de datos. Por lo tanto, es esencial aplicar filtros para limitar los datos a los paquetes relevantes. Los filtros pueden ser aplicados basados en diferentes criterios como direcciones IP, puertos, protocolos, etc.

3. **Análisis de Paquetes en Profundidad**: Una vez que se ha capturado el tráfico y se han aplicado los filtros necesarios, el siguiente paso es analizar los paquetes en detalle. En esta fase, se examinan los encabezados de los paquetes para comprender los diferentes protocolos involucrados, las direcciones de origen y destino, los datos transmitidos, los tiempos de respuesta, entre otros aspectos.

4. **Identificación de Problemas**: Una de las principales razones para utilizar Wireshark es identificar problemas de red. Durante el análisis de paquetes, se buscan anomalías como errores de p
5. rotocolo, congestión de red, latencia excesiva, pérdida de paquetes, entre otros. Estas anomalías pueden ayudar a identificar y solucionar problemas de rendimiento o seguridad en la red.

6. **Correlación de Datos**: En entornos complejos, puede ser necesario correlacionar datos de múltiples paquetes para comprender completamente un flujo de comunicación o un evento en la red. Wireshark proporciona herramientas para seguir flujos de datos y correlacionar paquetes relacionados.

7. **Generación de Informes**: Una vez completado el análisis, Wireshark ofrece la capacidad de generar informes detallados sobre el tráfico de red capturado. Estos informes pueden incluir estadísticas sobre el tráfico, resúmenes de problemas identificados, gráficos de flujo de datos, entre otros datos relevantes.

En resumen, el proceso de análisis de paquetes en Wireshark implica la captura de paquetes, el filtrado para reducir el volumen de datos, el análisis detallado de los paquetes para identificar problemas o anomalías, la correlación de datos para comprender completamente los flujos de comunicación, y finalmente la generación de informes para documentar los hallazgos.

# Algunos filtros de Wireshark:

| Tipo de filtro    | Explicación                                                                                                      | Ejemplo de uso                                   |
|-------------------|------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| Filtro por dirección IP | Permite filtrar los paquetes según la dirección IP de origen o destino.                                         | `ip.addr == 192.168.1.100`                      |
| Filtro por protocolo    | Filtra los paquetes según el protocolo utilizado, como TCP, UDP, ICMP, etc.                                     | `tcp`                                            |
| Filtro por puerto       | Permite filtrar los paquetes según el número de puerto de origen o destino.                                      | `tcp.port == 80`                                |
| Filtro por dirección MAC| Filtra los paquetes según la dirección MAC de origen o destino.                                                  | `eth.addr == 00:11:22:33:44:55`                 |
| Filtro por dirección de red| Permite filtrar los paquetes según la dirección de red de origen o destino.                                     | `eth.dst == 00:11:22:33:44:55`                  |
| Filtro por tipo de tráfico| Filtra los paquetes según el tipo de tráfico, como tráfico HTTP, DNS, FTP, etc.                                 | `http`                                           |
| Filtro por longitud del paquete| Filtra los paquetes según su longitud en bytes.                                                                  | `frame.len > 100`                               |
| Filtro por texto en el contenido| Filtra los paquetes que contienen cierto texto en su contenido, como palabras clave o cadenas específicas.      | `http.request.uri contains "login"`             |


##  Taller.
**Desarrollo practica básica** 

1. Instalación de wireshark sobre windows  (portable)
2. Desarrollar ejercicio propuesto en  https://www.incibe.es/sites/default/files/contenidos/webinars/webinar_wireshark_ejercicios.pdf
3. Para ello descargar las trazas https://www.incibe.es/sites/default/files/contenidos/webinars/ficheros_ejercicio_wireshark.7z

# VIDEO EXPLICACIÓN


[![VIDEO](https://github.com/jaiderospina/Hacking/blob/main/IMG/WIRESARK_INCIBE.png)](https://www.youtube.com/watch?v=L8kSqSSZ0Ug?si=wGmu8AY2Ic_CJTIl)


## REFERENCIAS.

1. https://www.wireshark.org/
2. Que es Wireshark y como usarlo? - cibernota.com. https://cibernota.com/que-es-wireshark.
3. Wireshark: La herramienta esencial para el análisis de Redes. https://sistemasenredes.com/herramientas/wireshark-la-herramienta-esencial-para-el-analisis-de-redes/.
4. Wireshark: Qué es y ejemplos de uso | OpenWebinars. https://openwebinars.net/blog/wireshark-que-es-y-ejemplos-de-uso/.
5.  Qué es Wireshark, para qué sirve y casos de uso. https://www.innovaciondigital360.com/iot/que-es-wireshark-y-casos-de-uso/.
6.  ¿Qué es Wireshark y para qué? - informatecdigital.com. https://informatecdigital.com/redes/que-es-wireshark-y-para-que/.
