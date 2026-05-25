# LinearPy: Tutor Inteligente de Álgebra Lineal y Geometría Analítica

**LinearPy** es una plataforma interactiva de cálculo simbólico y visualización 3D/2D diseñada como un complemento pedagógico de nivel profesional para cursos universitarios de **Álgebra Lineal y Geometría Analítica**.

Desarrollada con un enfoque didáctico riguroso y una interfaz minimalista inspirada en **GeoGebra**, la aplicación permite a los estudiantes comprender intuitivamente y verificar de manera exacta (sin pérdida por redondeo de coma flotante) sus procedimientos matemáticos paso a paso.

---

## 🎨 Características Principales

*   **Rigor Matemático Exacto**: Todo el procesamiento algebraico se ejecuta de forma simbólica mediante **SymPy**, devolviendo fracciones exactas, raíces y términos analíticos renderizados nativamente en $\LaTeX$.
*   **Procedimientos Paso a Paso**: Desgloses detallados y didácticos para normas vectoriales, producto escalar, producto cruz, ecuaciones de rectas y planos, desarrollos por cofactores de determinantes, inversiones de matrices por el método de la adjunta, y multiplicidades espectrales.
*   **Reducción Gauss-Jordan Interactiva**: Un motor personalizado que ilustra secuencialmente cada operación elemental de fila ($R_i \leftrightarrow R_j$, $R_i \leftarrow c \cdot R_i$, $R_i \leftarrow R_i + c \cdot R_j$) en formato $\LaTeX$ para matrices, sistemas de ecuaciones lineales, independencia lineal, núcleos, imágenes y cálculo de espacios propios.
*   **Visualización en Tiempo Real**:
    *   **Laboratorio 3D**: Representación tridimensional interactiva (Plotly) de vectores y productos vectoriales que se puede rotar y escalar libremente.
    *   **Laboratorio 2D**: Simulador dinámico para observar en tiempo real la deformación espacial bajo transformaciones lineales (rotación, escala, cizallamiento y reflexión).

---

## 📂 Estructura del Proyecto

*   `main.py`: Punto de entrada único que orquesta la navegación, el enrutamiento y aplica el diseño estético de alta fidelidad con CSS inyectado.
*   `tutor_componente.py`: Contiene los motores intermedios compartidos (Gauss-Jordan, expansión de cofactores de determinantes, desglose de matrices inversas y formateador de matrices con barras aumentadas en $\LaTeX$).
*   `bloque1_vectores.py`: Capítulo 1 -- Vectores y Geometría Analítica en el espacio $\mathbb{R}^3$.
*   `bloque2_matrices.py`: Capítulo 2 -- Matrices, determinantes, sistemas de ecuaciones lineales e independencia lineal.
*   `bloque3_transformaciones.py`: Capítulo 3 -- Núcleo, imagen y teorema de la dimensión de transformaciones lineales.
*   `bloque4_diagonalizacion.py`: Capítulo 4 -- Diagonalización espectral constructiva $A = PDP^{-1}$.
*   `requirements.txt`: Lista de dependencias del entorno de producción.

---

## 💻 Instalación y Ejecución Local

Para ejecutar **LinearPy** de manera local en tu computadora, sigue estos pasos:

1.  **Clona el repositorio**:
    ```bash
    git clone https://github.com/jorgesm03047-code/git1.git
    cd git1
    ```

2.  **Instala las dependencias**:
    Asegúrate de tener Python 3.9 o superior instalado. Luego, ejecuta:
    ```bash
    pip install -r requirements.txt
    ```

3.  **Ejecuta la aplicación**:
    ```bash
    streamlit run main.py
    ```

4.  **Accede al Tutor**: Abre tu navegador e ingresa a `http://localhost:8501`.

---

## 🚀 Despliegue en Streamlit Community Cloud (Gratis)

Puedes alojar este tutor de forma gratuita en la nube en menos de 2 minutos siguiendo estos pasos:

1.  Ve a [Streamlit Community Cloud](https://share.streamlit.io/) e inicia sesión con tu cuenta de GitHub.
2.  Haz clic en el botón **"New app"**.
3.  Configura los campos con los siguientes datos de tu repositorio:
    *   **Repository**: `jorgesm03047-code/git1`
    *   **Branch**: `main`
    *   **Main file path**: `main.py`
4.  Haz clic en el botón **"Deploy!"** y ¡listo! Tu aplicación estará en línea de forma pública y gratuita con un enlace personalizado compartible.
