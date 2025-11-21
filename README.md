# 🎓 Corrección Integral Fase 4 - Control Digital UNAD

## 📋 Información del Proyecto

**Institución**: Universidad Nacional Abierta y a Distancia (UNAD)
**Curso**: Control Digital (Grupo 203041_7)
**Actividad**: Fase 4 - Componente Práctico (Prácticas Simuladas)
**Estudiante**: Luis Fernando Orozco Arenas
**Método**: Ziegler-Nichols (Curva de Reacción)

---

## 🎯 Objetivo del Repositorio

Este repositorio contiene las herramientas automatizadas para generar:
1. **Informe académico profesional** en formato Word (.docx)
2. **Script MATLAB** para construcción automática de modelo Simulink
3. **Cálculos verificados** de parámetros PID según método Ziegler-Nichols

---

## 📦 Archivos Principales

### ✅ Para usar en Google Colab:

| Archivo | Descripción | Cómo usar |
|---------|-------------|-----------|
| **`Fase4_Control_Digital_Script_Colab.py`** | Script Python completo (RECOMENDADO) | Copiar y pegar en Colab |
| **`Fase4_Control_Digital_Correccion_Integral.ipynb`** | Notebook Jupyter | Subir a Drive y abrir con Colab |
| **`INSTRUCCIONES_GOOGLE_COLAB.md`** | Guía de uso paso a paso | Leer antes de empezar |

### 📄 Documentos de referencia:
- `CorreccionesSOLICItADAS.docx/pdf` - Feedback del docente
- `Informe_Fase4_PID_SIMULINK_Orozco_Luis (4).docx` - Informe anterior (con errores)
- `EJEMPLO_fase4_paul (2).pdf` - Ejemplo de referencia

---

## 🚀 Inicio Rápido

### Opción 1: Script Python (MÁS FÁCIL)

1. Abre [Google Colab](https://colab.research.google.com/)
2. Crea un nuevo notebook
3. Copia el contenido de `Fase4_Control_Digital_Script_Colab.py`
4. Pega en una celda y ejecuta (Shift + Enter)
5. Descarga los archivos generados

### Opción 2: Notebook Jupyter

1. Descarga `Fase4_Control_Digital_Correccion_Integral.ipynb`
2. Súbelo a Google Drive
3. Abre con Google Colaboratory
4. Ejecuta todas las celdas (Runtime → Run all)

**⚠️ IMPORTANTE**: NO ejecutes el archivo .ipynb como código Python normal, causará error `NameError: name 'null' is not defined`

---

## 🔬 Correcciones Implementadas

Este proyecto corrige los siguientes errores del informe anterior:

### ❌ Errores Identificados:
1. Parámetros de planta incorrectos (L y T)
2. Fórmulas PID erróneas
3. Dos controladores PID en paralelo (arquitectura incorrecta)
4. Perturbaciones sumadas a la referencia (no como carga)

### ✅ Correcciones Aplicadas:

#### 1. Parámetros Corregidos
```
L = 0.1 s   (tiempo de retardo)
T = 0.76 s  (constante de tiempo)
```

#### 2. Fórmulas Verificadas (Ziegler-Nichols)
```
Kp = 1.2 × (T/L) = 9.12
Ti = 2L = 0.2 s
Td = 0.5L = 0.05 s
Ki = Kp/Ti = 45.6
Kd = Kp×Td = 0.456
```

#### 3. Arquitectura Correcta
- ✅ Un solo controlador PID
- ✅ Perturbaciones como entradas de carga
- ✅ Realimentación negativa

#### 4. Perturbaciones de Carga
```
t = 0 s  → +2V
t = 5 s  → +5V
t = 12 s → -4V
```

---

## 📊 Resultados Generados

### 1. Informe_Corregido_Fase4.docx

Informe académico completo con:
- ✅ Introducción contextualizada
- ✅ Marco teórico con justificación de fórmulas
- ✅ Cálculos matemáticos paso a paso (LaTeX)
- ✅ Diseño del sistema de control
- ✅ Conclusiones técnicas
- ✅ Referencias bibliográficas
- ✅ Anexos de verificación

### 2. Crear_Simulink_Fase4_LuisOrozco.m

Script MATLAB que crea automáticamente:
- ✅ Modelo Simulink completo
- ✅ Configuración del PID con parámetros calculados
- ✅ Bloques de perturbaciones
- ✅ Planta con aproximación de Padé
- ✅ Scopes para visualización

**Para usar en MATLAB:**
```matlab
Crear_Simulink_Fase4_LuisOrozco
```

---

## 🛠️ Características Técnicas

### Tecnologías Utilizadas:
- **Python 3.x** - Lenguaje principal
- **Pandoc** - Conversión Markdown → Word
- **LaTeX** - Ecuaciones matemáticas
- **MATLAB/Simulink** - Modelado y simulación

### Funcionalidades:
- ✅ Instalación automática de dependencias
- ✅ Cálculos verificados de parámetros PID
- ✅ Generación automática de informe Word
- ✅ Generación automática de script MATLAB
- ✅ Descarga automática de archivos
- ✅ Verificación de cálculos incorporada
- ✅ Documentación LaTeX para ecuaciones
- ✅ Formato académico profesional

---

## 📐 Modelo del Sistema

### Función de Transferencia de la Planta:
```
G(s) = K × e^(-Ls) / (Ts + 1)
```

Donde:
- K = 1.0 (ganancia estática)
- L = 0.1 s (tiempo de retardo)
- T = 0.76 s (constante de tiempo)

### Controlador PID:
```
u(t) = Kp×e(t) + Ki×∫e(τ)dτ + Kd×de(t)/dt
```

Con parámetros:
- Kp = 9.12
- Ki = 45.6
- Kd = 0.456

---

## 📚 Referencias Bibliográficas

1. Ziegler, J. G., & Nichols, N. B. (1942). "Optimum Settings for Automatic Controllers"
2. Ogata, K. (2010). *Ingeniería de Control Moderna* (5ª ed.)
3. Åström, K. J., & Hägglund, T. (2006). *Advanced PID Control*
4. Franklin, G. F., et al. (2015). *Feedback Control of Dynamic Systems* (7ª ed.)

---

## 🐛 Solución de Problemas

### Error: "NameError: name 'null' is not defined"
**Solución**: NO ejecutes el .ipynb como script Python. Usa `Fase4_Control_Digital_Script_Colab.py` en su lugar.

### Error: "ModuleNotFoundError: No module named 'google.colab'"
**Solución**: Ejecuta el código EN Google Colab, no localmente.

### No se descargan los archivos
**Solución**: Permite descargas múltiples en tu navegador.

Consulta `INSTRUCCIONES_GOOGLE_COLAB.md` para más detalles.

---

## 📝 Checklist de Entrega

- [ ] Ejecutar script en Google Colab
- [ ] Descargar Informe_Corregido_Fase4.docx
- [ ] Descargar Crear_Simulink_Fase4_LuisOrozco.m
- [ ] Ejecutar script en MATLAB
- [ ] Simular modelo en Simulink
- [ ] Capturar screenshots de resultados
- [ ] Incluir gráficas en informe
- [ ] Verificar parámetros:
  - [ ] L = 0.1 s ✓
  - [ ] T = 0.76 s ✓
  - [ ] Kp = 9.12 ✓
  - [ ] Ki = 45.6 ✓
  - [ ] Kd = 0.456 ✓
- [ ] Verificar arquitectura (un solo PID) ✓
- [ ] Verificar perturbaciones de carga ✓

---

## 🤝 Contribuciones

Este proyecto fue desarrollado específicamente para la Fase 4 del curso de Control Digital de la UNAD.

---

## 📄 Licencia

Proyecto académico - UNAD 2024

---

## 📞 Contacto

**Estudiante**: Luis Fernando Orozco Arenas
**Grupo**: 203041_7
**Curso**: Control Digital - UNAD

---

## ⭐ Estructura del Repositorio

```
corregirdigital/
├── README.md                                          ← Estás aquí
├── INSTRUCCIONES_GOOGLE_COLAB.md                     ← Guía de uso
├── Fase4_Control_Digital_Script_Colab.py             ← Script principal (USAR ESTE)
├── Fase4_Control_Digital_Correccion_Integral.ipynb   ← Notebook alternativo
├── CorreccionesSOLICItADAS.docx                      ← Feedback docente
├── CorreccionesSOLICItADAS.pdf
├── Informe_Fase4_PID_SIMULINK_Orozco_Luis (4).docx   ← Informe anterior
├── EJEMPLO_fase4_paul (2).pdf                        ← Ejemplo referencia
└── Guía de aprendizaje-Fase 4...pdf                  ← Guía de la actividad
```

---

**Última actualización**: 2024
**Versión**: 1.0.0
**Estado**: ✅ Completado y verificado

---

🎉 **¡Éxito en tu proyecto!**
