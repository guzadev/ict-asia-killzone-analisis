# 📊 Análisis ICT: Influencia del Rango Asiático sobre el Resultado de la Operación

Este proyecto forma parte de un enfoque basado en la metodología **ICT (Inner Circle Trader)** y el concepto de **Smart Money**. El análisis busca determinar si la **amplitud del rango de la sesión asiática (Kill Zone)** respecto al **promedio de los últimos 5 días (AVG)** puede influir significativamente en la probabilidad de éxito de una operación, tanto en **EUR/USD** como en **NQ1!**.

## 🧠 Objetivo

Explorar si la condición *"Rango < Promedio 5 días"* es un **filtro válido** para decidir si vale la pena operar un día determinado según la estructura de mercado, ayudando a evitar escenarios poco favorables o entradas forzadas.

---

## 🧪 Enfoque de backtesting

Este proyecto se enmarca como un **backtesting personal y manual**, realizado originalmente mediante observación directa en **TradingView** y registro de datos en **Excel**.

> Para marcar los rangos de la sesión asiática y calcular su amplitud, se utilizó el indicador gratuito:  
> 📌 **ICT Killzones & Pivots [TFO]** creado por [`tradeforopp`](https://www.tradingview.com/u/tradeforopp/), disponible en la librería pública de TradingView.

No se trata de un sistema automatizado ni predictivo, sino de un análisis exploratorio orientado a validar hipótesis sobre condiciones históricas del mercado. El objetivo es identificar **patrones estadísticos repetibles** que puedan servir como filtro para aumentar la calidad de las decisiones operativas dentro de una estrategia basada en la estructura de mercado (Smart Money / ICT).

En este caso particular, se explora:

- ¿Tiene sentido filtrar días según la amplitud del rango asiático?
- ¿Aumenta la probabilidad de éxito si el rango es menor al promedio de los últimos 5 días?

---

## 📌 Contenido del proyecto

- 🔄 Limpieza de datos y estandarización (`none`, nulos, strings inconsistentes)
- 📊 Análisis exploratorio (EDA) con pandas
- 🧮 Tablas de doble entrada con `crosstab` (% por grupo)
- 🔥 Mapa de calor multivariable: activo + rango vs resultado
- 📉 Gráficos apilados personalizados con etiquetas
- ✅ Conclusiones operativas aplicables a trading ICT

---

## 📁 Estructura del proyecto

```
kill-zone-asia-analysis/
├── kill-zone-asia-analysis.ipynb       # Notebook principal con el análisis
├── README.md                           # Documentación del proyecto
├── requirements.txt                    # Dependencias necesarias
├── .gitignore                          # Exclusiones para Git
└── datos/
    └── asia.csv                        # Dataset utilizado (rango, AVG, resultado, activo)
```

---

## 📈 Resultados destacados

- Cuando el **rango es menor al promedio**, se observa una **mayor tasa de ganancia**, especialmente en **EUR/USD** (90.9% de aciertos).
- Cuando el **rango es mayor al promedio**, aumenta considerablemente la probabilidad de que **no se genere entrada válida**, sobre todo en días con estructura desfavorable.
- Este análisis respalda el uso del *"rango vs promedio"* como criterio para **filtrar días operables con mayor probabilidad de éxito**.

---

## ⚙️ Requisitos técnicos

- Python 3.10+
- pandas
- matplotlib
- seaborn
- jupyterlab (opcional, para edición visual del notebook)

Instalación rápida:

```bash
pip install -r requirements.txt
```

---

## 📤 Cómo ejecutar

1. Cloná el repositorio:
```bash
git clone https://github.com/guzadev/ict-asia-killzone-analisis.git
```

2. Iniciá el notebook:
```bash
cd mi-analisis-ict-rango
jupyter lab
```

3. Explorá el análisis en `analisis_rango.ipynb`.

---

## 👨‍💻 Autor

**[guzadev](https://github.com/guzadev/ict-asia-killzone-analisis)**  
Trader autodidacta explorando patrones estadísticos en estrategias de manipulación institucional.  
Apasionado por la automatización de filtros operativos basados en estructura de mercado.

---

## ⚠️ Disclaimer

Este análisis tiene fines educativos y de documentación técnica.  
No representa una recomendación financiera ni una estrategia de trading garantizada.
