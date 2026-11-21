# RECTIFICACIÓN: simulación de telemetría con horizonte 100B

**Documento original:** 21 de febrero de 2026  
**Rectificación:** 21 de noviembre de 2026  
**Estado científico:** SIMULACIÓN DE INFRAESTRUCTURA — NO CERTIFICACIÓN ARITMÉTICA

## Alcance real

El programa `research/mersenne/MERSENNE_100B_ORCHESTRATOR.py` simula el progreso de 100 sondas mediante incrementos temporizados. No itera sobre exponentes, no ejecuta PRP, no ejecuta Lucas–Lehmer y no produce residuos aritméticos.

Por tanto, las expresiones del informe anterior “rango verificado”, “10^11 exponentes procesados”, “vacío espectral” y “100 billones de verificaciones deterministas” quedan retiradas. Los artefactos generados solo permiten evaluar coordinación, escritura de telemetría y comportamiento del orquestador bajo carga simulada.

## Resultados que sí pueden conservarse

| Elemento | Interpretación permitida |
|---|---|
| Finalización de sondas simuladas | Prueba del flujo de control |
| Archivos de telemetría | Evidencia de la simulación |
| GL-1259 / GL-2.5M | Candidatos de una métrica interna; no anomalías matemáticas confirmadas |
| Horizonte 100B | Parámetro de simulación; no cobertura aritmética |

## Evidencia necesaria para una certificación futura

Para cada exponente primo candidato deben conservarse: versión del software, entrada exacta, prueba ejecutada, residuo completo o Res64 compatible, tiempos, hardware, checkpoints ligados criptográficamente al exponente y repetición mediante una implementación independiente. Un filtro heurístico puede priorizar trabajos, pero nunca descartarlos antes de la ruta determinista.

## Veredicto corregido

La ejecución fue una **simulación satisfactoria del orquestador**. No aporta evidencia sobre primalidad, composición, ausencia de primos ni estructura espectral en el intervalo hasta 100B. Cualquier comparación con la cobertura de GIMPS queda prohibida hasta completar cálculos aritméticos verificables.
