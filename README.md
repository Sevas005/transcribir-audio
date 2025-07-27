# Transcriptor de Audio con Whisper

Este es un script de Python que utiliza el modelo `whisper-large-v3-turbo` de OpenAI a través de la biblioteca `transformers` de Hugging Face para transcribir automáticamente archivos de audio a texto.

## Características

- **Modelo de Alta Calidad**: Utiliza `whisper-large-v3-turbo` para transcripciones precisas.
- **Soporte para GPU**: Detecta y utiliza automáticamente una GPU (CUDA) si está disponible, para acelerar el proceso.
- **Procesamiento por Lotes**: Procesa múltiples archivos de audio (`.mp3`, `.wav`, `.m4a`) de una carpeta específica.
- **Organización de Archivos**: Guarda cada transcripción como un archivo `.txt` en una carpeta de salida designada.

---

## Requisitos

- Python 3.8+
- [FFmpeg](https://ffmpeg.org/download.html) (Debe estar instalado en el sistema y accesible desde la línea de comandos).

Las bibliotecas de Python necesarias se listan en el archivo `requirements.txt`.

---

## Instalación

1.  **Clona el repositorio:**
    ```bash
    git clone [https://github.com/tu-usuario/tu-repositorio.git](https://github.com/tu-usuario/tu-repositorio.git)
    cd tu-repositorio
    ```

2.  **Crea un entorno virtual (recomendado):**
    ```bash
    python -m venv venv
    source venv/bin/activate  # En Windows: venv\Scripts\activate
    ```

3.  **Instala las dependencias:**
    ```bash
    pip install -r requirements.txt
    ```

---

## Uso

1.  **Configura las carpetas**:
    Abre el script `Codigo.py` y modifica las siguientes variables para que apunten a tus carpetas de audio y de salida:
    ```python
    # Ruta de la carpeta que contiene los audios
    audio_folder = "C:/Ruta/A/Tus/Audios"

    # Ruta de la carpeta donde se guardarán las transcripciones
    transcription_folder = "C:/Ruta/Para/Guardar/Transcripciones"
    ```

2.  **Añade tus archivos de audio**:
    Coloca todos los archivos de audio que quieras transcribir (en formato `.mp3`, `.wav` o `.m4a`) en la carpeta que especificaste en `audio_folder`.

3.  **Ejecuta el script**:
    Asegúrate de que tu entorno virtual esté activado y ejecuta el siguiente comando en tu terminal:
    ```bash
    python Codigo.py
    ```

El script mostrará el progreso en la terminal y guardará cada transcripción como un archivo de texto en la carpeta `transcription_folder`.
