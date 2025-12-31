# Predicción de Cancelación de Clientes (Churn) - Interconnect
## 1. Descripción del problema (Churn)
El objetivo de este proyecto es construir un modelo de Machine Learning que permita a la operadora de telecomunicaciones Interconnect pronosticar su tasa de cancelación de clientes. La detección temprana de usuarios que planean abandonar el servicio permitirá al equipo de marketing actuar proactivamente ofreciendo códigos promocionales y planes especiales para mejorar la retención.

## 2. Datos
- Se utilizó un conjunto de datos integrado a partir de cuatro fuentes principales mediante el identificador customerID:
- Datos Contractuales (contract.csv): Información sobre el tipo de contrato (mensual, anual, etc.), métodos de pago y cargos.
- Datos Personales (personal.csv): Género, si el cliente es adulto mayor y si tiene dependientes o pareja.
- Servicios de Internet (internet.csv): Tipo de conexión (DSL o Fibra Óptica) y servicios adicionales como seguridad y backup.
- Servicios de Telefonía (phone.csv): Si el cliente tiene líneas múltiples.

El dataset final consistió en 7,043 registros y 20 columnas. Durante el análisis exploratorio (EDA), se identificaron y manejaron valores nulos en servicios no contratados y se corrigieron errores en la columna TotalCharges.

## 3. Modelos 
En el desarrollo del proyecto se probaron distintas alternativas de modelado para clasificación binaria, incluyendo:
- Modelos Lineales: Regresión Logística.
- Modelos de Ensamble: Random Forest Classifier.
- Potenciación de Gradiente (Boosting): Gradient Boosting Classifier y XGBClassifier.

Se implementaron técnicas de preprocesamiento como OneHotEncoder para variables categóricas, StandardScaler para variables numéricas, y manejo de desequilibrio de clases mediante compute_sample_weight.

## 4. Métricas principales
La evaluación de los modelos se centró en métricas robustas para problemas de clasificación, tales como:
- ROC-AUC: Métrica principal para medir la capacidad de discriminación del modelo entre clientes que cancelan y los que no.
- F1-Score: Para balancear la precisión y el recobro (recall).
- Matriz de Confusión: Para visualizar el desempeño detallado de las predicciones.

## 5. Conclusión
En base al análisis realizado en el documento, se concluye que:
Se logró integrar y limpiar con éxito la información de diversas fuentes, generando variables clave como tenure (antigüedad) y el objetivo churn.
El manejo de valores nulos y la ingeniería de características fueron fundamentales para fortalecer el modelado.

La comparación de modelos permitió seleccionar la mejor alternativa justificada por las necesidades del negocio de Interconnect, demostrando capacidad para identificar patrones de comportamiento que preceden a la cancelación del servicio.

Nota: Asegúrate de completar los valores exactos de las métricas (como el valor final de ROC-AUC) que obtuviste en las últimas celdas de tu notebook antes de publicar el README.

