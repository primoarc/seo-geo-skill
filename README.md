# seo-geo-skill

Skill para agentes de código (Claude Code, Cursor y otros compatibles con [skills](https://github.com/vercel-labs/skills)) que aplica un método completo de **SEO + GEO**: posicionar un sitio en los primeros lugares orgánicos de Google y lograr que lo citen ChatGPT, Perplexity, Gemini y Google AI Overviews.

Funciona para cualquier proyecto web: negocios locales, servicios a domicilio, fintech y financiamiento, marketplaces, e-commerce, SaaS.

Está construida a partir de lo que funcionó (y lo que salió mal) lanzando sitios reales en Guatemala, como [llavesenguate.com](https://llavesenguate.com) y [polarizadoguatemala.com](https://polarizadoguatemala.com).

## Instalación

```bash
npx skills add primoarc/seo-geo-skill
```

Para instalarla en todos tus proyectos (global):

```bash
npx skills add primoarc/seo-geo-skill -g
```

## Cómo se usa

Pídele a tu agente cosas como:

- "Audita el SEO de mi sitio https://misitio.com"
- "Quiero salir primero en Google para meseros a domicilio en Guatemala, ¿qué páginas debería crear?"
- "Haz que mi sitio de financiamiento de celulares aparezca en ChatGPT"
- "Revisa Search Console y dime qué títulos cambiar"
- "Prepárame los textos para mi ficha de Google Business Profile"

La skill se activa sola cuando hablas de SEO, posicionamiento, Google, Search Console, ficha de Google o visibilidad en IA.

## Qué incluye

| Archivo | Contenido |
|---|---|
| `SKILL.md` | El método en 7 fases: diagnóstico, mapa de páginas, técnico, contenido, GEO, presencia local, medir e iterar |
| `references/estrategia.md` | Encontrar el hueco del nicho, mapa de intenciones, páginas programáticas, hubs, enlazado interno |
| `references/tecnico.md` | Checklist técnico, schema JSON-LD, rendimiento, trampas de Next.js/Vercel/WordPress |
| `references/contenido.md` | Contenido único sin inventar datos, FAQ, títulos que consiguen clics, YMYL |
| `references/geo.md` | Rastreadores de IA, `llms.txt`, pasajes citables, entidad consistente |
| `references/local-gbp.md` | Kit para Google Business Profile y cómo enlazarla al sitio |
| `references/search-console.md` | Verificación, sitemap, API con cuenta de servicio, ciclo de mejora |
| `references/verticales.md` | Cómo adaptar el método por tipo de proyecto |
| `references/casos.md` | Casos reales con lecciones concretas |
| `scripts/audit_pages.py` | Auditoría on-page de un sitio en vivo (solo librería estándar de Python) |
| `scripts/gsc.py` | Reportes de Search Console por API: rendimiento, consultas, oportunidades, indexación, sitemaps |

## Search Console por API (opcional)

1. Crea una cuenta de servicio en Google Cloud con la Search Console API habilitada y descarga su llave JSON.
2. Agrega el correo de la cuenta de servicio como usuario en tu propiedad de Search Console.
3. Guarda la llave en `.secrets/gsc-service-account.json` de tu proyecto y agrega `.secrets/` a `.gitignore`.
4. `pip install google-api-python-client google-auth`

Detalles en `references/search-console.md`.

## Principios

- Publica lo que nadie publica (precios, plazos, requisitos, garantías).
- Una página por intención de búsqueda, con datos concretos.
- Técnico impecable desde el día uno.
- Nunca inventar datos ni prometer lo que el negocio no confirmó.
- Medir con Search Console y ajustar al lenguaje real de la gente.

## Licencia

MIT
