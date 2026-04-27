# 📊 Calculadora del Baremo USAL

Una herramienta web interactiva y gratuita para estimar la puntuación en los concursos de selección de personal docente e investigador de la **Universidad de Salamanca**.

![HTML5](https://img.shields.io/badge/HTML5-E34C26?style=flat&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)
![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)

## 🎯 ¿Qué es?

Esta calculadora permite a candidatos de concursos docentes calcular **de forma orientativa** los puntos que obtendrían en cada sección del baremo oficial de la USAL, basándose en el **Consejo de Gobierno de 25 de julio de 2024**.

**Ideal para:**
- Candidatos que van a participar en concursos de la USAL
- Planificar qué méritos priorizar
- Estimar competitividad en una plaza
- Entender cómo se puntúan los diferentes méritos

## ✨ Características principales

### 📚 6 categorías de méritos
- **Formación académica e investigadora** — Expedientes, títulos, contratos predoctorales/postdoctorales
- **Docencia** — Experiencia docente, formación permanente, calidad, innovación, tutorización
- **Investigación** — Proyectos, publicaciones científicas, congresos, sexenios, estancias
- **Liderazgo** — Dirección de equipos, tesis, gestión, órganos científicos, premios
- **Actividad profesional** — Experiencia profesional relevante y gestión sanitaria
- **Méritos preferentes** — PDI en universidad pública, doctorado, acreditación PAD

### 🧮 Cálculo automático inteligente

**Contratos de investigación:**
- Introduce meses totales → el sistema calcula automáticamente ¼ del máximo por año
- Selecciona tipo (Beatriz Galindo > Juan de la Cierva > otros) → ajusta puntuación automáticamente

**Publicaciones científicas:**
- Ingresa cantidad por categoría (A, B, C, D)
- Sistema multiplica por tasa correspondiente a tu figura
- Respeta restricción de máximo 1/3 en categorías C+D

**Congresos y comunicaciones:**
- Cuenta por separado: invitaciones, presentaciones orales, pósters
- Diferencia entre internacionales y nacionales
- Sistema suma automáticamente con los coeficientes correctos

**Otros campos:**
- Docencia: años con cálculo especial para Catedráticos (×0.5)
- Sexenios: automáticamente ×0.25 o ×0.5 según figura
- Estancias: automáticamente ×0.1 o ×0.2 según figura

### 👥 7 figuras de PDI soportadas
- Asociado (ASO)
- Profesor Ayudante Doctor (PAD)
- Profesor Permanente Laboral (PPL) / Titular de Universidad (TU)
- PPL/TU Vinculado a institución sanitaria
- Catedrático de Universidad (CU)
- CU Vinculado
- Profesor Sustituto (SUS)

Cada figura tiene máximos y coeficientes específicos que se aplican automáticamente.

### 📊 Panel de resumen en tiempo real
- **Puntos por sección** con barras de progreso
- **Total estimado** actualizado en vivo
- **Máximos permitidos** para cada sección
- **Porcentaje de cobertura** visual

### 🎨 Interfaz moderna
- Diseño limpio y minimalista
- **Modo oscuro** automático según preferencias del sistema
- Totalmente **responsivo** (desktop, tablet, móvil)
- Secciones colapsables para mejor organización
- Sin dependencias externas

## 🚀 Cómo usar

### Opción 1: Online (sin instalación)
1. Abre el archivo `index.html` en tu navegador
2. ¡Listo! La app funciona completamente offline

### Opción 2: Clonar repositorio
```bash
git clone https://github.com/gabri15/CalculadoraPuntosPlazaUsal.git
cd CalculadoraPuntosPlazaUsal
# Abre index.html en tu navegador
```

### Opción 3: Descargar ZIP
1. Ve a este repositorio
2. Click en **Code** → **Download ZIP**
3. Descomprime y abre `index.html`

## 📖 Guía de uso paso a paso

### 1️⃣ Selecciona tu plaza
En la parte superior, elige tu tipo de figura (ASO, PAD, TU, CU, etc.). Los máximos se actualizarán automáticamente.

### 2️⃣ Completa tus datos
Abre cada sección haciendo clic en el encabezado:

**Campos simples:**
- Introduce directamente la puntuación estimada
- Ejemplo: nota de grado 3.5, títulos adicionales 2, etc.

**Campos complejos:**
El sistema calcula automáticamente por ti:

#### Contratos predoctorales
```
Meses: 48
Ámbito: Nacional
→ Sistema calcula: (48/48) × máximo = puntuación automática
```

#### Publicaciones
```
Categoría A: 5
Categoría B: 10  
Categoría C: 8
Categoría D: 3
→ Sistema multiplica por tasas según tu figura y respeta límites
```

#### Congresos
```
Internacionales - Invitaciones: 2
Internacionales - Orales: 5
Internacionales - Pósters: 3
Nacionales - Invitaciones: 1
Nacionales - Orales: 4
Nacionales - Pósters: 2
→ Sistema suma: 2×0.2 + 5×0.1 + 3×0.05 + 1×0.1 + 4×0.05 + 2×0.02 = 1.49 pts
```

### 3️⃣ Observa los resultados
El panel superior muestra:
- **Puntos por sección** en tiempo real
- **Barras de progreso** mostrando cobertura
- **Total estimado** que se actualiza con cada cambio
- **Máximos permitidos** para validación

### 4️⃣ Reinicia si es necesario
Usa el botón **"Reiniciar"** para limpiar todos los campos y empezar de nuevo.

## 📋 Ejemplos de cálculo

### Ejemplo 1: PAD con experiencia equilibrada
```
Formación:
- Grado: 3.5 pts
- Máster: 0.8 pts
- Doctorado con mención: 0.2 pts
Subtotal: 4.5 / 6.5

Docencia:
- 5 años docencia: 5 × 1 = 5 pts
Subtotal: 5 / 6

Investigación:
- 24 meses predoctoral (2 años): 1.5 pts
- 6 artículos Cat A: 6 × 0.4 = 2.4 pts
- 5 congresos internacionales (orales): 5 × 0.1 = 0.5 pts
Subtotal: 4.4 / 6.5

TOTAL ESTIMADO: ~14 pts
```

### Ejemplo 2: CU con investigación fuerte
```
Investigación:
- 15 artículos Cat A: 15 × 0.1 = 1.5 pts
- 20 artículos Cat B: 20 × 0.05 = 1 pt
- 3 sexenios: 3 × 0.5 = 1.5 pts
Subtotal: 4 / 6

Liderazgo:
- Dirección grupo investigación: 1 pt
- 10 tesis doctorales dirigidas: 1 pt
- Director Departamento (3 años): 3 × 0.2 = 0.6 pts
Subtotal: 2.6 / 3

TOTAL ESTIMADO: ~17+ pts
```

## ⚠️ Importante: Descargo de responsabilidad

Esta herramienta proporciona una **estimación orientativa** basada en los criterios del baremo oficial.

**NO es un cálculo oficial.** La evaluación definitiva corresponde a la comisión evaluadora, que:

✗ Aplica criterios cualitativos adicionales no incluidos aquí  
✗ Puede hacer ponderaciones específicas según especialidad de conocimiento  
✗ Valora elementos subjetivos (perfil, méritos preferentes, etc.)  
✗ Tiene discrecionalidad en ciertos aspectos del baremo  

**Usala como guía de estimación, no como predicción definitiva.**

## 📄 Documentación oficial

Para información completa y oficial, consulta:
- **Documento:** Criterios Generales de Aplicación del Baremo
- **Fuente:** Consejo de Gobierno, 25 de julio de 2024
- **Institución:** Universidad de Salamanca
- **Contacto:** vic.profesorado@usal.es

## 🔧 Tecnología

- **HTML5** — Estructura semántica
- **CSS3** — Estilos responsive y modo oscuro
- **JavaScript vanilla** — Sin dependencias externas
- **Funciona completamente offline** — No requiere conexión
- **Compatible con todos los navegadores modernos**

## 📊 Estructura del proyecto

```
├── index.html           # Aplicación completa (HTML + CSS + JS)
├── README.md            # Este archivo
├── .gitignore          # Configuración de Git
└── .netlify.toml       # Configuración para deploy en Netlify
```

El proyecto es una **single-page application (SPA)** con toda la lógica encapsulada en un único archivo HTML.

## 🎓 Características educativas

Esta herramienta también sirve como **referencia educativa** para:
- Entender la estructura del baremo de la USAL
- Ver cómo se puntúan diferentes tipos de méritos
- Comparar el peso de docencia vs investigación vs liderazgo
- Analizar cómo varían los máximos por figura

## 🤝 Contribuciones

Si encuentras:
- ❌ Errores en los cálculos
- 🐛 Bugs en la interfaz
- 💡 Mejoras sugeridas
- 📝 Cambios en el baremo oficial

**Abre un issue o envía un pull request.**

## 💬 Feedback

¿Tienes sugerencias? ¿Encontraste un error?
- Abre un **GitHub Issue**
- O contacta directamente

## 📝 Licencia

MIT License — Libre para usar, modificar y distribuir

```
Copyright (c) 2024

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.
```

## 🙏 Créditos

Desarrollado como herramienta de apoyo para candidatos a plazas docentes en la **Universidad de Salamanca**.

Basado en los criterios oficiales del baremo establecidos por el Consejo de Gobierno de la USAL.

---

**¿Útil?** Comparte esta herramienta con otros candidatos ⭐

**Última actualización:** 2024  
**Versión:** 1.0.0 (Beta)

---

## 🚀 Próximas mejoras (Roadmap)

- [ ] Exportar resultados a PDF
- [ ] Guardar cálculos en navegador (localStorage)
- [ ] Comparar perfiles de diferentes figuras
- [ ] Modo "simulador" para explorar escenarios
- [ ] Integración con especialidades de conocimiento
- [ ] Análisis de competitividad estimada

---

**Para comenzar:** Abre `index.html` en tu navegador y ¡empieza a calcular tus puntos!
