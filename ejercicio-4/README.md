# Ejercicio 4 – Centro Comercial y Tiendas

## 1. Enunciado
Se debe modelar un Centro Comercial que alberga varias tiendas, teniendo en cuenta la pertenencia de cada tienda a un único centro.

## 2. Clases
- CentroComercial
- Tienda

## 3. Diseño UML
Un CentroComercial puede albergar una o varias tiendas.
Cada Tienda pertenece obligatoriamente a un único CentroComercial.

La relación se representa mediante una asociación con multiplicidades, indicando que un centro tiene de 1 a muchas tiendas, mientras que cada tienda está asociada a un solo centro.

## 4. Diagrama de clases (Mermaid)
```mermaid
classDiagram
    class CentroComercial
    class Tienda

    CentroComercial "1" -- "1..*" Tienda