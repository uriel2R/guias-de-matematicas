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

El estudio preliminar del análisis real requiere determinar interceptos con los ejes cartesianos, simetrías geométricas de escala y la correcta definición del dominio de las funciones.

### Regla Teórica 1.1 - Interceptos, Simetría y Dominio

Para una función real y = f(x) o una ecuación en el plano:

- **Interceptos:** Se calculan haciendo y = 0 (eje x) o x = 0 (eje y).
- **Simetría con el eje y:** Se cumple si f(-x) = f(x) (función par).
- **Dominio de definición:** Es el conjunto de todos los números reales para los cuales la expresión de la función genera un valor real bien definido.

---

## 2. Propiedades Fundamentales de los Límites

El cálculo de límites analíticos se basa en propiedades teóricas que distribuyen el operador del límite sobre las operaciones aritméticas elementales de las funciones.

### Regla Teórica 2.1 - Propiedades de los Límites

Sean f(x) y g(x) dos funciones tales que sus límites cuando x → c existen, siendo lim f(x) = L y lim g(x) = M, y sea k una constante real:

1. Límite de una constante: lim k = k
2. Límite de la identidad: lim x = c
3. Límite de una suma o resta: lim [f(x) ± g(x)] = L ± M
4. Límite de un producto: lim [f(x) · g(x)] = L · M
5. Límite de un cociente: lim f(x)/g(x) = L/M, siempre que M ≠ 0
6. Límite de una potencia: lim [f(x)]ⁿ = Lⁿ, para n ∈ ℝ⁺

---

## 3. Definición Formal de Límite (ε-δ)

La definición Épsilon-Delta (ε-δ) introducida por Leithold proporciona el soporte matemático riguroso para formalizar la idea de aproximación local sin depender de nociones intuitivas de cercanía.

### Regla Teórica 3.1 - Criterio Épsilon-Delta

Decimos que el límite de f(x) cuando x se aproxima a c es el número real L, denotado como lim f(x) = L, si para cada número real ε > 0, existe un número real correspondiente δ > 0 tal que si:

```
0 < |x - c| < δ  ⇒  |f(x) - L| < ε
```

---

## 4. Técnicas Analíticas para el Cálculo de Límites

Cuando la sustitución directa produce formas indeterminadas del tipo 0/0, se aplican técnicas de factorización y racionalización para remover la indeterminación.

### Regla Teórica 4.1 - Técnicas Algebraicas

Para resolver límites con indeterminaciones del tipo 0/0 aplicamos:

- **Cancelación por factorización:** Se factorizan numerador y denominador para simplificar el factor que causa la indeterminación.
- **Racionalización por conjugado:** Se multiplica tanto el numerador como el denominador por el conjugado del término que contiene raíces para eliminar la anulación.

---

## 5. Continuidad y el Teorema del Valor Intermedio (TVI)

El Teorema del Valor Intermedio (TVI) es una de las implicaciones matemáticas más importantes de la continuidad, estableciendo la existencia de valores intermedios en intervalos continuos.

### Regla Teórica 5.1 - Teorema del Valor Intermedio

Si una función f es continua en el intervalo cerrado [a, b], y N es cualquier número real comprendido estrictamente entre f(a) y f(b) (donde f(a) ≠ f(b)), entonces existe al menos un número real c en el intervalo abierto (a, b) tal que:

```
f(c) = N
```

---

## 6. La Definición de la Derivada y Diferenciabilidad

La derivada representa formalmente la tasa de cambio instantáneo de una función y se define geométricamente como el límite de la pendiente de la recta secante.

### Regla Teórica 6.1 - La Derivada y la Relación con la Continuidad

La derivada de una función f en un punto x de su dominio viene dada por el límite del cociente de incrementos de diferencias:

```
f'(x) = lim [f(x + Δx) - f(x)] / Δx
       Δx→0
```

siempre que el límite exista. Además, si f es diferenciable en un punto x = c, se cumple de forma obligatoria que f es continua en x = c. Sin embargo, la continuidad no garantiza la diferenciabilidad.

---

## 7. Reglas Fundamentales de Derivación

Las leyes operativas del cálculo diferencial nos permiten calcular la derivada de funciones complejas de forma puramente analítica mediante reglas aritméticas establecidas.

### Regla Teórica 7.1 - Teoremas Analíticos de Derivación

Sean u(x) y v(x) funciones diferenciables:

- **Regla del Producto:** d/dx[u · v] = u · dv/dx + v · du/dx
- **Regla del Cociente:** d/dx[u/v] = (v · du/dx - u · dv/dx) / v²
- **Regla de la Cadena (Composición):** d/dx[f(g(x))] = f'(g(x)) · g'(x)
- **Derivadas Trigonométricas:** d/dx[sin(x)] = cos(x), d/dx[cos(x)] = -sin(x)

---

## 8. Derivación Implícita y Ritmos Relacionados

La diferenciación implícita constituye una extensión de la regla de la cadena que nos permite calcular ritmos de cambio en curvas algebraicas cerradas o ligadas al tiempo.

### Regla Teórica 8.1 - Diferenciación Implícita

En una curva algebraica definida implícitamente por la ecuación F(x, y) = 0, para calcular dy/dx se derivan ambos miembros de la ecuación respecto a la variable independiente x, aplicando la regla de la cadena para la variable y (añadiendo el factor dy/dx). posteriormente, se agrupan los factores diferenciales y se despeja dy/dx.

---

## 9. Conclusión

El estudio formal de las bases del cálculo diferencial, unificado bajo los enfoques de la Sexta Edición de Larson y la rigurosa perspectiva formal de Louis Leithold, proporciona un panorama conceptual robusto. La transición que inicia con la preparación algebraica (Capítulo P) se consolida a través de la formalización métrica ε-δ de límites y el Teorema del Valor Intermedio (Capítulo 1), sentando las bases teóricas necesarias para la construcción formal de la derivada, el análisis de diferenciabilidad y el modelado físico de tasas de cambio en el tiempo (Capítulo 2).

---

## Referencias

[1] Larson, R. E., Hostetler, R. P., y Edwards, B. H. (1999). *Cálculo y geometría analítica* (6.ª ed.). Vol. 1. McGraw-Hill / Interamericana.

[2] Leithold, L. (1998). *El cálculo* (7.ª ed.). Oxford University Press.
