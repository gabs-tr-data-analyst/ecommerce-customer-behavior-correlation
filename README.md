# 🛍️ Factores de comportamiento asociados al ingreso anual — NovaRetail+

> Análisis correlacional del comportamiento de clientes para el equipo de Crecimiento y Retención de una plataforma de e-commerce en Latinoamérica.

---

## 📌 Contexto

NovaRetail+ es una plataforma de e-commerce en Latinoamérica con millones de usuarios. Para el cierre de 2024, el equipo de **Crecimiento y Retención** necesitaba responder:

> **¿Qué factores del comportamiento del cliente están más fuertemente asociados con el ingreso anual generado?**

Se realizó un análisis correlacional completo sobre un dataset de **15,000 clientes** (comportamiento, satisfacción, segmentación y valor económico), con el objetivo de producir un reporte claro, responsable y accionable — sin caer en interpretaciones causales que los datos no respaldan.

---

## 🛠️ Stack

| Herramienta | Uso |
|---|---|
| 🐍 Python | Lenguaje principal del análisis |
| 🐼 pandas / NumPy | Limpieza y manipulación de datos |
| 📊 seaborn / Matplotlib | Visualización (scatterplots, heatmaps) |
| 📐 SciPy | Correlación punto-biserial, chi-cuadrado |

---

## 📁 Estructura del repositorio

```
novaretail-comportamiento-clientes/
│
├── 📓 notebook/
│   └── analisis_novaretail.ipynb     # Análisis completo, paso a paso
│
├── 🖼️ img/
│   └── heatmap_1.png                 # Visualización clave referenciada en este README
│
└── 📝 README.md
```

---

## 📊 Visualizaciones

![Heatmap de correlaciones](img/heatmap_1.png)
*Matriz de correlación completa — destaca la cadena publicidad → visitas → compras → ingreso (r=0.97 entre compras e ingreso) y la desconexión del programa Premium con el resto de las variables.*

---

## 🔍 Decisiones clave

- ⚖️ Se trató el análisis explícitamente como **correlacional, no causal**: el lenguaje de los hallazgos se ajustó para hablar de "asociación" en vez de "influencia" o "determina".
- 🎯 Se usó correlación **punto-biserial** solo para pares binaria-numérica, y **V de Cramér** para cruces categóricos, en vez de aplicar Pearson de forma genérica a todo el dataset.
- 🧹 Antes de correlacionar, se validó la carga de datos, los tipos y los valores faltantes, para no construir hallazgos sobre un dataset mal entendido.

---

## 📈 Hallazgos principales

**1️⃣ La cadena publicidad → visitas → compras → ingreso es clara... pero el freno está en la plataforma**
Correlación hasta r = 0.97 entre compras e ingreso. Sin embargo, el cuello de botella real está en la conversión dentro de la plataforma, no en el presupuesto publicitario.

**2️⃣ El programa Premium no está moviendo la aguja**
Correlaciones prácticamente nulas con ingreso y engagement — señal para que Producto reestructure sus beneficios.

**3️⃣ La demografía no predice comportamiento, pero hay un segmento oculto de "ballenas"**
Edad e ingreso no correlacionan con el comportamiento transaccional, pero el análisis reveló un nicho de clientes de alto gasto y pocas visitas.

**4️⃣ La satisfacción es un escudo débil contra el abandono**
No basta por sí sola para predecir retención (r = -0.026).

---

## ⚠️ Limitaciones y próximos pasos

**Limitaciones:** correlación ≠ causalidad · falta de contexto cualitativo (motivos reales de cancelación) · sin estacionalidad en el dataset.

**Próximos pasos propuestos:** segmentación regional · segmentación por tipo de dispositivo · análisis RFM · pruebas A/B en el programa Premium.

---

## 🔗 Enlaces

- 📘 [Caso completo con contexto de negocio →](https://app.notion.com/p/Gabriela-Triana-BI-Analyst-Power-BI-aadd07c9675c824bbe1001f9ba9db7b9?source=copy_link)
- 💼 [LinkedIn](https://www.linkedin.com/in/gabriela-triana-data-analyst/)
