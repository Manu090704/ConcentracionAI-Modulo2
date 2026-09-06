# ConcentracionAI-Modulo2

Proyecto de aprendizaje automático para predecir la calificación final (`final_exam_score`) de estudiantes a partir de sus hábitos de estudio. El análisis incluye exploración de datos y la comparación de una regresión lineal implementada manualmente, un árbol de decisión y un bosque aleatorio.

## Datos y resultados

El script descarga automáticamente el dataset **Student Performance and Study Habits Dataset** desde Kaggle mediante `kagglehub`; no es necesario descargar archivos de datos manualmente. Durante la ejecución se muestran estadísticas descriptivas, gráficas exploratorias y métricas MSE y R² para los conjuntos de entrenamiento, validación y prueba.

> **Nota:**
> El dataset se descarga desde Kaggle durante la ejecución, por lo que se necesita
> conexión a Internet. También es posible descargarlo manualmente desde la
> [página del dataset en Kaggle](https://www.kaggle.com/datasets/harshadapatil31/student-performance-and-study-habits-dataset/data)
> para conservar una copia local.
>
> Sin embargo, para ejecutar el proyecto completamente sin conexión es necesario
> modificar la sección de carga de datos del script y reemplazar la descarga con
> KaggleHub por una lectura del archivo local, por ejemplo:
>
> ```python
> df = pd.read_csv("student_performance_dataset.csv")
> ```
>
> Coloca `student_performance_dataset.csv` en la carpeta principal del proyecto.

## Requisitos previos
- Tener Python 3.9+ instalado ([python.org](https://www.python.org/downloads/))
- Verifica tu versión con:
  ```bash
  python3 --version
  ```
  (en Windows puede ser `python --version`)

## Pasos para correr el proyecto en local

### 1. Clonar el repositorio
```bash
git clone <url-del-repositorio>
cd ConcentracionAI-Modulo2
```

### 2. Crear el entorno virtual

**macOS / Linux**
```bash
python3 -m venv venv
```

**Windows (PowerShell o CMD)**
```bash
python -m venv venv
```

### 3. Activar el entorno virtual

**macOS / Linux**
```bash
source venv/bin/activate
```

**Windows (PowerShell)**
```powershell
venv\Scripts\Activate.ps1
```
> Si PowerShell bloquea la ejecución de scripts, corre esto una sola vez como administrador:
> ```powershell
> Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
> ```

**Windows (CMD)**
```cmd
venv\Scripts\activate.bat
```

Sabrás que el entorno está activo porque verás `(venv)` al inicio de la línea de comandos.

### 4. Instalar dependencias

Con el entorno virtual activado, instala las dependencias definidas en `requirements.txt`:

```bash
pip install -r requirements.txt
```

> El paquete de `scikit-learn` ya está incluido en el archivo de requisitos.

### 5. Correr el proyecto

```bash
python3 regresionStudentPerformance.py
```
(en Windows: `python regresionStudentPerformance.py`)

### 6. Desactivar el entorno virtual (al terminar)
```bash
deactivate
```

## Notas adicionales
- El script abre ventanas con las visualizaciones generadas; ciérralas para continuar con la siguiente gráfica.
- En macOS, el script configura el backend `TkAgg` de Matplotlib. Si aparece un error relacionado con Tk, instala el soporte de Tkinter correspondiente a tu instalación de Python.
- Recuerda no subir la carpeta `venv/` al repositorio. Agrégala a tu `.gitignore`:
  ```
  venv/
  __pycache__/
  *.pyc
  ```
