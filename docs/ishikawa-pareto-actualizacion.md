# Actualización de imágenes: Ishikawa y Pareto

La lista maestra de causas (CA1–CA7) es idéntica en `Estructura/capitulo2.tex` y `Estructura/capitulo3.tex`. Usa estos datos para actualizar visualmente `img/diagrama_ishikawa.png`, `img/diagrama_pareto_por_fenomeno.png` e `img/diagrama_problema.png`.

## 1) Diagrama de Ishikawa (`img/diagrama_ishikawa.png`) — ramas 6M con espinas

### Métodos (procesos y procedimientos)
- Espina: Recepción y comunicación por canales informales (WhatsApp/llamadas) sin registro. (CA2)
- Espina: Descoordinación y reubicación de horarios por cruces en visitas in-situ. (CA3)
- Espina: Retraso en el escalamiento e identificación del historial de tickets previos. (CA4)
- Espina: Verificación manual de términos y límites de servicio en contratos (SLA). (CA5)

### Mano de Obra (personal y coordinación)
- Espina: Descoordinación y reubicación de horarios por cruces en visitas in-situ. (CA3)
- Espina: Retraso en el escalamiento e identificación del historial de tickets previos. (CA4)

### Maquinaria/Tecnología (sistemas y herramientas)
- Espina: Búsqueda manual de datos de equipos en archivos Excel desactualizados. (CA1)
- Espina: Recepción y comunicación por canales informales (WhatsApp/llamadas) sin registro. (CA2)
- Espina: Carencia de indicadores de rendimiento (KPIs) para evaluar el tiempo de respuesta. (CA7)

### Materiales/Información (datos y registros)
- Espina: Búsqueda manual de datos de equipos en archivos Excel desactualizados. (CA1)
- Espina: Retraso en el escalamiento e identificación del historial de tickets previos. (CA4)
- Espina: Elaboración manual de reportes e informes de rendimiento de fin de mes. (CA6)

### Medio Ambiente (entorno organizacional y de servicio)
- Espina: Recepción y comunicación por canales informales (WhatsApp/llamadas) sin registro. (CA2)
- Espina: Descoordinación y reubicación de horarios por cruces en visitas in-situ. (CA3)

### Medición (métricas e indicadores)
- Espina: Verificación manual de términos y límites de servicio en contratos (SLA). (CA5)
- Espina: Elaboración manual de reportes e informes de rendimiento de fin de mes. (CA6)
- Espina: Carencia de indicadores de rendimiento (KPIs) para evaluar el tiempo de respuesta. (CA7)

## 2) Valores para `img/diagrama_pareto_por_fenomeno.png` (y `img/diagrama_problema.png`)

Base: tabla `tab:encuesta_causas` (Total General = 244). Orden descendente por puntaje.

| Orden | Código CA | Causa | Frecuencia (puntaje) | % individual | % acumulado |
|---|---|---|---|---|---|
| 1 | CA1 | Búsqueda manual de datos de equipos en archivos Excel desactualizados. | 43 | 17,62 % | 17,62 % |
| 2 | CA2 | Recepción y comunicación por canales informales (WhatsApp/llamadas) sin registro. | 39 | 15,98 % | 33,61 % |
| 3 | CA3 | Descoordinación y reubicación de horarios por cruces en visitas in-situ. | 39 | 15,98 % | 49,59 % |
| 4 | CA4 | Retraso en el escalamiento e identificación del historial de tickets previos. | 37 | 15,16 % | 64,75 % |
| 5 | CA5 | Verificación manual de términos y límites de servicio en contratos (SLA). | 34 | 13,93 % | 78,69 % |
| 6 | CA6 | Elaboración manual de reportes e informes de rendimiento de fin de mes. | 29 | 11,89 % | 90,57 % |
| 7 | CA7 | Carencia de indicadores de rendimiento (KPIs) para evaluar el tiempo de respuesta. | 23 | 9,43 % | 100,00 % |
| — | — | **Total** | **244** | **100,00 %** | — |

## 3) Lista maestra de causas (CA1–CA7) — idéntica en Cap. 2 y Cap. 3

| Código | Enunciado unificado |
|---|---|
| CA1 | Búsqueda manual de datos de equipos en archivos Excel desactualizados. |
| CA2 | Recepción y comunicación por canales informales (WhatsApp/llamadas) sin registro. |
| CA3 | Descoordinación y reubicación de horarios por cruces en visitas in-situ. |
| CA4 | Retraso en el escalamiento e identificación del historial de tickets previos. |
| CA5 | Verificación manual de términos y límites de servicio en contratos (SLA). |
| CA6 | Elaboración manual de reportes e informes de rendimiento de fin de mes. |
| CA7 | Carencia de indicadores de rendimiento (KPIs) para evaluar el tiempo de respuesta. |