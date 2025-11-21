# 🚀 INSTRUCCIONES PARA USAR EL SCRIPT EN GOOGLE COLAB

## ✅ SOLUCIÓN AL ERROR "NameError: name 'null' is not defined"

El archivo `.ipynb` es un formato JSON que **NO se ejecuta directamente** como código Python.
Debes usar **una de estas dos opciones**:

---

## 📋 OPCIÓN 1: COPIAR Y PEGAR EL SCRIPT PYTHON (MÁS FÁCIL)

### Paso 1: Abrir Google Colab
1. Ve a: https://colab.research.google.com/
2. Crea un nuevo notebook (File → New notebook)

### Paso 2: Copiar el código
1. Abre el archivo: **`Fase4_Control_Digital_Script_Colab.py`** desde el repositorio
2. Copia TODO el contenido (Ctrl+A, Ctrl+C)

### Paso 3: Pegar en Colab
1. En la celda de código de Colab, pega el código (Ctrl+V)
2. Presiona **Shift + Enter** o haz clic en el botón ▶️ (Run)

### Paso 4: Esperar la ejecución
El script hará automáticamente:
- ✅ Instalar Pandoc y librerías necesarias
- ✅ Calcular parámetros PID (Kp, Ki, Kd)
- ✅ Generar informe Word (.docx)
- ✅ Generar script MATLAB (.m)
- ✅ **Descargar los archivos automáticamente**

### Paso 5: Archivos descargados
Encontrarás en tu carpeta de Descargas:
- 📄 **Informe_Corregido_Fase4.docx** (Informe académico completo)
- 📄 **Crear_Simulink_Fase4_LuisOrozco.m** (Script para MATLAB)

---

## 📓 OPCIÓN 2: SUBIR EL NOTEBOOK .ipynb

### Paso 1: Subir a Google Drive
1. Descarga el archivo **`Fase4_Control_Digital_Correccion_Integral.ipynb`**
2. Súbelo a tu Google Drive

### Paso 2: Abrir con Google Colab
1. Haz clic derecho sobre el archivo en Google Drive
2. Selecciona: **Abrir con → Google Colaboratory**

### Paso 3: Ejecutar las celdas
1. Ejecuta cada celda en orden (o usa: Runtime → Run all)
2. Los archivos se descargarán automáticamente al final

---

## 🔧 QUÉ HACE EL SCRIPT

### Cálculos Implementados:
```
Parámetros de entrada (corregidos según feedback docente):
   L = 0.1 s  (tiempo de retardo)
   T = 0.76 s (constante de tiempo)

Fórmulas de Ziegler-Nichols aplicadas:
   Kp = 1.2 × (T/L) = 9.12
   Ti = 2L = 0.2 s
   Td = 0.5L = 0.05 s
   Ki = Kp/Ti = 45.6
   Kd = Kp×Td = 0.456
```

### Archivos Generados:

#### 1. Informe_Corregido_Fase4.docx
- Informe académico profesional en formato Word
- Incluye:
  - Introducción
  - Marco teórico completo
  - Cálculos matemáticos con ecuaciones LaTeX
  - Diseño del sistema de control
  - Conclusiones
  - Referencias bibliográficas
  - Anexos

#### 2. Crear_Simulink_Fase4_LuisOrozco.m
- Script MATLAB para crear el modelo Simulink automáticamente
- Configura:
  - Un solo controlador PID (NO dos)
  - Parámetros Kp, Ki, Kd calculados
  - Planta con retardo (aproximación de Padé)
  - Perturbaciones de carga: 2V (t=0), 5V (t=5), -4V (t=12)
  - Scopes para visualización

---

## 💻 USAR EL SCRIPT MATLAB

### En MATLAB:
1. Abrir MATLAB en tu computadora
2. Navegar al directorio donde descargaste el archivo `.m`
3. Ejecutar en la consola:
   ```matlab
   Crear_Simulink_Fase4_LuisOrozco
   ```
4. Se creará automáticamente el modelo Simulink
5. Hacer clic en **Run (▶️)** para simular
6. Observar las gráficas en los bloques Scope

---

## ❓ SOLUCIÓN DE PROBLEMAS

### Error: "NameError: name 'null' is not defined"
**Causa**: Estás intentando ejecutar el archivo .ipynb como código Python normal.
**Solución**: Usa la OPCIÓN 1 (copiar y pegar el script .py)

### Error: "ModuleNotFoundError: No module named 'google.colab'"
**Causa**: Estás ejecutando el código fuera de Google Colab.
**Solución**: Debes ejecutar el código EN Google Colab, no en tu computadora local.

### No se descargan los archivos
**Causa**: Tu navegador bloqueó las descargas múltiples.
**Solución**: Permite las descargas múltiples cuando el navegador lo solicite.

### Error al convertir a Word
**Causa**: Pandoc no se instaló correctamente.
**Solución**: Vuelve a ejecutar la celda completa desde el inicio.

---

## 📞 ARCHIVOS DISPONIBLES

En el repositorio encontrarás:

1. **Fase4_Control_Digital_Script_Colab.py** ← **USAR ESTE (COPIAR/PEGAR)**
   - Script Python puro
   - Copiar y pegar en Google Colab
   - Solución más simple

2. **Fase4_Control_Digital_Correccion_Integral.ipynb**
   - Notebook Jupyter completo
   - Subir a Google Drive y abrir con Colab
   - Más organizado visualmente

**Recomendación**: Usa el archivo `.py` (OPCIÓN 1) por simplicidad.

---

## ✅ CHECKLIST DE ENTREGA

Después de ejecutar el script:

- [ ] Descargado: Informe_Corregido_Fase4.docx
- [ ] Descargado: Crear_Simulink_Fase4_LuisOrozco.m
- [ ] Ejecutado el script en MATLAB
- [ ] Simulado el modelo en Simulink
- [ ] Capturadas gráficas (screenshots) de los Scopes
- [ ] Incluidas las gráficas en el informe Word
- [ ] Revisado que todos los cálculos sean correctos:
  - [ ] L = 0.1 s ✓
  - [ ] T = 0.76 s ✓
  - [ ] Kp = 9.12 ✓
  - [ ] Ki = 45.6 ✓
  - [ ] Kd = 0.456 ✓
- [ ] Verificado que haya un solo PID (no dos)
- [ ] Verificado que las perturbaciones sean de carga

---

## 📚 RESUMEN RÁPIDO

```
1. Abre Google Colab: https://colab.research.google.com/
2. Copia TODO el código de: Fase4_Control_Digital_Script_Colab.py
3. Pega en una celda de Colab
4. Ejecuta (Shift + Enter)
5. Descarga los archivos generados
6. Usa el .m en MATLAB para crear el modelo Simulink
```

---

**Desarrollado para**: Luis Fernando Orozco Arenas
**Curso**: Control Digital - UNAD (203041_7)
**Fase**: 4 - Componente Práctico

---

¿Necesitas ayuda? Revisa los errores comunes arriba o contacta al soporte técnico.
