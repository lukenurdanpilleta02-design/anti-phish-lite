# Anti Phish Lite

Analizador de enlaces y entrenamiento contra el phishing. Maqueta educativa de **For Security**, proyecto de colaboración España – Finlandia.

**Demo:** `https://TU-USUARIO.github.io/anti-phish-lite/` *(cámbialo por tu enlace cuando actives GitHub Pages)*

[English below](#english)

## Qué hace

- **Analizar enlace.** Separa la URL en sus partes (protocolo, subdominio, dominio real, ruta) y le aplica 10 reglas: IP en lugar de dominio, dominio que imita a una marca, letras de otros alfabetos (punycode), símbolo @, marca falsa en el subdominio, acortadores, palabras cebo, sin HTTPS, enlaces demasiado largos y extensiones engañosas. Cada regla suma puntos (hasta 100) y el total da un riesgo bajo, medio o alto.
- **Modo entrenamiento.** 10 mensajes de correo, SMS y chat para decidir si son legítimos o phishing, con las pistas de cada uno.
- **Cómo funciona.** Tabla con las reglas, los puntos y los niveles de riesgo.
- En español e inglés.

## Privacidad

Todo el análisis ocurre en el navegador. El enlace nunca se abre ni se envía a ningún servidor.

La página no carga nada de terceros: las fuentes están incluidas en la carpeta `fonts/`, y su política de seguridad (CSP) bloquea cualquier conexión externa. Lo único que guarda es el idioma elegido, en el propio navegador.

## Usarlo en tu ordenador

Abre `index.html` en el navegador. No hace falta instalar nada.

## Publicarlo con GitHub Pages

1. Crea un repositorio **público** en GitHub, por ejemplo `anti-phish-lite`.
2. Sube a la raíz del repositorio todo el contenido de esta carpeta: `index.html`, la carpeta `fonts/`, `README.md` y `LICENSE`.
3. En el repositorio, ve a **Settings → Pages**. En *Source* elige **Deploy from a branch**, rama **main** y carpeta **/ (root)**, y pulsa **Save**.
4. En unos minutos estará en `https://TU-USUARIO.github.io/anti-phish-lite/`.

## Estructura

```
anti-phish-lite/
├── index.html      la aplicación completa (HTML, CSS y JavaScript)
├── fonts/          fuentes y sus licencias
├── README.md
└── LICENSE
```

## Limitaciones

- Es una herramienta de reglas, no una lista de webs maliciosas. No detecta el phishing alojado en webs legítimas hackeadas ni en servicios conocidos (formularios, almacenamiento en la nube), y puede dar alguna falsa alarma. Por eso nunca muestra «100 % seguro».
- Las marcas reales solo aparecen en la lista de dominios oficiales, para reconocer cuándo alguien las imita. El proyecto no tiene relación con ellas y sus nombres pertenecen a sus propietarios.
- Las empresas y personas del modo entrenamiento son ficticias. Los enlaces de ejemplo se muestran como texto y no se pueden abrir.
- La IP de ejemplo (`203.0.113.4`) pertenece a un rango reservado para documentación (RFC 5737).

## Licencia

- Código: [MIT](LICENSE) © 2026 For Security.
- Fuentes: Archivo, Instrument Sans y JetBrains Mono, bajo la SIL Open Font License 1.1 (ver `fonts/`).

---

## English

**Anti Phish Lite** is a link checker and anti-phishing trainer, built as an educational prototype by For Security (a Spain – Finland collaboration project).

- **Check a link:** splits the URL into its parts and applies 10 rules. Each rule adds points (up to 100), giving a low, medium or high risk level.
- **Training mode:** 10 emails, text messages and chats from fictional companies. Decide whether each is legitimate or phishing, then see the clues.
- **How it works:** the rules, their points and the risk levels.

Everything runs in the browser. Links are never opened or sent anywhere, the page loads no third-party resources, and its Content Security Policy blocks all external connections. To use it, open `index.html`. To publish it, follow the GitHub Pages steps above.

Code under the [MIT License](LICENSE). Fonts under the SIL Open Font License 1.1.
