---
title: Asistente Mercado Capitales RAG
emoji: 📈
colorFrom: blue
colorTo: green
sdk: gradio
sdk_version: 5.33.0
app_file: app.py
pinned: false
---


# Asistente de Mercado de Capitales mediante RAG

## Integrantes

* Cynthia Guzmán
* Jose Navas

## Materia

Programación de Lenguajes Naturales (PLN)

## Año

2026

## Contexto del proyecto

Las personas que desean iniciarse en el mercado de capitales suelen encontrarse con una gran cantidad de documentación, conceptos técnicos y terminología especializada. Comprender términos como acción, bono, CEDEAR, caución, obligación negociable o perfil de inversor requiere consultar múltiples documentos y fuentes de información.

Para facilitar este proceso, se desarrolló un asistente basado en la técnica Retrieval-Augmented Generation (RAG), capaz de responder preguntas utilizando exclusivamente la información contenida en documentos especializados sobre mercado de capitales.

## Objetivo

Desarrollar un asistente educativo que permita consultar conceptos del mercado de capitales mediante lenguaje natural, reduciendo la necesidad de leer extensos documentos para encontrar definiciones o explicaciones específicas.

## ¿Para qué sirve?

El sistema permite que cualquier usuario pueda realizar preguntas sobre conceptos financieros y obtener respuestas rápidas basadas en la documentación cargada.

Algunos ejemplos de consultas son:

* ¿Qué es una acción?
* ¿Qué es un bono?
* ¿Qué es un CEDEAR?
* ¿Qué es una caución?
* ¿Qué es el riesgo financiero?
* ¿Qué diferencias existen entre renta fija y renta variable?
* ¿Qué perfiles de inversor existen?

## ¿Con qué documentos trabaja?

El sistema utiliza documentos PDF relacionados con educación financiera y mercado de capitales. Estos documentos son cargados por el usuario y posteriormente indexados para permitir búsquedas semánticas y recuperación de información relevante.

## Funcionamiento general

El sistema sigue las siguientes etapas:

1. Carga de documentos PDF.
2. Extracción del contenido textual.
3. División del texto en fragmentos (chunks).
4. Generación de embeddings.
5. Almacenamiento en ChromaDB.
6. Recuperación de los fragmentos más relevantes ante una consulta.
7. Generación de una respuesta utilizando un modelo de lenguaje.
8. Presentación de la respuesta junto con las fuentes consultadas.

## Interfaz de usuario

El sistema cuenta con una interfaz desarrollada en Gradio, accesible desde navegador web.

A través de esta interfaz el usuario puede:

1. Cargar uno o varios documentos PDF.
2. Indexar los documentos para su procesamiento.
3. Realizar preguntas en lenguaje natural.
4. Visualizar la respuesta generada por el sistema.
5. Consultar las fuentes utilizadas para elaborar la respuesta.

La interfaz fue desplegada en Hugging Face Spaces, permitiendo acceder al asistente sin necesidad de instalar software adicional.

## Tecnologías utilizadas

- Python
- LangChain
- ChromaDB
- Sentence Transformers
- Ollama (desarrollo y pruebas locales)
- Hugging Face Inference API (despliegue en Spaces)
- Gradio
- PyPDF

## Limitaciones observadas

Durante las pruebas se observó que el sistema funciona mejor cuando las consultas son específicas y están relacionadas con los conceptos presentes en los documentos. Algunas preguntas formuladas con terminología muy diferente a la utilizada en los PDF pueden dificultar la recuperación de información.

Observamos que el sistema puede tener dificultades cuando:

- La información está distribuida en varios fragmentos del documento.
- Se utilizan términos muy diferentes a los presentes en los PDF.
- El texto del PDF no puede extraerse correctamente.
- La respuesta existe en el documento pero no es recuperada entre los fragmentos más relevantes.

Asimismo, una respuesta incorrecta no necesariamente implica que el modelo desconozca el tema, sino que puede deberse a que no se recuperaron los fragmentos adecuados para responder la consulta.
Por este motivo, las respuestas deben interpretarse como una ayuda para la consulta y no como un reemplazo del documento original.

## Preguntas guía utilizadas para las pruebas

- ¿Qué es una acción?
- ¿Qué es un bono?
- ¿Qué es un CEDEAR?
- ¿Qué es una caución?
- ¿Qué es el riesgo financiero?
- ¿Qué diferencias existen entre renta fija y renta variable?
- ¿Qué perfiles de inversor existen?
- What is financial risk?
- What is a CEDEAR?
- What is a caución?

## Glosario de conceptos cubiertos

El asistente fue diseñado para responder consultas relacionadas con:

- Acciones
- Bonos
- CEDEARs
- Cauciones
- Fondos Comunes de Inversión
- Obligaciones Negociables
- Renta fija
- Renta variable
- Riesgo financiero
- Perfiles de inversor

## Conclusiones

Logramos desarrollar un asistente RAG capaz de responder preguntas sobre conceptos del mercado de capitales utilizando exclusivamente la información contenida en documentos PDF.
Las pruebas realizadas mostraron buenos resultados para preguntas directas y definiciones específicas, permitiendo acceder rápidamente a información que normalmente se encuentra dispersa en múltiples documentos.
El proyecto permitió aplicar conceptos de procesamiento de lenguaje natural, embeddings, recuperación semántica, bases vectoriales, modelos de lenguaje e interfaces conversacionales.

## Despliegue

El sistema fue publicado en Hugging Face Spaces y puede utilizarse desde un navegador web sin necesidad de instalar software adicional.


URL:https://cynthia2026-asistente-mercado-capitales-rag.hf.space


