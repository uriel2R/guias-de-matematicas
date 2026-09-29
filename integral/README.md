# Cálculo Integral

**Guía de Repaso: Cálculo Integral**
*Fundamentos de la Integral y Métodos de Sustitución*

**Autor:** Mario Uriel Juárez Rosales
**Facultad:** Facultad de Sistemas Biológicos e Innovación Tecnológica (FASBIT)

---

## Resumen

Esta guía constituye la primera entrega de una serie de cuatro partes de Cálculo Integral, basada rigurosamente en la Novena Edición de Purcell, Varberg y Rigdon. El contenido de este módulo inicial aborda la integral indefinida como operación inversa de la derivada, las leyes algebraicas de la notación sigma, la construcción formal de la integral definida a partir del límite de sumas de Riemann con su debida representación geométrica, la consolidación teórica del Teorema Fundamental del Cálculo, una tabla de integrales inmediatas para autoevaluación y el Teorema de Sustitución analítica mediante cambio de variable simple.

---

## 1. La Integral Indefinida (Antiderivada)

### 1.1 Definición

De acuerdo con el enfoque formal de Purcell, el proceso de recuperar la función original a partir de su ritmo de cambio instantáneo se define como la **antiderivación** o **integración indefinida**.

Decimos que F es una **antiderivada** de f en un intervalo I si F'(x) = f(x) para todo x en I. Al conjunto de todas las antiderivadas de f se le denomina **integral indefinida** de f, denotada por:

```
∫ f(x) dx = F(x) + C
```

donde C representa la **constante de integración** real arbitraria.

### 1.2 Propiedades de Linealidad

| Propiedad | Fórmula |
|-----------|---------|
| **Múltiplo constante** | ∫ kf(x) dx = k ∫ f(x) dx, para cualquier constante real k |
| **Suma y diferencia** | ∫ [f(x) ± g(x)] dx = ∫ f(x) dx ± ∫ g(x) dx |

---

## 2. Notación Sigma y Leyes de Sumación

La aproximación geométrica del área bajo una curva requiere compactar la suma de múltiples rectángulos infinitamente delgados empleando la **notación sigma** y sus respectivas propiedades algebraicas.

### 2.1 Definición de Notación Sigma

La suma de n términos se representa mediante el operador sigma:

```
n
Σ aᵢ = a₁ + a₂ + ⋯ + aₙ
i=1
```

### 2.2 Fórmulas de Sumación Especiales de Purcell

| Fórmula | Expresión |
|---------|-----------|
| **Suma de una constante** | Σ c = nc |
| **Suma de los primeros n enteros** | Σ i = n(n+1)/2 |
| **Suma de los primeros n cuadrados** | Σ i² = n(n+1)(2n+1)/6 |

---

## 3. La Integral Definida e Interpretación Gráfica

### 3.1 Definición Formal

La **integral definida** representa la acumulación de un cambio continuo. Geométricamente, si la función f es positiva en un intervalo cerrado [a, b], la integral definida equivale de forma exacta al área bajo la curva.

Sea f una función definida en el intervalo cerrado [a, b]. Si la norma de la partición P tiende a cero (||P|| → 0), la integral definida de f de a a b viene dada por:

```
b
∫ f(x) dx = lim Σ f(xᵢ)Δx
a         ||P||→0
```

donde:
- Δx = (b-a)/n representa el ancho de cada subintervalo homogéneo
- xᵢ = a + iΔx corresponde al punto de aproximación del extremo derecho

### 3.2 Representación Gráfica del Área y las Sumas de Riemann

```
    y
    │
    │    ┌───┐
    │    │   │┌──┐
    │    │   ││  │┌─┐
    │    │   ││  ││ │  ← Rectángulos de Riemann
    │    │   ││  ││ │    (extremo derecho)
    │   ╱│   ││  ││ │
    │  ╱ │   ││  ││ │
    │ ╱  │   ││  ││ │
    │╱   │   ││  ││ │
    └────┴───┴┴──┴┴─┴────→ x
    a                   b

    Área bajo la curva = lim Σ f(xᵢ)Δx
                        n→∞
```

---

## 4. El Teorema Fundamental del Cálculo

El **Teorema Fundamental del Cálculo** unifica los procesos analíticos de derivación e integración, demostrando que son operaciones inversas.

### 4.1 Primer Teorema Fundamental del Cálculo

Sea f una función continua en el intervalo cerrado [a, b] y sea x cualquier punto en (a, b). Si definimos la función de acumulación:

```
        x
G(x) = ∫ f(t) dt
        a
```

entonces:

```
G'(x) = d/dx ∫ f(t) dt = f(x)
              a
```

**Generalización (Regla de Leibniz):** Si el extremo superior es una función diferenciable u(x):

```
d/dx ∫ f(t) dt = f(u(x)) · u'(x)
      a
```

### 4.2 Segundo Teorema Fundamental del Cálculo

Sea f continua en [a, b]. Si F es cualquier antiderivada de f en dicho intervalo (es decir, F'(x) = f(x)), entonces:

```
b
∫ f(x) dx = F(b) - F(a)
a
```

### 4.3 Interpretación

El Segundo Teorema Fundamental del Cálculo nos permite calcular integrales definidas sin necesidad de calcular límites de sumas de Riemann. Solo necesitamos encontrar una antiderivada y evaluarla en los extremos.

---

## 5. Formularios Técnicos: Tabla de Integrales Inmediatas

Para agilizar el proceso analítico de integración de acuerdo con el texto de Purcell, es fundamental disponer de una tabla estructurada de las antiderivadas algebraicas, trascendentes e inversas más importantes del cálculo.

### 5.1 Fórmulas Fundamentales de Integración Inmediata

| Categoría | Estructura del Integrando | Antiderivada General |
|-----------|---------------------------|----------------------|
| **Algebraicas** | ∫ xⁿ dx (n ≠ -1) | xⁿ⁺¹/(n+1) + C |
| | ∫ 1/x dx | ln |x| + C |
| **Exponenciales** | ∫ eˣ dx | eˣ + C |
| | ∫ aˣ dx (a > 0, a ≠ 1) | aˣ/ln(a) + C |
| **Trigonométricas** | ∫ sin(x) dx | -cos(x) + C |
| | ∫ cos(x) dx | sin(x) + C |
| | ∫ sec²(x) dx | tan(x) + C |
| | ∫ csc²(x) dx | -cot(x) + C |
| | ∫ sec(x)tan(x) dx | sec(x) + C |
| | ∫ csc(x)cot(x) dx | -csc(x) + C |
| **Formas Racionales** | ∫ 1/(x²+a²) dx | (1/a)arctan(x/a) + C |
| | ∫ 1/√(a²-x²) dx | arcsin(x/a) + C |

---

## 6. Teorema de Sustitución (Cambio de Variable)

El **Teorema de Sustitución** representa el proceso analítico inverso de la regla de la cadena para funciones compuestas.

### 6.1 Regla de Sustitución para Integrales Indefinidas

Sea g una función diferenciable en un intervalo I y sea f continua en el rango de g. Si definimos el cambio de variable u = g(x), su diferencial correspondiente es du = g'(x) dx. Entonces:

```
∫ f(g(x))g'(x) dx = ∫ f(u) du
```

### 6.2 Pasos para Aplicar la Sustitución

1. **Identificar** la función interna u = g(x)
2. **Calcular** el diferencial du = g'(x) dx
3. **Sustituir** u y du en la integral original
4. **Integrar** respecto a la nueva variable u
5. **Regresar** a la variable original x

---

## 7. Conclusión

El estudio de los fundamentos de la integración planteado en la Novena Edición de Purcell, Varberg y Rigdon demuestra que la acumulación continua (Notación Sigma y Sumas de Riemann) converge de manera exacta en el concepto geométrico y físico de la integral definida. Los procesos de derivación e integración quedan formalmente unificados mediante el Teorema Fundamental del Cálculo, permitiendo evaluar áreas analíticamente a través de integrales inmediatas y del Teorema de Sustitución para variables complejas.

---

## Referencias

[1] Purcell, E. J., Varberg, D., y Rigdon, S. E. (2007). *Cálculo* (9.ª ed.). Pearson Educación / Prentice Hall.
