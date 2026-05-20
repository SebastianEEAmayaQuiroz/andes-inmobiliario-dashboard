<div align="center">

<!-- BANNER PRINCIPAL — click redirige a la página web del proyecto -->
<a href="https://sebastianeeamayaquiroz.github.io/andes-inmobiliario-dashboard/" target="_blank">
  <img src="https://img.shields.io/badge/🌐%20Ver%20Proyecto%20Completo%20en%20Web-%20Haz%20click%20aquí-1a6b4a?style=for-the-badge&labelColor=0b1a12&color=1a6b4a" alt="Ver proyecto completo" />
</a>

<br/><br/>

<!-- BANNER POWER BI -->
<a href="https://app.powerbi.com/view?r=eyJrIjoiOTk5NmVhYTQtNTUyMi00MGExLWIyNDItYjNkODkxYjVmNzQ0IiwidCI6ImY5NGJmNGQ5LTgwOTctNDc5NC1hZGY2LWE1NDY2Y2EyODU2MyIsImMiOjR9" target="_blank">
  <img src="https://img.shields.io/badge/Power%20BI-Ver%20Dashboard%20Interactivo-F2C811?style=for-the-badge&logo=powerbi&logoColor=black" alt="Abrir en Power BI" />
</a>

<!-- BANNER GOOGLE COLAB -->
<a href="https://colab.research.google.com/drive/1ExPBLFtuD6xTcBzFCy4YeweP5Rccl0B5?usp=sharing" target="_blank">
  <img src="https://img.shields.io/badge/Google%20Colab-Ver%20Notebook-F9AB00?style=for-the-badge&logo=googlecolab&logoColor=black" alt="Abrir en Google Colab" />
</a>

<br/><br/>

<img src="https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black" />
<img src="https://img.shields.io/badge/DAX-F2C811?style=for-the-badge&logo=powerbi&logoColor=black" />
<img src="https://img.shields.io/badge/Power%20Query-F2C811?style=for-the-badge&logo=powerbi&logoColor=black" />
<img src="https://img.shields.io/badge/Excel-217346?style=for-the-badge&logo=microsoftexcel&logoColor=white" />
<img src="https://img.shields.io/badge/Modelo%20Estrella-Esquema%20Dimensional-1a6b4a?style=for-the-badge" />

# 🏢 Dashboard Comercial Inmobiliario 2023–2024
### Grupo Andes Inmobiliario

**¿Qué tipos de propiedad, canales y segmentos de cliente generan más valor — y están volviendo a comprar?**

</div>

---

## 📌 Contexto del negocio

Grupo Andes Inmobiliario opera en **Colombia y México** (Bogotá y Ciudad de México) con tres tipos de propiedad: Casa, Departamento y Comercial. El equipo directivo necesitaba un dashboard ejecutivo de tres vistas para monitorear desempeño general, análisis comercial y recurrencia de clientes mediante cohortes — todo sobre un modelo estrella con datos reales de 8,500 transacciones.

---

## 🎯 Preguntas de negocio respondidas

| Dimensión | Pregunta |
|---|---|
| Desempeño general | ¿Cuál es el ingreso total, ventas, ticket promedio y comisión? |
| Análisis comercial | ¿Qué tipo de propiedad, canal y segmento generan más ingresos? |
| Análisis temporal | ¿Cómo evolucionan las ventas? ¿Hay crecimiento YoY? |
| Cohortes | ¿Los clientes vuelven a comprar? ¿Qué cohortes son más valiosas? |

---

## 📐 Modelo de datos — Esquema Estrella

```
                    ┌─────────────────┐
                    │   dim_fecha     │
                    │  (732 registros)│
                    └────────┬────────┘
                             │ 1:*
┌──────────────┐    *:1  ┌───┴──────────────────────┐  1:*  ┌──────────────────┐
│ dim_clientes │ ───────▶│  hecho_ventas_propiedades │◀───── │ dim_propiedades  │
│ (3,500 reg.) │         │      (8,500 hechos)       │       │  (8,000 reg.)    │
└──────────────┘         └──────────────────────────┘       └──────────────────┘
```

**Relaciones:** Cardinalidad uno a muchos (1:*) · Filtro simple (single) · Todas activas

---

## 📊 Métricas principales

| Métrica | Valor |
|---|---|
| **Ingreso Total** | $6,012,502,170 |
| **Cantidad de Ventas** | 8,500 transacciones |
| **Ticket Promedio** | $707,353 |
| **Comisión Total** | $200,627,166 |
| **Crecimiento YoY** | **+11.1%** (2023 → 2024) |

---

## 📐 Estructura del dashboard — 3 vistas

### Vista 1 — Overview Ejecutivo
*¿Cómo está el negocio en general?*

- KPIs: Ingreso Total · Cantidad de Ventas · Ticket Promedio · Comisión Total
- Tendencia de ventas mensual en el tiempo
- Ingresos / ventas por ciudad (Bogotá vs Ciudad de México)
- Crecimiento Year over Year (YoY)

### Vista 2 — Análisis Comercial
*¿Qué productos, canales y clientes generan más valor?*

- Ingreso por tipo de propiedad (Casa 37.3% · Comercial 32.0% · Departamento 30.7%)
- Ventas e ingresos por canal (Corredor vs Directo)
- Ventas e ingresos por segmento de cliente
- Tabla con formato condicional (semáforo): tipo_propiedad × Ingreso · Ventas · Ticket
- Tooltips con medidas de participación (%)

### Vista 3 — Análisis de Cohortes
*¿Vuelven a comprar los clientes?*

- Matriz de cohortes: filas → Mes Cohorte · columnas → Mes Venta
- Valores: Cantidad de Ventas o Ingreso Total
- Permite comparar retención y recurrencia entre cohortes

---

## 🔍 Hallazgos clave

- **Casa** es el tipo de propiedad con mayor revenue (37.3%), seguido de Comercial (32.0%) y Departamento (30.7%)
- **Ciudad de México** lidera en volumen de transacciones (4,123 vs 4,377 en Bogotá — mercados muy parejos)
- **Corredor** es el canal dominante (6,181 vs 2,319 Directo — 72.7% de las ventas)
- El negocio crece **+11.1% YoY** — señal de expansión sostenida
- El segmento **"Primera vez"** concentra la mayor parte del ingreso (1,906 clientes)
- La cohorte de **marzo 2023** muestra la mayor recurrencia de compra

---

## 💡 Insights accionables

1. **Diseñar productos para compradores "Primera vez"** — Son el segmento más voluminoso; financiamientos y comunicaciones diferenciadas pueden aumentar la tasa de retención
2. **Analizar la cohorte de marzo 2023** — Presenta mayor recurrencia; sus características de adquisición pueden replicarse como modelo
3. **Evaluar costo-beneficio del canal Corredor** — Domina en ingresos pero las comisiones son más altas; comparar margen neto vs canal Directo
4. **Casa y Comercial tienen distribución equilibrada** — Diversificar el portafolio entre las tres categorías reduce dependencia de un solo tipo

---

## 🛠️ Medidas DAX creadas

```dax
-- Medidas base
Ingreso Total = SUM(hecho_ventas_propiedades[precio_venta])
Cantidad Ventas = COUNTROWS(hecho_ventas_propiedades)
Ticket Promedio = DIVIDE([Ingreso Total], [Cantidad Ventas], 0)
Comisión Total = SUM(hecho_ventas_propiedades[monto_comision])

-- Medidas de participación (contexto de filtro)
% Participación Tipo Propiedad =
  DIVIDE(
    [Ingreso Total],
    CALCULATE([Ingreso Total], ALL(hecho_ventas_propiedades[tipo_propiedad])),
    0
  )

% Participación Canal =
  DIVIDE(
    [Ingreso Total],
    CALCULATE([Ingreso Total], ALL(hecho_ventas_propiedades[canal_venta])),
    0
  )

% Participación Segmento =
  DIVIDE(
    [Ingreso Total],
    CALCULATE([Ingreso Total], ALL(dim_clientes[segmento_comprador])),
    0
  )
```

---

## 📅 Tabla calendario DAX

```dax
dim_fecha =
ADDCOLUMNS(
  CALENDAR(
    MIN(hecho_ventas_propiedades[fecha_venta]),
    MAX(hecho_ventas_propiedades[fecha_venta])
  ),
  "Año", YEAR([Date]),
  "Mes", FORMAT([Date], "MMMM"),
  "Mes_Numero", MONTH([Date]),
  "Año_Mes", FORMAT([Date], "YYYY-MM")
)
```

---

## 📂 Dataset

| Tabla | Registros | Descripción |
|---|---|---|
| `hecho_ventas_propiedades` | 8,500 | Transacciones: precio, cliente, propiedad, canal, fecha |
| `dim_clientes` | 3,500 | Segmento, país, ciudad |
| `dim_propiedades` | 8,000 | Tipo, tamaño, ubicación, categoría |
| `dim_fecha` | 732 | Calendario: año, mes, mes_num, año-mes |

**Período:** Enero 2023 – Diciembre 2024 · **Países:** Colombia · México · **Ciudades:** Bogotá · Ciudad de México

---

## 🗂️ Estructura del proyecto

```
andes-inmobiliario-dashboard/
├── datos_inmobiliario_limpios.xlsx                         # Dataset (4 tablas · esquema estrella)
├── S11_Estudiante_Proyecto_InmobiliarioGrupoAndes.ipynb    # Notebook de planificación
├── index.html                                              # Página web del proyecto (GitHub Pages)
└── README.md
```

---

## 🚀 Acceder al proyecto

<div align="center">

[![Power BI Dashboard](https://img.shields.io/badge/Power%20BI-Abrir%20Dashboard%20Interactivo-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)](https://app.powerbi.com/view?r=eyJrIjoiOTk5NmVhYTQtNTUyMi00MGExLWIyNDItYjNkODkxYjVmNzQ0IiwidCI6ImY5NGJmNGQ5LTgwOTctNDc5NC1hZGY2LWE1NDY2Y2EyODU2MyIsImMiOjR9)

[![Google Colab](https://img.shields.io/badge/Google%20Colab-Ver%20Notebook%20de%20Planificación-F9AB00?style=for-the-badge&logo=googlecolab&logoColor=black)](https://colab.research.google.com/drive/1ExPBLFtuD6xTcBzFCy4YeweP5Rccl0B5?usp=sharing)

</div>

---

## 👤 Autor

**Sebastián Amaya** — Analista de Datos | Contador Público en formación

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/sebastianamayada)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/SebastianEEAmayaQuiroz)

---

*Proyecto desarrollado como parte del Bootcamp de Análisis de Datos — TripleTen (2025–2026)*
