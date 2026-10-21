# 📊 Medición y Evaluación de Mejoras

> 🎯 Herramientas para interpretar datos, comparar resultados y determinar si una mejora aporta valor al proceso.

## 🎯 1. Propósito

Establecer criterios y herramientas para analizar los resultados obtenidos durante las pruebas de mejora.

Este documento se centra en **cómo interpretar los datos y determinar qué significan para el proceso**, complementando la metodología general y el registro de experimentos.

## 📏 2. Selección de indicadores

Cada problema requiere indicadores específicos. No es necesario medir todo: se deben seleccionar las variables que permitan evaluar el objetivo de la mejora.

| Indicador | ¿Qué permite analizar? |
|---|---|
| ⏱️ Tiempo de ciclo | Duración de una operación o unidad de trabajo. |
| ⏳ Tiempo de espera | Tiempo durante el cual una actividad queda detenida esperando otra. |
| 📦 Producción | Cantidad de unidades completadas en un período. |
| ✅ Calidad | Errores, defectos y retrabajos detectados. |
| 🔄 Acumulación | Unidades o tareas pendientes entre etapas. |
| 🦺 Condiciones de trabajo | Ergonomía, seguridad, disponibilidad de recursos y dificultades operativas. |

La selección dependerá del problema estudiado y de la información que sea posible obtener.

## 🧮 3. Herramientas de análisis

### ⏱️ Variación del tiempo

Permite calcular cuánto cambió el tiempo de una operación después de una modificación.

\[
\text{Variación} = \text{Tiempo final} - \text{Tiempo inicial}
\]

Un resultado negativo indica una reducción del tiempo; uno positivo, un aumento.

### 📉 Porcentaje de reducción

Cuando el tiempo inicial es mayor que cero, se puede calcular la reducción porcentual:

\[
\text{Reducción (\%)} =
\frac{\text{Tiempo inicial}-\text{Tiempo final}}
{\text{Tiempo inicial}}\times100
\]

**Ejemplo hipotético:** si una operación pasa de 60 segundos a 48 segundos, la reducción es del 20 %.

Este ejemplo es ilustrativo y no representa una medición de los casos del portfolio.

### 📦 Variación de la producción

Permite comparar la cantidad producida durante períodos equivalentes:

\[
\text{Variación de producción} =
\text{Producción final} - \text{Producción inicial}
\]

La comparación solo será útil si se consideran las diferencias relevantes entre los períodos, como la duración de la jornada, el volumen de trabajo y la disponibilidad de materiales.

## 🔍 4. Interpretación de resultados

Los datos deben interpretarse dentro del contexto del proceso.

Una reducción del tiempo puede ser favorable, pero no demuestra por sí sola que el proceso haya mejorado.

También se deberá analizar:

- ✅ Si la calidad se mantiene o mejora.
- 🦺 Si las condiciones de seguridad siguen siendo adecuadas.
- 🔗 Si aparecen demoras o acumulaciones en otras etapas.
- 👥 Si la distribución del trabajo resulta viable.
- 💰 Si los recursos necesarios justifican la mejora.
- 📊 Si los resultados son consistentes o podrían deberse a condiciones particulares.

Cuando existan pocas observaciones o condiciones diferentes entre las pruebas, las conclusiones deberán presentarse con cautela.

## ⚠️ 5. Limitaciones de la medición

Toda evaluación tiene limitaciones que pueden afectar la interpretación de los resultados.

Entre ellas se encuentran:

- Datos incompletos o poco precisos.
- Diferencias entre las condiciones iniciales y finales.
- Cantidad insuficiente de observaciones.
- Cambios simultáneos que dificultan identificar la causa del resultado.
- Indicadores que no reflejan todos los efectos de una modificación.

Estas limitaciones deberán documentarse para evitar conclusiones más firmes de lo que permite la evidencia.

## 🧠 6. De los datos a la decisión

Los resultados de una evaluación pueden dar lugar a distintas conclusiones:

- 🟢 **Resultado favorable:** los datos respaldan la mejora y no se identifican efectos negativos relevantes.
- 🟡 **Resultado parcial:** existe una mejora en algún aspecto, pero quedan cuestiones por resolver.
- 🔵 **Resultado inconcluso:** la información disponible no permite determinar si la propuesta funciona.
- 🔴 **Resultado desfavorable:** la propuesta no alcanza el objetivo o genera consecuencias negativas relevantes.

La decisión final deberá considerar el conjunto del proceso, los criterios definidos antes de la prueba y las limitaciones de los datos.

## 🗂️ 7. Aplicación en los casos de estudio

Estas herramientas podrán utilizarse cuando existan datos suficientes para evaluar las propuestas de los casos documentados.

Por ejemplo, en el caso de preparación y montaje, podrían analizarse las interrupciones, los tiempos de preparación y montaje, las tareas pendientes y los posibles efectos sobre otras etapas.

Si no se dispone de mediciones, el caso podrá mantenerse como análisis cualitativo y propuesta pendiente de validación. No deberán inventarse valores para completar las tablas.

---

**🔑 Principio fundamental:** medir permite conocer qué cambió; analizar permite comprender qué significa ese cambio para el proceso.
