# Red-Neuronal-Simple
Este código implementa una red neuronal multicapa desde cero para resolver un problema de clasificación multiclase.
A continuación, se explica cómo funciona:

1. Generación de datos (generar_datos_clasificacion)
Genera datos de entrada para un problema de clasificación multiclase.
Los datos se distribuyen en forma de espirales, con cada clase ocupando una región distinta del espacio.
Cada punto tiene dos características (x1, x2) y pertenece a una clase específica (t).
2. Inicialización de pesos (inicializar_pesos)
Inicializa los pesos y sesgos de la red neuronal con valores aleatorios pequeños.
La red tiene:
Una capa de entrada con 2 neuronas (por las dos características de los datos).
Una capa oculta con un número configurable de neuronas.
Una capa de salida con tantas neuronas como clases.
3. Propagación hacia adelante (ejecutar_adelante)
Calcula las salidas de la red neuronal para un conjunto de entradas.
Utiliza:
ReLU como función de activación en la capa oculta.
Una función de activación lineal en la capa de salida.
Devuelve las activaciones intermedias y finales.
4. Clasificación (clasificar)
Clasifica los datos de entrada asignándolos a la clase con el puntaje más alto en la salida de la red.
5. Entrenamiento (train)
Entrena la red neuronal utilizando el algoritmo de backpropagation:
Propagación hacia adelante: Calcula las salidas de la red.
Cálculo de la pérdida:
Utiliza la función de pérdida de entropía cruzada.
Calcula las probabilidades de las clases usando softmax.
Propagación hacia atrás:
Calcula los gradientes de la pérdida con respecto a los pesos y sesgos.
Ajusta los pesos y sesgos usando gradiente descendente.
Validación (opcional):
Si se habilita, evalúa la pérdida en un conjunto de validación y detiene el entrenamiento si la pérdida de validación deja de mejorar.
6. Visualización
Durante el entrenamiento, grafica la pérdida en el conjunto de entrenamiento y, si corresponde, en el conjunto de validación.
También puede graficar los datos generados para mostrar su distribución.
7. Ejecución principal
La función iniciar:
Genera los datos de entrenamiento.
Inicializa los pesos de la red.
Entrena la red neuronal.
Evalúa la precisión en los datos de entrenamiento y prueba.
Al final, imprime la precisión de la red en los datos de prueba.
