# Ejercicio 5 – Sistema de pagos

## 1. Enunciado
Se debe diseñar un sistema de pagos flexible que permita utilizar distintos métodos de pago sin modificar la lógica del carrito.

## 2. Clases e interfaces
- MetodoPago (interfaz)
- Tarjeta
- Paypal
- Carrito

## 3. Diseño UML
La interfaz MetodoPago define el contrato que deben cumplir todos los métodos de pago mediante el método procesar(double importe).

Las clases Tarjeta y Paypal implementan la interfaz MetodoPago, proporcionando su propia forma de procesar el pago.

La clase Carrito no depende de una implementación concreta, sino que utiliza la interfaz MetodoPago de forma puntual en su método pagar, permitiendo aplicar polimorfismo.

## 4. Diagrama de clases (Mermaid)
```mermaid
classDiagram
    class MetodoPago {
        <<interface>>
        +procesar(double importe)
    }

    class Tarjeta
    class Paypal
    class Carrito {
        +pagar(MetodoPago miMetodo)
    }

    MetodoPago <|.. Tarjeta
    MetodoPago <|.. Paypal
    Carrito ..> MetodoPago : uso puntual