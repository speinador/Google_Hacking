# Ejercicios de Google Hacking - Práctica Guiada

## 🧪 Ejercicio 1: Encontrar paneles de administración

**Objetivo:** Descubrir interfaces de login administrativas.

**Dork:**
```
intitle:"Admin Login"
```

**Instrucciones:**
1. Ingresá el dork en Google.
2. Explorá los resultados.
3. Identificá si hay formularios de acceso visibles.
4. Anotá el dominio y la URL encontrada.

---

## 🧪 Ejercicio 2: Buscar archivos de configuración

**Objetivo:** Detectar archivos `.env` mal protegidos.

**Dork:**
```
filetype:env intext:"DB_HOST"
```

**Pasos:**
1. Pegá el dork en Google.
2. Analizá los resultados para ver si aparecen claves o usuarios.
3. Reflexioná cómo debería estar protegido ese archivo.

---

## 🧪 Ejercicio 3: Rastrear backups expuestos

**Dork:**
```
intitle:"index of" "backup"
```

**Actividad:**
1. Relevá sitios que expongan carpetas con archivos comprimidos.
2. Intentá identificar si contienen bases de datos u otros datos internos.

**¡Importante!** No descargues ningún archivo sin permiso del propietario del sitio.
