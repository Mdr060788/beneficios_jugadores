📊 De una intuición simple a un sistema basado en datos: 

Rediseñando beneficios con análisis de datos...
Para quienes no me conocen, desde los 6 años juego Pelota a Paleta. Como aficionado a esta disciplina, formo parte de una organización que convoca jugadores de todo el país.
Hace unos meses, nos enfrentamos una solicitud aparentemente simple: aplicar un esquema de beneficios para jugadores que viajen largas distancias a nuestros torneos.

La lógica inicial era directa:
👉 Si el jugador recorría más de 200 km en promedio → recibía un beneficio (bonificación o pase libre).
Parecía justo. Parecía claro. Hasta que decidí analizar los datos con más profundidad...

🚨 Al analizar los datos, apareció un caso que rompió el esquema:
Dos jugadores con UNA SOLA participación de 800 km de distancia.
Técnicamente, según el criterio de "200 km promedio", calificaban para el máximo beneficio.
Pero intuitivamente algo no cerraba:
¿Es justo equiparar una participación aislada con jugadores que viajan 150 km prom. pero participan en más de 10 torneos?
¿Deberíamos premiar solo la distancia, ignorando la constancia y el compromiso real?
Estos outliers no eran un error de datos. Era una señal de que el criterio era demasiado simplista.

🔬 De umbral fijo a índice multidimensional:
En lugar de parchear el caso puntual con excepciones, decidí replantear la métrica completa.
Construí un Índice de Esfuerzo que combina tres dimensiones:

📍 35% - Km totales acumulados (esfuerzo sostenido)
📍 25% - Percentil 90 de distancias (picos de esfuerzo)  
📍 40% - Cantidad de eventos (constancia y compromiso)

El resultado: Un sistema que premia tanto el sacrificio puntual como la dedicación en el tiempo.

📊 Los números no mienten

📌 Método Original (umbral fijo):
23 beneficiados (6.8%)
Criterio: km_prom > 200

🎯 Método Nuevo (índice multidimensional):
27 beneficiados (7.9%)
Criterio: percentil de esfuerzo integral

🔍 Impacto del cambio:
✔️ Correcto beneficiado (ambos métodos benefician): 2
✔️ Correcto NO beneficiado (ambos métodos no benefician): 291

❌ Sobre-beneficiados: 21 jugadores
(Recibían beneficios por alta distancia puntual, pero bajo esfuerzo sostenido)

✅ Sub-beneficiados rescatados: 26 jugadores
(Constancia y esfuerzo real que el método original ignoraba)

✔️ Coincidencias totales entre métodos: 293 jugadores
(2 beneficiados + 291 no beneficiados)

🎯 Tasa de acuerdo entre métodos: 86.2%
(293 de 340 jugadores coinciden en la clasificación)

📈 Resultado clave:
El nuevo método identificó 4 beneficiarios adicionales (+17%) con un perfil de esfuerzo más equilibrado, mientras eliminó asignaciones cuestionables basadas únicamente en distancia promedio.

Para finalizar, definimos escalas de beneficio según el percentil de esfuerzo: 
≥97 → 3 pases
≥95 → 2 pases
≥92 → 1 pase.


💡 Lecciones aprendidas

1️⃣ Los datos no solo validan decisiones, las cuestionan.
Un outlier no es solo ruido: puede ser la señal de que tu modelo es incompleto.

2️⃣ La mejor solución técnica no es la más sofisticada.
Es la que resuelve el problema real, de forma defendible, transparente y justa.
Lo importante es que los datos guíen la decisión, no la justifiquen después de tomarla.

¿Han tenido que replantear algún sistema de incentivos basándose en datos?
¿Aplicarían una métrica distinta a este proyecto?
¡Saludos y buena jornada!

PD: Les dejo el link a un dashboard interactivo para visualizar los resultados y al repo.
Dashboard: https://github.com/Mdr060788/beneficios_jugadores
Repositorio: https://mdr060788.github.io/beneficios_jugadores/

#DataScience #Analytics #DecisionesBasadasEnDatos #BusinessIntelligence #AnalisisdeDatos #PelotaPaleta