<b> CHURN MODEL - KKBOX ENTERPRISE</b>

* <b>KKBOX</b> es el servicio de transmisión de música líder en Asia, y cuenta con la biblioteca de música Asia-Pop más completa del mundo con más de 30 millones de canciones.

* El desafío consiste en desarrollar un algoritmo que prediga si un usuario de suscripción dejará de usar el servicio, esto, con un conjunto de testeo (Marzo 2017) de la empresa <b>KKBOX</b> .
 
* Para un negocio de suscripción, predecir con precisión el abandono es fundamental para el éxito a largo plazo. Incluso pequeñas variaciones en la rotación pueden afectar drásticamente las ganancias.

* La métrica de evaluación es <b>Log Loss</b>, donde <b>N</b> es el número de observaciones, Log es el logaritmo natural, <b>yi</b> es el objetivo binario y  <b>pi</b> es la probabilidad de predecir que <b>yi es igual a 1</b>

<p align="center">
<img src="./logloss.png" >
</p>


1. <b>Sprint 1: Datos transformados I</b>

Crear funciones que permitan construir los siguientes features para cada msno:
Recencia: cantidad de días desde el último evento de la tabla user_logs.csv
Frecuencia: cantidad de eventos entre los últimos N y N+M días de la tabla user_logs.csv
Money: cantidad de dinero pagado entre los últimos N y N+M días de la tabla transactions.csv
Utilizar valores de N y M que capturen comportamiento en última semana, últimas 2 semanas, último mes y últimos 2 meses (queda abierto si se quiere utilizar más valores).

<a href="./DBAnalytics_EDA_01.ipynb">DBAnalytics_EDA_01</a>: El objetivo de este notebook es realizar una primera aproximación a los dataset de KKBOX, para ello se utilizo el <a href="https://arxiv.org/pdf/1408.2041.pdf">framework de turi Graphlab</a> el que permite manejo de archivos de gran volumen, despues de revisar sus principales caracteristicas, se procedio a guardar los archivos en el formato nativo de Graphlab para en analisis EDA mas en detalle y con mejor velocidad de lectura.

<a href="./DBAnalytics_EDA_02.ipynb">DBAnalytics_EDA_02</a>: El objetivo de este notebook es entender en detalle las caracteristas de los usuarios que suscribieron el servicio de KKBOX, para ello se exploraran todos los dataset disponibles por la empresa.




