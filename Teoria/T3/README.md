# Tema 3: El anillo de los polinomios

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

Sea a(x) = a<sub>0</sub> + a<sub>1</sub>x + ... + a<sub>n</sub>x<sup>n</sup> ∈ K[x] y a ≠ 0, diremos que a(x) es un polinomio de grado n, y lo denotaremos gr(a(x)) = n. Por definición, gr(0) = -INF.

### Proposición

Sean a(x) y b(x) ∈ a K[x], entonces, gr(a(x) * b(x)) = gr(a(x)) + gr(b(x)).

---

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

U(Z<sub>5</sub>[x]) = {1, 2, 3, 4}

---

Un polinomio a(x) ∈ K[x] es irreducible si verifica:
- gr(a(x)) ≥ 1
- Si a(x) = b(x) * c(x) entonces 0 ∈ {gr(b(x)), gr(c(x))}

### Proposición

- Todo polinomio de K[x] de grado 1 es irreducible.
- Si a(x) ∈ K[x], u ∈ K - {0} y a(x) es irreducible, entonces u*a(x) es también irreducible.

---

Un polinomio diremos que es mónico si el coeficiente del término de mayor grado vale 1.

### Teorema

Todo polinomio a(x) ∈ K[x] de grado mayor o igual que 1 se puede poner de forma única como a(x) = u*p<sub>1</sub>(x)<sup>α<sub>1</sub></sup> * ... * p<sub>r</sub>(x)<sup>α<sub>r</sub></sup>, donde u ∈ K - {0}, α<sub>1</sub>, ..., α<sub>r</sub> ∈ N - {0} y p<sub>1</sub>(x), ..., p<sub>r</sub>(x) son polinomios mónicos e irreducibles.

---

A la expresión a(x) = u*p<sub>1</sub>(x)<sup>α<sub>1</sub></sup> * ... * p<sub>r</sub>(x)<sup>α<sub>r</sub></sup> la llamaremos la descomposición en irreducibles del polinomio a(x).

### Ejercicio

Calcular la descomposición en irreducibles de los polinomios a(x) = (4x + 3)(3x + 2) ∈ Z<sub>5</sub>[x] y b(x) = (2x + 3)(3x + 2)(4x + 1).

+ a(x) = 5(x + 6)(x + 3)
+ b(x) = 4(x + 4)<sup>3</sup>

---

Sean a(x) y b(x) ∈ K[x], diremos que a(x) divide a b(x) o que b(x) es un múltiplo de a(x) o que a(x) es un divisor de b(x) y lo denotaremos a(x) | b(x) si existe c(x) ∈ K[x] / b(x) = a(x) * b(x).
