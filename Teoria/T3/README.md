# Tema 3: El anillo de los polinomios

Sea K un cuerpo, el conjunto de los polinomio con coeficientes en el cuerpo K y en la indeterminada x es K[x] = {a<sub>0</sub> + a<sub>1</sub>x + ... + a<sub>n</sub>x<sup>n</sup>} tal que n ∈ a N (el conjunto de los números naturales)
y {a<sub>0</sub>, a<sub>1</sub>, ..., a<sub>n</sub>} ∈ K.

### Proposición

(K[x], +, \*) es un anillo conmutativo donde + y * son las operaciones usuales de suma y producto de polinomios. Además, (K[x], +, \*) no es un cuerpo.

#### Ejercicio

Sean a(x) = 3x<sup>4</sup> + 4x<sup>3</sup> + 2x<sup>2</sup> + 3x + 4 y b(x) = 3x<sup>2</sup> + 4x + 2 ∈ Z<sub>5</sub>. Calcular a(x) + b(x) y a(x) * b(x).

---

Sea a(x) = a<sub>0</sub> + a<sub>1</sub>x + ... + a<sub>n</sub>x<sup>n</sup> ∈ K[x] y a ≠ 0, diremos que a(x) es un polinomio de grado n, y lo denotaremos gr(a(x)) = n. Por definición, gr(0) = -INF.

### Proposición

Sean a(x) y b(x) ∈ a K[x], entonces, gr(a(x) * b(x)) = gr(a(x)) + gr(b(x)).

---

Un elemento a de un anillo (A, +, \*) es una unidad si tiene inverso para el producto. Si (K, +, \*) es un cuerpo, entonces, U(K) = K - {0}.

#### Ejercicio

Calcular las unidades de Z, Z<sub>5</sub> y Z<sub>6</sub>.

### Proposición

Las unidades de K[x] son lo polinomios de grado 0, es decir, K - {0}.

#### Ejercicio

Calcular las unidades de Z<sub>5</sub>[x].

---

Un polinomio a(x) ∈ K[x] es irreducible si verifica:
- gr(a(x)) >= 1
- Si a(x) = b(x) * c(x) entonces 0 ∈ {gr(b(x)), gr(c(x))}
