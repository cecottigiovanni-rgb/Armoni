# Auralis Academia de Música

Landing page creada con HTML y Tailwind CSS para presentar una academia de música con clases personalizadas de guitarra, violín, oboe, piano, audioperceptiva y armonía.

## Cómo abrir la página

Puedes abrir directamente `index.html` en el navegador o servirla localmente con Python:

```bash
cd C:/Users/Equipo/academia-musica
python -m http.server 8000
```

Luego entra a:

```text
http://localhost:8000
```

## Personalización

Puedes cambiar nombre, ubicación, WhatsApp, redes sociales y texto en `index.html`.

## Deploy en Netlify (recomendado)

1) En Netlify, clic en **Add new site → Import from Git** y conecta tu cuenta de GitHub.
2) Selecciona el repositorio `cecottigiovanni-rgb/Armoni`.
3) En la configuración del deploy deja:
	- Build command: (vacío)
	- Publish directory: `.`
4) Haz click en **Deploy site**.

Alternativa con Netlify CLI (si preferís ejecutar en tu cuenta):

```bash
# instalar netlify cli si no lo tenés
npm install -g netlify-cli

# autenticar (abrirá un navegador para loguearte)
netlify login

# desde la carpeta del proyecto
netlify deploy --dir=. --prod
```

Nota: ya incluí `netlify.toml` en el repo para que Netlify publique la raíz del proyecto.

## Integración con Formspree (formularios)

1) Creá una cuenta en https://formspree.io y crea un nuevo formulario.
2) Formspree te mostrará un identificador para el formulario — por ejemplo: `/f/mnqlpraj` o un ID corto `mnqlpraj`.
3) Abre `index.html` y en la cabecera reemplaza la meta `formspree-id` con tu ID (puede ser la forma `/f/XXX` o solo `XXX`).

Ejemplo (en `index.html`):
```html
<meta name="formspree-id" content="/f/tu_form_id" />
```

4) Guardá, commiteá y pusheá los cambios. El formulario enviará directamente a Formspree y mostrará un mensaje de confirmación en la página.

Si querés te lo configuro yo: pegá aquí el `formspree-id` que te muestra la plataforma y lo incorporo al repo, o seguí los pasos y te guío en directo.
