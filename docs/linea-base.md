# Linea base de ejecucion

Ejecutar el workflow tres veces desde la pestana Actions, con **Run workflow**,
sin modificar ningun archivo del repositorio. Registrar aqui los resultados.

| Ejecucion | Duracion | URL |
|---|---|---|
| 1 | 1m 11s | https://github.com/31adrianpc/INF384-lab2-20212137/actions/runs/34518804679 |
| 2 | 1m 8s | https://github.com/31adrianpc/INF384-lab2-20212137/actions/runs/34519127865 |
| 3 | 56s | https://github.com/31adrianpc/INF384-lab2-20212137/actions/runs/34519567386 |

## Declaracion de uso de IA generativa

Indicar si se utilizaron herramientas de IA generativa para completar este
trabajo previo, cuales, y con que proposito. Adjuntar los prompts utilizados.

Uso de Claude para repasar conceptos y comprender con más detalle el trabajo previo.
Prompts:
En esta parte, al registrarme con mi cuenta de github, Key es una Project Key? El repositorio que el profe quería que forkeemos dice esto.
Otra cosa, desmarco lo de "Automatically import new GitHub repositories"? No se por qué me aparece eso si al registrarme con github, antes de que me aparezca todo esto, me pidió que seleccionará sobre qué repositorios iba a instalar sonarcloud y solo seleccioné el repo forkeado.
1. Justo el último commit del repo dice esto: fix: sonar project key.
2. Al importar el repo en sonarcloud, parece que ya hizo un analisis automatico. No sé si debí haber evitado por lo que dice C.3, o era algo imposible de evitar porque así funciona sonarcloud. Básicamente me salía un botón de importar repo o algo así y luego me salió esta pantalla, selecciona el repo y lo analizó automaticamente.
1. Puedes explicar para qué es el SONAR_TOKEN? si desde github ya seleccioné que repositorios mostrar a sonarcloud y en sonarcloud ya importé el repo, sonarcloud no puede responder al pipeline automaticamente sin necesitar nada?
2. Por qué es necesario borrar el analisis automatico? eso se activa cada vez que se actualice mi repo? es decir, cuando haya una actualización sonarcloud analizará por su cuenta, sin que yo haya disparado el pipeline para que lo haga?
3. Puedes detallar lo del ejercicio de inyección de falla y las 20 líneas?
4. Acá debo crear el token? en token_name coloco SONAR_TOKEN?
5. Mi organization key es lo que puse al inicio no? y no lo que aparece encima de "user" como dice el pdf. porque sino sería "Adrian Picoy", lo cual no coincide con lo que puse al inicio.
6. El project key sí sé que se obtiene de la url. en mi caso sería: 31adrianpc_INF384-lab2-20212137. Aunque mi url es: https://sonarcloud.io/project/overview?id=31adrianpc_INF384-lab2-20212137 y no https://sonarcloud.io/project/information?id=josedelcastillo_INF384-lab2-20050452, que es lo que aparece en el pdf, supongo que es lo mismo no?

