# Cuando el camino más corto no es el mejor: Rutas de evacuación en zonas inundadas

Proyecto de búsqueda de rutas (pathfinding) que modela la evacuación de una zona inundada
como una cuadrícula con niveles de riesgo variables, y compara tres algoritmos de búsqueda
— BFS, Dijkstra y A* — para mostrar por qué la ruta más corta (menos pasos) no siempre es la
ruta más segura o conveniente (menor riesgo acumulado).

## Descripción

El terreno se representa como una matriz 2D donde cada celda tiene un costo asociado a su
nivel de inundación (0 = bloqueado, 1 = seguro, 3 = riesgo bajo, 5 = riesgo medio,
10 = riesgo alto). El notebook implementa y compara BFS, Dijkstra y A* sobre 6 escenarios de
prueba, incluyendo un validador programático de rutas y una suite de pruebas de casos borde.

## Requisitos de instalación

- Python 3.9 o superior
- Jupyter Notebook o JupyterLab
- Librerías: `numpy`, `pandas`, `matplotlib` (el resto son de la librería estándar:
  `heapq`, `collections`, `time`, `copy`)

Instalación de dependencias:

\`\`\`bash
pip install numpy pandas matplotlib notebook
\`\`\`

## Pasos de ejecución

1. Clonar este repositorio:
   \`\`\`bash
   git clone <url-del-repositorio>
   cd <nombre-del-repositorio>
   \`\`\`
2. Instalar las dependencias (ver sección anterior).
3. Abrir el notebook:
   \`\`\`bash
   jupyter notebook "Cuando el camino más corto no es el mejor - Rutas de evacuación en zonas inundadas.ipynb"
   \`\`\`
4. Ejecutar todas las celdas en orden (`Kernel -> Restart & Run All`). El notebook es
   autocontenido: no requiere archivos externos ni conexión a internet.
5. Revisar, para cada uno de los 6 escenarios, el gráfico comparativo, la tabla de métricas
   (`pandas.DataFrame`) y la celda de interpretación en Markdown.

## Estructura del notebook

1. Documentación de diseño y modelado del problema.
2. Implementación base: validador de rutas, validador de entrada, y los tres algoritmos
   (BFS, Dijkstra, A*) instrumentados con métricas reales de ejecución.
3. Motor de visualización (mapas de calor con `matplotlib`) y comparación (tablas con
   `pandas`).
4. Seis escenarios de prueba obligatorios (ruta estándar, bloqueo dinámico, refugio
   inaccesible, aumento de riesgo regional, atajo corto vs. rodeo seguro, y una suite de
   casos borde / caza-errores).
5. Declaración de uso de herramientas de IA y verificación del código.

## Licencia

Proyecto académico. Ajustar esta sección según los requisitos del curso o la institución.
```
