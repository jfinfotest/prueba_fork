# Evaluación de Archivos con Gemini

Este proyecto permite empaquetar indicaciones y rutas de archivos a evaluar en un archivo JSON, para ser procesados posteriormente por una aplicación (por ejemplo, usando Gemini).

## Estructura del archivo JSON para evaluación múltiple

El archivo JSON debe contener:
- Una lista de objetos, cada uno con:
  - `pregunta`: la indicación o pregunta para la evaluación.
  - `ruta_archivo`: la ruta relativa del archivo a evaluar.

### Ejemplo de `evaluacion.json`

```json
[
  {
    "pregunta": "Evalúa si el código sigue buenas prácticas de Python.",
    "ruta_archivo": "app1.py"
  },
  {
    "pregunta": "¿El código implementa correctamente la funcionalidad solicitada?",
    "ruta_archivo": "app2.py"
  }
]
```

## Instrucciones

1. Crea un archivo JSON siguiendo la estructura anterior.
2. Cada objeto puede tener una pregunta diferente y referirse a un archivo distinto.
3. Este archivo puede ser leído por una aplicación que recupere los archivos desde un fork de GitHub y realice la evaluación automáticamente.