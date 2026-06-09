# 📊 Reporte de Recursos Humanos – Power BI

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-0078D4?style=for-the-badge&logo=microsoft&logoColor=white)
![Status](https://img.shields.io/badge/Estado-Completado-brightgreen?style=for-the-badge)

---

## 📌 Descripción del Proyecto

Este proyecto presenta un **Reporte de Recursos Humanos** desarrollado en Power BI, cuyo objetivo es analizar el perfil demográfico, el desempeño y la estructura salarial de una organización de **194 empleados** distribuidos en 6 departamentos.

El informe está diseñado con enfoque ejecutivo para facilitar la toma de decisiones estratégicas en gestión del talento, compensaciones y desarrollo organizacional.

---

## 🎯 Objetivos del Análisis

- Conocer la composición demográfica del personal (edad, género, ubicación).
- Evaluar el desempeño de los empleados por departamento y grupo de evaluación.
- Analizar la estructura salarial por departamento y rango de sueldo.
- Identificar brechas de género en evaluación y compensación.
- Apoyar decisiones estratégicas de gestión del talento.

---

## 📊 Indicadores Clave (KPIs)

| Indicador | Valor |
|---|---|
| Total Empleados | 194 |
| Edad Promedio | 45,88 años |
| Evaluación Promedio | 7,56 / 10 |
| Sueldo Promedio | $74.721 |

---

## 📈 Visualizaciones Incluidas

- 📌 Tarjetas ejecutivas con KPIs principales
- 📌 Distribución de empleados por departamento
- 📌 Comparativa de sueldo promedio por departamento
- 📌 Evaluación de desempeño por departamento y grupo
- 📌 Distribución por género con métricas de sueldo y evaluación
- 📌 Segmentación por grupo de edad
- 📌 Distribución por rango salarial
- 📌 Filtros dinámicos por departamento, género y ubicación

---

## 🔎 Principales Hallazgos

✅ **Executive Office lidera en compensación** con un sueldo promedio de $124.304, seguido de Sales ($108.962) y Software Engineering ($90.164).

📊 **Production es el departamento más grande** con 73 empleados (37,6% del total), aunque su sueldo promedio ($61.737) está por debajo del promedio organizacional ($74.721).

🏆 **Admin Offices tiene la evaluación más alta** con 8,27 sobre 10, superando incluso al Executive Office (8,05), lo que sugiere un equipo de alto desempeño con compensación por debajo de su aporte.

⚠️ **Sales registra la evaluación más baja** (6,88) siendo a su vez el segundo departamento mejor remunerado, lo que podría indicar una oportunidad de revisión en la política de compensación variable.

👩‍💼 **Las mujeres representan el 55,7% del personal** (108 de 194) y tienen una evaluación promedio superior (7,62 vs. 7,49), aunque perciben un sueldo promedio menor ($71.160 vs. $79.194), una brecha del 10,2% respecto a los hombres.

📅 **El grupo de edad predominante es 29–39 años** (67 empleados, 34,5%), seguido de 40–49 (55) y 50–59 (54), lo que muestra una plantilla equilibrada con experiencia media-alta.

💰 **El 21,6% de los empleados supera los $100.000 de sueldo** (42 empleados), mientras que el 13,9% está por debajo de los $40.000, reflejando una distribución salarial amplia.

---

## 🧮 Medidas DAX Implementadas

```dax
Total Empleados = DISTINCTCOUNT('Tabla Empleados'[ID Empleado])

Edad Promedio = AVERAGE('Tabla Empleados'[Edad])

Evaluacion Promedio = AVERAGE('Tabla Evaluacion'[Evaluación])

Sueldo Promedio = 
CALCULATE(
    AVERAGE('Tabla Sueldo'[Sueldo]),
    'Tabla Sueldo'[Sueldo] > 0
)
```

---

## 🗂 Modelo de Datos

El modelo está compuesto por **3 tablas de datos** y **1 tabla de medidas**:

| Tabla | Descripción |
|---|---|
| `Tabla Empleados` | Datos maestros: ID, nombre, género, departamento, posición, jefe, edad, grupo de edad |
| `Tabla Evaluacion` | Evaluación de desempeño por empleado con categorización por grupo |
| `Tabla Sueldo` | Sueldo por empleado con categorización por rango salarial |

Relaciones: `Tabla Evaluacion` y `Tabla Sueldo` → `Tabla Empleados` a través de `ID Empleado` (Muchos a Uno)

---

## 🛠 Herramientas Utilizadas

- Power BI Desktop
- Power BI Service

## 🧩 Habilidades Aplicadas

- DAX (Data Analysis Expressions)
- Columnas calculadas
- Modelado de datos relacional
- Diseño de visualizaciones ejecutivas
- Storytelling con datos
- Análisis de recursos humanos

---

## 🧠 Enfoque Analítico

El dashboard fue diseñado bajo principios de:

- Jerarquía visual clara orientada a decisiones de RRHH
- Segmentación demográfica por edad, género y ubicación
- Análisis comparativo de desempeño vs. compensación
- Identificación de brechas salariales por género
- Diseño moderno corporativo con KPIs estratégicos

---

## 📂 Estructura del Proyecto

```
reporte-rrhh-powerbi/
│
├── data/
│   └── dataset.csv
│
├── dashboard/
│   └── reporte_rrhh.pbix
│
├── images/
│   └── preview.png
│
└── README.md
```

---

## 📌 Aplicabilidad Empresarial

Este tipo de análisis es útil para:

- Gerencia de Recursos Humanos
- Dirección General y Gerencia Financiera
- Equipos de Compensaciones y Beneficios
- Business Partners de RRHH
- Analistas de Business Intelligence con foco en People Analytics

---

## 👤 Autor

**Ruben Barrios**
Proyecto práctico desarrollado como parte de mi crecimiento profesional en análisis de datos y Business Intelligence.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/ruben-barrios-1430712ab)

---

## ⭐ Si este proyecto te parece interesante

No olvides darle una estrella al repositorio y conectar en LinkedIn.

`#DataAnalytics` `#PowerBI` `#BusinessIntelligence` `#PeopleAnalytics` `#RRHH` `#DAX` `#DataPortfolio` `#HRAnalytics` `#Datdata`
