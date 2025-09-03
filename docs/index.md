# Documentación del Proyecto

Bienvenido a la documentación de *Potential Carnival*.  
Aquí encontrarás guías y referencias para trabajar con el proyecto.

## Índice
- [Instalación](./setup.md)
- [Uso](./usage.md)
- [Solución de problemas](./troubleshooting.md)
- [Preguntas frecuentes](./faq.md)

---

# Pasos ejecutados en la consola de macOS

Estos son los comandos principales que seguí durante los ejercicios para crear y documentar el proyecto.

## 1. Clonar el repositorio desde GitHub
```bash
git clone https://github.com/AngelKst25/potential-carnival.git
cd potential-carnival
## 2. Configurar identidad en Git
## 3. Crear carpeta de documentacion
```bash
mkdir docs
## 4. Convertir PDF a texto y luego a MarkDowm
```bash
mv ~/Downloads/Visual_Board_Comunicacion_Negociacion.pdf ~/potential-carnival/
Extraer el texto del PDF:
```bash
pdftotext -layout Visual_Board_Comunicacion_Negociacion.pdf docs/raw.txt
Convertir a Markdown:
```bash
pandoc -f markdown -t gfm docs/raw.txt -o docs/raw.md
Crear indice de documentación
```bash
nano docs/index.md
Contenido añadido en index.md:
markdown (como la parte de arriba de este doc)
## 6. Subir cambios a GitHub
```bash
git add docs/
git commit -m "docs: agrega documentación en Markdown desde PDF"
git push origin main

