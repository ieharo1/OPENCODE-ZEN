# OpenCode Zen - Asistente de Codificación Open-Source

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Version](https://img.shields.io/badge/version-1.0.0-blue.svg)](https://github.com/tuusuario/OpencodeZen/releases)
[![Python](https://img.shields.io/badge/python-3.10+-blue.svg)](https://www.python.org/)
[![Build](https://img.shields.io/github/actions/workflow/status/tuusuario/OpencodeZen/python-app.yml?branch=main)](https://github.com/tuusuario/OpencodeZen/actions)
[![Docker](https://img.shields.io/badge/Docker-ready-blue.svg)](https://www.docker.com/)

OpenCode Zen es un **asistente de codificación gratuito, open-source y multiplataforma**, diseñado para **aprender, experimentar y automatizar tareas de programación**. Funciona directamente desde tu terminal o scripts Python, integrando generación de snippets, optimización de código, explicación de funciones y testing automático.  

---

## 🧑‍💻 Autor

**Isaac Haro**  
Ingeniero en Sistemas · Full Stack · Automatización · Data  

---

## 💡 Características Principales

- **CLI y Python**: Usa la terminal para tareas rápidas o integra en scripts y pipelines.  
- **Multilenguaje**: Python, SQL, JavaScript, Bash. Fácil de extender.  
- **Automatización**: Genera snippets, tests y documentación automáticamente.  
- **Debugging rápido**: Explica funciones complejas o código de terceros.  
- **CI/CD Ready**: Compatible con pipelines y Docker para entornos reproducibles.  
- **Comunidad Open-Source**: Totalmente gratuito, contribuciones bienvenidas.  

---

## ⚡ Instalación

### Windows

```powershell
git clone https://github.com/tuusuario/OpencodeZen.git
cd OpencodeZen

python -m venv venv
venv\Scripts\activate

pip install -r requirements.txt
python main.py
```

### Linux / Mac

```bash
git clone https://github.com/tuusuario/OpencodeZen.git
cd OpencodeZen

python3 -m venv venv
source venv/bin/activate

pip install -r requirements.txt
python3 main.py
```

### Docker (Opcional)

```bash
# Construir imagen
docker build -t opencodezen .

# Ejecutar contenedor interactivo
docker run -it --rm opencodezen
```

---

## 🖥️ Comandos CLI Esenciales

```bash
# Generar snippet de código
opencodezen generate "función que lea un CSV y filtre datos por columna"

# Optimizar código
opencodezen suggest "optimizar búsqueda en lista grande"

# Explicar código
opencodezen explain "def quicksort(arr): ..."

# Generar documentación automáticamente
opencodezen doc "script.py"

# Generar tests unitarios
opencodezen test "mi_funcion.py"

# Listar comandos disponibles
opencodezen help
```

> Tip: Combina `generate` y `explain` para aprender creando código y entendiendo su funcionamiento al mismo tiempo.  

---

## 🐍 Uso desde Python

```python
from opencodezen import Zen

zen = Zen()

# Generar snippet
snippet = zen.suggest("función que devuelva los 10 primeros registros de un DataFrame")
print("Snippet generado:\n", snippet)

# Explicar código
explanation = zen.explain("def suma(a, b): return a + b")
print("Explicación:\n", explanation)

# Generar tests automáticos
tests = zen.test("def suma(a, b): return a + b")
print("Tests generados:\n", tests)

# Documentar un script completo
doc = zen.doc("mi_script.py")
print("Documentación generada:\n", doc)
```

---

## 📚 Ejemplos prácticos que aportan a la comunidad

### 1️⃣ Automatización de CSV
```bash
opencodezen generate "script para leer un CSV, filtrar por 'edad > 18' y exportar a nuevo archivo"
```
- Útil para análisis rápido de datasets compartidos en la comunidad.

### 2️⃣ Testing rápido de funciones
```bash
opencodezen test "funcion_calculo.py"
```
- Genera tests unitarios básicos para funciones comunes antes de integrarlas en proyectos open-source.

### 3️⃣ Explicación de código externo
```bash
opencodezen explain "def merge_sort(arr): ..."
```
- Perfecto para comprender snippets de repositorios de terceros antes de usarlos.

### 4️⃣ Generación de documentación
```bash
opencodezen doc "mi_proyecto/"
```
- Ayuda a mantener repositorios bien documentados para otros colaboradores.

---

## 🔧 Buenas Prácticas

1. **Combinar CLI y Python**: CLI para pruebas rápidas; Python para pipelines, scripts y proyectos grandes.  
2. **Automatización reproducible**: Usa Docker y tests automáticos para proyectos compartidos.  
3. **Aprendizaje activo**: Genera código, entiende su lógica y modifica para mejorar patrones.  
4. **Integración en pipelines**: Añade `opencodezen test` en GitHub Actions para validar snippets automáticamente.  
5. **Contribuir al open-source**: Comparte tus snippets, tests y mejoras de documentación con la comunidad.  

---

## ❓ FAQ / Troubleshooting

**Q:** Python no reconoce `opencodezen`  
**A:** Activa tu entorno virtual y asegúrate de tener PATH configurado correctamente.

**Q:** Puedo generar código en otros lenguajes?  
**A:** Sí, soportamos Python, SQL, JavaScript y Bash. Pull requests son bienvenidos para nuevos lenguajes.

**Q:** Cómo extender el asistente para mi propio workflow?  
**A:** Puedes crear nuevos módulos Python y registrar comandos CLI personalizados siguiendo la estructura del proyecto.

**Q:** Cómo depuro errores en snippets generados?  
**A:** Usa `opencodezen explain` para entender la lógica del snippet y luego ajusta manualmente.

---

## 🚀 Contribuciones

Contribuye con:

- Nuevos comandos CLI  
- Integración de más lenguajes  
- Ejemplos prácticos y pipelines  
- Mejoras en documentación y tests  

Abre un **issue** o **pull request**, sigue las buenas prácticas y agrega tests si es posible.

---

## 🏁 Conclusión

OpenCode Zen combina **potencia, flexibilidad y comunidad**. Perfecto para:

- Aprender y enseñar a programar  
- Optimizar código existente  
- Automatizar tareas repetitivas y análisis de datos  
- Crear snippets, tests y documentación rápidamente  

---

## 📝 Licencia

MIT — contribuciones bienvenidas 🚀
