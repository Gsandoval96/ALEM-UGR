# Tema 1: Conjuntos, relaciones y aplicaciones

Un conjunto es una colección de objetos a los que llamaremos elementos del conjunto. Si x es un elemento de un conjunto A, diremos que x ∈ A. Diremos que un conjunto A es un **subconjunto** de un conjunto B, y lo denotaremos A ⊆ B, si todo elemento a ∈ A también pertenece a B. Dos conjuntos A y B son **iguales**, y lo denotaremos A = B, si A ⊆ B y B ⊆ A. Admitiremos la existencia de un conjunto sin elementos llamado el **conjunto vacío**, y lo denotaremos con ø. El conjunto vacío es subconjunto de cualquier conjunto.

---

## Operaciones con conjuntos

Sean A y B dos conjuntos:

1. La **intersección** de A y B es A∩B = { x ∈ A & x ∈ B }.
2. La **unión** de A y B es A∪B = { x ∈ A | x ∈ B }.
3. La **diferencia** de A y B es A\B = { x ∈ A / x ∉ B}.
4. El **conjunto partes** de A o conjunto potencia es P(A) = { X / X ⊆ A }.
5. El **producto cartesiano** de A y B es AxB = { (a,b) / a ∈ A y b ∈ B}.
6. Si A<sub>1</sub>, A<sub>2</sub>, ..., A<sub>n</sub> son conjuntos, el producto cartesiano de todos ellos A<sub>1</sub> x A<sub>2</sub> x ... x A<sub>n</sub> = { a<sub>1</sub>, a<sub>2</sub>, ..., a<sub>n</sub> } / a<sub>1</sub> ∈ A<sub>1</sub>, a<sub>2</sub> ∈ A<sub>2</sub>, ..., a<sub>n</sub> ∈ A<sub>n</sub> }. A los elementos de este conjunto se les llama n-tuplas.
7. Al conjunto A x A x ... x A n-veces lo denotaremos A<sup>n</sup>.

---

El cardinal de un conjunto es el número de elementos de dicho conjunto y lo denotaremos #A.

### Proposición

+ Si A es un conjunto, entonces #P(A) = 2<sup>#A</sup>
+ Sean A<sub>1</sub>, A<sub>2</sub>, ..., A<sub>n</sub> conjuntos, entonces el cardinal #( A<sub>1</sub> x A<sub>2</sub> x ... x A<sub>n</sub> ) = #A<sub>1</sub> x #A<sub>2</sub> x ... x #A<sub>n</sub>

---

## Relaciones de equivalencia

Sea A un conjunto. Una relación binaria sobre el conjunto A es un subconjunto R de de AxA. Si ( x, y ) ∈ R, escribiremos xRy y diremos que x está relacionado con y.

Una relación binaria R sobre un conjunto A diremos que es una **relación binaria de equivalencia** si verifica las siguientes propiedades:

+ **Reflexiva**: si a ∈ A, entonces aRa.
+ **Simétrica**: si aRb, entonces bRa.
+ **Transitiva**: si aRb y bRc, entonces aRc.

Si R es una relación de equivalencia sobre un conjunto A y a ∈ A, entonces la **clase del elemento** a se denota [a] = { x ∈ A / xRa }. El **conjunto cociente** se denota A/~ = { [a] / a ∈ A }.

#### Ejercicio

Sean A = { 1, 2, 3, 4, 5 } y R = { (1,1), (1,2), (3,4), (5,2), (3,1), (4,2) }, calcular el conjunto cociente.

---

### Proposición

Sea R una relación de equivalencia sobre un conjunto A:
+ Si aRb, entonces [a] = [b]
+ Si a~~R~~[b, entonces [a]∩[b] = ø

#### Ejercicio

En el conjunto Z = { 0, 1, -1, 2, -2, ... }, el conjunto de los números enteros, definimos la relación binaria aRb si b-a es múltiplo de 3:

1. Demuestra que R es una relación de equivalencia.
2. Calcular [0].
3. Calcular el cardinal del conjunto cociente.

---

## Relaciones de orden

Una relación binaria ≤ sobre un conjunto A diremos que es una **relación de orden** si verifica:

+ **Reflexiva**: si a ∈ A, entonces a≤a.
+ **Antisimétrica**: si a≤b, entonces b≤a.
+ **Transitiva**: si a≤b y b≤c, entonces a≤c.

Algunas relaciones de equivalencia son:

+ ≤<sub>u</sub> orden usual del conjunto N
+ ≤<sub>m</sub> orden ser múltiplo
+ ≤<sub>i</sub> orden inclusión

#### Ejercicio

Demostrar que ≤<sub>m</sub> es una relación de orden.

---

Una relación de orden ≤ sobre un conjunto A diremos que es una **relación de orden total** si verifica:

+ Si ( a, b ) ∈ AxA, entonces a ≤ b ó b ≤ a

#### Ejercicio

Demostrar que las siguientes relaciones son relaciones de orden total.

1. ( N, ≤<sub>u</sub> )
2. ( N, ≤<sub>m</sub> )

## Elementos notables de un conjunto ordenada

Sea ( A, ≤ ) un conjunto ordenado y B ⊆ A:

1. **MAXIMALES**: un elemento β ∈ B diremos que es un MAXIMAL de B si verifica: b ∈ B y β ≤ b, entonces β = b.
2. **MÁXIMO**: un elemento β ∈ B diremos que es el MÁXIMO de B si verifica: b ≤ β ∀ b ∈ B.
3. **MINIMALES**: un elemento β ∈ B diremos que es un MINIMAL de B si verifica: b ∈ B y b ≤ β, entonces b = β.
4. **MÍNIMO**: un elemento β ∈ B diremos que es el MÍNIMO de B si verifica: β ≤ b ∀ b ∈ B.
5. **COTAS SUPERIORES**: un elemento a ∈ A diremos que es una COTA SUPERIOR de B si b ≤ a ∀ b ∈ B.
6. **SUPREMO**: el SUPREMO de B es el mínimo del conjunto formado por todas las cotas superiores de B.
7. **COTAS INFERIORES**: un elemento a ∈ A diremos que es una COTA INFERIOR de B si a ≤ b ∀ b ∈ B.
8. **ÍNFIMO**: el ÍNFIMO de B es el máximo del conjunto formado por todas las cotas inferiores de B.

#### Ejercicio

Dado el conjunto ordenado ( N, ≤<sub>m</sub> ) y B = { 1, 2, 3, 4, 5 }, calcular los elementos notables de B.
