# Ejercicio 1 – Usuario de plataforma de streaming

## 1. Enunciado
Se debe diseñar una clase que represente a un usuario de una plataforma de streaming, aplicando encapsulación para proteger los datos sensibles.

## 2. Clases
- Usuario

## 3. Diseño UML
La clase Usuario contiene atributos privados para el nombre de usuario y la contraseña.
El correo electrónico es público.
El método cambiarPassword es público, mientras que validarEmail es privado porque es un método interno de validación.

## 4. Diagrama de clases (Mermaid)
```mermaid
classDiagram
    class Usuario {
        -String nombreUsuario
        -String contraseña
        +String correo
        +cambiarPassword(String nueva)
        -validarEmail()
    }