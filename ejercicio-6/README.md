# Ejercicio 6 – Sistema de Gestión de Biblioteca Universitaria

## 1. Enunciado
Se debe diseñar un sistema básico para gestionar los recursos de una biblioteca universitaria y los préstamos realizados a los usuarios.

## 2. Clases
- Recurso
- Libro
- Revista
- Usuario

## 3. Diseño UML
La clase Recurso actúa como clase padre y representa cualquier elemento prestable de la biblioteca.  
Contiene atributos privados comunes y métodos públicos para gestionar el préstamo y la devolución.

Las clases Libro y Revista heredan de Recurso y añaden atributos específicos propios de cada tipo de recurso.

La clase Usuario representa a las personas que pueden realizar préstamos.  
Un usuario puede tener prestados uno o varios recursos al mismo tiempo.

La relación entre Usuario y Recurso es una asociación con multiplicidad de uno a muchos (1 a 0..*).

## 4. Diagrama de clases (Mermaid)
```mermaid
classDiagram
    class Recurso {
        -int id
        -String titulo
        +prestar()
        +devolver()
    }

    class Libro {
        -String isbn
    }

    class Revista {
        -int numeroEdicion
    }

    class Usuario {
        -String nombre
        -int numCarnet
    }

    Recurso <|-- Libro
    Recurso <|-- Revista

    Usuario "1" -- "0..*" Recurso