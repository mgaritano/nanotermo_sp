(entropy)=
## **_B_** _Entropía_

El propósito de este apéndice es hacer ver que la naturaleza de la entropía es diferente a la de otras variables extensivas
{cite}`hill, entropy`. Para ello, partimos de la ecuación de Boltzmann presentada en la introducción: $S = k_{\mathrm{B}}\ln\Omega$. Supongamos que disponemos de un conjunto que consta de $\mathscr{N}$ sistemas, los cuales los dividiremos en $n$ estados cuánticos. Cada uno de ellos contendrá $\mathscr{N}_{i}$ sistemas. Por lo tanto, $\sum_{i=1}^{n} \mathscr{N}_{i} = \mathscr{N}$ . También definiremos la expresión $p_{i} = \mathscr{N}_{i}/\mathscr{N}$, el cual representa la probabilidad de que una partícula se encuentre en el estado $i$. Como todas las variables son equivalentes, libres y distinguibles, el número de microestados sigue la expresión


$$
\Omega = \frac{\mathscr{N} !}{\mathscr{N} _ {1}!\cdot ... \cdot \mathscr{N}_{n}!} \; .
$$ (omega_ent)

Si aceptamos que el número de réplicas cumple  $\mathscr{N}\rightarrow\infty$, podremos hacer uso de la aproximación de Stirling: $\ln \mathscr{N}! \approx \mathscr{N}\ln\mathscr{N} - \mathscr{N}$. Por lo tanto,

$$
\ln\Omega \approx \mathscr{N}\ln\mathscr{N} - \sum_{i=1}^{n}\mathscr{N} _ {i}\ln\mathscr{N}_{i} \; .
$$ (ln_omega_ent)

Si realizamos las operaciones pertinentes, llegaremos a una expresión equivalente para la entropía:

$$
 S_{t} = -\mathscr{N}k_{\mathrm{B}}\sum_{i=1}^{n}\frac{\mathscr{N}_ {i}}{\mathscr{N}}\ln \left(\frac{\mathscr{N}_ {i}}{\mathscr{N}}\right) = \mathscr{N}\left(-k_{\mathrm{B}}\sum_{i=1}^{n}p_{i}\ln p_{i}\right) = \mathscr{N}S \; .
 $$ (entropy_def)

De la ecuación que acabamos de obtener se pueden sacar dos conclusiones principales: la magnitud $S$ de las réplicas es _acumulativa_ (extensiva), pero, sin embargo no representa el promedio de una propiedad mecánica. De hecho, no es posible asignar una determinada entropía a un solo estado cuántico, puesto que ésta es dependiente de la distribución de probabilidades a través de todos los sistemas pequeños.

Como sugiere la propia ecuación, si el número de microestados compatibles con el macroestado fuera alto, la distribución de probabilidad sería lo suficientemente uniforme, es decir, la disponibilidad de un microestado (o algunos) en particular no prevalecería sobre la de los demás. Así, todos los $p_{i}$ serían extremadamente pequeños y, por tanto, sus logaritmos serían enormes en módulo, pero por debajo de cero, reforzando el aumento de entropía. Por el contrario, si solo se permitieran unos pocos estados, la entropía total $S_{t}$ disminuiría $(p_{i}\rightarrow 1)$, aumentando el orden estadístico del sistema y, a fin de cuentas, la previsibilidad del conjunto de sistemas.

Considerando lo mencionado, sugerir que cada subsistema tiene una cierta entropía alrededor de un valor promedio de $\overline{S}$ es inconsistente con el carácter de esta magnitud.

