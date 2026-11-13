# PautIA

El procedimiento junto a la camilla: cálculos, mapa y trazabilidad. Aplicación web de un solo fichero.

**Usar la app:** https://fborrasumh.github.io/pautia/

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.24196829.svg)](https://doi.org/10.5281/zenodo.24196829)

**Idiomas:** español (por defecto), inglés, portugués; selector en la barra superior (o `?lang=en` / `?lang=pt` en la URL).

## Qué hace

Cuarta app del [Kit EstéticIA](https://fborrasumh.github.io/kitesteticia/): el registro del procedimiento junto a la camilla.

- **Sesión**: lee la ficha de [AnamnesIA](https://fborrasumh.github.io/anamnesia/) (identificador, peso, técnicas y avisos de «no tratar ahora») o se rellena a mano.
- **Productos y trazabilidad**: nombre, tipo, lote y caducidad de cada producto; viales reconstituidos o jeringas abiertas. Aviso si está caducado, si caduca en 30 días o si falta el lote.
- **Cálculos**: reconstitución de toxina (U/mL, unidades por 0,1 mL y volumen usado), dosis máxima orientativa de anestésico local por peso y fluencia del láser a partir de la energía y el spot.
- **Mapa de puntos**: se toca la cara y el punto se añade con su producto, cantidad, zona y lado; también se puede añadir desde la lista de zonas con el teclado. Plano y técnica por punto. Totales por producto y por zona.
- **Avisos**: relleno en zonas de riesgo vascular alto (glabela, nariz, surco nasogeniano, frente, sien, región infraorbitaria) y puntos que suman más de lo preparado.
- **Hoja de tratamiento** con incidencias inmediatas y observaciones, en Word o impresa, y **sesión JSON** (`kitesteticia-sesion/1`) para SeguimIA.

No usa IA y no hace ninguna llamada de red. Español, inglés y portugués.

## Privacidad

Todo se guarda en el navegador. Nada sale hacia ningún servidor. Se recomienda usar un identificador en lugar del nombre del paciente.

## Límites

Hace la aritmética y el registro; no decide dosis ni técnica. Manda la ficha técnica de cada producto y el criterio clínico. Las dosis de anestésico son orientativas para adultos. Las zonas del mapa son aproximadas y no sustituyen al conocimiento anatómico.

## Pruebas

`node tests/test_nucleo.js` (cálculos, zonas, avisos, hoja y sesión) y `python3 tests/smoke.py` (lee una ficha descargada de AnamnesIA; productos, mapa con clic y con teclado, hoja, sesión JSON, persistencia, tres idiomas, accesibilidad WCAG 2.2 AA, CSP y móvil).

## Autoría

Fernando Borrás Rocher (Universidad Miguel Hernández de Elche) y Elena Caride Miana (Dra. Caride Medicina Estética & Antiaging).

Cuarta app del Kit EstéticIA, diseñado para el alumnado del Máster de Formación Permanente en Medicina Estética Integral y Antienvejecimiento (UMH).

ORCID: Fernando Borrás Rocher [0000-0002-5519-4573](https://orcid.org/0000-0002-5519-4573) · Elena Caride Miana [0000-0002-7620-4857](https://orcid.org/0000-0002-7620-4857)

## Cómo citar

Borrás Rocher, F. y Caride Miana, E. (2026). *PautIA* (v1.0.0) [Software]. DOI: [10.5281/zenodo.24196829](https://doi.org/10.5281/zenodo.24196829)

## Licencia

MIT. Véase [LICENSE](LICENSE).
