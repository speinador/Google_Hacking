
# 🕵️ Google Hacking - Manual de Pentesting Ético con Google

Este repositorio contiene un **manual práctico y educativo sobre Google Hacking (Google Dorking)**, una técnica utilizada en auditorías de seguridad para descubrir información sensible publicada accidentalmente en Internet. Está orientado a estudiantes, docentes y profesionales de ciberseguridad interesados en el uso ético de estas herramientas.

> ⚠️ **Advertencia Legal:** Este material es para fines exclusivamente educativos. No debe ser utilizado para acceder a sistemas sin autorización. Toda actividad debe realizarse en entornos controlados o con permiso explícito.

---

## 📚 Contenido del Repositorio

- ✅ ¿Qué es Google Hacking?
- 🧠 Conceptos clave y terminología
- 🔎 Operadores de búsqueda avanzados
- 💡 Dorks útiles con ejemplos reales
- 🧪 Casos prácticos paso a paso
- 🗂 Archivos y directorios vulnerables comunes
- 🛠 Herramientas complementarias
- 🔐 Riesgos y tipos de ataques
- 🛡 Ética del hacking y recomendaciones legales

---

## 🧠 ¿Qué es Google Hacking?

Google Hacking, también conocido como Google Dorking, es el uso avanzado de operadores de búsqueda en Google para encontrar información que, aunque no esté protegida o cifrada, no debería ser accesible públicamente. Estas búsquedas pueden revelar vulnerabilidades, configuraciones mal implementadas, cámaras web, archivos de contraseñas, bases de datos, documentos internos, etc.

---

## 🧾 Términos clave

- **Google Dork**: Consulta avanzada con operadores que busca información específica.
- **Operadores booleanos**: Combinan o excluyen palabras clave (AND, OR, -).
- **Reconocimiento pasivo**: Recolectar información sin interactuar directamente con el objetivo.
- **Footprinting**: Fase de recopilación de datos en pruebas de penetración.
- **OSINT**: Inteligencia de fuentes abiertas.

---

## 🔎 Operadores de búsqueda avanzados

| Operador       | Descripción                                          | Ejemplo                                        |
|----------------|------------------------------------------------------|------------------------------------------------|
| `site:`        | Restringe la búsqueda a un dominio específico        | `site:gov.ar filetype:xls`                     |
| `filetype:`    | Busca un tipo de archivo específico                  | `filetype:pdf presupuesto salud`               |
| `intitle:`     | Término en el título de la página                    | `intitle:"login page"`                         |
| `inurl:`       | Término en la URL                                    | `inurl:admin`                                  |
| `intext:`      | Término dentro del contenido de la página            | `intext:"DB_PASSWORD"`                         |
| `allinurl:`    | Todos los términos deben estar en la URL             | `allinurl:admin login`                         |
| `allintitle:`  | Todos los términos deben estar en el título          | `allintitle:index of`                          |
| `cache:`       | Muestra la versión en caché de una página            | `cache:ejemplo.com`                            |
| `link:`        | Páginas que enlazan a una URL                        | `link:facebook.com`                            |
| `related:`     | Páginas similares a una URL                          | `related:nytimes.com`                          |
| `*`            | Comodín                                               | `"base de datos * acceso"`                     |

---

## 💡 Dorks útiles con ejemplos

```bash
intitle:"index of" inurl:admin
filetype:sql intext:"password"
inurl:wp-content/uploads filetype:pdf
intext:"Index of /" "backup"
filetype:env "DB_PASSWORD"
```

---

## 🧪 Casos prácticos

1. **Buscar bases de datos SQL expuestas**
   ```
   filetype:sql intext:"password"
   ```

2. **Buscar archivos de entorno**
   ```
   filetype:env intext:"DB_HOST"
   ```

3. **Buscar cámaras IP abiertas**
   ```
   inurl:view/index.shtml
   intitle:"webcamXP 5"
   ```

4. **Buscar paneles de login**
   ```
   inurl:admin intitle:"login"
   ```

---

## 🗂 Directorios y Archivos comunes

- `index of /admin`
- `index of /backup`
- `.sql`, `.env`, `.log`, `.conf`, `.ini`, `.bak`, `.zip`
- Archivos PDF, Excel o Word con datos internos

---

## 🛠 Herramientas útiles para complementar

- **Google Hacking Database (GHDB)**: https://www.exploit-db.com/google-hacking-database
- **Shodan.io**: Buscador de dispositivos conectados a Internet
- **FOCA**: Extrae metadatos de documentos
- **Recon-ng**, **SpiderFoot**, **Maltego**

---

## 🔐 Tipos de ataques facilitados por Google Hacking

| Tipo de Ataque        | Descripción                                                  |
|-----------------------|--------------------------------------------------------------|
| Exposición de datos   | Archivos con contraseñas, emails o configuraciones sensibles |
| Acceso a paneles      | Portales internos o de administración                        |
| Directory Traversal   | Navegación por carpetas no protegidas                        |
| Phishing o suplantación | Descubrimiento de recursos falsificados                     |
| Ingeniería social     | Recopilación de datos para ataques dirigidos                 |

---

## ⚖️ Ética del Hacking

- Solo usar dorks en laboratorios o entornos donde tengas autorización.
- Documentar hallazgos si estás haciendo una auditoría autorizada.
- No explotar información encontrada ilegalmente.
- Siempre seguir las normas de hacking ético y legal.

---

## 🧑‍🏫 Autor

Explicación elaborada por [Sebastian Peinador](https://www.linkedin.com/in/sebastian-j-peinador/) para propósitos didácticos y de investigación en ciberseguridad ofensiva.

---

## 📄 Licencia

Este proyecto está licenciado bajo la [MIT License](LICENSE).
