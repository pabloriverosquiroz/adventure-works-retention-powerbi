# 🚲 Adventure Works — Customer Retention & Sales Analysis

Análisis de retención de clientes y comportamiento de ventas para **Adventure Works**, empresa ficticia de bicicletas con operaciones en Asia, Europa y Norteamérica.

Proyecto final de la certificación **Microsoft Power BI Data Analyst** en Coursera, desarrollado en **Power BI Desktop** como análisis de datos end-to-end.

---

## 📊 Páginas del Dashboard

### 1. Cohorte — Retención de Clientes
Tabla de cohortes que muestra la tasa de retención mensual (`Customer Retention Rate %`) por fecha de primera compra. Permite identificar qué cohortes retienen mejor a sus clientes a lo largo del tiempo.

### 2. Árbol de Descomposición
Visualización jerárquica que descompone el volumen de clientes por **Región → Segmento de Cliente**:
- Asia: 195.901
- Europa: 194.330
- Norteamérica: 194.105

Dentro de Asia, los Retail Stores representan 156.281 clientes frente a 39.620 de Individual Customers.

### 3. Previsión (Forecast)
Serie temporal de nuevos clientes (`Customer ID count`) con modelo de previsión integrado de Power BI, incluyendo bandas de confianza para el período proyectado (2022–2023).

---

## 🗃️ Modelo de Datos

| Tabla | Descripción |
|---|---|
| `Sales` | Tabla principal con 584.336 filas de transacciones |
| `Months After Purchase` | Tabla calculada para análisis de cohortes |

**Campos clave en Sales:**
`Purchase Date`, `Customer ID`, `Customer Segments`, `Product`, `Description`, `Region`, `Age`, `Gender`, `Income`, `Quantity`, `Unit Price`, `Sales Amount`, `Marketing Email Sent`, `First Purchase Date`

**Medidas DAX:**
- `Customer Retention` — clientes que repiten compra por cohorte
- `Customer Retention Rate %` — tasa de retención calculada con `CALCULATE` y `FILTER`

---

## 🛠️ Tecnologías

- **Power BI Desktop**
- **DAX** — medidas y tablas calculadas
- **Power Query (M)** — transformación y limpieza de datos

---

## 💡 Highlights técnicos

- Análisis de cohortes construido desde cero con DAX usando `CALCULATE`, `FILTER` y la tabla auxiliar `Months After Purchase`
- Dataset de más de **584.000 filas** procesado en Power Query
- Segmentación por región, género, edad e ingreso para análisis de comportamiento
- Forecast nativo de Power BI aplicado sobre serie temporal de adquisición de clientes
- Income total analizado: **19,34 mil M**

---

## 🎓 Certificación

Proyecto final del **Microsoft Data Visualization Professional Certificate** — Coursera (Mayo 2025)

5 cursos completados:
- Data Visualization Fundamentals
- Data Preparation and Management
- Data Modeling and Architecture
- Visualization for Data Analysis with Power BI
- Building Powerful Reports and Dashboards in Power BI

🔗 [Verificar certificado](https://coursera.org/verify/professional-cert/RN95VGMJJ1JA)

---

## 📁 Archivos

```
📦 adventure-works-retention-powerbi
 ┗ 📊 Tarea_final_curso.pbix
```

---

## 🚀 Cómo usar

1. Descargar el archivo `.pbix`
2. Abrir con **Power BI Desktop** (gratuito)
3. Navegar entre las 3 páginas: `cohorte`, `arbol`, `Prevision`

> Los datos están embebidos en el archivo, no se requiere conexión a fuente externa.
