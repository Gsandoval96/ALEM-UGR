# **Tema 1: Conjuntos, relaciones y aplicaciones**

# Conjuntos

Un conjunto es una colección de objetos a los que llamaremos elementos del conjunto. Si x es un elemento de un conjunto A, diremos que x ∈ A. Diremos que un conjunto A es un **subconjunto** de un conjunto B, y lo denotaremos A ⊆ B, si todo elemento a ∈ A también pertenece a B. Dos conjuntos A y B son **iguales**, y lo denotaremos A = B, si A ⊆ B y B ⊆ A. Admitiremos la existencia de un conjunto sin elementos llamado el **conjunto vacío**, y lo denotaremos con ø. El conjunto vacío es subconjunto de cualquier conjunto.

#### Ejemplo
+ **A = { 1, 2, 3, 4, 5 }**
+ 1 ∈ A  ✓
+ 7 ∈ A ✗
+ {1} ⊆ A  ✓
+ {1,7} ⊆ A ✗
+ 0 ⊆ A  ✓
+ 0 ∈ A ✗
+ {2} ∈ A ✗
+ 2 ≠ {2} ✓
---

## Operaciones con conjuntos

Sean A y B dos conjuntos:

1. La **intersección** de A y B es A∩B = { x ∈ A & x ∈ B }.
2. La **unión** de A y B es A∪B = { x ∈ A | x ∈ B }.
3. La **diferencia** de A y B es A\B = { x ∈ A tal que x ∉ B}.
4. El **conjunto partes** de A o conjunto potencia es P(A) = { X tal que X ⊆ A }.
5. El **producto cartesiano** de A y B es AxB = { (a,b) tal que a ∈ A y b ∈ B}.
6. Si A<sub>1</sub>, A<sub>2</sub>, ..., A<sub>n</sub> son conjuntos, el producto cartesiano de todos ellos A<sub>1</sub> x A<sub>2</sub> x ... x A<sub>n</sub> = { a<sub>1</sub>, a<sub>2</sub>, ..., a<sub>n</sub> } tal que a<sub>1</sub> ∈ A<sub>1</sub>, a<sub>2</sub> ∈ A<sub>2</sub>, ..., a<sub>n</sub> ∈ A<sub>n</sub> }. A los elementos de este conjunto se les llama n-tuplas.
7. Al conjunto A x A x ... x A n-veces lo denotaremos A<sup>n</sup>.

#### Ejemplo
+ **A = { 1, 2, 3, 4, 5 }, B = { 2, 4, 6, 7 }**
+ A∩B = { 2, 4 }
+ A∪B = { 1, 2, 3, 4, 5, 6, 7 }
+ A\B = { 1, 3, 5 }
+ B\A = { 6, 7 }
+ P({1, 2, 3}) = [ {1}, {2}, {3}, {1,2}, {2,3}, {1,3}, {1,2,3}, 0 ]
+ P(0) = {0}
+ {1,2,3} X {2,4} = { (1,2), (1,4), (2,2), (2,4), (3,2), (3,4) }
+ {1,2}<sup>3</sup> = {(1,1,1), (1,1,2), (1,2,1), (1,2,2), (2,1,1), (2,1,2), (2,2,1), (2,2,2) }
---

## Cardinal de un conjunto

El **cardinal** de un conjunto es el número de elementos de dicho conjunto y lo denotaremos #A.

### Proposición

+ Si A es un conjunto, entonces #P(A) = 2<sup>#A</sup>
+ Sean A<sub>1</sub>, A<sub>2</sub>, ..., A<sub>n</sub> conjuntos, entonces el cardinal #( A<sub>1</sub> x A<sub>2</sub> x ... x A<sub>n</sub> ) = #A<sub>1</sub> x #A<sub>2</sub> x ... x #A<sub>n</sub>

---

# Relaciones

## Relaciones de equivalencia

Sea A un conjunto. Una relación binaria sobre el conjunto A es un subconjunto R de de AxA. Si ( x, y ) ∈ R, escribiremos xRy y diremos que x está relacionado con y.

#### Ejemplo
+ **A = { 1, 2, 3, 4, 5 }, R = { (1,1), (1,2), (3,4), (5,2), (3,1), (4,2) }**
+ R es una relación binaria del conjunto A
+ 1 R 2 ✓
+ 1 R 5 ✗

Una relación binaria R sobre un conjunto A diremos que es una **relación binaria de equivalencia** si verifica las siguientes propiedades:

+ **Reflexiva**: si a ∈ A, entonces aRa.
+ **Simétrica**: si aRb, entonces bRa.
+ **Transitiva**: si aRb y bRc, entonces aRc.

#### Ejemplo
+ **A = { 1, 2, 3, 4, 5 }, R = { (1,1), (2,2), (3,3), (4,4), (5,5), (1,2), (2,1), (3,4), (4,3) }**
+ Es reflexiva
+ Es simétrica
+ Es transitiva

Si R es una relación de equivalencia sobre un conjunto A y a ∈ A, entonces la **clase del elemento** a se denota [a] = { x ∈ A tal que xRa }. El **conjunto cociente** se denota A/R = { [a] tal que a ∈ A }.

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

Algunas relaciones de orden son:

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

---

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

---

## Representación gráfica de órdenes

Dados dos elementos a y b, a ≤ b si existe un camino siempre ascendente que conecta a y b.

---

# Aplicaciones

Sean A y B dos conjuntos, una aplicación f de A en B, que denotaremos f:A->B, es una correspondencia que a cada elemento del conjunto A le asocia un único elemento del conjunto B. Si a ∈ A, entonces al elemento que f le asocia B lo denotaremos f(a) y diremos que es la imagen del elemento a. A los conjuntos A y B los llamaremos el dominio y codominio de f respectivamente. Llamaremos imagen de f a Im(f) = { f(a) tal que a ∈ A }.

## Tipos de aplicaciones

Una aplicación f:A->B es:
+ **Inyectiva**: si f(x) = f(y), entonces x = y.
+ **Sobreyectiva**: si Im(f) = B, para demostrar que f es sobreyectiva basta con ver que B ⊆ Im(f), ya que siempre se tiene que la Im(f) ⊆ B.
+ **Biyectiva**: si es inyectiva y sobreyectiva.

#### Ejercicio

Estudiar la biyectividad de las siguientes aplicaciones:
+ f:N->Z tal que f(x) = x - 5
+ f:Z->N tal que f(x) = x<sup>2</sup>
+ f:Q->Q tal que f(x) = (2x + 1) / 3

---

## Composición de Aplicaciones

Sea f:A->B y g:B->C dos aplicaciones, llamaremos **aplicación composición** de f y g a la aplicación gof:A->C y está definida por gof(a) = g( f(a) ).

#### Ejercicio

Sea f:Z->N tal que f(x) = x<sup>2</sup> y g(y) = ( 2y + 3 ) / 7, calcular la gof.

### Proposición

La composición de aplicaciones es asociativa, pero no es conmutativa.

Que la composición de aplicaciones es asociativa significa que si tenemos f:A->B, g:B->C y h:C->D, entonces ho(gof) = (hog)of.

Que la composición de aplicaciones no es conmutativa significa que si tenemos f:A->A y g:A->A, no implica que gof = fog.

---

## Aplicación identidad

Sea A un conjunto, llamaremos **aplicación identidad** sobre el conjunto a 1<sub>A</sub>:A->A tal que 1<sub>A</sub>(a) = a.

---

## Aplicación inversa

### Proposición

Si f:A->B es una aplicación biyectiva, entonces existe una única aplicación g:B->A tal que gof = 1<sub>A</sub> y fog = 1<sub>B</sub>. A dicha aplicación la llamaremos la **inversa** de f y la denotaremos f<sup>-1</sup>.

#### Ejercicio

Dada la aplicación biyectiva f:Q->Q tal que f(x) = ( 2x +3 ) / 5, calcular su inversa.
