
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

Google Hacking (o Google Dorking) consiste en utilizar operadores avanzados del buscador de Google para encontrar archivos, configuraciones, cámaras IP, bases de datos y otros recursos expuestos accidentalmente.

Se considera una técnica de **reconocimiento pasivo** y es clave en auditorías de seguridad o investigaciones OSINT.

---

## 🔍 Ejemplos de Dorks

```bash
inurl:admin intitle:"login"
filetype:env intext:"DB_PASSWORD"
intitle:"index of" "backup"
filetype:sql "insert into"
site:gov filetype:xls intext:password
```

Cada uno permite descubrir configuraciones, contraseñas, directorios públicos, paneles de administración o documentos sensibles.

---

## 📂 Directorios y Archivos Comunes

- `index of /backup`
- `index of /admin`
- `*.bak`, `*.sql`, `*.zip`, `*.env`, `*.ini`
- PDF internos, planillas, manuales y más

---

## 🛠 Herramientas Sugeridas

- [Google Hacking Database (GHDB)](https://www.exploit-db.com/google-hacking-database)
- [Shodan.io](https://www.shodan.io)
- FOCA (Fingerprinting Organizations with Collected Archives)
- Spiderfoot, Maltego, Recon-ng

---

## 🧪 Casos Prácticos Incluidos

- 📌 Encontrar paneles de login expuestos
- 📌 Descubrir backups sin protección
- 📌 Detectar cámaras IP abiertas
- 📌 Encontrar archivos `.env` con contraseñas
- 📌 Extraer documentos internos en PDF

Cada ejemplo está explicado paso a paso con su dork correspondiente, interpretación y recomendaciones de mitigación.

---

## ⚖️ Ética y Buenas Prácticas

- ✅ Usar solo en laboratorios, entornos de prueba o con permiso del propietario.
- ✅ Documentar hallazgos para informes de seguridad.
- ❌ Prohibido acceder, explotar o distribuir información sensible sin consentimiento.

---

## 🧑‍🏫 Autor

**Sebastián Peinador**  
👨‍💼 Jefe de Soporte y Sistemas - Hospital José M. Penna (CABA)  
👨‍🏫 Docente - CFP36, Ministerio de Educación (CABA)  
💻 Especialista en Tecnología, Educación y Ciberseguridad

---

## 📄 Licencia

Este proyecto está licenciado bajo la [MIT License](LICENSE).

---

## 🤝 Contribuciones

¡Sos bienvenido/a a colaborar! Podés:

- Sugerir nuevos dorks
- Agregar ejemplos con capturas
- Crear ejercicios prácticos
- Reportar errores en los comandos

---

## ⭐ ¡Apoyá el proyecto!

Si este repositorio te resulta útil, dejá una estrella ⭐ y compartilo con colegas o estudiantes.
