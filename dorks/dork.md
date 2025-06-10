
# Ejemplos de Google Dorks

## Buscar archivos con contraseñas

filetype:env intext:"DB_PASSWORD"
filetype:sql intext:"password"
filetype:log intext:"admin"

## Paneles de login expuestos

intitle:"Admin Login"
inurl:admin intitle:"login"

## Directorios de respaldo y configuración

intitle:"index of /backup"
intitle:"index of /config"
inurl:backup filetype:zip

## Cámaras IP abiertas

inurl:"view/index.shtml"
intitle:"webcamXP 5"

## Archivos sensibles en sitios gubernamentales

site:gov filetype:xls intext:password
