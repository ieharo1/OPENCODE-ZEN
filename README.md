# OpenCode Zen - Asistente de Codificación Open-Source

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Version](https://img.shields.io/badge/version-1.0.0-blue.svg)](https://github.com/tuusuario/OpencodeZen/releases)
[![Python](https://img.shields.io/badge/python-3.10+-blue.svg)](https://www.python.org/)
[![Build](https://img.shields.io/github/actions/workflow/status/tuusuario/OpencodeZen/python-app.yml?branch=main)](https://github.com/tuusuario/OpencodeZen/actions)
[![Docker](https://img.shields.io/badge/Docker-ready-blue.svg)](https://www.docker.com/)

OpenCode Zen es un **asistente de codificación gratuito, open-source y multiplataforma** que funciona desde **terminal, scripts Python y flujos de automatización**. Permite **aprender, experimentar y automatizar tareas de programación**, integrando generación de código, explicación de funciones, testing automático y soporte para **modelos gratuitos de IA** y **automatización con n8n**.

---

## 💡 Características Principales

- CLI y Python para máxima flexibilidad
- Compatible con **Windows, Linux y Mac**
- Generación de snippets en múltiples lenguajes: Python, SQL, JavaScript, Bash
- Explicación de código y debugging rápido
- Automatización de tareas repetitivas y pipelines de CI/CD
- Integración con **modelos gratuitos de IA**
- Compatible con **n8n** para automatización de flujos y procesos
- Totalmente open-source, contribuciones bienvenidas

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

### Integración con n8n

Si deseas automatizar flujos con OpenCode Zen en **n8n**, puedes ejecutar scripts Python desde un nodo `Execute Command` o `Execute Python`:

```python
from opencodezen import Zen

zen = Zen(model="free")
snippet = zen.suggest("script que lea un CSV y filtre registros mayores a 18 años")
print(snippet)
```

> Esto permite integrar generación de código y tests automáticos dentro de pipelines sin escribir código manual repetitivo.

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

---

## 🐍 Uso desde Python

```python
from opencodezen import Zen

zen = Zen(model="free")  # Modelos gratuitos de IA

# Generar snippet
snippet = zen.suggest("función que devuelva los 10 primeros registros de un DataFrame")
print(snippet)

# Explicar código
explanation = zen.explain("def suma(a, b): return a + b")
print(explanation)

# Generar tests automáticos
tests = zen.test("def suma(a, b): return a + b")
print(tests)

# Documentar un script completo
doc = zen.doc("mi_script.py")
print(doc)
```

---

## 📚 Ejemplos Avanzados que Aportan a la Comunidad

### 1️⃣ Automatización de CSV y datasets
```bash
opencodezen generate "script para leer un CSV, filtrar registros mayores a 18 años y exportar a nuevo archivo"
```

### 2️⃣ Testing rápido de funciones
```bash
opencodezen test "funcion_calculo.py"
```

### 3️⃣ Explicación de código externo
```bash
opencodezen explain "def merge_sort(arr): ..."
```

### 4️⃣ Documentación automática de repositorios
```bash
opencodezen doc "mi_proyecto/"
```

### 5️⃣ Flujos n8n
- Ejecuta scripts Python de OpenCode Zen desde n8n para:
  - Generar snippets automáticamente al recibir datos
  - Explicar o validar código antes de desplegar
  - Integrar tests automáticos en pipelines

### 6️⃣ Uso con modelos gratuitos de IA
- Aprende, genera y prueba código sin costo
- Compatible con flujos locales y pipelines en Docker

---

## 🔧 Buenas Prácticas y Tips Avanzados

1. **Combina CLI y Python**: CLI para pruebas rápidas, Python para pipelines y scripts más complejos.
2. **Automatización reproducible**: Docker + n8n + tests automáticos para proyectos consistentes.
3. **Aprendizaje activo**: Genera código, explícalo y modifícalo para mejorar patrones de desarrollo.
4. **Integración CI/CD**: Añade `opencodezen test` en pipelines GitHub Actions para validar snippets automáticamente.
5. **Extensión comunitaria**: Crea módulos Python personalizados y comparte con la comunidad.
6. **Productividad máxima**: Flujo recomendado: `generate` → `explain` → `test` → integrar en n8n/Docker.

---

## ❓ FAQ / Troubleshooting

**Q:** Python no reconoce `opencodezen`  
**A:** Activa el entorno virtual y asegúrate de que PATH incluya la carpeta de scripts.

**Q:** Puedo generar código en otros lenguajes?  
**A:** Sí, Python, SQL, JavaScript y Bash están soportados. Pull requests para más lenguajes son bienvenidos.

**Q:** Cómo depuro errores en snippets generados?  
**A:** Usa `opencodezen explain` para entender la lógica y ajusta manualmente.

**Q:** Cómo usar modelos gratuitos de IA?  
**A:** Crea el objeto Zen con `model="free"`. Ideal para aprender y experimentar sin suscripción.

**Q:** Cómo integrar OpenCode Zen con n8n?  
**A:** Usa nodos `Execute Python` o `Execute Command` para ejecutar scripts Zen dentro de flujos. Esto permite automatizar generación de código, tests y documentación.

**Q:** Cómo integrar en pipelines CI/CD?  
**A:** Ejecuta `opencodezen test` o tus scripts Python dentro de contenedores Docker, asegurando reproducibilidad y control de versiones.

---

## 🚀 Contribuciones

Contribuye con:

- Nuevos comandos CLI y módulos Python
- Integración de más lenguajes y modelos gratuitos
- Ejemplos prácticos, pipelines y flujos n8n
- Mejoras en documentación, tests y badges CI/CD

Abre un **issue** o **pull request** y ayuda a la comunidad a crecer.

---

## 🏁 Conclusión

OpenCode Zen combina **potencia, flexibilidad y comunidad**, ideal para:

- Aprender a programar con ejemplos prácticos
- Optimizar y explicar código existente
- Automatizar tareas repetitivas
- Crear snippets, tests y documentación rápida
- Integrar **modelos gratuitos de IA y flujos n8n** para pipelines reales

---

## 👨‍💻 Desarrollado por Isaac Esteban Haro Torres

**Ingeniero en Sistemas · Full Stack · Automatización · Data**

- 📧 Email: zackharo1@gmail.com
- 📱 WhatsApp: 098805517
- 💻 GitHub: https://github.com/ieharo1
- 🌐 Portafolio: https://ieharo1.github.io/portafolio-isaac.haro/

---

## 📄 Licencia

© 2026 Isaac Esteban Haro Torres - Todos los derechos reservados.
