# Scripts del perfil

Todo se ejecuta desde la raíz del repo.

## Banner animado

```bash
pip install -r scripts/banner/requirements.txt
python scripts/banner/generate.py
```

- Edita `YAML_ROWS` y `THEMES` en `scripts/banner/generate.py` para cambiar el texto y los colores.
- **Foto:** si pones una imagen en `assets/source/portrait.png` (de preferencia con fondo transparente), el banner usa tu cara punteada. Si no existe, dibuja un chip como marcador.
- **Logos:** las siluetas PNG/WebP de `scripts/banner/logos/` son las que aparecen en la animación (hoy: espressif, python, react, postgresql). Agrega o quita archivos y vuelve a correr el script. Más logos significan un SVG más pesado, así que conviene mantenerlo en 4 a 6.

## Radares

```bash
python scripts/radar.py --data assets/skills.json  -o assets/radar
python scripts/radar.py --data assets/langmix.json -o assets/radar-langs
# o con datos reales de tus repos públicos:
python scripts/radar.py --github TU_USUARIO -o assets/radar-langs
```

Los valores de los JSON son una autoevaluación de ejemplo: ajústalos a lo que puedas defender en una entrevista.
