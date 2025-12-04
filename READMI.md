EVALUACIÓN FINAL MOD 3
1 Fase 1: Exploración y limpueza
 - se cargaronlos archivos:
   - Customer Flight Activity
   - Customer Loyalty History
- Se ha revisado estructura, duplicados y nulos usando: 
 -    info(), describe(), nunique(), isnull().sum()

PRINCIPALES HALLAZGOS
 - Activity: sin nulos, datos completos
 - History:
    - Salary - 25% nulosç
    - Cancellation Year y Cancellation Month -87% nulos
    - resto sin problemas.

DECISONES TOMADAS
 - Union de tablas por Loyalty Number mediante un merge eficiente.
 - Valores imposibles: no se detectaron en activity.
 - Duplicados: no son relevantes; se mantienen como registros temporales legítimos.
 - Nulos tratados:
    -Salary: imputando con la moda.
    - Cancellation Year/Month los nulos significan que no hubo cancelación  por lo que no se imputan
    - se creo una columna boleana llamada cancelado
 Tipos de datos
 - se convirtieron columnas numericas que venian  como str a numerico
 Duplicados
 - se revisaron los duplicados y no había filas problemáticas
 Valores atípicos /imposibles
  - se revisan si habia distancias negativas u valores no validos.
  - no se detectaron valores imposibles dentro de las columnas clave.
VISUALIZACION
        - Vuelos por mes → línea temporal para ver estacionalidad.

        - Distance vs Points Accumulated → scatter para ver relación.

        - Clientes por provincia → barras para comparar volumen.

        - Salario por nivel educativo → boxplot para comparar distribución.

        - Tipos de tarjeta de fidelidad → gráfico de barras con porcentajes.

        - Estado civil vs género → barras agrupadas para comparar proporciones.

        - Cada gráfico incluye una breve interpretación.  

CONCLUSIONES

Los datos de actividad están completos; los de historial requieren tratamiento puntual.

Salary se imputó con moda, lo cual mantiene coherencia y simplicidad.

Las columnas de cancelación no deben imputarse, ya que los nulos tienen significado propio.

Las visualizaciones permiten entender comportamiento de clientes, estacionalidad y distribución demográfica.

