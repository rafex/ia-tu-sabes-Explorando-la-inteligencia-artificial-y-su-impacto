
# Actividades Interactivas

## Simulación en Tiempo Real
1. **Chat con una IA:**
   - Proponer temas y mostrar cómo la IA genera ideas o textos en segundos.
   - Ejemplo: "Explícale a alguien qué es un algoritmo en palabras simples."

2. **Desafío rápido:**
   - Responder preguntas complejas o resolver problemas en tiempo real.

---

## Mini Taller de Código
**Objetivo:** Crear un modelo simple de análisis de texto con IA.

```python
from sklearn.feature_extraction.text import CountVectorizer
from sklearn.naive_bayes import MultinomialNB

texts = ["Me encanta este lugar", "Este producto es terrible", "El servicio es excelente", 
         "No volveré jamás", "Estoy muy feliz con mi compra", "Es lo peor que he probado"]
labels = ["positivo", "negativo", "positivo", "negativo", "positivo", "negativo"]

vectorizer = CountVectorizer()
X = vectorizer.fit_transform(texts)

model = MultinomialNB()
model.fit(X, labels)

test_texts = ["Me gusta mucho", "Es horrible", "Estoy satisfecho con el producto"]
X_test = vectorizer.transform(test_texts)
predictions = model.predict(X_test)

for text, sentiment in zip(test_texts, predictions):
    print(f"'{text}' → Sentimiento: {sentiment}")
```

---

## Pregunta Final:
¿Qué pasos tomarás para integrar la IA en tus estudios o trabajo?
