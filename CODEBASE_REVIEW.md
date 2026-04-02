# Revisión del código base y tareas propuestas

## Alcance de la revisión
Se revisó el contenido versionado del repositorio y actualmente solo existe `README.md` con un encabezado (`# Music`).

## Problemas encontrados
1. **Falta de contenido funcional**: no hay código fuente, por lo que no es posible validar comportamiento ni detectar errores de ejecución reales.
2. **Documentación mínima**: el `README.md` no describe propósito, instalación, uso ni convenciones del proyecto.
3. **Ausencia de pruebas**: no hay estructura de tests ni criterios de aceptación automáticos.
4. **Ausencia de comentarios técnicos**: al no haber código ni documentación técnica extendida, no se puede verificar consistencia entre implementación y comentarios.

## Tareas propuestas

### 1) Tarea para corregir un error tipográfico
**Título**: Normalizar estilo y ortografía en títulos y textos de documentación inicial.

**Descripción**:
- Crear una sección de “Documentación base” en `README.md`.
- Revisar ortografía, capitalización y consistencia de términos (por ejemplo, nombres de módulos/comandos en formato uniforme).
- Añadir una verificación en CI con un corrector ortográfico para Markdown.

**Criterio de aceptación**:
- `README.md` contiene texto revisado y sin errores ortográficos detectados por la herramienta elegida.

### 2) Tarea para corregir una falla
**Título**: Implementar una funcionalidad mínima ejecutable y manejar errores de entrada.

**Descripción**:
- Crear un módulo inicial (por ejemplo, carga de una lista de canciones desde archivo).
- Definir validaciones de entrada (archivo inexistente, formato inválido, campos faltantes).
- Devolver mensajes de error claros en lugar de fallar abruptamente.

**Criterio de aceptación**:
- La ejecución no termina con error no controlado ante entradas inválidas y reporta errores comprensibles.

### 3) Tarea para corregir discrepancias en comentarios/documentación
**Título**: Alinear documentación con comportamiento real del módulo inicial.

**Descripción**:
- Añadir documentación de API/CLI para la funcionalidad mínima implementada.
- Escribir comentarios breves en funciones clave (qué hacen, entradas, salidas y casos límite).
- Revisar que ejemplos del README coincidan con la salida real del programa.

**Criterio de aceptación**:
- Los ejemplos documentados se ejecutan y su salida coincide con lo descrito.

### 4) Tarea para mejorar una prueba
**Título**: Crear batería de pruebas inicial con casos nominales y de borde.

**Descripción**:
- Añadir pruebas unitarias para flujo exitoso (entrada válida).
- Añadir pruebas para errores esperados (archivo no encontrado, JSON/CSV malformado, datos vacíos).
- Integrar cobertura mínima de pruebas en CI (umbral sugerido inicial: 70%).

**Criterio de aceptación**:
- El comando de test se ejecuta en CI y valida tanto casos válidos como de error.
