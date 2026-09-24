**Grupo: Algoritmos 3 y 4 (Encontrar el Máximo y Encontrar el Mínimo)**

* **Pregunta 1:** ¿Por qué la variable de inicialización se define utilizando el primer elemento del arreglo en lugar de un valor externo arbitrario?
* **Respuesta 1:** Se define utilizando el primer elemento porque asegura que, al evaluar el subarreglo inicial de un solo elemento, este constituya trivialmente su propio extremo, validando la inicialización del invariante sin depender de valores fuera del conjunto de datos.


* **Pregunta 2:** ¿De qué manera afecta a la fase de mantenimiento si el extremo buscado se ubica en la primera posición del arreglo?
* **Respuesta 2:** La variable que almacena el extremo no se actualiza durante el bucle porque la condición de reemplazo no se cumple, preservando el estado del invariante de forma intacta hasta la terminación.



**Algoritmo 13: Selection Sort**

* **Pregunta 1:** ¿Por qué la ejecución completa del algoritmo garantiza realizar un máximo de $n-1$ intercambios?
* **Respuesta 1:** Porque se realiza estrictamente un solo intercambio al finalizar cada iteración del bucle externo, posicionando el mínimo del subarreglo restante directamente en su ubicación final definitiva.


* **Pregunta 2:** ¿Cómo se demuestra el ordenamiento total del arreglo mediante el invariante en la fase de terminación?
* **Respuesta 2:** Al finalizar el bucle, el subarreglo procesado de longitud $n-1$ está ordenado y todos sus elementos son menores o iguales al único elemento restante, lo que por transitividad demuestra el orden total de la estructura.



**Algoritmo 15: Quick Sort**

* **Pregunta 1:** Durante el procedimiento de partición, ¿qué garantiza la fase de mantenimiento cuando se evalúa un elemento mayor al pivote?
* **Respuesta 1:** El algoritmo no ejecuta ninguna modificación posicional, dejando al elemento en la región derecha de evaluación y preservando la separación estricta requerida por el invariante.


* **Pregunta 2:** ¿Bajo qué condiciones posicionales específicas se produce el peor caso de complejidad temporal de $O(n^2)$ sin el uso de optimizaciones?
* **Respuesta 2:** El peor caso de complejidad ocurre ante particiones altamente desequilibradas, específicamente cuando la estructura ya se encuentra ordenada o en orden inverso y el pivote es seleccionado en un extremo.



**Algoritmo 14: Merge Sort**

* **Pregunta 1:** ¿Cuál es la justificación lógica del invariante durante la inicialización del caso base del procedimiento recursivo?
* **Respuesta 1:** Cuando los índices cumplen la condición de que el subarreglo se reduce a cero o a un elemento, se considera lógicamente ordenado de forma trivial, validando la afirmación inicial sin requerir operaciones adicionales.


* **Pregunta 2:** En el procedimiento de fusión, ¿cómo mantiene el bucle el ordenamiento relativo de los elementos procesados?
* **Respuesta 2:** El algoritmo selecciona secuencialmente el elemento menor entre los dos subarreglos disponibles, garantizando que cada inserción preserve el orden relativo frente a los elementos restantes.



**Algoritmo 8: Invertir un Arreglo**

* **Pregunta 1:** ¿Por qué la condición de terminación del bucle iterativo ocurre de forma exacta en la mitad de la longitud del arreglo?
* **Respuesta 1:** Porque en esa iteración específica todos los pares simétricos de la estructura han sido intercambiados en su espacio de memoria, completando la inversión sin requerir un doble procesamiento que revierta los cambios.


* **Pregunta 2:** ¿Cómo procesa la lógica del invariante un arreglo cuya capacidad corresponde a una cantidad impar de elementos?
* **Respuesta 2:** El elemento ubicado en la posición central matemática no experimenta movimientos ni intercambios, manteniendo la validez del invariante aplicada exclusivamente sobre los elementos situados en los extremos simétricos.



**Algoritmo 6: Verificar Arreglo Ordenado**

* **Pregunta 1:** ¿Qué condición de evaluación específica interrumpe el análisis del invariante antes de recorrer la totalidad de la estructura?
* **Respuesta 1:** La evaluación finaliza anticipadamente retornando falso al detectar una pareja consecutiva donde el primer elemento posee un valor estrictamente mayor al segundo.


* **Pregunta 2:** ¿Por qué la evaluación del invariante se mantiene afirmativa cuando el arreglo procesa elementos duplicados consecutivos?
* **Respuesta 2:** Porque la condición de validación algorítmica exige un ordenamiento no decreciente, lo cual permite igualdades posicionales continuas y valida la ejecución sin interrumpir el bucle.



**Algoritmo 9: Máximo Subarreglo (Kadane)**

* **Pregunta 1:** Durante la fase de mantenimiento, ¿qué determinación binaria modela la actualización algorítmica de la variable de suma actual?
* **Respuesta 1:** Modela la determinación de reiniciar la sumatoria exclusivamente a partir del elemento en curso, o de anexar dicho elemento al cálculo óptimo proveniente del subarreglo continuo anterior.


* **Pregunta 2:** Si la totalidad de los datos de entrada se compone de valores negativos, ¿cuál es el estado de evaluación del invariante en la etapa de terminación?
* **Respuesta 2:** La fase de terminación concluye identificando individualmente al elemento de valor menos negativo, el cual constituye por definición el subarreglo óptimo de longitud unitaria.



**Algoritmo 7: Suma de un Arreglo**

* **Pregunta 1:** ¿Cómo se sustenta la validez formal del invariante en la etapa previa a ingresar a la primera iteración del bucle?
* **Respuesta 1:** La variable de acumulación se inicializa en cero, lo que equivale algebraicamente al concepto de una suma vacía sobre un conjunto sin elementos, certificando la premisa inicial.


* **Pregunta 2:** ¿Qué actualización experimenta la declaración del invariante durante el mantenimiento al avanzar el índice de control?
* **Respuesta 2:** Al integrar el valor del índice en curso, el estado acumulador se actualiza para representar la sumatoria formal exacta desde la posición inicial hasta el límite actual del ciclo.



**Algoritmo 5: Verificar Elementos Positivos**

* **Pregunta 1:** ¿Bajo qué principio de lógica matemática se aprueba la inicialización del invariante al comenzar con un rango de índices vacío?
* **Respuesta 1:** Se aprueba porque la validación recae sobre un conjunto carente de elementos, lo que da como resultado una afirmación vacuamente verdadera.


* **Pregunta 2:** ¿Qué consecuencia algorítmica genera la evaluación de un elemento numérico equivalente a cero durante el mantenimiento?
* **Respuesta 2:** El procesamiento detiene la ejecución iterativa por incumplimiento de la regla de evaluación estrictamente positiva, finalizando el mantenimiento de forma inmediata y emitiendo un retorno negativo.



**Algoritmo 12: Insertion Sort**

* **Pregunta 1:** ¿Por qué la proposición del invariante en el bucle principal omite la inclusión y el procesamiento de la primera posición del arreglo?
* **Respuesta 1:** Porque el subconjunto inicial conformado exclusivamente por el elemento de la primera posición se asume lógicamente ordenado por definición técnica, cumpliendo la etapa de inicialización directamente.


* **Pregunta 2:** ¿Qué instrucción específica del mantenimiento permite asegurar la propiedad de estabilidad posicional al operar con elementos duplicados?
* **Respuesta 2:** La estabilidad se asegura mediante el desplazamiento condicional que afecta exclusivamente a los elementos que superan de forma estricta el valor de referencia de la clave, conservando intacto el orden original de entrada para las igualdades.



**Algoritmo 2: Contar Ocurrencias de x**

* **Pregunta 1:** ¿Cuál es la respuesta de la fase de mantenimiento cuando el elemento analizado difiere lógicamente del parámetro objetivo de búsqueda?
* **Respuesta 1:** La variable acumuladora de recuento permanece inalterada, lo que consolida y mantiene la exactitud de los valores calculados en relación con el volumen de posiciones previamente escrutadas.


* **Pregunta 2:** ¿Bajo qué características técnicas la complejidad espacial de este procedimiento se determina como constante o de orden $O(1)$?
* **Respuesta 2:** Se determina bajo el fundamento de que su ejecución consume únicamente memoria orientada a variables de control acumulativas, independientemente de la longitud paramétrica del arreglo.



**Algoritmo 10: Suma Máxima de Ventana Fija**

* **Pregunta 1:** ¿Qué diseño aritmético incorporado en la etapa de mantenimiento permite estabilizar la complejidad temporal en un orden lineal?
* **Respuesta 1:** La sumatoria asociada a la ventana de medición se actualiza añadiendo el elemento entrante al rango y restando el elemento saliente del límite opuesto, limitando el proceso a operaciones de costo constante por ciclo.


* **Pregunta 2:** ¿Qué ejecución reporta el algoritmo frente al caso límite en el que la longitud de la ventana es idéntica a la capacidad máxima del arreglo?
* **Respuesta 2:** El mecanismo de bucle diseñado para el deslizamiento es omitido completamente por el flujo, lo que deriva en el retorno directo de la sumatoria precalculada en la fase inicial como ventana única.



**Algoritmo 11: Bubble Sort**

* **Pregunta 1:** Una vez concluido un ciclo correspondiente al bucle delimitador externo, ¿qué validación estructural certifica la proposición del invariante?
* **Respuesta 1:** El invariante certifica estructuralmente que la porción terminal de elementos evaluados en el arreglo se encuentra plenamente ordenada y fijada de manera inamovible en su posición de destino final.


* **Pregunta 2:** ¿Qué condición de los datos de entrada o adición metodológica habilita el registro del mejor caso de complejidad temporal teórica?
* **Respuesta 2:** El mejor caso equivalente a $O(n)$ se activa ante estructuras previamente ordenadas en su totalidad, siempre y cuando el diseño incorpore una variable de control o bandera que aborte la ejecución al verificar la ausencia de intercambios físicos.



**Algoritmo 1: Búsqueda Lineal**

* **Pregunta 1:** ¿Qué garantía proporciona la aseveración del invariante sobre el conjunto de datos en el instante previo a evaluar un índice de memoria específico?
* **Respuesta 1:** La aseveración del invariante garantiza que el parámetro objetivo de la búsqueda es totalmente inexistente dentro del rango de posiciones correspondientes a los índices ya evaluados en las iteraciones anteriores.


* **Pregunta 2:** Al agotar todas las iteraciones naturales programadas en el bucle principal, ¿qué inferencia utiliza el algoritmo para fundamentar su respuesta final?
* **Respuesta 2:** El recorrido íntegro de la estructura evidencia mediante la conclusión del invariante que el parámetro evaluado es completamente ajeno al arreglo, infiriendo y fundamentando así el retorno de un índice negativo o código de ausencia.



**Algoritmo 16: Two-Sum (Par con Suma Objetivo)**

* **Pregunta 1:** En el algoritmo Two-Sum, ¿por qué se revisa primero si el complemento $x - A[i]$ ya está en la tabla hash y recién después se inserta $A[i]$?
* **Respuesta 1:** Para asegurar que un elemento nunca se empareje consigo mismo. Al revisar el complemento antes de guardar el valor actual, solo se forman pares con índices distintos (el complemento debe haber aparecido en una posición anterior).

* **Pregunta 2:** ¿Qué devuelve el algoritmo si recorre todo el arreglo y ningún par de elementos suma el objetivo?
* **Respuesta 2:** Devuelve $-1$, indicando que no existe solución. El invariante garantiza que, si el arreglo se agota sin encontrar ningún par, entonces ningún par de $A[1..n]$ suma $x$.