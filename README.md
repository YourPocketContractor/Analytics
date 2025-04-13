# Analytics

## Metodologia:


### Ciclo 1

1. Dada una descripcion de la aplicacion, generar una lista de aplicaciones similares con su respectivo score de similitud y razones por las que difiere.

 **Identificación de Aplicaciones Similares**  
   *Input:* Descripción funcional de la plataforma (MVP Scope)
  
   *Proceso:*  
   - 1.1 Definición de métricas de similitud:  
     $$s = \sum \beta_i\cdot \text{metrica}$$  

2. Filtrar las aplicaciones con mas similitud, basado en metricas

3. Realizar analisis de mercado de cada una de las aplicaciones resultantes, analisis de mercado formal, usando ecoonometria, que cubre:
  *Modelos a aplicar:*  
   
   3.1 **Análisis de Demanda**  
   - Regresión lineal múltiple para estimar:  
     ```
     DAU = β₀ + β₁(precio_servicio) + β₂(disponibilidad_contratistas) + β₃(rating_plataforma) + ε
     ```  
   - Test de Dickey-Fuller para estacionalidad en uso de plataforma  

   3.2 **Análisis de Oferta**  
   - Modelo Logit para probabilidad de adopción por contratistas:  
     ```
     P(adopción) = 1/(1 + e^-(θ₀ + θ₁(ingreso_potencial) + θ₂(costo_implementación)))
     ```  
   - Análisis de clusters para segmentación de contratistas  

4. **Socialización de Resultados**  
   *Entregables en [Business-Economia](https://github.com/...):*  
   - Reporte técnico en LaTeX (`/informes/analisis_mercado.pdf`)  
   - Dashboard ejecutivo (Power BI) con:  
     - Heatmap de competencia  
     - Proyección de adopción regional  
     - Sensitivity analysis de precios  
   - Presentación stakeholders (`/presentaciones/ciclo1.pptx`)

### Metodo

1.
   1.1 Definicion de Cliente MCP:
    1.1.1 Creacion de **sampling**, metricas que determinan grado de similitud, sobre el cual se hace el criterio de busqueda.

   1.2 Uso de MCP con servidores web-scrapers parta obtener aplicaciones similares
