# EDA-Cristiano_Ronaldo
Este documento describe el análisis exploratorio de datos (EDA) realizado sobre un conjunto de datos que registra los goles y eventos asociados a la carrera de un futbolista de élite, presumiblemente Cristiano Ronaldo. El objetivo principal fue identificar patrones de puntuación, asistencia y vulnerabilidad de los rivales utilizando técnicas de agrupación de datos con pandas y visualizaciones interactivas y no convencionales con plotly.express.

#Análisis Detallado de las Gráficas

El análisis se centró en cuatro áreas clave del registro goleador, utilizando gráficos que priorizan la visualización de proporciones y la comparación de rangos:

Goles por Competición Esta visualización, implementada con un Gráfico de Área de Embudo (Funnel Area Chart) o Treemap, muestra la proporción de goles marcados en cada torneo. El área de cada sector es directamente proporcional al total de goles. El análisis confirmó que las competiciones principales, como LaLiga y la UEFA Champions League, dominan el registro goleador, lo que se refleja en la inmensa área que ocupan en el gráfico. Este método ofrece una alternativa visualmente impactante a un gráfico de pastel tradicional para mostrar jerarquía y magnitud.

Asistencias por Club De manera similar al análisis de competiciones, se utilizó un gráfico proporcional para visualizar el total de goles que tuvieron una asistencia por cada club. Se asume que la columna Club en cada fila (gol) representa al equipo que marcó. El gráfico permite comparar rápidamente qué clubes generaron la mayor cantidad de goles asistidos, señalando los entornos de equipo más efectivos en la creación de oportunidades. La magnitud de cada sección representa el volumen absoluto de asistencias generadas mientras el jugador militaba en ese club.

Goles por Oponente El Gráfico de Árbol (Treemap) se empleó para visualizar el total de goles marcados contra cada equipo rival. Esta es una visualización excelente para grandes cantidades de categorías, donde el área de cada rectángulo corresponde al número de veces que ese oponente encajó un gol. La interpretación principal es directa: los rectángulos de mayor tamaño identifican inmediatamente a los oponentes históricamente más vulnerables (como el Sevilla FC y el Atlético Madrid, si están en la parte superior del conteo).

Minuto Histórico Más Débil (Pico de Goles) por Oponente (Gráfico de Dumbbell Adaptado) Esta es la visualización más compleja y reveladora, diseñada para mostrar el minuto pico de vulnerabilidad para cada rival. Se implementó un Gráfico de Dumbbell Adaptado (usando go.Scatter):

La Línea Gris Horizontal en cada fila representa el rango completo de minutos en el que se ha marcado al menos un gol contra ese oponente, dando un contexto de cuándo suelen recibir goles.

El Punto de Color (la "pesa" del dumbbell) marca el minuto exacto en el que ese equipo ha encajado la mayor cantidad de goles en su historial contra el jugador.

El Color y el Tamaño del punto están ligados a la escala de color (ej., de rojo oscuro a amarillo claro), donde los colores más claros indican una mayor cantidad de goles en ese minuto pico. Esto permite comparar qué equipos tienen un "minuto débil" más pronunciado.

En conjunto, este gráfico es una herramienta táctica que permite identificar tendencias temporales (equipos débiles al inicio o al final del partido) y cuantificar el impacto de los minutos más vulnerables para cada rival.
