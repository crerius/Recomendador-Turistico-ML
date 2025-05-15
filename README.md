# Sistema de Recomendación Turística para Colombia
Este README también está disponible en Inglés más abajo. / This README is also available in English below.

Este proyecto es un sistema de recomendación de destinos turísticos y hoteles en Colombia, desarrollado en Python. El sistema interactúa con el usuario para entender sus preferencias de viaje y, basándose en ellas, sugiere los destinos más adecuados junto con opciones de alojamiento relevantes.

Este proyecto fue desarrollado como parte fundamental de mi aprendizaje y aplicación práctica de conocimientos durante el bootcamp de **Talento Tech**.

## 📜 Descripción General

El objetivo principal es ofrecer una herramienta interactiva que, a partir de las preferencias del usuario (como tipo de actividades, ambiente, etc.), pueda filtrar y presentar los destinos colombianos que mejor se adaptan a sus deseos. Adicionalmente, para los destinos sugeridos, se proporcionan ejemplos de hoteles.

## ✨ Características Principales

- Recomendaciones personalizadas de más de 20 destinos turísticos en Colombia.
- Sugerencias de hoteles para cada destino recomendado, incluyendo tipo, rango de precio estimado y características clave.
- Entrada interactiva de preferencias del usuario (playa, cultura, naturaleza, vida nocturna, gastronomía) mediante la consola.
- Opción para que el usuario finalice la entrada de preferencias de manera anticipada.
- Uso de DataFrames de Pandas para gestionar la información de destinos (con detalles climáticos) y hoteles.

## 🛠️ Tecnologías Utilizadas

- **Lenguaje:** Python 3.x
- **Bibliotecas Principales:**
    - **Pandas:** Para la estructuración y manipulación de datos.
    - **NumPy:** Para operaciones numéricas y la manipulación de arrays.
    - **Scikit-learn:** Para el preprocesamiento de datos (`StandardScaler`) y cálculo de similitud (`cosine_similarity`).
    - **IPython:** Para la visualización mejorada de DataFrames en entornos de desarrollo (`display`).

## ⚙️ Configuración y Uso

Sigue estos pasos para configurar y ejecutar el proyecto en tu entorno local:

### Prerrequisitos

- Python 3.7 o superior.
- pip (manejador de paquetes de Python).
- Git (para clonar el repositorio).

### Instalación

1.  **Clona el repositorio:**
    ```bash
    git clone [https://github.com/crerius/Recomendador-Turistico-ML](https://github.com/crerius/Recomendador-Turistico-ML)
    cd Recomendador-Turistico-ML
    ```

2.  **(Recomendado) Crea y activa un entorno virtual:**
    ```bash
    python -m venv venv
    ```
    * En Windows:
        ```bash
        venv\Scripts\activate
        ```
    * En macOS/Linux:
        ```bash
        source venv/bin/activate
        ```

3.  **Instala las dependencias:**
    Crea un archivo llamado `requirements.txt` en la raíz de tu proyecto con el siguiente contenido:
    ```txt
    pandas
    numpy
    scikit-learn
    ipython
    ```
    Luego, ejecuta en tu terminal:
    ```bash
    pip install -r requirements.txt
    ```

### Ejecución

1.  Asegúrate de estar en el directorio raíz del proyecto donde se encuentra tu script principal.
2.  Ejecuta el script desde tu terminal:
    ```bash
    python Hoteles_modelo_ML.py
    ```

3.  Sigue las instrucciones que aparecerán en la consola para ingresar tus preferencias de viaje.

## 🧠 Cómo Funciona

El sistema sigue estos pasos para generar recomendaciones:

1.  **Entrada de Preferencias:** El usuario especifica qué características busca en un destino (playa, cultura, etc.) mediante entradas binarias (1 para Sí, 0 para No).
2.  **Preprocesamiento:** Las preferencias del usuario y las características de los destinos se escalan usando `StandardScaler` de Scikit-learn. Esto normaliza los datos y asegura que todas las características contribuyan de manera equitativa al cálculo de similitud.
3.  **Similitud de Destinos:** Se calcula la similitud del coseno entre el vector de preferencias del usuario (escalado) y los vectores de características de cada destino (escalados). Los destinos se ordenan según esta puntuación para identificar los más afines.
4.  **Sugerencia de Hoteles:**
    * Se calcula una puntuación de "similitud artificial" para todos los hoteles (adaptando sus puntuaciones para que tengan una dimensionalidad compatible con las preferencias del usuario, como se solicitó para mantener la estructura de cálculo).
    * Finalmente, y más importante, **se muestran hoteles pertenecientes a los destinos que fueron recomendados al usuario**, ordenados dentro de cada ciudad.
5.  **Datos:** La información se maneja a través de dos DataFrames de Pandas: uno para los destinos y otro para los hoteles.

## 🚀 Posibles Mejoras Futuras

- Integrar un sistema de ponderación para las preferencias del usuario (ej. que la cultura sea más importante que la playa).
- Expandir la base de datos de destinos y hoteles, o conectarla a APIs externas para obtener datos actualizados.
- Desarrollar una interfaz gráfica de usuario (GUI) o una aplicación web para una mejor experiencia.
- Implementar algoritmos de recomendación más sofisticados (ej. filtrado colaborativo si se recolectaran datos de múltiples usuarios).
- Añadir más filtros para hoteles (ej. rango de precio exacto, servicios específicos, accesibilidad).
- Mejorar la lógica de similitud de hoteles para que se base en características más directas del hotel en relación con las preferencias del usuario.

## 🙏 Agradecimientos

Este proyecto es el resultado del aprendizaje y la aplicación de los conocimientos adquiridos durante el bootcamp de **Talento Tech**. Agradezco a los instructores y al programa por la valiosa formación.

---

---

## English Version

# Colombia Tourism Recommendation System

This project is a recommendation system for tourist destinations and hotels in Colombia, developed in Python. The system interacts with the user to understand their travel preferences and, based on these, suggests the most suitable destinations along with relevant accommodation options.

This project was developed as a fundamental part of my learning and practical application of knowledge during the **Talento Tech** bootcamp.

## 📜 Overview

The main objective is to offer an interactive tool that, based on user preferences (such as type of activities, ambiance, etc.), can filter and present Colombian destinations that best suit their desires. Additionally, for the suggested destinations, examples of hotels are provided.

## ✨ Key Features

- Personalized recommendations for over 20 tourist destinations in Colombia.
- Hotel suggestions for each recommended destination, including type, estimated price range, and key features.
- Interactive console-based input for user preferences (beach, culture, nature, nightlife, gastronomy).
- Option for the user to end the preference input process prematurely.
- Use of Pandas DataFrames to manage destination information (including climate details) and hotel data.

## 🛠️ Technologies Used

- **Language:** Python 3.x
- **Main Libraries:**
    - **Pandas:** For data structuring and manipulation.
    - **NumPy:** For numerical operations and array manipulation.
    - **Scikit-learn:** For data preprocessing (`StandardScaler`) and similarity calculation (`cosine_similarity`).
    - **IPython:** For enhanced display of DataFrames in development environments (`display`).

## ⚙️ Setup and Usage

Follow these steps to set up and run the project in your local environment:

### Prerequisites

- Python 3.7 or higher.
- pip (Python package manager).
- Git (to clone the repository).

### Installation

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/crerius/Recomendador-Turistico-ML.git](https://github.com/crerius/Recomendador-Turistico-ML.git)
    cd Recomendador-Turistico-ML
    ```

2.  **(Recommended) Create and activate a virtual environment:**
    ```bash
    python -m venv venv
    ```
    * On Windows:
        ```bash
        venv\Scripts\activate
        ```
    * On macOS/Linux:
        ```bash
        source venv/bin/activate
        ```

3.  **Install dependencies:**
    Create a file named `requirements.txt` in the root of your project with the following content:
    ```txt
    pandas
    numpy
    scikit-learn
    ipython
    ```
    Then, run in your terminal:
    ```bash
    pip install -r requirements.txt
    ```

### Running the Project

1.  Ensure you are in the root directory of the project where your main script is located.
2.  Run the script from your terminal:
    ```bash
    python Hoteles_modelo_ML.py
    ```
3.  Follow the on-screen prompts to enter your travel preferences.

## 🧠 How it Works

The system follows these steps to generate recommendations:

1.  **Preference Input:** The user specifies what features they are looking for in a destination (beach, culture, etc.) using binary inputs (1 for Yes, 0 for No).
2.  **Preprocessing:** User preferences and destination features are scaled using Scikit-learn's `StandardScaler`. This normalizes the data and ensures all features contribute પાણીquitably to the similarity calculation.
3.  **Destination Similarity:** Cosine similarity is calculated between the user's scaled preference vector and the scaled feature vectors of each destination. Destinations are ranked according to this similarity score to identify the best matches.
4.  **Hotel Suggestions:**
    * An "artificial similarity" score is calculated for all hotels (by adapting their scores to have a dimensionality compatible with user preferences, as requested to maintain the calculation structure).
    * Finally, and most importantly, **hotels belonging to the destinations recommended to the user are displayed**, ordered within each city.
5.  **Data:** Information is managed through two Pandas DataFrames: one for destinations and another for hotels.

## 🚀 Potential Future Enhancements

- Integrate a weighting system for user preferences (e.g., culture being more important than beach).
- Expand the database of destinations and hotels, or connect it to external APIs for updated data.
- Develop a graphical user interface (GUI) or a web application for a better user experience.
- Implement more sophisticated recommendation algorithms (e.g., collaborative filtering if multi-user data were available).
- Add more filters for hotels (e.g., exact price range, specific amenities, accessibility).
- Improve the hotel similarity logic to be based on more direct hotel features in relation to user preferences.

## 🙏 Acknowledgements

This project is the result of learning and applying knowledge acquired during the **Talento Tech** bootcamp. I am grateful to the instructors and the program for the valuable training.
