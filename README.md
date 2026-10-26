# secretario-oauth

Puente OAuth estático para el Secretario (asistente personal local).

Slack solo acepta redirects HTTPS, así que `slack.html` recibe `?code=&state=` y los reenvía a la app local en
`http://127.0.0.1:8765/oauth/slack/callback`. No guarda ni envía datos a ningún otro sitio. El `code` no sirve sin el
client secret, que solo está en el llavero del equipo donde corre la app.
