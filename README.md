# Generador de Clases de Alemán con IA

## Flujo de Datos
```mermaid
graph TD
    A["Usuario accede al Space<br/>Hugging Face"] --> B["Interfaz Gradio<br/>Formulario"]
    ... (todo el código del diagrama)
```
```

## 2. **En Notion**
- Abre una página en Notion
- Escribe `/diagrama` o `/mermaid`
- Pega el código

## 3. **En Obsidian o Markdown Editor**
- Rodea el código con:
```
\`\`\`mermaid
graph TD
    A["Usuario accede al Space<br/>Hugging Face"] --> B["Interfaz Gradio<br/>Formulario"]
    
    B --> C["Ingresa:<br/>- Nivel MCER<br/>- Tema<br/>- Duración<br/>- Objetivo"]
    
    C --> D{"Clic en<br/>Generar"}
    
    D --> E["🔐 Verificar API Key<br/>OPENAIKEY"]
    
    E --> F{"API Key<br/>válida?"}
    
    F -->|No| G["Retornar error"]
    F -->|Sí| H["✅ Validar entrada<br/>- Tema 3-200 caracteres<br/>- Duración 5-60 min<br/>- Objetivo max 500 caracteres"]
    
    H --> I{"Entrada<br/>válida?"}
    
    I -->|No| J["Retornar errores"]
    I -->|Sí| K["📝 Generar clase<br/>con GPT-4"]
    
    K --> L["OpenAI API<br/>gpt-4o"]
    
    L --> M["Clase de Alemán<br/>6 secciones Markdown"]
    
    M --> N["Mostrar en interfaz<br/>Usuario revisa"]
    
    N --> O{"¿Usuario descarga?"}
    
    O -->|PowerPoint| P["📊 Crear PowerPoint<br/>python-pptx"]
    O -->|Video| Q["🎬 Generar Video<br/>ffmpeg + gTTS"]
    O -->|Word| R["📄 Crear Word<br/>python-docx"]
    
    P --> S["Convertir PPTX → PNG"]
    S --> T["Agregar personajes<br/>aleatorios de /1-9.jpg"]
    T --> U["🎨 Generar imágenes<br/>DALL-E 3"]
    U --> V["Compilar video<br/>+ narración audio"]
    V --> W["Archivo .pptx<br/>Descargar"]
    
    Q --> X["Extraer frames del PPTX"]
    X --> Y["Generar voz narrada<br/>gTTS español"]
    Y --> Z["Codificar con ffmpeg"]
    Z --> AA["Archivo .mp4<br/>Descargar"]
    
    R --> AB["Parsear Markdown"]
    AB --> AC["Crear estructura Word"]
    AC --> AD["Archivo .docx<br/>Descargar"]
    
    W --> AE["Usuario descarga<br/>todos los archivos"]
    AA --> AE
    AD --> AE
    
    style A fill:#e22416,color:#fff
    style B fill:#f2b903,color:#000
    style K fill:#900f2b,color:#fff
    style L fill:#e22416,color:#fff
    style M fill:#f2b903,color:#000
    style W fill:#110f0f,color:#fff
    style AA fill:#110f0f,color:#fff
    style AD fill:#110f0f,color:#fff
    style AE fill:#900f2b,color:#fff
\`\`\`
