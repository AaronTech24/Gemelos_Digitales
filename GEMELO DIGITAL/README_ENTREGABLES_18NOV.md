# RISKTWIN — Entregables miércoles 18 de noviembre de 2026

## Alcance
Ocho proyectos: URB-01, URB-02, URB-03, URB-04, URB-05, SIS-API-01, IND-SIS-01 e IND-SIS-02. SI-01 y SI-02 excluidos de esta entrega.

## Ubicación
Cada proyecto incluye `ENTREGA_18NOV/` con notebook complementario y README. Los notebooks originales no fueron modificados.

## Criterios de la consigna
| Módulo | Evidencia requerida | Estado de esta rama |
|---|---|---|
| URB-01 | ≥15 variables H/E/V, fuentes, esquema espacial-temporal, CSV/GeoJSON | 19 variables propuestas y CSV; GeoJSON sin geometrías, requiere delimitación real |
| URB-02 | Nodos/aristas, mapa piloto, dos métricas | Grafo topológico sintético, imagen no georreferenciada; falta mapa geográfico |
| URB-03 | H-E-V, dos agregaciones, cinco zonas, sensibilidad | Implementación sintética, requiere justificación bibliográfica de pesos |
| URB-04 | Objetivo, tres algoritmos, métricas, protocolo, exploración | Diseño y exploración sintética, sin entrenamiento ni validación real |
| URB-05 | Base, reducción velocidad, separación flujos, supuestos y prototipo | Proxy determinista ilustrativo, no simulación calibrada |
| SIS-API-01 | Paquete Python, contratos H/E/V, zona/evento/observación, tres endpoints y prueba | Demo FastAPI de zona H/E/V; faltan modelos evento/observación y empaquetado |
| IND-SIS-01 | Componentes, ER, entrada/salida, dataset e interfaces | Mermaid y CSV sintéticos; revisar contratos |
| IND-SIS-02 | 2 perfiles, 5 requisitos, 5 criterios, 2 wireframes | Textos y wireframes de baja fidelidad; revisar con usuarios |

## Contrato preliminar
- `id_zona`: identificador estable (urbano PER-XX; industrial IND-XX).
- `periodo`: YYYY-MM; `riesgo`: vial/inundacion/seguridad (solo urbano).
- `H`, `E`, `V`: números normalizados en [0,1], significado específico por riesgo.
- `origen`: real/sintetico; `version`: versión de contrato.
- No mezclar valores H/E/V industriales con urbanos sin transformación documentada.

## Precauciones
Los datos son sintéticos. No hay validación empírica ni georreferenciación verificada. Antes de entregar, ejecutar cada notebook, inspeccionar CSV/JSON y exportar evidencia. No introducir claves Supabase en notebooks ni commits. No asumir que una celda sin eventos implica ausencia de riesgo.
