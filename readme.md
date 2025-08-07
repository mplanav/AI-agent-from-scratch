# 🧠 Research Assistant CLI Tool

Este proyecto es un **asistente de investigación por línea de comandos** que utiliza modelos de lenguaje (LLMs) para responder consultas, buscar información en la web y Wikipedia, y guardar resultados en archivos de texto.

---

## 🚀 Características

- Utiliza **LangChain** con modelos de OpenAI.
- Usa herramientas personalizadas para:
  - Buscar en **DuckDuckGo**
  - Consultar **Wikipedia**
  - **Guardar** resultados con marca de tiempo en archivos de texto.
- Devuelve resultados estructurados en formato Pydantic.

---

## 📂 Estructura del proyecto

```
📁 proyecto/
│
├── main.py               # Ejecuta el asistente de investigación
├── tools.py              # Define herramientas personalizadas
├── requirements.txt      # Dependencias del proyecto
└── .env                  # Variables de entorno (no se incluye por seguridad)
```

---

## ⚙️ Requisitos

- Python 3.9+
- Tener una clave API válida para OpenAI o para Anthropic
- Variables de entorno definidas en un archivo `.env`:

```env
OPENAI_API_KEY=tu_clave_openai
ANTHROPIC_API_KEY=tu_clave_anthropic
```

---

## 🧪 Instalación

1. **Clona el repositorio**

```bash
git clone https://github.com/mplanav/AI-agent-from-scratch.git
cd AI-agent-from-scratch
```

2. **Crea y activa un entorno virtual (opcional pero recomendado)**

```bash
python -m venv venv
source venv/bin/activate   # En Linux/macOS
venv\Scripts\activate      # En Windows
```

3. **Instala las dependencias**

```bash
pip install -r requirements.txt
```

4. **Crea un archivo `.env` con tus claves de API**

---

## 🧠 Uso

Ejecuta el script principal:

```bash
python main.py
```

El programa te preguntará:

```
What can I help you to research today?
```

Introduce tu pregunta y el asistente se encargará del resto: buscar, procesar y mostrar resultados, además de guardarlos si es necesario.

---

## 🛠️ Herramientas integradas

| Nombre             | Descripción                                        |
|--------------------|----------------------------------------------------|
| `search`           | Busca información en la web usando DuckDuckGo      |
| `wiki_tool`        | Consulta Wikipedia para obtener contenido relevante |
| `save_text_to_file`| Guarda la salida en un archivo `.txt` con timestamp |

---

## 📤 Ejemplo de salida estructurada

```json
{
  "topic": "Inteligencia Artificial",
  "summary": "La IA es una rama de la informática...",
  "sources": [
    "https://es.wikipedia.org/wiki/Inteligencia_artificial",
    "https://duckduckgo.com/?q=IA"
  ],
  "tools_used": ["search", "wiki_tool"]
}
```

---

## 🧾 Licencia

MIT License. Libre para usar, modificar y distribuir.

---

## 🤝 Agradecimientos

- [LangChain](https://github.com/langchain-ai/langchain)
- [OpenAI](https://openai.com/)
- [Anthropic](https://www.anthropic.com/)
- [DuckDuckGo Search](https://duckduckgo.com/)
- [Wikipedia](https://www.wikipedia.org/)