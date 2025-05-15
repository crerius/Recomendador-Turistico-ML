Sistema de Recomendación Turística para Colombia
Este proyecto es un sistema de recomendación de destinos turísticos y hoteles en Colombia, desarrollado en Python. El sistema interactúa con el usuario para entender sus preferencias de viaje y, basándose en ellas, sugiere los destinos más adecuados junto con opciones de alojamiento relevantes.

Este proyecto fue desarrollado como parte fundamental de mi aprendizaje y aplicación práctica de conocimientos durante el bootcamp de Talento Tech.

📜 Descripción General
El objetivo principal es ofrecer una herramienta interactiva que, a partir de las preferencias del usuario (como tipo de actividades, ambiente, etc.), pueda filtrar y presentar los destinos colombianos que mejor se adaptan a sus deseos. Adicionalmente, para los destinos sugeridos, se proporcionan ejemplos de hoteles.

✨ Características Principales
Recomendaciones Personalizadas: Sugiere más de 20 destinos turísticos en Colombia basándose en la similitud con las preferencias del usuario.
Sugerencias de Hoteles: Para cada destino principal recomendado, muestra una lista de hoteles con detalles como tipo, rango de precio estimado y características destacadas.
Entrada de Preferencias Interactiva: Permite al usuario ingresar sus gustos (playa, cultura, naturaleza, vida nocturna, gastronomía) a través de la consola.
Opción de Salida Anticipada: El usuario puede decidir terminar el proceso de ingreso de preferencias en cualquier momento.
Manejo de Datos: Utiliza DataFrames de Pandas para una gestión estructurada de la información de destinos (incluyendo datos climáticos) y hoteles.
🛠️ Tecnologías Utilizadas
Lenguaje: Python 3.x
Bibliotecas Principales:
Pandas: Para la creación, manipulación y análisis de DataFrames.
NumPy: Para operaciones numéricas y la manipulación de arrays (ej. en la adaptación de características de hoteles).
Scikit-learn: Para el preprocesamiento de datos (StandardScaler) y el cálculo de similitud (cosine_similarity).
IPython: Para la visualización mejorada de DataFrames en entornos de desarrollo (display).
⚙️ Configuración y Uso
Sigue estos pasos para configurar y ejecutar el proyecto en tu entorno local:

Prerrequisitos
Python 3.7 o superior.
pip (manejador de paquetes de Python).
Git (para clonar el repositorio).
Instalación
Clona el repositorio:

Bash

git clone https://github.com/TU_USUARIO_GITHUB/NOMBRE_DE_TU_REPOSITORIO.git
cd NOMBRE_DE_TU_REPOSITORIO
(Reemplaza TU_USUARIO_GITHUB y NOMBRE_DE_TU_REPOSITORIO)

(Recomendado) Crea y activa un entorno virtual:

Bash

python -m venv venv
En Windows: venv\Scripts\activate
En macOS/Linux: source venv/bin/activate
Instala las dependencias:
Crea un archivo llamado requirements.txt en la raíz de tu proyecto con el siguiente contenido:

Plaintext

pandas
numpy
scikit-learn
ipython
Luego, ejecuta:

Bash

pip install -r requirements.txt
Ejecución
Asegúrate de estar en el directorio raíz del proyecto donde se encuentra tu script principal.
Ejecuta el script desde tu terminal:
Bash

python tu_script_principal.py
(Reemplaza tu_script_principal.py con el nombre real de tu archivo Python)
Sigue las instrucciones que aparecerán en la consola para ingresar tus preferencias de viaje.
🧠 Cómo Funciona
El sistema sigue estos pasos para generar recomendaciones:

Entrada de Preferencias: El usuario especifica qué características busca en un destino (playa, cultura, etc.) mediante entradas binarias (1 para Sí, 0 para No).
Preprocesamiento: Las preferencias del usuario y las características de los destinos se escalan usando StandardScaler de Scikit-learn. Esto normaliza los datos y asegura que todas las características contribuyan de manera equitativa al cálculo de similitud.
Similitud de Destinos: Se calcula la similitud del coseno entre el vector de preferencias del usuario (escalado) y los vectores de características de cada destino (escalados). Los destinos se ordenan según esta puntuación para identificar los más afines.
Sugerencia de Hoteles:
Se calcula una puntuación de "similitud artificial" para todos los hoteles (adaptando sus puntuaciones para que tengan una dimensionalidad compatible con las preferencias del usuario, como se solicitó para mantener la estructura de cálculo).
Finalmente, y más importante, se muestran hoteles pertenecientes a los destinos que fueron recomendados al usuario, ordenados dentro de cada ciudad (por ejemplo, por la similitud artificial o por su puntuación original).
Datos: La información se maneja a través de dos DataFrames de Pandas: uno para los destinos y otro para los hoteles.
🚀 Posibles Mejoras Futuras
Integrar un sistema de ponderación para las preferencias del usuario (ej. que la cultura sea más importante que la playa).
Expandir la base de datos de destinos y hoteles, o conectarla a APIs externas para obtener datos actualizados.
Desarrollar una interfaz gráfica de usuario (GUI) o una aplicación web para una mejor experiencia.
Implementar algoritmos de recomendación más sofisticados (ej. filtrado colaborativo si se recolectaran datos de múltiples usuarios).
Añadir más filtros para hoteles (ej. rango de precio exacto, servicios específicos, accesibilidad).
Mejorar la lógica de similitud de hoteles para que se base en características más directas del hotel en relación con las preferencias del usuario.
🙏 Agradecimientos
Este proyecto es el resultado del aprendizaje y la aplicación de los conocimientos adquiridos durante el bootcamp de Talento Tech. Agradezco a los instructores y al programa por la valiosa formación.
