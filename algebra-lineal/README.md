# Álgebra Lineal

**Un Repaso General de Álgebra Lineal**
*Álgebra de Matrices, Sistemas de Ecuaciones, Ajuste de Curvas y Cayley-Hamilton*

**Autor:** Mario Uriel Juárez Rosales
**Facultad:** Facultad de Sistemas Biológicos e Innovación Tecnológica (FASBIT)

---

## Resumen

Este documento presenta una síntesis de los conceptos y métodos fundamentales de un curso de álgebra lineal, alineado con el enfoque pedagógico de Ron Larson. Se introduce formalmente el álgebra de matrices, la multiplicación y sus propiedades algebraicas restrictivas. posteriormente, se revisan los sistemas de ecuaciones lineales y su resolución mediante el método de eliminación de Gauss-Jordan, el método de la matriz inversa y la Regla de Cramer. Además, se expone la aplicación práctica del ajuste polinomial de curvas y se introduce el Teorema de Cayley-Hamilton como herramienta avanzada para el análisis matricial.

---

## 1. Sistemas de Ecuaciones Lineales

### 1.1 Definición

Un **sistema de m ecuaciones lineales con n variables** tiene la forma general:

```
a₁₁x₁ + a₁₂x₂ + ⋯ + a₁ₙxₙ = b₁
a₂₁x₁ + a₂₂x₂ + ⋯ + a₂ₙxₙ = b₂
⋮
aₘ₁x₁ + aₘ₂x₂ + ⋯ + aₘₙxₙ = bₘ
```

donde:
- **aᵢⱼ** son los coeficientes reales (i = 1,...,m; j = 1,...,n)
- **xⱼ** son las incógnitas o variables
- **bᵢ** son los términos constantes

### 1.2 Forma Matricial

Este sistema se puede expresar de forma matricial compacta como:

**Ax = b**

donde:

```
     ┌ a₁₁ a₁₂ ⋯ a₁ₙ ┐       ┌ x₁ ┐       ┌ b₁ ┐
     │ a₂₁ a₂₂ ⋯ a₂ₙ │       │ x₂ │       │ b₂ │
A =  │  ⋮   ⋮  ⋱  ⋮  │,  x = │ ⋮  │,  b = │ ⋮  │
     │ aₘ₁ aₘ₂ ⋯ aₘₙ │       │ xₙ │       │ bₘ │
     └              ┘       └    ┘       └    ┘
```

- **A** ∈ ℝᵐˣⁿ es la **matriz de coeficientes**
- **x** ∈ ℝⁿ es el **vector de variables**
- **b** ∈ ℝᵐ es el **vector de constantes**

### 1.3 Clasificación de Sistemas

De acuerdo con el texto de Larson, un sistema de ecuaciones lineales puede presentar tres escenarios posibles para su conjunto solución:

| Tipo | Descripción | Condición |
|------|-------------|-----------|
| **Consistente determinado** | Una solución única | rango(A) = rango([A|b]) = n |
| **Consistente indeterminado** | Infinitas soluciones | rango(A) = rango([A|b]) < n |
| **Inconsistente** | Sin solución | rango(A) ≠ rango([A|b]) |

---

## 2. Álgebra de Matrices y Sus Propiedades

### 2.1 Multiplicación de Matrices

Sean A una matriz de tamaño m × n y B una matriz de tamaño n × p. El producto **C = AB** es una matriz de tamaño m × p donde cada componente cᵢⱼ se calcula mediante el producto punto del renglón i de A y la columna j de B:

```
cᵢⱼ = Σₖ₌₁ⁿ aᵢₖbₖⱼ = aᵢ₁b₁ⱼ + aᵢ₂b₂ⱼ + ⋯ + aᵢₙbₙⱼ
```

> **⚠️ Requisito indispensable:** El número de columnas de la matriz de la izquierda (A) debe ser exactamente igual al número de renglones de la matriz de la derecha (B).

### 2.2 La Matriz Identidad

La **matriz identidad** de orden n, denotada como Iₙ, es una matriz cuadrada cuyos elementos de la diagonal principal son iguales a 1 y todos los demás elementos son 0:

```
     ┌ 1 0 ⋯ 0 ┐
     │ 0 1 ⋯ 0 │
Iₙ = │ ⋮ ⋮  ⋱ ⋮ │
     │ 0 0 ⋯ 1 │
     └         ┘
```

Esta matriz actúa como el **elemento neutro multiplicativo** en el álgebra matricial:

```
AIₙ = A  y  IₘA = A
```

### 2.3 Propiedades Fundamentales de la Multiplicación

A diferencia de la aritmética ordinaria de los números reales, el producto de matrices posee restricciones y propiedades algebraicas particulares:

| Propiedad | Descripción | Fórmula |
|-----------|-------------|---------|
| **No conmutatividad** | En general, AB ≠ BA | AB ≠ BA |
| **Asociatividad** | El producto es asociativo | A(BC) = (AB)C |
| **Distributividad izquierda** | Se distribuye respecto a la suma | A(B + C) = AB + AC |
| **Distributividad derecha** | Se distribuye respecto a la suma | (A + B)C = AC + BC |
| **Transpuesta de un producto** | La transpuesta del producto | (AB)ᵀ = BᵀAᵀ |

> **Nota importante:** Incluso si ambos productos AB y BA están definidos y producen matrices del mismo tamaño, los resultados numéricos suelen diferir.

---

## 3. Métodos de Resolución de Sistemas de Ecuaciones

### 3.1 Eliminación de Gauss-Jordan

Este método consiste en aplicar **operaciones elementales de renglón** a la matriz aumentada [A | b] para llevarla a su forma escalonada reducida por renglones.

**Operaciones elementales permitidas:**
1. Intercambiar dos renglones: Rᵢ ↔ Rⱼ
2. Multiplicar un renglón por una constante no nula: Rᵢ → kRᵢ
3. Sumar a un renglón un múltiplo de otro: Rᵢ → Rᵢ + kRⱼ

### 3.2 Método de la Matriz Inversa

Si A es una matriz cuadrada y det(A) ≠ 0, entonces el sistema Ax = b tiene una solución dada por:

```
x = A⁻¹b
```

**Pasos para calcular A⁻¹:**
1. Plantear la matriz aumentada conjunta [A | Iₙ]
2. Aplicar operaciones elementales para transformar el bloque izquierdo en la identidad
3. El bloque derecho resultante será A⁻¹

### 3.3 Regla de Cramer

La **Regla de Cramer** proporciona la solución de Ax = b mediante determinantes:

```
xᵢ = det(Aᵢ) / det(A)
```

donde Aᵢ es la matriz A con la columna i reemplazada por el vector b.

> **⚠️ Limitación:** Solo funciona cuando det(A) ≠ 0 (matriz no singular).

---

## 4. Ajuste Polinomial de Curvas

### 4.1 Definición

El **ajuste de curvas** consiste en hallar un polinomio de grado n que pase a través de n + 1 puntos de coordenadas distintas en el plano cartesiano.

Dados los puntos (x₀, y₀), (x₁, y₁), ..., (xₙ, yₙ), buscamos un polinomio:

```
p(x) = a₀ + a₁x + a₂x² + ⋯ + aₙxⁿ
```

que satisfaga p(xᵢ) = yᵢ para todo i = 0, 1, ..., n.

### 4.2 Sistema de Ecuaciones

Sustituyendo cada punto en el polinomio, obtenemos un sistema de ecuaciones lineales:

```
a₀ + a₁x₀ + a₂x₀² + ⋯ + aₙx₀ⁿ = y₀
a₀ + a₁x₁ + a₂x₁² + ⋯ + aₙx₁ⁿ = y₁
⋮
a₀ + a₁xₙ + a₂xₙ² + ⋯ + aₙxₙⁿ = yₙ
```

Este sistema puede resolverse mediante cualquiera de los métodos anteriores (Gauss-Jordan, matriz inversa o Cramer).

---

## 5. El Teorema de Cayley-Hamilton

### 5.1 Definición

El **Teorema de Cayley-Hamilton** establece que una matriz cuadrada A satisface su propio polinomio característico.

El **polinomio característico** de A es:

```
p(λ) = det(λI - A)
```

### 5.2 Enunciado del Teorema

Toda matriz cuadrada satisface su propia ecuación característica. Es decir, si el polinomio característico de A es p(λ), entonces al sustituir la variable escalar λ por la matriz A (y el término constante c₀ por c₀Iₙ), se obtiene la matriz nula O:

```
p(A) = Aⁿ + cₙ₋₁Aⁿ⁻¹ + ⋯ + c₁A + c₀Iₙ = O
```

### 5.3 Aplicación

Este teorema es útil para:
- Calcular potencias altas de matrices
- Calcular la inversa de una matriz
- Simplificar expresiones matriciales

---

## 6. Conclusión

El estudio formal de los sistemas de ecuaciones y sus métodos analíticos constituye el núcleo operativo del álgebra lineal. El ajuste polinomial ilustra la utilidad práctica de estos conceptos al modelar fenómenos continuos. Finalmente, herramientas teóricas avanzadas como el Teorema de Cayley-Hamilton demuestran la profunda interconexión que existe entre el álgebra polinomial y la teoría de matrices.

---

## Referencias

[1] Larson, R. (2019). *Fundamentos de álgebra lineal* (8.ª ed.). Cengage Learning.
