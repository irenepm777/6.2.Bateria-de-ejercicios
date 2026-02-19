# Ejercicio 2 – Persona y Estudiante

## 1. Enunciado
En un sistema escolar se modelan Personas y Estudiantes.  
Un Estudiante es una Persona, pero además posee información académica adicional.

## 2. Clases
- Persona
- Estudiante

## 3. Diseño UML
La clase Persona actúa como clase base y contiene los atributos comunes a cualquier persona: nombre y DNI.  
La clase Estudiante hereda de Persona y añade sus propios atributos: número de expediente y nota media.  

No se repiten los atributos heredados en la clase Estudiante, ya que estos provienen de la clase padre.

## 4. Diagrama de clases (Mermaid)
```mermaid
classDiagram
    class Persona {
        -String nombre
        -String dni
    }

    class Estudiante {
        -int numeroExpediente
        -double notaMedia
    }

    Persona <-- Estudiante