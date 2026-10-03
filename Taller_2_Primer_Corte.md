# UNIVERSIDAD PEDAGÓGICA Y TECNOLÓGICA DE COLOMBIA
## INGENIERÍA DE SISTEMAS Y COMPUTACIÓN
## SIMULACIÓN DE COMPUTADORES
# TALLER

Desarrollar en C# una aplicación que simule el movimiento parabólico de un objeto a partir de un conjunto de condiciones iniciales. La aplicación debe implementar el modelo matemático del movimiento, representar gráficamente la trayectoria y permitir analizar las principales variables cinemáticas durante la simulación.

Para este ejercicio se desprecia la resistencia del aire. La aceleración gravitacional se considera constante y dirigida verticalmente hacia abajo.

## Condiciones iniciales y modelo matemático

La aplicación debe permitir que el usuario configure, antes de iniciar cada simulación, como mínimo los siguientes parámetros:

- Posición horizontal inicial.
- Altura inicial.
- Magnitud de la velocidad inicial.
- Ángulo de lanzamiento, medido respecto al eje horizontal.
- Valor de la aceleración gravitacional.

A partir de la magnitud y el ángulo de la velocidad inicial, el programa debe calcular sus componentes en x y y. (Math)

## Variables y métricas de la simulación

Durante la ejecución, la aplicación debe mostrar en tiempo real:

- Tiempo transcurrido.
- Posición actual x(t) y y(t).
- Velocidad horizontal vx(t).
- Velocidad vertical vy(t).
- Magnitud de la velocidad.
- Ángulo instantáneo del vector velocidad respecto al eje horizontal.

El programa también debe calcular y presentar:

- Tiempo total de vuelo.
- Altura máxima alcanzada.
- Instante en el que se alcanza la altura máxima.
- Posición horizontal correspondiente a la altura máxima.
- Desplazamiento horizontal total o alcance.
- Velocidad en el punto de máxima altura:
  - componente horizontal;
  - componente vertical;
  - magnitud;
  - ángulo.
- Velocidad inmediatamente antes del impacto con el suelo:
  - componente horizontal;
  - componente vertical;
  - magnitud;
  - ángulo.

## Comparación entre modelo teórico y simulación

La aplicación debe diferenciar entre los resultados obtenidos analíticamente mediante las ecuaciones del modelo y los resultados registrados durante la ejecución de la simulación.

Como mínimo, se deben comparar:

- Tiempo total de vuelo.
- Altura máxima.
- Tiempo hasta alcanzar la altura máxima.
- Alcance horizontal.

Para cada variable se debe presentar el valor teórico, el valor obtenido mediante la simulación y su diferencia.

Esta comparación debe permitir analizar el efecto que tiene el tamaño del intervalo temporal Δt sobre los resultados obtenidos.

## Representación gráfica

Durante o al finalizar la simulación, la aplicación debe generar las siguientes gráficas:

- y vs. t: posición vertical respecto al tiempo.
- x vs. t: posición horizontal respecto al tiempo.
- y vs. x: trayectoria del objeto.
- vx vs. t: velocidad horizontal respecto al tiempo.
- vy vs. t: velocidad vertical respecto al tiempo.
- |v| vs. t: magnitud de la velocidad respecto al tiempo.
- θ vs. t: ángulo del vector velocidad respecto al tiempo.

Las gráficas deben incluir identificación de los ejes y sus respectivas unidades. Los puntos correspondientes a la altura máxima, impacto y rebotes deben poder identificarse visualmente cuando corresponda.

## Objetivo y colisiones

Al iniciar una nueva simulación, el programa debe generar aleatoriamente un objetivo fijo horizontal dentro del escenario.

El programa deberá determinar automáticamente si la trayectoria del objeto intersecta el objetivo.

Si ocurre una colisión:

1. Se debe registrar el instante y la posición de la colisión.
2. Se deben registrar las componentes de la velocidad inmediatamente antes del impacto.
3. El objeto debe realizar un rebote.
4. Después del rebote continuará su movimiento hasta colisionar con el suelo.
5. Al colisionar con el suelo deberá realizar un segundo rebote.
6. Después del segundo rebote, el movimiento continuará hasta que el objeto vuelva a alcanzar el suelo, momento en el cual finalizará la simulación.

Para simplificar el modelo, en cada rebote las componentes de la velocidad deberán actualizarse de manera que la magnitud correspondiente se reduzca en un 40 %. La componente vertical deberá cambiar de sentido como consecuencia del rebote.

Los cambios producidos por las colisiones deben reflejarse tanto en la animación como en las gráficas.

La aplicación debe almacenar, para cada colisión:

- Tiempo.
- Posición x,y.
- vx antes y después del impacto.
- vy antes y después del impacto.
- Magnitud y ángulo de la velocidad antes y después del impacto.

## Interfaz y funcionamiento

La aplicación debe permitir:

- Ingresar y modificar las condiciones iniciales.
- Iniciar una simulación.
- Pausar y continuar la ejecución.
- Reiniciar la simulación.
- Ejecutar nuevamente el modelo con otros parámetros.
- Visualizar la animación del movimiento en el plano.
- Consultar las variables actuales durante la ejecución.
- Consultar los resultados finales.
- Visualizar las gráficas solicitadas.

La representación gráfica debe conservar una relación coherente entre las coordenadas del modelo matemático y las coordenadas utilizadas para dibujar la animación en pantalla. Las unidades físicas del modelo no deben confundirse con píxeles.

## Consideraciones

El modelo utilizado en este taller supone:

- Aceleración gravitacional constante.
- Ausencia de resistencia del aire.
- Movimiento en dos dimensiones.
- Objeto tratado como una partícula.
- Ausencia de fuerzas externas diferentes a la gravedad durante el vuelo.
- Pérdida del 40 % de la magnitud indicada de la velocidad durante los rebotes.

Los equipos pueden definir libremente la apariencia visual del escenario, el objeto y el objetivo.

Sin embargo, la representación gráfica debe corresponder con los valores calculados por el modelo y no con una trayectoria previamente definida mediante una animación.

## Rúbrica de evaluación

| Componente | Porcentaje |
|---|---|
| Implementación del modelo matemático, condiciones iniciales y cálculos | 25 % |
| Gráficas y representación de resultados | 20 % |
| Detección de colisiones, rebotes y registro de eventos | 25 % |
| Interfaz, animación y presentación de la aplicación | 20 % |
| Comparación entre resultados teóricos y simulados | 10 % |

## Entrega

El taller se desarrollará en equipos de máximo 4 estudiantes.

No se pueden generar controles por código. No se pueden modificar propiedades visuales por código.

Incluir en la interfaz una etiqueta (label) con los nombres de los integrantes.

Cada equipo deberá entregar el proyecto completo en C#, incluyendo el código fuente y todos los recursos necesarios para ejecutar la aplicación.

Copia en código (total o parcial) nota igual a cero.

**Fecha de entrega:** octubre 5, 8am (lunes semana 9).
