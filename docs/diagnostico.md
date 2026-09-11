# 1.1
1. Publicación del artefacto sin esperar al análisis de sonarcloud: faltaría un "needs: validar" en publicar, pipeline.yml, sonarcloud funcionaría como un generador de reportes en lugar de intervenir.
2. Variaciones en los artefactos generados: diferentes artefactos en diferentes ambientes, dependencias desde el .lock.
3. Incremento en lead time: no hay un cache entre las ejecuciones del pipeline para las dependencias.
4. Trazabilidad de los artefactos: siempre se sobreescribe el artefacto y no contiene un identificador de referencia al commit.

# 1.2
El primer defecto explica la duración registrada en linea-base.md. Por ejemplo, el primer pipeline ejecutado duró 1m 11s, pero cada job duró 1m y 17s respectivamente, por lo que se ejecutaron en paralelo.

# 1.3
En el caso 6 se menciona que "Casi la mitad de los incidentes son cosas que funcionaban en el ambiente de pruebas. Las configuraciones de
los ambientes se fueron separando y nadie sabe cuál es la buena". Ello se debe a un defecto que también se encuentra aquí y es el hecho de instalar las dependencias desde un archivo distinto al archivo de bloqueo.

# 1.4
Con la intervención se espera mover la métrica "Lead time para cambios" gracias al uso de un caché de dependencias, lo que reduce minutos por ejecución.

# 1.5
Para sustentar que la métrica se movió mediremos la duración de la ejecución del pipeline.

# 4.1
Los valores del proxy después de la intervención: 1m 44s, 1m 22s, 1m 25s
Los valores del proxy antes de la invervención (línea base): 56s, 1m 8s, 1m 11s
Se ve un aumento en los tiempos dado que ahora los jobs se realizan de manera secuencial, además de  de colocar el uso de cache también en "validar" y utilizar el archivo de bloqueo en "publicar". Dado que no estaba permitido cambiar lo ya hecho durante el laboratorio, no ha sido corregido.

# 4.2
Se declaró la versión 1.2.1 dado que no representa una nueva funcionalidad en el código, como sí lo son los commits anteriores: 4e0df78d18cc6cf40e1f5c0e693a2b7c2b37fb97, 0b981cafd7d985f3ca03709db9496339f7ea4443 y b7e44ce6388bba91ebe4d465476531ac6ae40c71

# 4.3
Puede ser que el pipeline se ejecuta ante un push en general, sin limitarlo a la rama main por lo que ante un push a un rama intermedia, el código de dicha rama será publicada, en este caso no se envía a ningún ambiente, pero podría mandarse a producción una versión del código intermedio o de desarrollo.

# 4.4
Se usó la IA del navegador Google para encontrar el args (-Dsonar.qualitygate.wait=true) que hacía falta para que el pipeline espere al resultado de sonarcloud, para generar la función con lógica real de 3.2 y para saber cómo leer el archivo "VERSION" y colocarlo en el nombre del artefacto (tarea 2.4).
