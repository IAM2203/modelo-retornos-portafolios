# Modelado de Retornos de Portafolios

## Descripción del Proyecto
Este proyecto analiza y compara el rendimiento histórico de portafolios de inversión bajo diferentes estrategias de gestión. 

Utilizando Python, el script descarga datos financieros reales, simula el comportamiento de los activos a lo largo del tiempo y calcula métricas clave de retorno para determinar la estrategia ganadora.

## Características del Análisis
* **Ingesta de Datos:** Descarga automática de precios históricos ajustados utilizando la librería `yfinance` (Yahoo Finance API).
* **Análisis Descriptivo:** Exploración inicial del comportamiento de los activos individuales.
* **Simulación de Estrategias:**
    * **Retornos Logaritmicos:** Se usan retornos lograitmicos por la facilidad de su uso.
    * **Sesgo y Curtosis:** Análisis de sesgo y curtosis de la distribución de un activo.
    * **Simulaciones Monte Carlo:** se hacen simulaciones Monte Carlo para los reotrnos tanto de un activo como diversos portafolios.
    * **VaR:** Se calcula la máxima perdida esperada después de n días con 95% de confianza.
    * **Optimización de Portafolios:** Se usa el Sharpe Ratio para encontrar la ditribución de activos mas optima. Se encuentra el drawdown para comparar perdida máxima de diversos portafolios en el tiempo.
    * **Modelo GARCH:** Se buscó un modelo con volatilidad cambiante en el tiempo ya que estos modelan de mejor manera el comportamiento real del mercado.
    * **Análisis de Noticias:** Se hace un primer acercamiento a modelos que leen noticias analizan el impacto que estas tendrían en la volatilidad.
    * **Buy & Hold (Sin tocar):** Simulación de una cartera estática donde no se intervienen los pesos iniciales
    * **Rebalanceo Trimestral:** Ajuste periódico de la cartera para mantener la asignación de activos objetivo.
* **Resultados:** Cálculo comparativo del rendimiento total (%) y visualización del valor del portafolio en el tiempo (Base $100).

## Tecnologías Utilizadas
* **Python 3.11**
* **yfinance:** Para la obtención de datos de mercado.
* **Pandas & NumPy:** Para la manipulación de series de tiempo y cálculos financieros vectorizados.
* **Matplotlib:** Para la generación de gráficos comparativos (Curvas de equidad).

## Visualización
El proyecto genera gráficos que permiten visualizar la divergencia entre estrategias, destacando momentos clave donde el rebalanceo protegió capital o limitó ganancias (según el comportamiento del mercado).

---
*Proyecto desarrollado por Iñaki Aréchiga como parte de mi portafolio de Data Science y Finanzas.*
