## Dask - ML

Dask es una librería de Python que facilita el procesamiento paralelo y distribuido de grandes volúmenes de datos. Está diseñada para escalar desde un solo ordenador hasta clústeres de máquinas, lo que la convierte en una herramienta poderosa para manejar Big Data de forma eficiente. A diferencia de otras librerías como NumPy o Pandas, Dask permite trabajar con conjuntos de datos que no caben completamente en la memoria, distribuyendo el trabajo entre múltiples núcleos de CPU o incluso diferentes máquinas.

## Índice
1. ✨ [Introducción](#introducción)  
   Descubre los conceptos básicos y el propósito de esta guía.
   
2. 🔍 [¿Cómo funciona Dask por detrás?](#cómo-funciona-dask-por-detrás)  
   Una mirada bajo el capó del motor de Dask.

3. 🧮 [El `dask.array`](#el-daskarray)  
   Exploramos cómo usar arrays distribuidos con Dask.

4. ⚔️ [Dask vs NumPy](#dask-vs-numpy)  
   Comparativa práctica entre estas dos herramientas.

5. 📚 [Referencias](#referencias)  
   Fuentes de información y bibliografía adicional.

---

## Introducción

Este artículo explora **Dask** como herramienta para la computación paralela en Python, haciendo hincapié en su uso en tareas de Inteligencia Artificial. En el artículo, explicamos cómo Dask permite distribuir el procesamiento de datos en múltiples núcleos de CPU y máquinas, ofreciendo una solución escalable para grandes volúmenes de datos.

**¿Qué es la computación en paralelo?**  
La computación en paralelo permite realizar múltiples operaciones al mismo tiempo, aprovechando los múltiples núcleos de la CPU. Dask implementa esta capacidad en Python, optimizando el procesamiento sin necesidad de reestructurar el código.

---

## ¿Cómo funciona Dask por detrás?

Al utilizar **Dask Arrays**, no se ejecutan cálculos de inmediato. En lugar de ello, Dask crea un **gráfico de tareas** o **DAG** (*Directed Acyclic Graph*), que define las dependencias de cada tarea antes de ejecutarla. Este enfoque permite optimizar la ejecución al no procesar las tareas hasta que realmente sea necesario (cuando se llama a `.compute()`).

### Características del DAG:
- **Nodos**: Representan las operaciones a realizar.
- **Aristas**: Indican las dependencias entre operaciones.
- **Ejecución Diferida**: Las tareas no se ejecutan hasta que es estrictamente necesario.

Dask es similar a herramientas como **Spark** en la forma en que utiliza estos gráficos para optimizar el flujo de trabajo y reducir la sobrecarga en la memoria.

---

## El `dask.array`

En Dask, los **arrays distribuidos** permiten dividir grandes datasets en bloques y procesarlos de manera paralela. Dask permite realizar operaciones de álgebra lineal y manipulación de matrices de manera eficiente, haciendo uso de la computación paralela en una sola máquina o un clúster de máquinas.

---

## Dask vs NumPy

En esta sección, comparamos el enfoque tradicional de **NumPy** para el procesamiento de datos en un solo núcleo frente al modelo de **Dask** de paralelización en múltiples núcleos. Dask permite trabajar con datasets mucho mayores que la memoria RAM de la máquina, utilizando gráficos de tareas para manejar la ejecución de operaciones de manera eficiente.

---

## Referencias

- [Dask Documentation](https://docs.dask.org)
- [NumPy Documentation](https://numpy.org/doc/)
- Artículos sobre computación paralela y DAGs.

---

**¡Gracias por leer!**  
Para más información sobre computación paralela en Python, no dudes en revisar la documentación oficial de Dask y explorar más sobre sus aplicaciones en IA.
