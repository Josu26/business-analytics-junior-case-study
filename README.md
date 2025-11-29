# Business Analytics Junior – Case Study (Power BI)

Este repositorio recoge una prueba técnica de **Business Analytics / Data Analyst Junior**, basada en un programa de **activaciones comerciales** realizadas por vendedores en distintos puntos de venta de un cliente del sector **FMCG (gran consumo)**.

El objetivo del caso es **construir un cuadro de mando en Power BI** que permita:

- Analizar la evolución temporal del programa (semanal, mensual, trimestral).
- Medir el funnel comercial completo: Visitas → Contactos → Presentaciones → Leads → Ventas.
- Comparar la estructura real de **POS** y **Vendedores** frente a la estructura teórica del programa.
- Calcular el **coste semanal, coste por hora y coste por activación** por canal y perfil profesional.

> ⚠️ Por confidencialidad, los datos originales no se incluyen en este repositorio. El proyecto se basa en una prueba técnica de selección y se ha anonimizado el contexto del cliente.

---

## 🧩 Estructura del proyecto

- `/docs`
  - `DOCUMENTO_EJECUTIVO_PUBLICO.pdf`  
    Documento ejecutivo donde se explica el contexto de negocio, el enfoque de análisis, el modelado de datos y las conclusiones clave.
- `/img`
  - `dashboard_page1_overview.png` – Página 1: Evolución & funnel comercial.
  - `dashboard_page2_pos_vendors.png` – Página 2: Corrección de POS y vendedores (real vs teórico).
  - `dashboard_page3_costs.png` – Página 3: Costes del programa (coste semanal, hora y activación).
- `Business_Analytics_Junior_Case_Study_Public.pbix`  
  Archivo de Power BI Desktop con el modelo de datos y el informe completo.

---

## 🧠 Enfoque de trabajo

El trabajo se organiza siguiendo una estructura tipo CRISP-DM:

### 1. Business Understanding

- Definición de objetivos del cliente:
  - Medir rendimiento del programa de activaciones.
  - Entender dónde se pierden oportunidades en el funnel.
  - Validar si la estructura de POS y vendedores coincide con el plan teórico.
  - Evaluar la rentabilidad y los costes por canal y perfil. 

### 2. Data Understanding

- Análisis exploratorio de la tabla operativa (visitas, activaciones, horas, contactos, presentaciones, leads, ventas, pruebas guiadas).
- Revisión de la tabla de costes (roles, coste semanal, % de participación y canal).
- Detección de:
  - Inconsistencias textuales (por ejemplo en tipos de POS).
  - Meses en texto, necesidad de convertir a fechas estándar.
  - Valores atípicos y posibles errores en estructura (POS y vendedores). :contentReference[oaicite:6]{index=6}

### 3. Data Preparation & Modeling

- Limpieza y estandarización:
  - Eliminación de registros vacíos o sin identificadores.
  - Normalización de `POS_TYPE` (Retail, Horeca, T&P).
  - Creación de la columna `Date` y derivadas: `Month_Number`, `Quarter`, `WeekOfYear`. 
- Cálculo de KPIs del funnel con medidas seguras:
  - `Contact_Rate`, `Presentation_Rate`, `Lead_Rate`, `Purchase_Rate`, `GT_Purchase_Rate`.
- Modelado en forma de **estrella**:
  - Tablas de hechos separadas por canal (Retail, Horeca, T&P).
  - Dimensiones para canal y costes.
  - Medidas DAX para costes:
    - Coste semanal del programa.
    - Coste por hora (40h/semana).
    - Coste por activación global y por canal. 

---

## 📊 Diseño del dashboard

### Página 1 – Evolución & Funnel

- KPIs de volumen (activaciones, presentaciones, leads, ventas, tasa de contacto). :contentReference[oaicite:9]{index=9}
- Gráficos de:
  - Evolución mensual de activaciones, leads, ventas y presentaciones.
  - Evolución semanal y trimestral de activaciones.
- Funnel completo desde contactos hasta ventas, mostrando:
  - Totales por etapa.
  - Porcentajes de conversión.
  - Pérdidas por fase.

### Página 2 – POS & Vendedores (Real vs Teórico)

- KPIs:
  - POS según plan vs POS reales.
  - Vendedores según plan vs vendedores reales.
- Tablas por isla, destacando el exceso de POS y de vendedores respecto al diseño teórico del programa. :contentReference[oaicite:10]{index=10}
- Texto ejecutivo explicando el impacto y la necesidad de depuración del dataset de origen.

### Página 3 – Costes del Programa

- KPIs:
  - Coste semanal del programa.
  - Coste por hora.
  - Coste por activación.
- Tabla comparativa por rol:
  - Coordinator, Vendor, Manager: coste semanal, horas, activaciones, coste/hora y coste/activación. :contentReference[oaicite:11]{index=11}
- Gráficos por canal (Retail, Horeca, T&P) para analizar diferencias de coste por activación.

---

## 🔍 Principales insights

Algunos ejemplos de conclusiones obtenidas:

- Eficiencia global del funnel en torno al **6–7%** (Ventas / Contactos), con las mayores caídas entre contactos → smokers y presentaciones → leads. 
- Exceso importante de POS y vendedores respecto al diseño teórico, lo que sugiere problemas en el registro de datos o un sobredimensionamiento operativo.
- Coste semanal del programa en torno a los **4.5k €**, con coste/hora competitivo y un coste por activación que varía significativamente por canal, siendo **Horeca** el más costoso y **Retail** el más equilibrado en relación coste–eficiencia. 

---

## 🛠️ Tecnologías y habilidades utilizadas

- **Power BI Desktop**
  - Power Query (M) para limpieza y transformación.
  - Modelado en estrella y relaciones 1:N.
  - Medidas DAX para KPIs de negocio y costes.
- **Análisis de negocio**
  - Definición de KPIs alineados con los objetivos del cliente.
  - Diseño de dashboards ejecutivos enfocados en decisiones.
- **Storytelling con datos**
  - Documentos ejecutivos (versión extendida y compacta).
  - Insights claros y accionables para dirección y operaciones.

---

## ▶️ Cómo abrir el informe

1. Descarga el archivo `Business_Analytics_Junior_Case_Study_Public.pbix`.
2. Ábrelo con **Power BI Desktop** (versión actual).
3. Navega por las 3 páginas del informe:
   - Página 1: Evolución & Funnel.
   - Página 2: POS & Vendedores.
   - Página 3: Costes.
