# Proyecto ConnectaTel - Análisis de clientes

## 📌 Descripción del proyecto

Este proyecto analiza el comportamiento de los clientes de ConnectaTel utilizando
información sobre usuarios, planes y registros de uso.

El objetivo es identificar patrones de consumo, detectar valores atípicos y
segmentar a los clientes según su edad y nivel de uso.

## 📊 Datos utilizados

El análisis utiliza tres conjuntos de datos:

- `plans.csv`: información de los planes disponibles.
- `users_latam.csv`: información de los clientes.
- `usage.csv`: registros de llamadas y mensajes.

## 🧹 Limpieza de datos

Durante el análisis se detectaron y trataron diferentes problemas:

- Valores `-999` en la columna `age`.
- Valores `"?"` y valores nulos en `city`.
- Fechas de registro posteriores a 2024.
- Valores nulos en `date`.
- Valores nulos en `duration` y `length`, relacionados con el tipo de registro.

Los valores de `duration` y `length` relacionados con el tipo de uso se
mantuvieron como nulos cuando no eran aplicables.

## 👥 Segmentación de clientes

Se crearon dos tipos de segmentos.

### Segmentación por edad

- **Joven:** menores de 30 años.
- **Adulto:** entre 30 y 59 años.
- **Adulto Mayor:** 60 años o más.

### Segmentación por nivel de uso

- **Bajo uso:** menos de 5 llamadas y menos de 5 mensajes.
- **Uso medio:** menos de 10 llamadas y menos de 10 mensajes.
- **Alto uso:** el resto de los usuarios.

## 📈 Principales hallazgos

El análisis mostró que la mayoría de los usuarios presenta niveles moderados
de llamadas y mensajes. También se identificaron usuarios con consumos
considerablemente superiores al comportamiento habitual.

Los valores atípicos encontrados en mensajes, llamadas y minutos de llamada
no fueron eliminados automáticamente, ya que pueden representar usuarios
reales con un consumo elevado.

## 💡 Recomendaciones

- Diferenciar la oferta de planes según el nivel de consumo.
- Analizar oportunidades comerciales para usuarios de alto consumo.
- Considerar beneficios específicos para diferentes segmentos de clientes.
- Mejorar los procesos de captura y validación de datos.
- Utilizar la segmentación para desarrollar estrategias de retención y
  personalización.

## 🛠️ Herramientas utilizadas

- Python
- Pandas
- Seaborn
- Matplotlib
- Jupyter Notebook

## 📁 Archivos del proyecto

- `S7 Version-Estudiante-Project-ConnectaTel.ipynb`
- `README.md`
