# Calculadora de Matrices

## Descripción
Este proyecto es una calculadora de matrices implementada en Python utilizando un notebook de Jupyter. Permite crear matrices, realizar operaciones matemáticas básicas y avanzadas, y gestionar matrices a través de una interfaz de consola interactiva. El código está diseñado para ser educativo y funcional, cubriendo conceptos de álgebra lineal como determinantes, inversas, transpuestas, entre otros.

## Características
- **Creación de Matrices**: Ingreso manual o generación aleatoria de valores.
- **Operaciones Básicas**:
  - Suma y resta de matrices.
  - Multiplicación y división de matrices.
  - Multiplicación por escalar.
  - Producto Hadamard (elemento a elemento).
- **Operaciones Avanzadas**:
  - Cálculo de transpuesta.
  - Cálculo de determinante (usando expansión por cofactores).
  - Cálculo de adjunta.
  - Cálculo de inversa (para matrices cuadradas no singulares).
- **Gestión de Matrices**:
  - Modificación de matrices (completa o por índice).
  - Visualización de matrices existentes.
  - Guardado y carga desde archivos CSV.
- **Interfaz de Consola**: Menú interactivo para seleccionar operaciones.
- **Validaciones**: Verificación de dimensiones compatibles, rangos de valores, etc.

## Instalación
### Requisitos
- Python 3.x (recomendado 3.8 o superior).
- Jupyter Notebook (para ejecutar el archivo `.ipynb`).
- Bibliotecas estándar: `functools`, `random`, `csv` (incluidas en Python).

### Pasos
1. Clona o descarga el repositorio.
2. Abre el archivo `MatricesCalculadora.ipynb` en Jupyter Notebook.
3. Ejecuta las celdas en orden para cargar las clases y funciones.

No se requieren instalaciones adicionales, ya que todas las dependencias son parte de la biblioteca estándar de Python.

## Uso
1. Abre el notebook en Jupyter.
2. Ejecuta todas las celdas de código hasta la función `menu()`.
3. Ejecuta la celda final que llama a `menu()` para iniciar el programa.
4. Sigue las instrucciones en la consola:
   - Selecciona opciones del menú (1-12).
   - Ingresa datos según se solicite (número de filas/columnas, valores, etc.).
   - Las matrices se almacenan con nombres (A, B, C, ...).
5. Para salir, selecciona la opción 12.

### Ejemplo de Uso
- Opción 1: Crear una matriz A de 2x2 con valores aleatorios.
- Opción 7: Calcular el determinante de A.
- Opción 9: Calcular la inversa de A (si es posible).
- Opción 11: Ver todas las matrices creadas.

## Clases y Funciones Principales

### Clase `Matriz`
Representa una matriz con sus datos y operaciones básicas.

- `__init__(filas, columnas, nombre)`: Inicializa la matriz.
- `crear_aleatoria(minimo, maximo)`: Genera valores aleatorios.
- `ingresar_datos()`: Permite ingreso manual o aleatorio.
- `crear_con_datos(nombre)`: Método de clase para crear una matriz completa.
- `mostrar_matriz()`: Imprime la matriz formateada.
- `modificar_matriz()`: Modifica la matriz completa o por índice.
- `pedir_entero(mensaje, minimo, maximo)`: Valida entrada de enteros.
- `pedir_decimal(mensaje, minimo, maximo)`: Valida entrada de decimales.

### Clase `OperacionesMatrices`
Contiene métodos estáticos para operaciones entre matrices.

- `validar_multiplicacion_entre_matrices(matriz1, matriz2)`: Verifica compatibilidad para multiplicación.
- `validar_suma_resta_matrices(matriz1, matriz2)`: Verifica compatibilidad para suma/resta.
- `validar_matriz_cuadrada(matriz1)`: Verifica si es cuadrada.
- `multiplicar_dividir_matrices(matriz1, matriz2, opcion)`: Multiplica o divide matrices.
- `multiplicacion_hadamard(matriz1, matriz2)`: Producto Hadamard.
- `multiplicar_dividir_por_escalar(matriz1, escalar, opcion)`: Operación con escalar.
- `suma_resta_entre_matrices(matriz1, matriz2, opcion)`: Suma o resta.
- `calcular_transpuesta(matriz1)`: Calcula la transpuesta.
- `calcular_adjunta(matriz1)`: Calcula la adjunta.
- `calcular_determinante(matriz1)`: Calcula el determinante.
- `obtener_cofactor(matriz, fila, columna)`: Obtiene cofactor.
- `tiene_inversa(matriz)`: Verifica si tiene inversa.
- `calcular_inversa(matriz1)`: Calcula la inversa.

### Funciones Auxiliares
- `guardar_matriz_csv(matriz, nombre_archivo)`: Guarda matriz en CSV.
- `cargar_matriz_csv(nombre_archivo)`: Carga matriz desde CSV.
- `ingresar_opcion_menu()`: Valida opción del menú.
- `seleccionar_matriz_existente(matrices, prompt)`: Selecciona matriz existente.
- `ingresar_operacion(mensaje, opciones_validas)`: Valida operación.
- `requiere_matrices(minimo)`: Decorador para verificar mínimo de matrices.
- `mensaje_menu()`: Imprime el menú.
- `accion_*()`: Funciones para cada opción del menú (modificar, sumar, etc.).
- `menu()`: Función principal que maneja el flujo del programa.

## Notas
- Las matrices están limitadas a 10x10 para simplicidad.
- Los valores numéricos están restringidos entre -1000 y 1000.
- El programa maneja errores comunes y proporciona mensajes informativos.
- Para extensiones futuras, se podría agregar una interfaz gráfica (GUI) usando Tkinter, como se menciona en versiones anteriores del código.

## Contribuciones
Si deseas contribuir, puedes:
- Reportar bugs.
- Sugerir nuevas funcionalidades.
- Mejorar el código o la documentación.

## Licencia
Este proyecto es de código abierto. Úsalo libremente para fines educativos.
