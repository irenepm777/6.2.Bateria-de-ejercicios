# Ejercicio 3 – Computadora, PlacaBase y Ratón

## 1. Enunciado
Se debe modelar una Computadora y sus componentes, diferenciando entre relaciones de composición y agregación.

## 2. Clases
- Computadora
- PlacaBase
- Raton

## 3. Diseño UML
La Computadora tiene una relación de composición con la PlacaBase, ya que esta no puede existir de forma independiente: si la computadora se destruye, la placa base también.

Por otro lado, la Computadora tiene una relación de agregación con el Ratón, ya que el ratón puede existir y utilizarse de forma independiente aunque la computadora deje de existir.

## 4. Diagrama de clases (Mermaid)
```mermaid
classDiagram
    class Computadora
    class PlacaBase
    class Raton

    Computadora *-- PlacaBase : composición
    Computadora o-- Raton : agregación