# Ecuaciones Diferenciales

**Guía de Repaso: Ecuaciones Diferenciales**
*Métodos Analíticos para Ecuaciones de Primer Orden*

**Autor:** Mario Uriel Juárez Rosales
**Facultad:** Facultad de Sistemas Biológicos e Innovación Tecnológica (FASBIT)

---

## Resumen

Esta guía proporciona un compendio teórico y práctico de los métodos analíticos para resolver ecuaciones diferenciales ordinarias (EDO) de primer orden, fundamentado en el texto de Dennis G. Zill. Se abordan de forma sistemática los conceptos de separación de variables, ecuaciones lineales, ecuaciones exactas, factores integrantes para convertirlas en exactas, sustituciones homogéneas y la transformación de Bernoulli, ofreciendo reglas de identificación claras y un ejemplo resuelto de forma continua y fluida.

---

## 1. Variables Separables

### 1.1 Definición

Una ecuación diferencial de primer orden es **separable** si puede expresarse en una forma donde cada variable y su diferencial respectivo puedan agruparse de manera independiente en lados opuestos de la igualdad.

### 1.2 Forma General

Una ecuación diferencial de primer orden de la forma:

```
dy/dx = g(x)h(y)
```

es de variables separable. Al asumir que h(y) ≠ 0, puede reescribirse mediante la separación algebraica de sus términos diferenciales como:

```
(1/h(y)) dy = g(x)dx
```

### 1.3 Solución General

La solución general se obtiene mediante la integración directa de ambos miembros de la ecuación:

```
∫ (1/h(y)) dy = ∫ g(x)dx + C
```

donde C representa una constante de integración arbitraria.

---

## 2. Ecuaciones Diferenciales Lineales

### 2.1 Definición

Las ecuaciones diferenciales de primer orden **lineales** se caracterizan porque la variable dependiente y y su derivada y' aparecen únicamente elevadas a la primera potencia y no forman parte de argumentos de funciones no lineales.

### 2.2 Forma Estándar

La forma estándar de una ecuación diferencial lineal de primer orden es:

```
dy/dx + P(x)y = f(x)
```

donde P(x) y f(x) son funciones continuas en un intervalo común I.

### 2.3 Factor Integrante

El método analítico clásico de Zill requiere calcular un **factor integrante** μ(x) definido como:

```
μ(x) = e^(∫ P(x)dx)
```

Al multiplicar la forma estándar por μ(x), el miembro izquierdo se convierte en la derivada del producto del factor por la variable dependiente:

```
d/dx [μ(x)y] = μ(x)f(x)
```

lo que permite integrar directamente:

```
μ(x)y = ∫ μ(x)f(x)dx + C
```

---

## 3. Ecuaciones Exactas

### 3.1 Definición

Las ecuaciones exactas se basan en el concepto de la **diferencial total** de una función de varias variables.

### 3.2 Forma Diferencial

Una ecuación diferencial escrita en su forma diferencial:

```
M(x, y)dx + N(x, y)dy = 0
```

### 3.3 Condición de Exactitud

Es una ecuación exacta en una región rectangular del plano si las funciones M y N son continuas y tienen primeras derivadas parciales continuas que cumplen la condición matemática de simetría:

```
∂M/∂y = ∂N/∂x
```

### 3.4 Solución General

Si se cumple esta condición, existe una función f(x, y) tal que su diferencial total es df = M dx + N dy. La solución general implícita de la EDO viene dada por la relación:

```
f(x, y) = C
```

---

## 4. Ecuaciones Convertibles a Exactas

Cuando una ecuación diferencial escrita de la forma M(x, y)dx + N(x, y)dy = 0 no es exacta (∂M/∂y ≠ ∂N/∂x), en ocasiones es posible transformarla multiplicándola por un factor integrante μ adecuado.

### 4.1 Determinación del Factor Integrante

Para hallar un factor integrante μ, se analizan dos casos según la dependencia de las variables de las funciones resultantes:

| Caso | Condición | Factor Integrante |
|------|-----------|-------------------|
| **Caso I** | (∂M/∂y - ∂N/∂x)/N = P(x) es función solo de x | μ(x) = e^(∫ P(x)dx) |
| **Caso II** | (∂N/∂x - ∂M/∂y)/M = Q(y) es función solo de y | μ(y) = e^(∫ Q(y)dy) |

---

## 5. Ecuaciones Homogéneas

### 5.1 Definición de Homogeneidad

Una función f(x, y) es **homogénea de grado n** si cumple con la relación:

```
f(tx, ty) = tⁿf(x, y)
```

### 5.2 Ecuación Homogénea

Una ecuación diferencial M(x, y)dx + N(x, y)dy = 0 es homogénea si tanto M como N son funciones homogéneas del mismo grado n.

### 5.3 Sustituciones

Toda ecuación homogénea puede convertirse en separable mediante cualquiera de las siguientes sustituciones algebraicas:

| Sustitución | Diferencial |
|-------------|-------------|
| y = ux | dy = udx + xdu |
| x = vy | dx = vdy + ydv |

---

## 6. Ecuaciones de Bernoulli

### 6.1 Definición

La ecuación de **Bernoulli** es una extensión de las ecuaciones lineales que incorpora un término de potencia no lineal en la variable dependiente.

### 6.2 Forma General

La ecuación diferencial de primer orden de Bernoulli tiene la forma matemática:

```
dy/dx + P(x)y = f(x)yⁿ
```

donde n es cualquier número real.

### 6.3 Casos Especiales

| Valor de n | Tipo de ecuación | Método |
|------------|------------------|--------|
| n = 0 | Lineal | Factor integrante |
| n = 1 | Lineal | Factor integrante |
| n ≠ 0, 1 | Bernoulli | Sustitución u = y¹⁻ⁿ |

### 6.4 Transformación

Para n ≠ 0, 1, la ecuación se reduce a una forma lineal para la variable dependiente u mediante la sustitución no lineal:

```
u = y¹⁻ⁿ
```

La ecuación lineal resultante para la variable transformada u(x) tiene la forma:

```
du/dx + (1-n)P(x)u = (1-n)f(x)
```

---

## 7. Conclusión

El estudio de las ecuaciones diferenciales de primer orden analizadas bajo el enfoque clásico de Dennis G. Zill expone la transición estructurada entre métodos operativos directos (separación de variables y factor integrante lineal) hacia metodologías de transformación de variables algebraicas más complejas (ecuaciones exactas, transformaciones homogéneas y ecuaciones de Bernoulli). El dominio analítico de estas técnicas representa una de las bases operativas más importantes para el modelado matemático en diversas áreas de la ingeniería.

---

## Referencias

[1] Zill, D. G. (2018). *Matemáticas avanzadas para ingeniería* (3.ª ed.). Vol. 1: Ecuaciones diferenciales. Cengage Learning.
