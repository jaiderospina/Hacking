### WIRESHARK

**Wireshark** es una herramienta de análisis de protocolos de red de código abierto⁴. Originalmente conocido como Ethereal, ampliamente empleada para diversas tareas, incluyendo:

1. **Solución de problemas de red**: Wireshark permite a los usuarios capturar y examinar datos de tráfico en tiempo real, lo que ayuda a identificar y resolver problemas de red.

2. **Análisis de protocolos**: Wireshark puede ser utilizado para el desarrollo y depuración de protocolos, proporcionando una visibilidad detallada del tráfico de red.

3. **Auditoría de seguridad**: Wireshark es una herramienta valiosa para los profesionales de la seguridad informática, ya que puede ser utilizada para detectar anomalías de red y posibles amenazas de seguridad.
   
5.  **Hacking en cualquiera de sus "sombreros". 


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


##  Taller No 1.
**Desarrollo practica básica** 

1. Instalación de wireshark sobre windows  (portable)
2. Desarrollar ejercicio propuesto en  https://www.incibe.es/sites/default/files/contenidos/webinars/webinar_wireshark_ejercicios.pdf
3. Para ello descargar las trazas https://www.incibe.es/sites/default/files/contenidos/webinars/ficheros_ejercicio_wireshark.7z

[![VIDEO](https://github.com/jaiderospina/Hacking/blob/main/IMG/WIRESARK_INCIBE.png)(https://www.youtube.com/watch?v=L8kSqSSZ0Ug?si=r5zLXk7LhvGHBcCu)]


## REFERENCIAS.

1. https://www.wireshark.org/
2. Que es Wireshark y como usarlo? - cibernota.com. https://cibernota.com/que-es-wireshark.
3. Wireshark: La herramienta esencial para el análisis de Redes. https://sistemasenredes.com/herramientas/wireshark-la-herramienta-esencial-para-el-analisis-de-redes/.
4. Wireshark: Qué es y ejemplos de uso | OpenWebinars. https://openwebinars.net/blog/wireshark-que-es-y-ejemplos-de-uso/.
5.  Qué es Wireshark, para qué sirve y casos de uso. https://www.innovaciondigital360.com/iot/que-es-wireshark-y-casos-de-uso/.
6.  ¿Qué es Wireshark y para qué? - informatecdigital.com. https://informatecdigital.com/redes/que-es-wireshark-y-para-que/.
