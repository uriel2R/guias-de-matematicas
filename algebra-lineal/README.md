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

Un sistema de m ecuaciones lineales con n variables tiene la forma general:

```
a₁₁x₁ + a₁₂x₂ + ⋯ + a₁ₙxₙ = b₁
a₂₁x₁ + a₂₂x₂ + ⋯ + a₂ₙxₙ = b₂
⋮
aₘ₁x₁ + aₘ₂x₂ + ⋯ + aₘₙxₙ = bₘ
```

donde aᵢⱼ representan los coeficientes reales, xⱼ las incógnitas y bᵢ los términos constantes. Este sistema se puede expresar de forma matricial compacta como:

**Ax = b**

donde A ∈ ℝᵐˣⁿ es la matriz de coeficientes, x ∈ ℝⁿ es el vector de variables y b ∈ ℝᵐ es el vector de constantes.

De acuerdo con el texto de Larson, un sistema de ecuaciones lineales puede presentar tres escenarios posibles para su conjunto solución:

- Una solución única (sistema consistente determinado).
- Infinitas soluciones (sistema consistente indeterminado).
- Sin solución (sistema inconsistente).

---

## 2. Álgebra de Matrices y Sus Propiedades

### 2.1 Multiplicación de Matrices

Sean A una matriz de tamaño m × n y B una matriz de tamaño n × p. El producto C = AB es una matriz de tamaño m × p donde cada componente cᵢⱼ se calcula mediante el producto punto del renglón i de A y la columna j de B:

```
cᵢⱼ = Σ aᵢₖbₖⱼ = aᵢ₁b₁ⱼ + aᵢ₂b₂ⱼ + ⋯ + aᵢₙbₙⱼ
```

Es un requisito indispensable para la multiplicación que el número de columnas de la matriz de la izquierda (A) sea exactamente igual al número de renglones de la matriz de la derecha (B).

### 2.2 La Matriz Identidad

La matriz identidad de orden n, denotada como Iₙ, es una matriz cuadrada cuyos elementos de la diagonal principal son iguales a 1 y todos los demás elementos son 0. Formalmente:

```
Iₙ = [rᵢⱼ] donde rᵢⱼ = 1 si i = j, 0 si i ≠ j
```

Esta matriz actúa como el elemento neutro multiplicativo en el álgebra matricial. Si A es una matriz de tamaño m × n, entonces se cumple que:

```
AIₙ = A  y  IₘA = A
```

### 2.3 Propiedades Fundamentales de la Multiplicación

A diferencia de la aritmética ordinaria de los números reales, el producto de matrices posee restricciones y propiedades algebraicas particulares:

- **No conmutatividad:** En el caso general, el producto de matrices no es conmutativo: AB ≠ BA
- **Asociatividad:** El producto es asociativo siempre que los tamaños sean compatibles: A(BC) = (AB)C
- **Propiedades distributivas:** A(B + C) = AB + AC y (A + B)C = AC + BC
- **Transpuesta de un producto:** (AB)ᵀ = BᵀAᵀ

---

## 3. Métodos de Resolución de Sistemas de Ecuaciones

### 3.1 Eliminación de Gauss-Jordan

Este método consiste en aplicar operaciones elementales de renglón a la matriz aumentada [A | b] para llevarla a su forma escalonada reducida por renglones.

### 3.2 Método de la Matriz Inversa

Si A es una matriz cuadrada y det(A) ≠ 0, entonces el sistema Ax = b tiene una solución dada por x = A⁻¹b.

### 3.3 Regla de Cramer

La Regla de Cramer proporciona la solución de Ax = b mediante determinantes: xᵢ = det(Aᵢ)/det(A).

---

## 4. Ajuste Polinomial de Curvas

El ajuste de curvas consiste en hallar un polinomio de grado n que pase a través de n + 1 puntos de coordenadas distintas en el plano cartesiano.

---

## 5. El Teorema de Cayley-Hamilton

El teorema establece que una matriz cuadrada A satisface su propio polinomio característico p(λ) = det(λI - A) = 0.

Toda matriz cuadrada satisface su propia ecuación característica. Es decir, si el polinomio característico de A es p(λ), entonces al sustituir la variable escalar λ por la matriz A (y el término constante c₀ por c₀Iₙ), se obtiene la matriz nula O:

```
p(A) = Aⁿ + cₙ₋₁Aⁿ⁻¹ + ⋯ + c₁A + c₀Iₙ = O
```

---

## 6. Conclusión

El estudio formal de los sistemas de ecuaciones y sus métodos analíticos constituye el núcleo operativo del álgebra lineal. El ajuste polinomial ilustra la utilidad práctica de estos conceptos al modelar fenómenos continuos. Finalmente, herramientas teóricas avanzadas como el Teorema de Cayley-Hamilton demuestran la profunda interconexión que existe entre el álgebra polinomial y la teoría de matrices.

---

## Referencias

[1] Larson, R. (2019). *Fundamentos de álgebra lineal* (8.ª ed.). Cengage Learning.
