# Ataque con Rainbow Tables a MD5

Este repositorio contiene una implementación y análisis de ataques a contraseñas utilizando **Rainbow Tables** aplicadas al algoritmo hash **MD5**. El proyecto incluye simulaciones, análisis de colisiones y propuestas de mejoras para mitigar este tipo de ataques.

## Contenido

### 1. Introducción
Se presenta el objetivo del proyecto: implementar y evaluar un ataque con Rainbow Tables sobre un conjunto limitado de contraseñas numéricas de 4 dígitos.

### 2. Fundamentos criptográficos
Se explican los conceptos básicos necesarios para entender el ataque:
- **Funciones Hash**: Definición, propiedades y ejemplos.
- **Esquema Merkle–Damgård**: Base estructural de MD5.
- **Algoritmo MD5**: Detalles del funcionamiento del algoritmo.

### 3. Rainbow Table
Se describe el concepto de Rainbow Tables, incluyendo:
- **Definición**: Cómo funcionan y su propósito.
- **Función Reducción**: Transformación de hashes en contraseñas.
- **Colisiones y Limitaciones**: Tipos de colisiones (internas y externas) y falsos positivos.
- **Trade-Off**: Equilibrio entre tiempo y memoria en el diseño de tablas.

### 4. Simulación del ataque
Se implementa un ataque práctico con Rainbow Tables, generando tablas y comparando dos métodos de reducción:
- **Reducción simple**.
- **Reducción con paso** (introduce aleatoriedad para reducir colisiones).

### 5. Análisis de los Resultados
Se evalúan los resultados obtenidos:
- Comparación entre métodos de reducción.
- Análisis de colisiones en función del número de pasos.
- Tasa de éxito en la recuperación de contraseñas.

### 6. Conclusiones y Mejoras
Se discuten las limitaciones de las Rainbow Tables y las técnicas modernas para mitigar estos ataques:
- **Funciones hash lentas**: Como `bcrypt`, `scrypt` y `Argon2`.
- **Salt y Pepper**: Introducción de aleatoriedad y secretos globales para proteger contraseñas.

### 7. Uso Real
Se incluye un ejemplo práctico utilizando la herramienta **RainbowCrack** para descifrar hashes con tablas precomputadas.

---

## Requisitos

- **Python 3.x**
- Librerías: `hashlib`, `matplotlib`, `numpy`

## Ejecución

1. Clona el repositorio:
   ```bash
   git clone https://github.com/martinagg7/cripto_rainbow.git
   cd cripto_rainbow