# ConcentracionAI-Modulo2

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

Con el entorno virtual activado, instala todas las dependencias:

```bash
pip install matplotlib scikit-learn numpy seaborn kagglehub pandas
```

O instalarlas una por una:

| Librería | Comando |
|---|---|
| Matplotlib | `pip install matplotlib` |
| Scikit-learn | `pip install scikit-learn` |
| NumPy | `pip install numpy` |
| Seaborn | `pip install seaborn` |
| Kagglehub | `pip install kagglehub[pandas-datasets]` |
| Pandas | `pip install pandas` |

> ⚠️ **Nota:** el paquete correcto en PyPI es `scikit-learn`, **no** `sklearn` (ese nombre está deprecado). Si usas `sklearn` en pip fallará la instalación.

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
- Si usas macOS y `matplotlib` falla al abrir la ventana de gráficos, agrega esto al inicio del script:
  ```python
  import matplotlib
  matplotlib.use('TkAgg')
  ```
- Recuerda no subir la carpeta `venv/` al repositorio. Agrégala a tu `.gitignore`:
  ```
  venv/
  __pycache__/
  *.pyc
  ```
