# forecast-time-series-suite

Escenario
- Fuentes de datos nuevas y cambiantes
- Poca información histórica
- Se van agregando fuentes de ingresos; horizonte de predicción variable
- Poco tiempo de salida para entregar MVP
- Capacidad limitada de entrenamiento

Solución
- Para la implementación se utilizaron modelos preentrenados de la librería TimeSeriesLib, orientados al pronóstico de series temporales. Cada semana, todos los modelos competirán entre sí y se seleccionará aquel que haya demostrado el mejor rendimiento durante el mes anterior. El flujo de trabajo está diseñado para que, cada vez que se añada un nuevo modelo a TimeSeriesLib, este pueda competir con cambios mínimos en el código, garantizando que las predicciones sean homogéneas. Además, se podrán configurar dinámicamente distintos horizontes de tiempo, frecuencia y métricas.
- Modelos preentrenados
- Librería TimeSeriesSuite: multifrecuencia, multidominio (varios datasets), multihorizonte, dimensión variable, zero shot forecasting (sin historico). 
- Salesforce: Moirai
- Amazon: Chronos

Arquitectura: 
1. Data Ingestion
2. Feature Engineering (transformación y normalización de variables)
3. Prediction
4. Evaluation  
