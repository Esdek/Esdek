# Esdek - Gestión de producción

## Consideraciones iniciales

Esdek ha decidido fabricar los tres productos que se presentan a continuación:

![1](Soporte.png)
![2](Bandeja.png)
![3](Mesa.png)

Estos productos comparten más del 70% de sus materias primas, de acuerdo con la tabla que se presenta a continuación:
![4](TablaMateriales.png)

Adicionalmente, se identifican los siguientes procesos necesarios para la fabricación de cada producto:
![5](TablaProcesos.png)

Dado que se comparten una gran cantidad de procesos que pueden ser realizados con las mismas máquinas y equipos de manufactura, se decide fabricar los tres productos de forma simultánea.

### Entrada y salida de material

Con una producción mensual de 200 unidades de cada producto, se requiere:
- 67 láminas de MDF 1.2 x 185 x 244 cm (se obtienen 3 sets de 3 productos de cada lámina)
- 200 tubos de aluminio de 0.5mm x 1m (se obtiene 1 set de 3 productos de cada tubo)
- 800 cajas de cartón
- 61 litros de laca
- 21 litros de pintura
- 20 kg pegamento PVAc (100g por cada set de productos)
- 9600 tarugos de madera 6 x 30 mm (48 por cada set de productos)
- 3200 tornillos #7 x 3/4" (16 por cada set de productos)

Como salida, se tiene mensualmente una entrega de 2400 productos, 800 de cada tipo.

### Tiempos estimados de producción por producto (planta original)

<br/>  
Para el corte manual se realiza con una sierra sin fin. En este proceso, un trabajador suele cortar a una velocidad aproximada de 0.03 m/s. El tiempo entre cortes puede ser de hasta 30 segundos. Para producir un productos se requieren realizar aproximadamente 14 cortes, y la longitud de corte calculada por producto es de 6.6m. Teniendo en cuenta el tiempo que se tarda pegando la plantilla de corte sobre el material (calculado en 180 segundos), y el tiempo que se tarda retirando las piezas tras el corte (calculado en 120 segundos) se obtienen los tiempos:
<br/>  
<br/> Tiempo de corte: 6.6/0.03 = 220 segundos
<br/> Th: 14 * 30 = 420 segundos
<br/> Tiempo de ciclo: 640 segundos
<br/> Tiempo de setup: 180 segundos
<br/> Tiempo de recuperación: 120 segundos
<br/> No. Operarios: 1
<br/> No. Maquinas: 1
<br/>  
<br/> Adicionalmente, sabiendo que la vida útil de la sierra es de 12 horas de corte, se encuentra:
<br/> MTBF: 43200 segundos
<br/> MTTR: 600 segundos
<br/> Disponibilidad: 98.6%

<br/>  
<br/>  
En el proceso de pintado (dos capas), un operario suele demorarse 150 segundos por metro cuadrado. Se tiene en cuenta que son aproximadamente 14 piezas por producto, con un área a a pintar de 0.86 metros cuadrados (0.43 cada lado).Se considera un tiempo de setup de 120 segundos que incluye preparar la pintura y herramientas, así como disponer las piezas. Se tiene en cuenta también que para cada pieza, el proceso de pintado de bordes tarda en promedio 15 segundos. Además, se otorgan 15 minutos de secado por cada cara , pero durante este tiempo se puede pintar una cara del siguiente producto. Haciendo los cálculos, se encuentra que esto equivale a un tiempo de recuperación total por producto de 928 segundos.
<br/>  
<br/> Tiempo de pintado: 0.86*150 = 129 segundos
<br/> Tiempo de pintado (bordes): 14*15 = 210 segundos
<br/> Tiempo de ciclo: 339 segundos
<br/> Tiempo de setup: 120 segundos
<br/> Tiempo de recuperación: 928 segundos
<br/> No. Operarios: 1
<br/> No. Maquinas: 1
<br/>  
<br/> La pistola de pintura debe limpiarse cada turno, es decir, tras 7.5 horas de uso. El tiempo de limpiado es de aproximadamente 15 minutos. Así, obtenemos:
<br/> MTBF: 27000 segundos
<br/> MTTR: 900 segundos
<br/> Disponibilidad: 96.8%

<br/>  
<br/>  
Para el lacado, se tienen los mismos tiempos de cambio de pieza, setup, y recuperación de la operación de pintado. En cuanto al tiempo de lacado, es de 125 segundos por metro cuadrado. El área es la misma, de donde resulta:
<br/>  
<br/> Tiempo de lacado: 0.86*125 = 108 segundos
<br/> Tiempo de lacado (bordes): 14*15 = 210 segundos
<br/> Tiempo de ciclo: 318 segundos
<br/> Tiempo de setup: 120 segundos
<br/> Tiempo de recuperación: 933 segundos
<br/> No. Operarios: 1
<br/> No. Maquinas: 1
<br/>  
<br/> La pistola para lacar tiene las mismas condiciones de mantenimiento que la pistola de pintura, así:
<br/> MTBF: 27000 segundos
<br/> MTTR: 900 segundos
<br/> Disponibilidad: 96.8%

<br/>  
<br/>  
El corte de tubos de metal se realiza con una tronzadora, donde el operario es quien maneja las distancias y realiza el corte. Para cada set de productos se necesitan 18 tubos de 2.4cm, 1 de 26cm y 1 de 7.2cm. El tiempo de cada corte es de 3 segundos, y el de manipulación entre cortes es de 6 segundos. El setup time está dado por el tiempo de encendido de la máquina y de ubicación del tubo, y se estima en 20 segundos. El tiempo de recuperación se estima en 10 segundos. Así, resulta:
<br/>  
<br/> Bandeja (16 tubos):
<br/> Tiempo de ciclo: 144 segundos
<br/> Tiempo de setup: 20 segundos
<br/> Tiempo de recuperación: 10 segundos
<br/>  
<br/> Soporte (3 tubos):
<br/> Tiempo de ciclo: 27 segundos
<br/> Tiempo de setup: 20 segundos
<br/> Tiempo de recuperación: 10 segundos
<br/> 
<br/> No. Operarios: 1
<br/> No. Maquinas: 1
<br/> La limpieza de la tronzadora se realiza cada turno de trabajo, es decir, tras 7.5 horas de corte. El mantenimiento, que comprende remoción de viruta, limpieza y engrasado semanal, tarda aproximadamente 10 minutos:
<br/> MTBF: 27000 segundos
<br/> MTTR: 600 segundos
<br/> Disponibilidad: 97.8%

<br/>  
<br/>  
El doblez de tubos de metal únicamente se necesita para un tubo (el de 26 cm). Se realizan manualmente 4 dobleces, cada uno tarda 2 segundos, y el tiempo de medición y manipulación del tubo se estima en 18 segundos entre dobleces. Debido a que es solo una pieza que se dobla con soportes mecánicos, tanto el tiempo de setup como de recuperación son de solo 15 segundos cada uno.
<br/>  
<br/> Tiempo de doblez: 2*4 = 8 segundos
<br/> Th: 4 * 18 = 72 segundos
<br/> Tiempo de ciclo: 140 segundos
<br/> Tiempo de setup: 15 segundos
<br/> Tiempo de recuperación: 15 segundos
<br/> No. Operarios: 1
<br/> No. Maquinas: 0
<br/> El proceso es manual y no se requiere realizar mantenimiento a ninguna máquina. Por lo anterior, se considera una disponibilidad del 100%.

<br/>  
<br/>  
El taladrado ocupa 6 segundos por cada agujero. A esto se le suma por cada agujero 20 segundos de medición y marcación, y 10 segundos de manipulación de la herramienta (taladro). También se considera que se cambia dos veces la broca, en lo cual el operario tarda 45 segundos cada vez. La cantidad aproximada de agujeros por producto es de 58. Se supone un tiempo de setup de 120 segundos en el que se conecta el taladro y se ajusta la broca, así como un tiempo de recuperación de 20 segundos, en el que se desconecta la herramienta.
<br/>  
<br/> Tiempo de taladrado: 6*58 = 348 segundos
<br/> Th: 20 * 58 = 1160 segundos
<br/> Tth: 10*58 + 2*45 = 670 segundos
<br/> Tiempo de ciclo: 2178 segundos
<br/> Tiempo de setup: 120 segundos
<br/> Tiempo de recuperación: 20 segundos
<br/> No. Operarios: 1
<br/> No. Maquinas: 1
<br/> El mantenimiento del taladro se realiza cada 100 horas de uso, y tarda aproximadamente una hora (limpieza y lubricación):
<br/> MTBF: 360000 segundos
<br/> MTTR: 3600 segundos
<br/> Disponibilidad: 99.0%

<br/>  
<br/>  
El proceso de empacado requiere que el trabajador empaque todos los materiales necesarios para que el usuario arme el mueble. Esto incluye las piezas de madera (50 segundos por producto), los tubos metálicos cortados (30 segundos para la bandeja, 20 segundos para el soporte, 10 segundos para la mesa), los tarugos y tornillos que se empacan junto al pegante en una bolsa (30 segundos por producto). También se suman por producto 90 segundos que tarda el operario sellando cada caja. El setup time se establece en 60 segundos y corresponde al tiempo en que el operario prepara la caja y las partes, y el recovery time es de tan solo 15 segundos, pues es el tiempo en el que el operario desplaza las cajas para dar espacio a la siguiente operación de empacado.
<br/>  
<br/> Bandeja:
<br/> Tiempo de empacado: 50 + 30 + 30 + 90 = 200 segundos
<br/> Tiempo de ciclo: 200 segundos
<br/> Tiempo de setup: 60 segundos
<br/> Tiempo de recuperación: 15 segundos
<br/> No. Operarios: 1
<br/> No. Maquinas: 0
<br/>  
<br/> Soporte:
<br/> Tiempo de empacado: 50 + 20 + 30 + 90 = 190 segundos
<br/> Tiempo de ciclo: 190 segundos
<br/> Tiempo de setup: 60 segundos
<br/> Tiempo de recuperación: 15 segundos
<br/> No. Operarios: 1
<br/> No. Maquinas: 0
<br/>  
<br/> Mesa:
<br/> Tiempo de empacado: 50 + 10 + 30 + 90 = 180 segundos
<br/> Tiempo de ciclo: 180 segundos
<br/> Tiempo de setup: 60 segundos
<br/> Tiempo de recuperación: 15 segundos
<br/> No. Operarios: 1
<br/> No. Maquinas: 0
<br/>  
<br/> El proceso de empacado es manual y no se requiere realizar mantenimiento a ninguna máquina. Por lo anterior, se considera una disponibilidad del 100%.

<br/>  
<br/>  
El proceso de paletizado ocupa un setup time de 40 segundos en que el operario prepara la estiba, no se considera necesario ningún recovery time, y para cada producto el operario tarda 20 segundos ubicándolo, de donde resulta:
<br/>  
<br/> Tiempo de ciclo: 20 segundos
<br/> Tiempo de setup: 40 segundos
<br/> Tiempo de recuperación: 0 segundos
<br/> No. Operarios: 1
<br/> No. Maquinas: 0
<br/> El proceso es manual y no se requiere realizar mantenimiento a ninguna máquina. Por lo anterior, se considera una disponibilidad del 100%.
<br/>

### Tiempos estimados de producción (planta automatizada)

<br/>  
<br/>  
Tras automatizar el corte empleando una máquina de corte láser, el tiempo de corte para los tres productos es de 339 segundos (según indica un programa simulador de corte láser, con las condiciones de material adecuadas). El setup time es el tiempo que el operario tarda ubicando la lámina de madera e iniciando el programa, lo que se estima en 60 segundos. El tiempo que el operario tarda retirando las piezas está considerado en el tiempo de setup del pintado automatizado, por lo que el tiempo de recuperación es cero. Si se considera que el tiempo de corte es el mismo para cada producto, se encuentra:
<br/>  
<br/> Tiempo de ciclo: 113 segundos
<br/> Tiempo de setup: 60 segundos
<br/> Tiempo de recuperación: 0 segundos
<br/> No. Operarios: 1
<br/> No. Maquinas: 1
<br/> El mantenimiento de la máquina de corte se realiza al finalizar cada turno, consiste en retirar el polvo y resíduos de grabado y limpiar los espejos y la lente, lo que tarda aproximadamente 10 minutos:
<br/> MTBF: 27000 segundos
<br/> MTTR: 600 segundos
<br/> Disponibilidad: 97.8%

<br/>  
<br/>  
Para los procesos de lacado y pintado automatizados, se tiene un tiempo de proceso de 47 segundos para cada set de tres productos por cada cara. Se considera un tiempo de secado por cara de 15 minutos, un setup time de un minuto (tiempo de transporte de piezas de corte láser a pintado, o de pintado a lacado), y un tiempo de 150 segundos para darle la vuelta a las piezas. Adicionalmente, mientras se seca una cara de un set de productos se puede pintar o lacar una cara del siguiente. Haciendo los cálculos, se obtiene para cada producto:
<br/>  
<br/> Tiempo de ciclo: 94/3 + 150/3 = 81 segundos
<br/> Tiempo de setup: 20 segundos
<br/> Tiempo de recuperación: 176 segundos
<br/> No. Operarios: 1
<br/> No. Maquinas: 1
<br/>  


<br/>  
<br/>  
La información sobre el proceso automatizado de taladrado con robot aún no se ha calculado, pues se requiere primero programar la rutina en el robot. Se puede afirmar desde ahora que se empleará un robot y un operario para el mismo.
<br/>  
<br/> No. Operarios: 1
<br/> No. Maquinas: 1
<br/> Un robot ABB requiere una inspección anual, que tarda aproximadamente una hora, y cada tres años esta inspección va en conjunto con cambio de aceite, baterías y limpieza general, lo que lleva aproximadamente 4 horas.
<br/> MTBF: 31536000 segundos
<br/> MTTR: 7200 segundos
<br/> Disponibilidad: 99.8%

<br/>  
<br/>  
El proceso automatizado de corte de tubos, pese a que no se tiene aún información certera sobre sus tiempos, se estima que tarda 3 segundos en realizar los 19 cortes más pequeños, y 7 segundos en el corte largo. Teniendo un setup time y recovery time de 30 segundos, obtenemos:
<br/>  
<br/> Bandeja (16 tubos):
<br/> Tiempo de ciclo: 3*16 = 48 segundos
<br/> Tiempo de setup: 30 segundos
<br/> Tiempo de recuperación: 30 segundos
<br/>  
<br/> Soporte (3 tubos):
<br/> Tiempo de ciclo: 3*3 + 7 = 16 segundos
<br/> Tiempo de setup: 30 segundos
<br/> Tiempo de recuperación: 30 segundos
<br/> No. Operarios: 1
<br/> No. Maquinas: 1

### Cálculo del Takt time

Se considera una cantidad de 20 días de trabajo por mes. Cada día se trabaja un turno, el cual es de 8 de la mañana a 5 de la tarde. Se tiene en cuenta un tiempo de almuerzo de una hora, así como dos descansos de 15 minutos cada uno. Así, se encuentra:
<br/> Tiempo disponible al día: 3600*(9-1-0.5) = 27000 segundos

<br/>  
<br/> Con una demanda de 40 unidades de cada producto por día, se obtiene el takt time, que es igual para los tres productos (que se fabrican simultáneamente):

<br/> T = 27000/40 = 675 segundos/producto

<br/> Es decir, cada 675 segundos debe estar listo un nuevo set de productos para producir la cantidad que se necesita para satisfacer la demanda.

### Cálculo de KPI

El cálculo de los KPI se encuentra en el archivo adjunto de Excel, llamado "GestionProduccion.xslx".

### VSM

A continuación se presenta el VSM creado a partir de la información mencionada.

![6](VSMpreautomatizacion.png)