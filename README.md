# Portafolio de Romina Román

Sitio estático listo para publicar en Cloudflare Pages. No requiere framework, dependencias ni comando de compilación.

## Publicar desde el panel de Cloudflare

1. Sube este proyecto a un repositorio Git (GitHub o GitLab).
2. En Cloudflare: **Workers & Pages → Create application → Pages → Connect to Git**.
3. Selecciona el repositorio.
4. Usa estos valores:

   - **Framework preset:** None
   - **Build command:** dejar vacío
   - **Build output directory:** `.`
   - **Root directory:** `/` (la raíz del repositorio)

5. Guarda y despliega.

## Publicar desde la terminal

Con Wrangler instalado o usando `npx`:

```bash
npx wrangler login
npx wrangler pages project create romina-portafolio
npx wrangler pages deploy . --project-name romina-portafolio
```

El primer comando abre el inicio de sesión de Cloudflare. Si el proyecto de Pages ya existe, omite `pages project create`.

## Dominio personalizado

Después del primer despliegue, entra a **Pages → romina-portafolio → Custom domains** y agrega tu dominio. Si el dominio ya usa Cloudflare DNS, la conexión suele configurarse automáticamente.

## Estructura

- `index.html`: página principal.
- `media/`: videos del portafolio.
- `_headers`: políticas de seguridad y caché para Pages.
- `robots.txt`: permite indexación pública.
- `wrangler.toml`: identifica el proyecto y define la raíz de publicación.
