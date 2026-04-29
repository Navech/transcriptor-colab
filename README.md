# Transcriptor Colab

Notebook de Google Colab para transcribir audios o videos con Whisper.

Permite usar archivos desde una carpeta de Google Drive o subir archivos directamente desde el computador. Al terminar, puede guardar las transcripciones como Google Docs, archivos TXT descargables o ambos.

## Archivo principal

- `Transcriptor_10_colab_limpio.ipynb`: notebook principal para abrir y ejecutar en Google Colab.

## Como descargar el notebook desde GitHub

1. Entra al repositorio:

   ```text
   https://github.com/Navech/transcriptor-colab
   ```

2. Haz click en el archivo `Transcriptor_10_colab_limpio.ipynb`.
3. Descarga el archivo a tu computador.
   - Puedes usar el boton de descarga de GitHub.
   - Si no aparece, puedes entrar a `Raw` y guardar el archivo desde el navegador.

## Como importarlo a Google Colab

1. Abre Google Colab:

   ```text
   https://colab.research.google.com
   ```

2. En Colab, entra a `Archivo` > `Subir notebook`.
3. Selecciona el archivo `Transcriptor_10_colab_limpio.ipynb` que descargaste desde GitHub.
4. Espera a que el notebook se abra en Colab.

## Como configurarlo y ejecutarlo en Google Colab

1. Conectate a un entorno de ejecucion.
2. En Colab, entra a `Entorno de ejecucion` > `Cambiar tipo de entorno de ejecucion`.
3. Configura:
   - Tipo de entorno de ejecucion: `Python 3`
   - Acelerador por hardware: `GPU T4`
4. Guarda la configuracion.
5. Ejecuta el notebook con `Ejecutar todas las celdas` o ejecuta la celda principal manualmente.
6. Sigue las preguntas que aparecen en pantalla.

Con esa configuracion deberia funcionar correctamente.

## Que permite hacer

- Tomar archivos desde una carpeta de Google Drive.
- Subir uno o varios archivos desde el computador.
- Guardar transcripciones como Google Docs.
- Guardar transcripciones como archivos TXT descargables.
- Procesar varios archivos en lote.

## Uso recomendado para probar rapido

Si solo quieres probar el notebook sin usar Google Drive:

1. Elige `Subir archivos desde mi computador`.
2. Elige `Archivos TXT descargables`.
3. Selecciona uno o varios audios/videos.

Ese flujo no requiere permisos de Google Drive ni Google Docs.

## Como usar una carpeta de Google Drive

Si eliges trabajar con una carpeta de Google Drive, el notebook te va a pedir el ID de la carpeta.

Para obtenerlo:

1. Abre Google Drive.
2. Entra a la carpeta donde estan tus audios o videos.
3. Copia la parte final de la URL, justo despues de `/folders/`.
4. Pega ese texto en Colab cuando el notebook te pida el ID.

Ejemplo:

```text
https://drive.google.com/drive/folders/1ABCdefGHIjklMNOpqrSTUvwxYZ123456
```

En ese caso, el ID de la carpeta es:

```text
1ABCdefGHIjklMNOpqrSTUvwxYZ123456
```

No hay que pegar la URL completa, solo el ID.

## Donde guardar las transcripciones

El notebook puede guardar los resultados de tres formas:

- `Google Docs`: crea documentos editables en tu Google Drive.
- `Archivos TXT descargables`: descarga archivos de texto a tu computador.
- `Ambos`: crea Google Docs y ademas descarga los TXT.

Si usas Google Docs o una carpeta de Drive, Colab te pedira iniciar sesion y autorizar permisos de Google. El notebook usara la cuenta de quien lo esta ejecutando.

## Errores comunes

### `module 'torch' has no attribute '_utils'`

Puede pasar si Colab queda con PyTorch cargado de forma inconsistente.

Solucion recomendada:

1. Ve a `Entorno de ejecucion`.
2. Elige `Reiniciar sesion`.
3. Vuelve a ejecutar el notebook desde cero.

### La transcripcion tarda mucho

Puede pasar si el archivo es largo o si no estas usando GPU.

Revisa que el acelerador por hardware sea `GPU T4`.

### No encuentra archivos en Drive

Revisa que:

- El ID de carpeta este bien copiado.
- La carpeta tenga audios o videos.
- La cuenta de Google tenga permiso para ver esa carpeta.

## Dudas o comentarios

Si tienes cualquier duda, consulta o problema usando el notebook, me puedes escribir o dejar un comentario.
