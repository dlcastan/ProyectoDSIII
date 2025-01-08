# ProyectoDSIII

Data Science III: Data Science III: NLP & Deep Learning aplicado a Ciencia de Datos

Comisión: 61625

Alumno: Diego Lopez Castan

# **Presentación del proyecto**

# Abstract

Este conjunto de datos proporciona una visión detallada de los 100 libros más vendidos de Amazon, junto con sus reseñas de clientes, calificaciones, precios y más. Datos recopilados en noviembre de 2023.


# Objetivo

**Analizar las relaciones entre el rating de un libro y sus géneros:**
Identificar si ciertos géneros están asociados con mejores ratings en general.

**Estudio de la relación entre el número de géneros y el rating de un libro:** Analizar si los libros que pertenecen a un genero específico recibe mejor rating.


# Hipotesis

El análisis de los comentarios de los usuarios permite identificar con precisión el sentimiento asociado (positivo o negativo) a los libros más relevantes del sitio amazon.com, utilizando características textuales como las palabras empleadas, su frecuencia y contexto."

**Fuente**

https://www.kaggle.com/datasets/anshtanwar/top-200-trending-books-with-reviews/data

# Lectura de datos

## Campos del archivo Top-100_Trending_Books.csv

**Book Rank: :** Indica la posición del libro entre los 100 más vendidos de Amazon.

**Book Title:** El nombre del libro.

**Price:** El precio del libro en dólares estadounidenses (USD).

**Rating:** La calificación promedio del libro, en una escala de 1 a 5.

**Author:** El autor o autora del libro.

**Year of Publication:** El año en el que el libro fue publicado.

**Genre:** La categoría o género al que pertenece el libro.

**URL:** Enlace al libro en la plataforma de Amazon.

**Review Title:** El título de la reseña del libro.

**Reviewer:** Nombre de la persona que escribió la reseña del libro.

**Reviewer Rating:** La calificación otorgada por el reseñador, en una escala de 1 a 5.

**Review Description:** El texto completo de la reseña escrita por el cliente.

**Is_verified:** Indica si la reseña está verificada como una opinión genuina de un cliente.

**Date:** La fecha en la que la reseña fue publicada.

**Timestamp:** Indica el momento exacto en el que la reseña fue publicada.

**ASIN:** Número estándar de identificación asignado a los productos en Amazon.






## Campos del archivo customer_reviews.csv


**Sno:** Un número secuencial único que representa el índice de cada registro en el conjunto de datos. Es útil para identificar cada fila de manera individual.

**Book Name:** El título del libro al que pertenece la reseña.

**Review Title:** El título o encabezado breve proporcionado por el reseñador para resumir su opinión sobre el libro.

**Reviewer:** El nombre o identificador del usuario que escribió la reseña.

**Reviewer Rating:** La calificación otorgada al libro por el reseñador, en una escala de 1 a 5. Representa la percepción general del usuario sobre el libro.

**Review Description:** El texto completo de la reseña escrita por el usuario, donde detalla su experiencia y opinión sobre el libro.

**Is_Verified:** Un indicador booleano (True/False) que señala si la reseña proviene de una compra verificada en Amazon.

**Date:** La fecha en que la reseña fue publicada.

**Timestamp:** El sello de tiempo exacto que indica el momento en que la reseña fue registrada en el sistema.

**ASIN:** El Amazon Standard Identification Number, un identificador único asignado a cada producto en Amazon. Permite vincular cada reseña a un libro específico.

**Description Length:** La longitud de la reseña en términos de número de caracteres. Es útil para analizar la extensión de las opiniones de los usuarios.



# Campos creados

**polarity:** es un valor flotante dentro del rango [-1.0, 1.0] donde -1.0 indica una emoción negativa muy fuerte y 1.0 indica una emoción positiva muy fuerte. Cero indica neutralidad.

**subjectivity:** Es un valor flotante dentro del rango [0.0, 1.0] donde 0.0 es muy objetivo y 1.0 es muy subjetivo. Las oraciones subjetivas generalmente se refieren a opinión, emoción o juicio mientras que las oraciones objetivas se refieren a hechos informativos.


**polarity_desc:** descripción del campo de polaridad.

**subjectivity_desc:** descripción del campo subjetividad.

**comentario:** 1 indica que el comentario es positivo y 0 que el comentario es negativo.

## **Anexos I**


Utilizo la biblioteca de PyCaret la automatización de tareas comunes como la preparación de datos, la selección y comparación de modelos, el ajuste de hiperparámetros, y la implementación de modelos en producción.


## **Anexos II**


Modifico el dataset utilizando un modelo de Emotion Analysis con HugginFace.


## **Anexos III**


Creo un recomendador basado en contenido textual. Identifico la similitud de los libros basándome en sus descripciones o características textuales.


## **Archivos**


Genero dos archivos para podes correr las aplicaciones creadas con Gradio y las aplicaciones creadas con Streamlit. Los mismos son:

**Top-100_Trending_Books.csv:** en este archivo se encuentran los top 100 libros de Amazon.

**customer_reviews.csv:** en este archivo están las review de los libros encontrados en el archivo Top-100_Trending_Books.csv.
