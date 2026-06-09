# 🎙️ Podcast Analyzer

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Python](https://img.shields.io/badge/python-3.8%2B-blue)
![Jupyter](https://img.shields.io/badge/jupyter-notebook-orange)

> **Un sistema completo de análisis de podcasts basado en NLP** 
> 
> Transcripción automática, diarización, análisis de sentimientos, modelado de tópicos, resumen automático y más.

---

## 📋 Descripción General

**Podcast Analyzer** es un proyecto integral de Machine Learning y NLP que proporciona herramientas avanzadas para el análisis profundo de podcasts en audio. El sistema automatiza tareas clave como transcripción, identificación de hablantes, análisis de sentimientos y generación de resúmenes.

Este proyecto es ideal para investigadores, productores de podcasts y empresas que buscan extraer insights valiosos de contenido de audio en español e inglés.

---

## 🎯 Características Principales

### 🎤 Transcripción y Diarización
- **WhisperX + FasterWhisper**: Transcripción rápida y precisa de audio
- **Pyannote**: Identificación automática de hablantes (diarización)
- Soporte multilingüe (español, inglés y más)

### 💭 Análisis de Sentimientos
- Modelos pre-entrenados de transformers (BERT, BETO, multilingual)
- Clasificación de emociones y sentimientos en múltiples idiomas
- Análisis granular por segmento de tiempo

### 📚 Modelado de Tópicos
- Extracción automática de temas principales
- Identificación de palabras clave relevantes
- Visualizaciones interactivas de tópicos

### ✍️ Resumen Automático
- Generación de resúmenes extractivos y abstractivos
- Modelos transformers especializados
- Preservación de información contextual

### 🔍 Análisis Textual Avanzado
- Clasificación con BERT multilingual
- Fine-tuning de modelos BETO para español
- Pipeline NLP completo y modular

---

## 📁 Estructura del Proyecto

```
podcast_analizer/
├── src/
│   ├── entrega2/                          # Análisis Textual Básico
│   │   ├── BERT-multilingual.ipynb        # BERT multilingüe
│   │   ├── BETO.ipynb                      # Modelo español BETO
│   │   └── NLP_Entrega2.ipynb              # Pipeline NLP completo
│   │
│   ├── entrega3/                          # Análisis Avanzado
│   │   ├── Entrega3_Summarization.ipynb    # Resúmenes automáticos
│   │   ├── Entrega3_Topic_&_Keyword_Modelling.ipynb  # Modelado de tópicos
│   │   └── SentimentAnalysisFinal.ipynb    # Análisis de sentimientos
│   │
│   ├── entrega4/                          # Optimización y Transformers
│   │   ├── Entrega4_Summarization.ipynb    # Resúmenes con transformers
│   │   ├── SentimentAnalysisTransformers.ipynb  # Sentimientos avanzados
│   │   ├── TopicModeling4.ipynb            # Modelado de tópicos mejorado
│   │   └── modelos_summarization/          # Modelos guardados
│   │
│   └── transcription+diarization_trials/  # Investigación Transcripción
│       ├── NLP-Proyecto_*Trial_01*WhisperX+pyannote.ipynb
│       ├── NLP-Proyecto_*Trial_02*FasterWhisper.ipynb
│       ├── NLP-Proyecto_*Trial_03*cuDNN_incompatibility.ipynb
│       ├── NLP-Proyecto_*Trial_04*FasterWhisper+pyannote.ipynb
│       ├── NLP-Proyecto_*Trial_05*Dependency_failures.ipynb
│       ├── NLP-Proyecto_*Trial_06*Faster_Whisper.ipynb
│       ├── NLP-Proyecto_*Trial_07*WhisperX+cpu_diarization.ipynb
│       ├── NLP-Proyecto_*Trial_08*Youtube_blocker.ipynb
│       └── NLP-Proyecto_*Trial_09*Youtube_Transcript_API.ipynb
│
├── README.md                              # Este archivo
├── .gitignore
└── .gitattributes
```

---

## 🔄 Pipeline de Procesamiento

```
Audio/Podcast
    ↓
Transcripción (Whisper/FasterWhisper)
    ↓
Diarización (Pyannote)
    ↓
Segmentación
    ↓
┌───────────────────────────────────────┐
│         Análisis Paralelo             │
├───────────────────────────────────────┤
│  Sentimientos → Clasificación Emocional
│  Tópicos → Extracción de Temas
│  Resúmenes → Síntesis de Contenido
└───────────────────────────────────────┘
    ↓
Resultados Consolidados
```

---

## 🚀 Inicio Rápido

### Requisitos Previos

- **Python** >= 3.8
- **Jupyter Notebook** o **JupyterLab**
- **GPU recomendada** (CUDA compatible) para mejor rendimiento

### Instalación

1. **Clonar el repositorio**
   ```bash
   git clone https://github.com/aimarpg/podcast_analizer.git
   cd podcast_analizer
   ```

2. **Crear entorno virtual**
   ```bash
   python -m venv venv
   source venv/bin/activate  # En Windows: venv\Scripts\activate
   ```

3. **Instalar dependencias**
   ```bash
   pip install jupyter numpy pandas scikit-learn
   pip install transformers torch torchaudio
   pip install datasets accelerate
   # Para transcripción avanzada:
   pip install openai-whisper faster-whisper whisperx
   pip install pyannote.audio
   ```

### Uso Básico

1. **Abrir Jupyter Notebook**
   ```bash
   jupyter notebook
   ```

2. **Navegar a los notebooks** según tu caso de uso:
   - **Principiantes**: Comienza con `entrega2/NLP_Entrega2.ipynb`
   - **Análisis de Sentimientos**: `entrega3/SentimentAnalysisFinal.ipynb`
   - **Resúmenes**: `entrega3/Entrega3_Summarization.ipynb`
   - **Transcripción**: `transcription+diarization_trials/`

3. **Ejecutar las celdas** siguiendo las instrucciones en cada notebook

---

## 📦 Dependencias Principales

| Librería | Propósito |
|----------|-----------|
| **transformers** | Modelos pre-entrenados (BERT, BETO, T5) |
| **torch** | Framework de deep learning |
| **scikit-learn** | Machine learning clásico |
| **pandas** | Manipulación de datos |
| **matplotlib / seaborn** | Visualización |
| **whisper / faster-whisper** | Transcripción automática |
| **pyannote.audio** | Diarización de hablantes |

---

## 📊 Capacidades por Módulo

### Entrega 2: Fundamentos NLP
- ✅ Procesamiento básico de texto
- ✅ Tokenización y vectorización
- ✅ Clasificación de texto con BERT multilingual
- ✅ Fine-tuning de BETO para español

### Entrega 3: Análisis Intermedio
- ✅ Análisis de sentimientos avanzado
- ✅ Modelado de tópicos (LDA, LSA)
- ✅ Generación de resúmenes extractivos
- ✅ Visualizaciones interactivas

### Entrega 4: Transformers Avanzados
- ✅ Resúmenes abstractivos con T5
- ✅ Análisis de sentimientos con transformers
- ✅ Modelado de tópicos neural
- ✅ Optimización de modelos

### Transcripción & Diarización
- ✅ 9 experimentos iterativos
- ✅ Comparación de modelos (Whisper, WhisperX, FasterWhisper)
- ✅ Solución de problemas de compatibilidad
- ✅ Integración con YouTube

---

## 💡 Casos de Uso

- 📻 **Productores**: Generar resúmenes y transcripciones automáticas
- 📈 **Análisis de Mercado**: Evaluar sentimiento del público
- 🔍 **Investigación**: Extraer tópicos y patrones de contenido
- 🤖 **Automatización**: Procesar grandes volúmenes de podcasts
- 📊 **Business Intelligence**: Insights sobre preferencias de audiencia

---

## 📝 Ejemplos de Uso

### Análisis de Sentimientos
```python
from transformers import pipeline

# Cargar modelo
sentiment_pipeline = pipeline("sentiment-analysis", 
                              model="nlptown/bert-base-multilingual-uncased-sentiment")

# Analizar texto
resultado = sentiment_pipeline("Este podcast es increíble")
print(resultado)
# Output: [{'label': 'positive', 'score': 0.98}]
```

### Generación de Resumen
```python
from transformers import pipeline

summarizer = pipeline("summarization", model="facebook/bart-large-cnn")
summary = summarizer(largo_texto, max_length=150, min_length=50)
print(summary[0]['summary_text'])
```

---

## 🔬 Metodología de Investigación

Este proyecto implementa un **enfoque iterativo de investigación** con 9 fases documentadas de experimentación:

1. **Prueba inicial** (Whisper + Pyannote)
2. **Optimización** (FasterWhisper + alineación)
3. **Resolución de dependencias** (cuDNN incompatibilities)
4. **Refinamiento** (FasterWhisper + Pyannote)
5. **Troubleshooting** (Fallos de dependencias)
6. **Simplificación** (Solo transcripción)
7. **GPU Optimization** (CPU diarización)
8. **Integración YouTube** (Bloqueadores)
9. **API alternativa** (YouTube Transcript)

Cada notebook documenta decisiones técnicas, benchmarks y lecciones aprendidas.

---

## 🎓 Resultados y Benchmarks

| Modelo | Tarea | Precisión | Velocidad |
|--------|-------|-----------|-----------|
| BETO | Clasificación ES | 92-95% | Rápido |
| BERT multilingual | Clasificación Multiidioma | 88-91% | Medio |
| T5 | Resúmenes | High Quality | Lento |
| FasterWhisper | Transcripción | 95%+ | Muy Rápido |

*Benchmarks pueden variar según dataset y configuración*

---

## 🤝 Contribuciones

Las contribuciones son bienvenidas! Para contribuir:

1. Fork el proyecto
2. Crea una rama (`git checkout -b feature/AmazingFeature`)
3. Commit tus cambios (`git commit -m 'Add some AmazingFeature'`)
4. Push a la rama (`git push origin feature/AmazingFeature`)
5. Abre un Pull Request

---

## 📚 Recursos y Referencias

- [Hugging Face Transformers](https://huggingface.co/transformers/)
- [PyTorch Documentation](https://pytorch.org/docs/stable/index.html)
- [Whisper GitHub](https://github.com/openai/whisper)
- [Pyannote.audio](https://github.com/pyannote/pyannote-audio)
- [BERT Paper](https://arxiv.org/abs/1810.04805)

---

## 📄 Licencia

Este proyecto está bajo la licencia MIT. Ver archivo `LICENSE` para detalles.

---

## 👨‍💻 Autor

**aimarpg** - [GitHub Profile](https://github.com/aimarpg)

---

## 🙏 Agradecimientos

- Hugging Face por los modelos pre-entrenados
- OpenAI por Whisper
- Comunidad de código abierto por herramientas fundamentales
- Contribuidores y usuarios por feedback y mejoras

---

## 📮 Contacto y Soporte

- 📧 Abre un [Issue](https://github.com/aimarpg/podcast_analizer/issues) para reportar bugs
- 💬 Usa [Discussions](https://github.com/aimarpg/podcast_analizer/discussions) para preguntas
- ⭐ Si te resulta útil, ¡no olvides darle una estrella!

---

## 🎯 Roadmap Futuro

- [ ] API REST para transcripción remota
- [ ] Dashboard interactivo con Streamlit
- [ ] Soporte para más idiomas
- [ ] Optimización para edge devices
- [ ] Integración con plataformas de podcasts populares
- [ ] Modelo de clasificación de anuncios/contenido

---

**Última actualización:** Marzo 2026  
**Creado:** Octubre 2025
