# Template para Charlas de AndesTech

Usa esta carpeta como plantilla para agregar tu charla.

## Pasos:

1. **Copia esta carpeta** con el nombre de tu charla:
   ```bash
   cp -r TEMPLATE "2026-XX-NOMBRE-DE-TU-CHARLA"
   ```

2. **Edita el README.md** con la información de tu charla

3. **Agrega tus archivos:**
   - `slides.pdf` o `slides.pptx` - Tu presentación
   - `codigo/` - Código de ejemplo (si aplica)

4. **Haz un commit y push** a tu fork, luego abre un PR

## Formato de nombre de carpeta

```
AAAA-MM-nombre-corto-charla
```

Ejemplos:
- `2026-04-devcafe-intro-llm`
- `2026-03-birras-kubernetes`
- `2026-05-workshop-typescript`

## Frontmatter para README.md

```yaml
---
titulo: "Tu Charla"
fecha: "2026-04-01"
evento: "devcafe|birras|workshop|blockchain|legal"
speaker: "Tu Nombre"
duracion: "45 min"
tags: ["Tag1", "Tag2"]
---
```
