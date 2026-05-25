# LinearPy: Tutor Cientifico de Algebra Lineal y Geometria Analitica

LinearPy es una plataforma interactiva de computo algebraico simbolico y visualizacion geometrica disenada como una herramienta de apoyo didactico de nivel universitario para cursos de Algebra Lineal y Geometria Analitica. 

La plataforma provee soluciones exactas y desgloses paso a paso para los problemas fundamentales de la disciplina, combinando el rigor del algebra computacional con graficas interactivas bidimensionales y tridimensionales, bajo un diseno minimalista y formal de alta fidelidad.

---

## Funcionalidades del Sistema

El ecosistema esta dividido en cuatro modulos academicos principales y una seccion de referencias complementarias:

### Capitulo 1: Vectores y Geometria Analitica
*   **Magnitudes y Normas**: Calculo de la norma euclidiana exacta en el espacio tridimensional R3 mediante desgloses de raiz cuadrada.
*   **Producto Escalar**: Procedimiento detallado de multiplicacion por componentes, evaluacion de ortogonalidad y determinacion del coseno del angulo entre vectores.
*   **Producto Cruz**: Construccion y desarrollo por cofactores paso a paso del determinante 3x3 para obtener el vector perpendicular y el area exacta del paralelogramo.
*   **Vector Unitario y Cosenos Directores**: Obtencion de las componentes normalizadas y angulos directores con respecto a los ejes cartesianos, incluyendo proteccion automatica contra division entre cero para el vector nulo.
*   **Geometria en el Espacio**: Construccion interactiva paso a paso de la ecuacion vectorial y parametrica de la recta, y expansion término a término de la ecuacion general del plano partiendo de la condicion de ortogonalidad normal.

### Capitulo 2: Matrices y Sistemas de Ecuaciones
*   **Determinante paso a paso**: Desarrollo exacto por cofactores detallando los determinantes de las submatrices menores de orden n-1 para dimensiones desde 2x2 hasta 5x5.
*   **Matriz Inversa por la Adjunta**: Procedimiento completo de factorizacion que incluye la obtencion de la matriz transpuesta, la matriz de cofactores, la matriz adjunta y el cociente final por el determinante.
*   **Motor Gauss-Jordan (RREF)**: Reduccion por filas interactiva que registra y muestra de forma secuencial cada operacion elemental ($R_i \leftrightarrow R_j$, $R_i \leftarrow c \cdot R_i$, $R_i \leftarrow R_i + c \cdot R_j$) en formato LaTeX.
*   **Sistemas de Ecuaciones Lineales (SEL)**: Reduccion de la matriz aumentada y clasificacion analitica mediante la aplicacion rigurosa del Teorema de Rouche-Frobenius, derivando la solucion unica o la solucion parametrizada con variables libres.
*   **Independencia Lineal**: Analisis de dependencia o independencia de un conjunto de vectores colocados en formato matricial por filas utilizando el motor de Gauss-Jordan para contar pivots.

### Capitulo 3: Transformaciones Lineales
*   **Nucleo (Kernel)**: Resolucion exacta del sistema homogeneo Ax = 0, identificando variables libres y principales para derivar la base y la dimension (Nulidad).
*   **Imagen (Espacio Columna)**: Analisis de las columnas pivote en la forma RREF para seleccionar la base de vectores de la matriz original A y determinar la dimension (Rango).
*   **Teorema de la Dimension**: Validacion simbolica interactiva de la relacion Rango-Nulidad con respecto a la dimension del espacio vectorial de partida.
*   **Laboratorio 2D**: Simulador de deformacion geometrica interactiva para observar transformaciones compuestas (rotacion, escala, cizallamiento y reflexion). La matriz compuesta final se calcula mediante multiplicacion simbolica de derecha a izquierda libre de retrasos de CPU.

### Capitulo 4: Diagonalizacion y Analisis Espectral
*   **Polinomio Caracteristico**: Evaluacion paso a paso de la ecuacion secular det(A - lambda I) = 0, resolviendo la expansion simbolica en terminos de la variable lambda.
*   **Autovalores y Espacios Propios**: Determinacion de las raices caracteristicas con su multiplicidad algebraica (m.a.) y resolucion del sistema homogeneo para hallar los autovectores generadores con su multiplicidad geometrica (m.g.).
*   **Descomposicion Canonica**: Construccion de la matriz diagonal D y la matriz modal P. Calculo paso a paso de la inversa P^-1 y comprobacion secuencial del producto matricial P * D * P^-1 = A.

---

## Guia de Instalacion y Ejecucion Local

Sigue estos pasos detallados para instalar las dependencias necesarias y ejecutar LinearPy de forma local en tu computadora:

### Requisitos Previos
*   **Python**: Se requiere Python 3.9, 3.10 o 3.11 instalado.
*   **Git**: Opcional, para clonar el repositorio.

### Paso 1: Obtener el Codigo Fuente
Si tienes git instalado, clona el repositorio:
```bash
git clone https://github.com/jorgesm03047-code/git1.git
cd git1
```
De lo contrario, puedes descargar y extraer el archivo ZIP directamente en tu computadora y abrir la terminal en el directorio raiz del proyecto.

### Paso 2: Crear un Entorno Virtual (Recomendado)
Para evitar conflictos de librerias globales, crea un entorno virtual aislado:

*   **En macOS / Linux**:
    ```bash
    python3 -m venv venv
    source venv/bin/activate
    ```
*   **En Windows**:
    ```bash
    python -m venv venv
    venv\Scripts\activate
    ```

### Paso 3: Instalar las Librerias y Dependencias
Instala todas las dependencias necesarias listadas en el archivo de requisitos. Estas librerias incluyen el motor Streamlit, el procesador algebraico SymPy, las herramientas graficas Plotly y Matplotlib, y el modulo numerico NumPy:

```bash
pip install -r requirements.txt
```

### Paso 4: Ejecutar la Aplicacion
Una vez instaladas las librerias, arranca la plataforma web ejecutando el comando:

```bash
streamlit run main.py
```

### Paso 5: Acceder al Tutor
La terminal mostrara las direcciones de conexion local. Abre tu navegador web favorito (Chrome, Safari, Firefox o Edge) e ingresa a la siguiente direccion:
```text
http://localhost:8501
```

---

## Despliegue en la Nube (Deploy)

Para desplegar y publicar el proyecto de forma gratuita y permanente en Streamlit Community Cloud:

1.  Crea una cuenta en [Streamlit Share](https://share.streamlit.io/) vinculando tu cuenta de GitHub.
2.  Haz clic en el boton **"New app"**.
3.  Ingresa los siguientes datos exactos de tu repositorio:
    *   **Repository**: `jorgesm03047-code/git1`
    *   **Branch**: `main`
    *   **Main file path**: `main.py`
4.  Haz clic en **"Deploy!"**.
