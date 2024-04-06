(euler)=
## **_A_** _Ecuación de Euler_

Una función homogénea del orden $ k $ satisface la siguiente expresión:

$$
f(\lambda x_{1},...,\lambda x_{n}) = \lambda^{k}f(x_{1},...,x_{n}), \; \; \forall x_{1},...,x_{n} \; \textrm{eta} \; \lambda \neq 0 \; .
$$ (f_def)

Siguiendo el libro de Callen {cite}`callen`, las ecuaciones fundamentales de un sistema macroscópico son funciones homogéneas de **primer orden**. Esto posibilita escribir la expresiones de una manera muy útil, esto es, en la _forma de Euler_. Para resumir la explicación, supongamos que la energía interna es solo función de la entropía y el volumen. En este caso, tomando cualquier $\lambda$, y $k = 1$, la forma mencionada sería la siguiente:


$$
E(\lambda S, \lambda V) = \lambda E(S, V) \; .
$$ (e_euler)

Al derivar esta ecuación, tendríamos

$$
\frac{\partial E(\lambda S, \lambda V)}{\partial (\lambda S)}\frac{\partial(\lambda S)}{\partial \lambda} + \frac{\partial E(\lambda S, \lambda V)}{\partial (\lambda V)}\frac{\partial(\lambda V)}{\partial \lambda} = E(S,V) \; .
$$ (euler_2)

En concreto, tomando $\lambda = 1$, 

$$
 \frac{\partial E(S,  V)}{\partial S}S + \frac{\partial E(S, V)}{\partial V}V = E(S,V) \; .
$$ (euler_3)

O bien, sustituyendo las variables conjugadas de $S$ y $V$,

 $$
 \boxed{E(S, V) = TS - pV} \; .
 $$ (euler_4)

La presión y la temperatura, al ser de orden cero, cumplirán

 $$
 f(\lambda S, \lambda V) = \lambda^{0}f(S, V) = f(S, V) \; .
 $$ (euler_5)

En otras palabras, son funciones intensivas.
