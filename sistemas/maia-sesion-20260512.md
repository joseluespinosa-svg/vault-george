# MAIA — Sesión 12 Mayo 2026

## Resumen
Sesión larga de mejoras al sistema OCR de MAIA (maia.pitifred.com).

## Lo hecho

### Login
- Añadido timeout 10s al botón de login (evita botón pillado)
- Fix: isGasHospital ahora detecta tipo=gas (no solo nombre)

### OCR Contadores de Agua
- Gemini API key cargada en servidor (era la causa del fallo)
- Multi-rotación: si OCR devuelve retroceso, prueba 90/180/270°
- Corrección heurística de dígitos por contexto histórico
- Compresión de imágenes en frontend (1600px max, evita error Anthropic)

### OCR Contador Gas (manómetro analógico Rochester)
- Detector geométrico OpenCV implementado: HoughCircles + anillo radial
- Calibración: START=90°, SWEEP=270° CW
- Anti-ambigüedad: descarta contrapeso (opuesto 180°)
- Resultado: ±5% de error en prueba real

### OCR Contador Luz (digital LCD)
- Preprocessador LCD implementado: crop azul HSV + threshold adaptativo
- Tesseract mejorado para 7-segmentos

## Problemas Pendientes
- Anthropic API: sin créditos → recargar en console.anthropic.com
- Gemini: rate limit free tier (se resetea en ~24h)
- Agua Hospital: OCR aún impreciso (foto con Cyble encima muy difícil)
- Gas: calibración aguja necesita afinar con más fotos reales
- Luz: Tesseract LCD necesita más mejoras

## Backup
`/root/backups/maia-backup-20260512-2238/`

## Para mañana
1. Recargar Anthropic credits
2. Mejorar OCR LCD local para Tesseract
3. Calibrar aguja gas con foto frontal limpia
4. Revisar router WiFi (solo funciona con 5G/datos)
