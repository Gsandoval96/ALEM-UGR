# Tema 3: El anillo de los polinomios

## Propiedades de la suma y el producto

Un anillo es una terna (A, +, \*), donde A es un conjunto y + y * son operaciones que verifican las siguientes propiedades:

1. La operación + es asociativa, conmutativa, tiene elemento neutro (que denotaremos como 0) y tiene inverso (para un elemento x, lo denotaremos -x).
2. La operación * es asociativa, tiene elemento neutro (que denotaremos como 1) y verifica la propiedad distributiva para la suma (a(b+c) = a*b + a*c).

Si además la operación * es conmutativa, diremos que el anillo es conmutativo. Un cuerpo es una anillo conmutativo en el que todo elemento distinto de 0 tiene inverso para el producto (para un elemento x, lo denotaremos x<sup>-1</sup>).

#### Ejemplo

+ (N, +, \*) > No tiene inverso para la suma, por lo que no es un anillo.
+ (Z, +, \*) > Cumple ambas propiedades y la operación * es conmutativa, por lo que es un anillo conmutativo.
+ (Q, +, \*) > Cumple ambas propiedades y la operación * es conmutativa, por lo que es un anillo conmutativo. Además, todo elemento distinto de 0 tiene inverso para el producto, por lo que es un cuerpo.
+ (Z<sub>6</sub>, +, \*) > Cumple ambas propiedades y la operación * es conmutativa, por lo que es un anillo conmutativo. Como hay elementos sin inverso para el producto distintos de 0, como por ejemplo el 2 o el 3, por lo que no es un cuerpo.
+ (Z<sub>5</sub>, +, \*) > Cumple ambas propiedades y la operación * es conmutativa, por lo que es un anillo conmutativo. Además, todo elemento distinto de 0 tiene inverso para el producto, por lo que es un cuerpo.

Podremos decir que (Z<sub>n</sub>, +, \*) es siempre un anillo conmutativo. Además, será un cuerpo sí y solo sí n es un número primo.

---

Sea K un cuerpo, el conjunto de los polinomio con coeficientes en el cuerpo K y en la indeterminada x es K[x] = {a<sub>0</sub> + a<sub>1</sub>x + ... + a<sub>n</sub>x<sup>n</sup>} tal que n ∈ a N y {a<sub>0</sub>, a<sub>1</sub>, ..., a<sub>n</sub>} ∈ K.

### Proposición

(K[x], +, \*) es un anillo conmutativo donde + y * son las operaciones usuales de suma y producto de polinomios. Además, (K[x], +, \*) no es un cuerpo.

#### Ejercicio

Sean a(x) = 3x<sup>4</sup> + 4x<sup>3</sup> + 2x<sup>2</sup> + 3x + 4 y b(x) = 3x<sup>2</sup> + 4x + 2 ∈ Z<sub>5</sub>. Calcular a(x) + b(x) y a(x) * b(x).

+ a(x) + b(x) = 3x<sup>4</sup> + 4x<sup>3</sup> + 2x + 1
+ a(x) * b(x) = 4x<sup>6</sup> + 4x<sup>5</sup> + 3x<sup>4</sup> + 3x<sup>2</sup> +2x + 3

---

## Grado de un polinomio

Sea a(x) = a<sub>0</sub> + a<sub>1</sub>x + ... + a<sub>n</sub>x<sup>n</sup> ∈ K[x] y a ≠ 0, diremos que a(x) es un polinomio de grado n, y lo denotaremos gr(a(x)) = n. Por definición, gr(0) = -INF.

### Proposición

Sean a(x) y b(x) ∈ a K[x], entonces, gr(a(x) * b(x)) = gr(a(x)) + gr(b(x)).

---

## Unidades

Un elemento a de un anillo (A, +, \*) es una unidad si tiene inverso para el producto. Si (K, +, \*) es un cuerpo, entonces, U(K) = K - {0}.

#### Ejercicio

Calcular las unidades de Z, Z<sub>5</sub> y Z<sub>6</sub>.

+ U(Z) = {1, -1}
+ U(Z<sub>5</sub>) = {1, 2, 3, 4}
+ U(Z<sub>6</sub>) = {1, 5}

### Proposición

Las unidades de K[x] son lo polinomios de grado 0, es decir, K - {0}.

#### Ejercicio

Calcular las unidades de Z<sub>5</sub>[x].

U( Z<sub>5</sub>[x] ) = {1, 2, 3, 4}

---

## Polinomios irreducibles y polinomios mónicos

Un polinomio a(x) ∈ K[x] es irreducible si verifica:
- gr(a(x)) ≥ 1
- Si a(x) = b(x) * c(x) entonces 0 ∈ {gr(b(x)), gr(c(x))}

### Proposición

- Todo polinomio de K[x] de grado 1 es irreducible.
- Si a(x) ∈ K[x], u ∈ K - {0} y a(x) es irreducible, entonces u*a(x) es también irreducible.

---

Un polinomio diremos que es mónico si el coeficiente del término de mayor grado vale 1.

## Descomposición en irreducibles de un polinomio

### Teorema

Todo polinomio a(x) ∈ K[x] de grado mayor o igual que 1 se puede poner de forma única como a(x) = u*p<sub>1</sub>(x)<sup>α<sub>1</sub></sup> * ... * p<sub>r</sub>(x)<sup>α<sub>r</sub></sup>, donde u ∈ K - {0}, α<sub>1</sub>, ..., α<sub>r</sub> ∈ N - {0} y p<sub>1</sub>(x), ..., p<sub>r</sub>(x) son polinomios mónicos e irreducibles.

---

A la expresión a(x) = u*p<sub>1</sub>(x)<sup>α<sub>1</sub></sup> * ... * p<sub>r</sub>(x)<sup>α<sub>r</sub></sup> la llamaremos la descomposición en irreducibles del polinomio a(x).

#### Ejercicio

Calcular la descomposición en irreducibles de los polinomios a(x) = (4x + 3)(3x + 2) ∈ Z<sub>5</sub>[x] y b(x) = (2x + 3)(3x + 2)(4x + 1).

+ a(x) = 5(x + 6)(x + 3)
+ b(x) = 4(x + 4)<sup>3</sup>

---

## Definición de divisor

Sean a(x) y b(x) ∈ K[x], diremos que a(x) divide a b(x) o que b(x) es un múltiplo de a(x) o que a(x) es un divisor de b(x) y lo denotaremos a(x) | b(x) si existe c(x) ∈ K[x] tal que b(x) = a(x) * b(x).

---

## Máximo común divisor

Sean a(x) y b(x) ∈ K[x] tal que a(x) ≠ 0 ó b(x) ≠ 0. Un polinomio d(x) ∈ K[x] diremos que es un máximo común divisor de a(x) y b(x) si verifica:

+ d(x) | a(x) y d(x) | b(x)
+ Si c(x) | a(x) y c(x) | b(x), entonces c(x) | d(x)

Si d(x) es un máximo común divisor de a(x) y b(x) y u ∈ K - {0}, entonces u*d(x) es también un máximo común divisor de a(x) y b(x). Denotaremos como mcd{ a(x), b(x) } al único máximo común divisor que es mónico.

#### Ejercicio

Sea a(x) y b(x) ∈ Z<sub>5</sub>[x] y 3x<sup>2</sup> + x + 1 es un máximo común divisor de a(x) y b(x). Calcule todos los máximos comunes divisores de a(x) y b(x) y calcule el mcd{ a(x), b(x)}.

---

## Mínimo común múltiplo

Sean a(x) y b(x) ∈ K[x]. Un polinomio m(x) ∈ K[x] diremos que es un mínimo común múltiplo de a(x) y b(x) si verifica:

+ a(x) | m(x) y b(x) | m(x)
+ Si a(x) | c(x) y b(x) | c(x), entonces m(x) | c(x)

Si m(x) es un mínimo común múltiplo de a(x) y b(x) y u ∈ K - {0}, entonces u*m(x) es también un mínimo común múltiplo de a(x) y b(x). Denotaremos como mcm{ a(x), b(x) } al único mínimo común múltiplo que es mónico.

---

### Teorema

Sean a(x) = u*p<sub>1</sub>(x)<sup>α<sub>1</sub></sup> * ... * p<sub>r</sub>(x)<sup>α<sub>r</sub></sup> y b(x) = v*p<sub>1</sub>(x)<sup>β<sub>1</sub></sup> * ... * p<sub>r</sub>(x)<sup>β<sub>r</sub></sup> tal que a(x), b (x) ∈ K[x], u, v  ∈ K - {0}, { α<sub>1</sub>, ..., α<sub>r</sub>, β<sub>1</sub>, ..., β<sub>r</sub> } ∈ n y p<sub>1</sub>(x), ..., p<sub>r</sub>(x) son polinomios mónicos e irreducibles, entonces:

+ mcd{ a(x). b(x) } = p<sub>1</sub><sup>min{ α<sub>1</sub>, β<sub>1</sub> }</sup> \* ... \* p<sub>1</sub><sup>min{ α<sub>1</sub>, β<sub>1</sub> }</sup>
+ mcm{ a(x). b(x) } = p<sub>1</sub><sup>max{ α<sub>1</sub>, β<sub>1</sub> }</sup> \* ... \* p<sub>1</sub><sup>max{ α<sub>1</sub>, β<sub>1</sub> }</sup>

#### Ejercicio

Sea a(x) = ( x + 1 )( 2x + 3 ) y b(x) = ( x + 2 )( 4x + 1 ) de Z<sub>5</sub>[x]. Calcular el mcd{ a(x), b(x) } y el mcm{ a(x), b(x) }.

---

## Propiedad de la división

Si a(x) y b(x) ∈ K[x] y b(x) ≠ 0, entonces existen unos únicos polinomios q(x) y r(x) ∈ K[x] tal que a(x) = q(x) * b(x) + r(x) y gr( r(x) ) < gr ( b(x) ). A q(x) y r(x) los llamaremos el cociente y el resto de dividir a(x) entre b(x) y los denotaremos a(x) div b(x) y a(x) mod b(x) respectivamente.

#### Ejercicio

Sean a(x) = 3x<sup>3</sup> + 4x<sup>2</sup> + 2x + 3 y b(x) = 2x<sup>2</sup> + 2x + 1 dos polinomios de Z<sub>5</sub>[x]. Calcular a(x) div b(x) y a(x) mod b(x).

---

## Algoritmo de Euclides

+ **ENTRADA**: a(x), b(x) ∈ K[x] - {0}
+ **SALIDA**: Un máximo común divisor de a(x) y b(x)

( a<sub>0</sub>(x), a<sub>1</sub>(x) ) = ( a(x), b(x) )  
Mientras a<sub>1</sub>(x) ≠ 0  
( a<sub>0</sub>(x), a<sub>1</sub>(x) ) = ( a<sub>1</sub>(x), a<sub>0</sub>(x) mod a<sub>1</sub>(x) )  
Cuando a<sub>1</sub>(x) = 0  
Devuelve a<sub>0</sub>(x)

### Proposición

Si d(x) es un máximo común divisor de a(x) y b(x), entonces ( a(x) * b(x) ) div d(x) es un mínimo común múltiplo de a(x) y b(x).

#### Ejercicio

Calcular un máximo común divisor y un mínimo común múltiplo de los polinomios a(x) = x<sup>4</sup> + x + 1 y b(x) = 3x<sup>2</sup> + x + 4 en Z<sub>5</sub>[x].

#### Ejercicio

Sea a(x) = 5x<sup>4</sup> + 3x<sup>3</sup> + 2<sup>2</sup> + 4x + 1 y b(x) = 4x<sup>2</sup> + 5x + 2 de Z<sub>7</sub>[x]. Calcular el cociente y el resto de dividir a(x) entre b(x).

---
