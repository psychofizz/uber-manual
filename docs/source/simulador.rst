Simulador
=========

¿Cómo funciona?
---------------

El simulador, tal como está implementado a la fecha de redacción de este documento, funciona de la siguiente manera:

1. **Inicio de la simulación:** Al comenzar, el simulador localiza un pasajero. Se ubica en la posición de este pasajero para recogerlo, lo que genera un pequeño costo operativo.

2. **Recogida del pasajero:** Una vez que el pasajero o los pasajeros se suben al vehículo, el simulador encuentra una ruta óptima entre el punto de partida y el destino deseado por el pasajero.

3. **Uso de la tecnología de Google Maps:** Para determinar la mejor ruta, se utiliza la API de JavaScript de Google Maps. Esta API proporciona información valiosa sobre la ruta óptima, el tiempo estimado de viaje y la distancia entre los dos puntos. Sin embargo, el acceso a datos de tráfico en tiempo real puede ser limitado.

4. **Consideración del tráfico:** Para mitigar la dificultad de acceder a datos de tráfico durante el día, se ha implementado una tabla que toma en cuenta las variaciones del tráfico según la hora del día.

5. **Estimación de precios:** Con la información obtenida, como distancia y duración, se calcula un precio estimado del viaje. Este precio es considerado como el ingreso.

6. **Cálculo de gastos:** Luego, se calcula el gasto operativo del vehículo. Para hacer esto de manera precisa, se solicita al usuario que ingrese el valor de km/L del vehículo, lo que permite estimar el consumo real de combustible.

7. **Suma de ingresos y gastos:** Los valores de ingreso y gasto se van sumando al total del día.

8. **Finalización del viaje:** Después de completar el transporte del pasajero, visible en el mapa de Google, el conductor realiza una breve ruta de reposicionamiento antes de comenzar el ciclo nuevamente. Este proceso se repite hasta que se alcanza la hora de finalización del conductor de Uber.

¿Cómo se calcula el precio?
----------------------------

Para calcular el precio, la API de Google Maps debe devolver valores clave como la distancia y la duración del viaje. Con estos datos y la hora de la simulación, se determina un precio estimado.

Para lograr una estimación precisa, se han tomado lecturas de viajes reales con Uber a varias ubicaciones en Tegucigalpa. Estas lecturas sirven como referencia para ajustar el modelo a la realidad local.

En cuanto a otros países, se puede adaptar el simulador ajustando las tablas de tráfico y los valores de referencia para las tarifas, asegurando que las estimaciones reflejen las condiciones locales de cada región.
