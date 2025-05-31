# Capstone Project – Apertura Óptima de una Cafetería en Toronto

## Descripción del Problema y Antecedentes

Abrir una cafetería puede parecer una idea sencilla, pero elegir **dónde abrirla** marca la diferencia entre el éxito y el fracaso. La ciudad de Toronto, con su diversidad cultural, gran población urbana y alto flujo de visitantes, es un lugar con mucho potencial… pero también con mucha competencia.

En este contexto, este análisis tiene como objetivo **identificar las zonas más prometedoras de Toronto para establecer una nueva cafetería**, teniendo en cuenta tres factores clave:  

- La **densidad de población** (cuántas personas viven en la zona)  
- El **número de cafeterías existentes** (para estimar la competencia)  
- La **presencia de otros puntos de interés**, como oficinas, tiendas o parques (que atraen flujo de personas)

La idea es sencilla: si una zona tiene **mucha gente**, **poca competencia** y **alta actividad**, entonces es una buena candidata para abrir una nueva cafetería.

Este tipo de análisis puede ser muy útil para emprendedores, pequeñas empresas o cadenas que buscan expandirse de manera inteligente, **basando sus decisiones en datos reales y no solo en intuición**.  
Además, al usar datos abiertos y herramientas de análisis geoespacial, se ofrece una metodología que podría replicarse en otras ciudades o negocios similares.

---

## Fuente e Ingesta de Datos

Para llevar a cabo este análisis se utilizan tres fuentes de datos principales:

### 1. API de Foursquare (versión 3)

Se utiliza la API oficial de Foursquare para obtener información geolocalizada de lugares en la ciudad de Toronto, incluyendo:

- **Ubicación de cafeterías**: para estimar la competencia en cada zona (FSA)
- **Otros puntos de interés**: oficinas, tiendas, parques, etc., que generan tráfico peatonal

Para cada lugar se recopilan datos como el nombre, categoría, dirección y coordenadas geográficas.

### 2. Datos censales de Toronto

Se utilizan los datos abiertos del Gobierno de Toronto que contienen información sociodemográfica por código postal (FSA), especialmente la **densidad de población**.

Esta variable es fundamental para estimar la demanda potencial de cada zona.

### 3. Coordenadas geográficas por FSA

Para visualizar correctamente los resultados en un mapa, se incorpora un conjunto de datos externo que proporciona las coordenadas (latitud y longitud promedio) asociadas a cada FSA.

Fuente: [Canadian Forward Sortation Areas with Coordinates – Mendeley Data](https://data.mendeley.com/datasets/9yj9d4dsnf/1)

---

## Integración de Datos

Todos los datos obtenidos se integran en un único conjunto estructurado, donde cada fila representa un FSA y contiene:

- Código postal (FSA)
- Densidad de población
- Número de cafeterías
- Número de puntos de interés
- Coordenadas geográficas

Esta estructura permite aplicar técnicas de análisis espacial, clustering y visualización para responder a la pregunta central:  
**¿Dónde es mejor abrir una nueva cafetería en Toronto?**

---

_Entrega correspondiente a la Semana 1 del proyecto final del curso "Applied Data Science Capstone" de Coursera._
