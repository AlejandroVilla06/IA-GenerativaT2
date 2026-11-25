# IA Generativa — Trayecto 2

Entregables del módulo de IA del Trayecto 2 en Riwi (Cohorte C8, Medellín).
Célula Odin, Clan Loki.

El macro reto del módulo es un **asistente de conocimiento** para los coders de Riwi. Cada semana suma una pieza.

| Semana | Tema | Carpeta |
|--------|------|---------|
| 1 | Taller de experiencia de usuario para una aplicación con IA | [`S2-ia-responsable/`](S2-ia-responsable/) (maqueta del asistente) |
| 2 | IA responsable desde el inicio | [`S2-ia-responsable/`](S2-ia-responsable/) |

## Qué hay y dónde

| Pieza | Qué es | Dónde |
|-------|--------|-------|
| Diseño y reglas | Maqueta del asistente, lista de decisiones de uso responsable, funciones y pruebas | Este repo, carpeta [`S2-ia-responsable/`](S2-ia-responsable/) |
| Asistente con IA real | El mismo asistente conectado a un modelo, construido en Lovable | [asistente-riwi-ia-responsable.lovable.app](https://asistente-riwi-ia-responsable.lovable.app) |

La maqueta de este repo usa respuestas preparadas para mostrar el flujo y las reglas. La app de Lovable aplica las mismas reglas con un modelo real:

1. **Antes del modelo:** `protegerDatos()` oculta correos, celulares y documentos.
2. **Alto impacto:** si `requiereHumano()` detecta salud, notas, permanencia o dinero, no se llama al modelo y se deriva a una persona.
3. **Después del modelo:** `aviso()` indica que la respuesta la generó una IA.

La conversación no se guarda: desaparece al recargar. El código de la app de Lovable no está en este repo.

## Cómo ejecutar

```bash
cd S2-ia-responsable
node pruebas.js        # 12 pruebas: 7 checks del laboratorio de Moodle + 5 propios
xdg-open index.html    # maqueta del asistente y evidencia en el navegador
```

Requiere Node.js. No usa dependencias externas.

Los entregables del Trayecto 1 están en el repo [IA-Generativa](https://github.com/AlejandroVilla06/IA-Generativa).
