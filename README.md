# LM Profesionales — Proyecto Coderhouse
## Primera entrega: obtención de insights a partir de visualizaciones
### Problema de negocio
LM Profesionales necesita una visión integrada de sus registros para identificar qué servicios generan más importe y contribución, cómo se distribuye la actividad por localidad, cuál es el estado operativo de los trabajos y qué nivel de concentración existe en la cartera de clientes.
### Entregables
- `notebooks/LM_Profesionales_EDA.ipynb`: notebook Python para Google Colab/Jupyter con importación de datos, limpieza, validaciones, EDA, visualizaciones e insights.
- `entregables/LM_Profesionales_Coderhouse_Primera_Entrega.pptx`: presentación ejecutiva de 10 diapositivas.
- `data/01_base_lm_anonimizada.csv`: base de trabajo anonimizada. Los nombres fueron reemplazados por etiquetas derivadas del ID de cliente.
- `figures/`: gráficos utilizados en la presentación.
### Cómo ejecutar el notebook
1. Abrir `notebooks/LM_Profesionales_EDA.ipynb` en Google Colab o Jupyter.
2. Mantener la estructura de carpetas del proyecto o subir `data/01_base_lm_anonimizada.csv` cuando el notebook lo solicite.
3. Ejecutar las celdas en orden.
4. La consulta a Georef requiere conexión a Internet. Si la API no está disponible, el análisis financiero continúa con la base local.
### Fuentes
- Base operativa: archivo Excel provisto por LM Profesionales para esta entrega.
- Georef, Datos Argentina: https://www.argentina.gob.ar/georef
- API Georef: https://apis.datos.gob.ar/georef/api
### Principales resultados de la muestra
- 100 registros, 9 variables, 50 clientes únicos, 7 localidades, 7 servicios y 3 estados.
- Importe registrado: 15.239.270.
- Costo registrado: 4.702.887.
- Ganancia registrada (Importe − Costo): 10.536.383.
- Margen registrado agregado: 69,1%.
- 67% de los registros no figura como finalizado en la extracción.
### Limitaciones de interpretación
- La moneda no está identificada en el archivo; se conservan los importes en su unidad original.
- `Ganancia` representa Importe menos Costo informado; no equivale a utilidad neta contable.
- Los estados no incluyen fechas de inicio, vencimiento ni finalización, por lo que no permiten medir antigüedad o demoras.
- No se informa fecha de cobro; el importe de registros abiertos no debe interpretarse como deuda o facturación impaga.
- 2026 contiene datos solo hasta el 26 de junio; no debe compararse como año completo.
- La hoja de fórmulas menciona métricas GA4, pero esas métricas no están presentes en la base adjunta y no se analizan.
- La muestra actual de 100 registros es apropiada para un EDA inicial, pero no para sostener un modelo predictivo robusto.
### Próxima etapa sugerida
Ampliar la base con fechas de ciclo, horas profesionales, costos indirectos, cobros, canales comerciales, consultas y presupuestos. Con mayor historia y calidad de datos se podrán evaluar modelos de pronóstico de demanda, alertas tempranas de demoras y detección de márgenes atípicos.
