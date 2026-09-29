# Cálculo Diferencial

**Guía de Repaso: Cálculo Diferencial**
*Análisis Completo de Límites, Continuidad y Técnicas de Derivación*

**Autor:** Mario Uriel Juárez Rosales
**Facultad:** Facultad de Sistemas Biológicos e Innovación Tecnológica (FASBIT)

---

## Resumen

Esta guía proporciona un repaso estructurado y sistemático de los conceptos fundamentales de Cálculo Diferencial correspondientes a los Capítulos P (Preparación para el Cálculo), 1 (Límites y sus propiedades) y 2 (Derivación) de la sexta edición del texto clásico de Larson, Hostetler y Edwards, complementado con el rigor analítico de la séptima edición de El Cálculo de Louis Leithold.

---

## 1. Preparación para el Cálculo: Gráficas y Funciones

### 1.1 Interceptos

Los **interceptos** son los puntos donde la gráfica de una función cruza los ejes coordenados:

- **Intercepto con el eje x:** Se calcula haciendo y = 0 y resolviendo para x
- **Intercepto con el eje y:** Se calcula haciendo x = 0 y evaluando f(0)

### 1.2 Simetría

| Tipo de simetría | Condición | Descripción |
|------------------|-----------|-------------|
| **Simetría respecto al eje y** | f(-x) = f(x) | Función **par** |
| **Simetría respecto al origen** | f(-x) = -f(x) | Función **impar** |
| **Simetría respecto al eje x** | f(x) = -f(x) | No es una función (salvo f(x) = 0) |

### 1.3 Dominio

El **dominio** de una función es el conjunto de todos los números reales para los cuales la expresión de la función genera un valor real bien definido.

**Restricciones comunes:**
- El denominador no puede ser cero
- El radicando de una raíz par debe ser no negativo
- El argumento de un logaritmo debe ser positivo

---

## 2. Propiedades Fundamentales de los Límites

El cálculo de límites analíticos se basa en propiedades teóricas que distribuyen el operador del límite sobre las operaciones aritméticas elementales de las funciones.

### Regla Teórica 2.1 - Propiedades de los Límites

Sean f(x) y g(x) dos funciones tales que sus límites cuando x → c existen, siendo lim f(x) = L y lim g(x) = M, y sea k una constante real:

| Propiedad | Fórmula |
|-----------|---------|
| Límite de una constante | lim k = k |
| Límite de la identidad | lim x = c |
| Límite de una suma o resta | lim [f(x) ± g(x)] = L ± M |
| Límite de un producto | lim [f(x) · g(x)] = L · M |
| Límite de un cociente | lim f(x)/g(x) = L/M, siempre que M ≠ 0 |
| Límite de una potencia | lim [f(x)]ⁿ = Lⁿ, para n ∈ ℝ⁺ |
| Límite de una constante por función | lim [k · f(x)] = k · L |

---

## 3. Definición Formal de Límite (ε-δ)

La definición **Épsilon-Delta** (ε-δ) introducida por Leithold proporciona el soporte matemático riguroso para formalizar la idea de aproximación local sin depender de nociones intuitivas de cercanía.

### Regla Teórica 3.1 - Criterio Épsilon-Delta

Decimos que el límite de f(x) cuando x se aproxima a c es el número real L, denotado como:

```
lim f(x) = L
x→c
```

si para cada número real ε > 0, existe un número real correspondiente δ > 0 tal que si:

```
0 < |x - c| < δ  ⇒  |f(x) - L| < ε
```

### Interpretación Gráfica

```
    y
    │
 L + ε ┤ ┌─────────────┐
    │ │             │
    │ │   Región    │
 L ──┤ │   donde     │
    │ │   se cumple  │
    │ │   |f(x)-L|<ε │
 L - ε ┤ └─────────────┘
    │
    └──────┬─────┬──────┬──→ x
          c-δ   c    c+δ
```

---

## 4. Técnicas Analíticas para el Cálculo de Límites

Cuando la sustitución directa produce formas indeterminadas del tipo 0/0, se aplican técnicas de factorización y racionalización para remover la indeterminación.

### 4.1 Formas Indeterminadas Comunes

| Forma | Descripción | Técnica |
|-------|-------------|---------|
| 0/0 | Numerador y denominador tienden a 0 | Factorización, racionalización |
| ∞/∞ | Numerador y denominador tienden a ∞ | Dividir entre la mayor potencia |
| ∞ - ∞ | Diferencia de infinitos | Racionalización |
| 0 · ∞ | Producto de cero por infinito | Reescribir como cociente |
| 1^∞, ∞⁰, 0⁰ | Formas exponenciales | Usar logaritmos |

### 4.2 Técnicas Algebraicas

**Cancelación por factorización:**
Se factorizan numerador y denominador para simplificar el factor que causa la indeterminación.

**Racionalización por conjugado:**
Se multiplica tanto el numerador como el denominador por el conjugado del término que contiene raíces para eliminar la anulación.

---

## 5. Continuidad y el Teorema del Valor Intermedio (TVI)

### 5.1 Definición de Continuidad

Una función f es **continua** en un punto x = c si se cumplen tres condiciones:

1. f(c) está definida
2. lim f(x) existe cuando x → c
3. lim f(x) = f(c) cuando x → c

### 5.2 Teorema del Valor Intermedio (TVI)

Si una función f es continua en el intervalo cerrado [a, b], y N es cualquier número real comprendido estrictamente entre f(a) y f(b) (donde f(a) ≠ f(b)), entonces existe al menos un número real c en el intervalo abierto (a, b) tal que:

```
f(c) = N
```

### Interpretación Gráfica del TVI

```
    y
    │
 f(b) ┤─────────────●
    │             ╱
    │           ╱
 N ──┤─────────●──────  ← Existe c tal que f(c) = N
    │       ╱
    │     ╱
 f(a) ┤───●
    │
    └──────┬──────────┬──→ x
           a          b
```

---

## 6. La Definición de la Derivada y Diferenciabilidad

### 6.1 Definición de Derivada

La **derivada** de una función f en un punto x de su dominio viene dada por el límite del cociente de incrementos de diferencias:

```
f'(x) = lim [f(x + Δx) - f(x)] / Δx
       Δx→0
```

siempre que el límite existe.

### 6.2 Interpretación Geométrica

La derivada f'(x) representa la **pendiente de la recta tangente** a la curva y = f(x) en el punto (x, f(x)).

```
    y
    │      ╱
    │    ╱  ← Recta tangente
    │  ╱     pendiente = f'(x)
    │╱
    ●──────────
    │  (x, f(x))
    │
    └──────────────→ x
```

### 6.3 Relación entre Diferenciabilidad y Continuidad

> **Teorema:** Si f es diferenciable en un punto x = c, entonces f es continua en x = c.

> **⚠️ Importante:** La continuidad NO garantiza la diferenciabilidad. Una función puede ser continua en un punto pero no diferenciable (ejemplo: f(x) = |x| en x = 0).

---

## 7. Reglas Fundamentales de Derivación

Las leyes operativas del cálculo diferencial nos permiten calcular la derivada de funciones complejas de forma puramente analítica mediante reglas aritméticas establecidas.

### Regla Teórica 7.1 - Teoremas Analíticos de Derivación

Sean u(x) y v(x) funciones diferenciables:

| Regla | Fórmula |
|-------|---------|
| **Regla del Producto** | d/dx[u · v] = u · dv/dx + v · du/dx |
| **Regla del Cociente** | d/dx[u/v] = (v · du/dx - u · dv/dx) / v² |
| **Regla de la Cadena** | d/dx[f(g(x))] = f'(g(x)) · g'(x) |

### Derivadas de Funciones Trigonométricas

| Función | Derivada |
|---------|----------|
| sin(x) | cos(x) |
| cos(x) | -sin(x) |
| tan(x) | sec²(x) |
| cot(x) | -csc²(x) |
| sec(x) | sec(x)tan(x) |
| csc(x) | -csc(x)cot(x) |

---

## 8. Derivación Implícita y Ritmos Relacionados

### 8.1 Diferenciación Implícita

En una curva algebraica definida implícitamente por la ecuación F(x, y) = 0, para calcular dy/dx se derivan ambos miembros de la ecuación respecto a la variable independiente x, aplicando la regla de la cadena para la variable y (añadiendo el factor dy/dx). posteriormente, se agrupan los factores diferenciales y se despeja dy/dx.

### 8.2 Pasos para la Derivación Implícita

1. Derivar ambos lados de la ecuación respecto a x
2. Aplicar la regla de la cadena cuando derivemos y (multiplicar por dy/dx)
3. Agrupar los términos con dy/dx en un lado
4. Factorizar dy/dx
5. Despejar dy/dx

---

## 9. Conclusión

El estudio formal de las bases del cálculo diferencial, unificado bajo los enfoques de la Sexta Edición de Larson y la rigurosa perspectiva formal de Louis Leithold, proporciona un panorama conceptual robusto. La transición que inicia con la preparación algebraica (Capítulo P) se consolida a través de la formalización métrica ε-δ de límites y el Teorema del Valor Intermedio (Capítulo 1), sentando las bases teóricas necesarias para la construcción formal de la derivada, el análisis de diferenciabilidad y el modelado físico de tasas de cambio en el tiempo (Capítulo 2).

---

## Referencias

[1] Larson, R. E., Hostetler, R. P., y Edwards, B. H. (1999). *Cálculo y geometría analítica* (6.ª ed.). Vol. 1. McGraw-Hill / Interamericana.

[2] Leithold, L. (1998). *El cálculo* (7.ª ed.). Oxford University Press.
