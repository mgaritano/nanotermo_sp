(elek_mag)=
## Sistemas eléctricos y magnéticos

Los dos primeros apartados están orientados a la reexaminación de dos sistemas previamente trabajados, a los que añadiremos efectos eléctricos. Primeramente, vamos deformar el sistema de "hélice-ovillo" del {numref}`ejemplo {number} <helix_coil>`, añadiendo a cada lado dos cargas de signo opuesto. A continuación, abordaremos el agregado lineal que figura en el {numref}`ejemplo {number}<mupt_linagg>`, y consideraremos cada uno de los constituyentes como un dipolo eléctrico con orientación aleatoria a la dirección $z$. En ambos casos, los sitemas se implantarán bajo la influencia de un campo eléctrico externo, para seguidamente acometer su estudio termodinámico.

En la tercera parte abordaremos la cadena unidimensional de Ising, con la que trabajaremos principalmente en el conjunto nanocanónico,
el cual nos permitirá alcanzar el equilibrio térmico correspondiente a la distribución del conjunto.

(heco_elek)=
### Transición hélice-ovillo, bajo infulencia del campo externo $\mathbf{E}$ 

Al analizar los sistemas eléctricos, trabajaremos con un nuevo par de variables: el campo eléctrico $\mathbf {E} $ y su conjugado extensivo: el momento dipolar eléctrico del sistema, $\mathbf {p} $. Así las cosas, en este ejemplo tendremos como objeto de estudio la cadena "hélice-ovillo" modificada de la {numref}`figura {number} <heco>`, la cual se muestra en {numref}`figura {number} <heco_e>`.


```{figure} heco_efield.jpg
---
height: 200px
name: heco_e
---
  Hemos añadido cargas $\pm q $ en cada extremo a la cadena "hélice-ovillo". Por ello, a través de la cadena emergerá el momento dipolar eléctrico $\vert\mathbf {p}\vert = ql $, siendo $l$ la longitud de la cadena. Asimismo, asignaremos a cada unidad de hélice y ovillo la polarizabilidad $\alpha $. Pues bien, al establecer el campo eléctrico $\mathbf {E} $ $(\mathbf {E}\parallel\mathbf {p})$, ambos factores nuevos conllevarán a un aporte energético para el sistema, como se detalla a continuación.
```

Pues bien, si tomamos $q,\vert\mathbf {E}\vert > 0 $, el campo eléctrico aumentará la longitud de la cadena, es decir, acentuará la transición de fase hélice-ovillo. Recordemos que en el {numref}`ejemplo {number} <helix_coil>` aceptamos que las unidades de ovillo son más largas que las unidades de hélice $(l_C>l_H)$. Por ello, en el límite $\vert\mathbf {E}\vert\rightarrow\infty $, podemos predecir que la magnitud $\overline {n} _H/N $ tenderá cero.


$$
\\
$$


Iniciando el análisis termodinámico del sistema, el conjunto de variables ambientales disponibles en el conjunto canónico es $(T, l, N,\vert\mathbf {E}\vert) $. Por lo tanto, para construir la función de partición $Q (T, l, N,\vert\mathbf {E}\vert)$, debemos computar las contribuciones a la energía interna de los factores adicionales que aparecen en la {numref}`figura {number} <heco_e>`, los cuales designaremos como $U_p$ y $U_{\alpha}$, siendo

$$
U_{p} = - \mathbf{p}\cdot \mathbf{E} = -lq\vert\mathbf{E}\vert \; ,
$$ (u_p_heco)

y,

$$
U_{\alpha} = N\left(-\int_0^{\vert\mathbf{E}\vert} \mathrm{d}\vert\mathbf{E}\vert^{\prime} \; \alpha\vert\mathbf{E}\vert^{\prime} \right) = -\frac{1}{2}N\alpha \vert\mathbf{E}\vert^2 \; .
$$ (u_alpha_heco)

Así, partiendo de la expresión $Q (T, l, N) $ del ejemplo original, la nueva función de partición será

$$
Q(T,l,N,\vert\mathbf{E}\vert) = Q(T,l,N)\cdot Q_p\cdot Q_{\alpha} = Q(T,l,N)\exp\left(\frac{lq\vert\mathbf{E}\vert}{k_{\mathrm{B}}T}\right)\exp\left(\frac{N\alpha\vert\mathbf{E}\vert^2}{2k_{\mathrm{B}}T}\right) \; .
$$ (heco_e_q)

Teniendo eso en cuenta, pasaremos a la colectividad isotérmica-isobárica:

$$
\Delta(T,f,N,\vert\mathbf{E}\vert) = \sum_{l}Q(T,l,N,\vert\mathbf{E}\vert)\;e^{fl/k_{\mathrm{B}}T} = \exp\left(\frac{N\alpha\vert\mathbf{E}\vert^2}{2k_{\mathrm{B}}T}\right)\sum_{l}Q(T,l,N)\;e^{(q\vert\mathbf{E}\vert+f)l/k_{\mathrm{B}}T} \; ,
$$ (heco_e_delta)

o bien,

$$
\Delta(T,f,N,\vert\mathbf{E}\vert) = \exp\left(\frac{N\alpha\vert\mathbf{E}\vert^2}{2k_{\mathrm{B}}T}\right) \Delta(T,f + q\vert\mathbf{E}\vert,N) \; .
$$ (heco_e_delta_2)

Pues bien, si se mantenemos la aproximación empleada en el {numref}`ejemplo {number} <helix_coil>` (todas las unidades en el estado $H$ o todas las unidades en el estado $C$), el término $\Delta(T,f + q\vert\mathbf{E}\vert,N)$ de la expresión {eq}`heco_e_delta_2` se corresponderá con la función de partición de la ecuación {eq}`d_short`; es decir,


$$
\Delta(T,f,N,\vert\mathbf{E}\vert) = \exp\left(\frac{N\alpha\vert\mathbf{E}\vert^2}{2k_{\mathrm{B}}T}\right) \; r_C^N\left(1+r^N\right) \; .
$$ (heco_e_delta_3)

Eso sí, deberemos adaptar las magnitudes $r_C$, $r_H$ y $r$ al presente estudio:

$$
r_{C,H} = q_{C,H}\exp\left(l_{C,H}\frac{f+q\vert\mathbf{E}\vert}{k_{\mathrm{B}}T}\right) \quad , \quad r = \frac{r_H}{r_C} \; .
$$


De la ecuación {eq}`heco_e_delta_3` de arriba, adquiriremos los potenciales químicos $\widehat{\mu}$ y $\mu$:

$$
\widehat{\mu} = -\frac{1}{2}\alpha \vert\mathbf{E}\vert^2 - k_{\mathrm{B}}T\left[\ln r_{C} + \frac{1}{N}\ln\left(1+r^N\right)\right] \; ,
$$ (heco_e_muhat)

$$
\mu = - \frac{1}{2}\alpha \vert\mathbf{E}\vert^2 - k_{\mathrm{B}}T\left[\ln r_{C} + \frac{r^N\ln r}{1 + r^N}\right] \; .
$$ (heco_e_mu)

Observemos que, dado que la contribución a la energía de la polarizabilidad $\alpha $ es lineal respecto a $N $, la expresión del potencial de subdivisión no ha variado (ecuación {eq}`epsilonhelix`).

También resultará interesante calcular el promedio del momento dipolar del sistema:

$$
\overline{\vert\mathbf{p}\vert} := k_{\mathrm{B}}T\left(\frac{\ln\Delta}{\partial \vert\mathbf{E}\vert}\right)_{T,f,N} = N\alpha\vert\mathbf{E}\vert + q\left[Nl_C+\frac{r^{N+1}\ln r}{1+r^N}\left(l_H-l_C\right)\right] = N\alpha\vert\mathbf{E}\vert + q\bar{l} \, .
$$ (heco_e_pbar)

##### Ejercicio
Verifica que ambas partes de la ecuación {eq}`heco_e_pbar` son coincidentes. Para ello, construye la expresión de la longitud media $\bar{l}$ de la cadena.

```{dropdown} __Solución__

Atendiendo a la definición de $\overline{l}$,

$$
\bar{l} := k_{\mathrm{B}}T\left(\frac{\ln\Delta}{\partial f}\right)_{T,N, \vert\mathbf{E}\vert} \; .
$$ (heco_e_lbar)

Al realizar cálculos con la función de partición {eq}`heco_e_delta_3`, obtendremos la expresión entre corchetes de la ecuación {eq}`heco_e_pbar`.

```
**----------------------------------------------------**

Para culminar esta breve revisión, nos centraremos en la cuestión previamente mencionada. Sustituyendo la nueva definición de la magnitud $r$ en la ecuación {eq}`fraction_N` de la fracción media de las unidades de hélice, llegaremos a

$$
\frac{\overline{n}_H}{N} = \frac{\left[\frac{q_H}{q_C}\exp\frac{\left(l_H-l_C\right)\left(f+q\vert\mathbf{E}\vert\right)}{k_{\mathrm{B}}T}\right]^N}{1 + \left[\frac{q_H}{q_C}\exp\frac{\left(l_H-l_C\right)\left(f+q\vert\mathbf{E}\vert\right)}{k_{\mathrm{B}}T}\right]^N} \; .
$$ (heco_e_nbar)

Dado que se cumple que $l_H-l_C<0$, la fracción de unidades hélice tenderá a cero de forma exponencial, pues a medida que aumentamos el módulo del campo eléctrico $\mathbf{E}$, prevalecerá la fase del ovillo. En consecuencia, la fracción $\frac{\overline{n}_H}{N} $ acrecentará, y, al mismo tiempo, la longitud media de la cadena, reforzando el momento dipolar a través de ella.

(agg_elek)=
### Agregado lineal, bajo influencia del campo externo $\mathbf{E}$ 

Analicemos la {numref}`figura {number} <agg_e>` que tenemos debajo:

```{figure} aggregate_efield.jpg
---
height: 225px
name: agg_e
---
En el caso del agregado lineal, también añadiremos algunas modificaciones. Por un lado, al igual que en la {numref}`figura {number} <heco_e>`, hemos asignado a cada una de las unidades la polarizabilidad $\alpha $. Sin embargo, esta vez consideraremos cada uno de ellos como un dipolo eléctrico, con un momento dipolar $\mathbf {p_0} $; asimismo, el vector $\mathbf {p_0} $ y el eje que atraviesa la cadena no estarán alineados, sino que formarán un ángulo $\theta $. Así las cosas, se analizarán a continuación las aportaciones que generará la implantación externa de un campo eléctrico $\mathbf {E} $.
```

Dicho lo dicho, emprenderemos ahora la construcción de la función de paritición canónica $Q(T, N,\vert\mathbf {E}\vert)$. Para ello, por un lado, tomaremos en consideración las aportaciones presentadas en el {numref}`ejemplo {number} <mupt_linagg>`. Éstas quedan recogidas en la ecuación {eq}`qagg`, que incluye la función particional intrínseca $j (T) $ de los monomeros, la rotación del agregado y la interacción entre primeros vecinos:

$$
Q_0(T,N) = c(T)\;N^3j(T)^N\;e^{-N\epsilon/k_{\mathrm{B}}T} \quad (N\geq 1) \; .
$$ (agg_e_q0)

Además de eso, debemos también calcular el aporte eléctrico, atendiendo a la {numref}`figura {number} <agg_e>`. Considerando que el agregado contiene en su conjunto $N$ unidades, la contribución a la función de partición resultante de la polarizabilidad $\alpha $ es $Q_ {\alpha}$, procedente de la ecuación {eq}`u_alpha_heco` del apartado anterior. Pero en lo concerniente a la segunda aportación, dado que el momento intrínseco $\mathbf {p_0}$ por unidad y el campo externo $\mathbf {E} $ ya no son paralelos, el cálculo del segundo tema $Q_ {p}$ relacionado con ellos ya no es inmediato. De hecho, ahora tenemos que

$$
 U_{p_0}(\theta) = -Np_0\vert\mathbf{E}\vert \cos \theta \; .
$$ (agg_e_u_p0)


La cuestión es que debemos tener en cuenta la orientación del vector $\mathbf {p_0} $. Si no aplicaramos ningún campo externo, todas las orientaciones de este vector serían equiprobables en el espacio de coordenadas $(\theta,\varphi) $. Por ello, la probabilidad para que la orientación del momento se encuentre en el intervalo $\mathrm {d}\theta\;\mathrm {d}\varphi$ sería proporcional al ángulo sólido diferencial $\sin\theta\;\mathrm {d}\theta\;\mathrm {d}\varphi $. Sin embargo, al establecer un campo eléctrico, ciertas orientaciones determinadas prevalecerán frente a otras, debido a la energía de interacción $U_ {p_0} (\theta)$. Reflejaremos estos factores en la siguiente función de partición normalizada, integrando el factor de Boltzmann asociado a la energía de interacción a través del ángulo sólido diferencial:


$$
 Q_{p_0} = \frac{\int_0^{2\pi}\mathrm{d}\varphi\int_0^{\pi}\mathrm{d}\theta\;\sin \theta \; e^{-U_{p_0}(\theta)/k_\mathrm{B}T}}{\int_0^{2\pi}\mathrm{d}\varphi\int_0^{\pi}\mathrm{d}\theta\;\sin \theta} = \frac{1}{2}\int_0^{\pi}\mathrm{d}\theta\;\sin \theta \; \exp\left(\frac{Np_0\vert\mathbf{E}\vert \cos \theta}{k_\mathrm{B}T}\right) = \frac{\sinh (Ny)}{Ny} \; ,
$$ (agg_e_q_p0)

donde hemos sustituido $y = p_0\vert\mathbf{E}\vert/(k_\mathrm{B}T)$.

$$
\\
$$

Para aligerar los cálculos que prosiguen, consideraremos a partir de ahora el _límite del campo eléctrico pequeño_ $(\vert\mathbf {E}\vert \ll 1) $. Además de eso, tengamos en cuenta que el agregado lineal que tenemos entre manos es en sí un sistema _pequeño_, es decir, no trabajamos en el límite $N\rightarrow\infty $. Por esta razón, nos es lícito afirmar que $Ny\ll 1$. Así las cosas, escribamos la serie de la función $\sinh (Ny)$:

$$
\sinh(Ny) = \sum_{n=0}^{\infty}\frac{(Ny)^{2n+1}}{(2n+1)!} \; .
$$ (agg_e_sinh)


Siguiendo el razonamiento expuesto, emplearemos la siguiente aproximación:

$$
\frac{\sinh(Ny)}{Ny} = 1 + \frac{N^2y^2}{6} + \mathscr{O}\left[(Ny)^4\right] \; .
$$ (agg_e_approx)

En consecuencia, como la función de partición eléctrica y la del sistema son, respectivamente, $Q_1 = Q_{\alpha} \cdot Q_{p_0}$ y $Q(T,N,\vert\mathbf{E}\vert) = Q_0(T,N)\cdot Q_1(T,N,\vert\mathbf{E}\vert)$, llegaremos a esta expresión:

$$
\boxed{Q(T,N,\vert\mathbf{E}\vert) \approx c(T)\;N^3j(T)^N\exp\left(-\frac{N\epsilon}{k_{\mathrm{B}}T}\right) \exp\left(\frac{N\alpha \vert\mathbf{E}\vert^2}{2k_\mathrm{B}T}\right)\left[1 + \frac{1}{6}\left(\frac{Np_0\vert\mathbf{E}\vert}{k_\mathrm{B}T}\right)^2 \right]} \quad (N\geq 1) \; .
$$ (agg_q_tot)

$$
\\
$$

Partiendo de la ecuación {eq}`agg_q_tot`, vamos a calcular las magnitudes termodinámicas más relevantes en la  **colectividad canónica**.

##### Ejercicio

$(a)$ Calcula los potenciales $\widehat{\mu}$ y $\mu$, y el límite $\mu^{(0)}$. Junto a ellos, escribe la expresión del potencial de subdivisión.

```{dropdown} __Solución__

$$
\left.\begin{array}{l}
\frac{\widehat{\mu}}{k_{\mathrm{B}}T} = -\frac{\ln Q}{N} = -\ln j + \frac{N-1}{N} \frac{\epsilon}{k_{\mathrm{B}}T} - \frac{\ln(\xi N^3)}{N} - \frac{\alpha \vert\mathbf{E}\vert^2}{2k_\mathrm{B}T} - \frac{1}{N}\ln\left(1 + \frac{N^2y^2}{6}\right) \\\\
\frac{\mu}{k_{\mathrm{B}}T} = -\ln j + \frac{\epsilon}{k_{\mathrm{B}}T} - \frac{3}{N} - \frac{\alpha \vert\mathbf{E}\vert^2}{2k_\mathrm{B}T} - \frac{2Ny^2}{6+N^2y^2}
\end{array}\right\}\underset{(N \rightarrow \infty)}{\boldsymbol{\longrightarrow}} \; \frac{\mu^{(0)}}{k_{\mathrm{B}}T} = -\ln j + \frac{\epsilon}{k_{\mathrm{B}}T} - \frac{\alpha \vert\mathbf{E}\vert^2}{2k_\mathrm{B}T} 
$$ (agg_elek_mu)

$$
\frac{\mathscr{E}(T,N)}{k_\mathrm{B}T} = \frac{N(\widehat{\mu}-\mu)}{k_\mathrm{B}T} = -\frac{\epsilon}{k_\mathrm{B}T} + 3  -\ln(\xi N^3) - \ln\left(1+\frac{N^2y^2}{6}\right)  + \frac{2N^2y^2}{6+N^2y^2}
$$ (agg_elek_epsilon_k)

```


$(b)$ Calcula la expresión $S(T,N,\vert\mathbf{E}\vert)$ de la entropía. De ahí, obtén la ecuación macroscópica $S^{(0)}$ y el término de exceso $S^{(x)}(T,N,\vert\mathbf{E}\vert) = S(T,N,\vert\mathbf{E}\vert) - S^{(0)}$.

```{dropdown} __Solución__

Haciendo uso de la ecuación de $\widehat{\mu}$ calculada en el apartado $(a)$,

$$
 \frac{S(T,N,\vert\mathbf{E}\vert)}{k_\mathrm{B}} := -\frac{1}{k_\mathrm{B}}\left[\frac{\partial (\widehat{\mu}N)}{\partial T}\right]_{N,\vert\mathbf{E}\vert} = N\left(\ln j + T\frac{\mathrm{d}\ln j}{\mathrm{d}T}\right) + \color{red}\left\{ \color{black} \ln(\xi N^3)+1 + \ln\left(1+\frac{N^2y^2}{6}\right) + \frac{2N^2y^2}{6+N^2y^2} \color{red} \right\}\; \color{black} ,
$$ (agg_e_stn)

en la cual podemos diferenciar los términos

$$
\frac{S^{(0)}}{k_\mathrm{B}} = N\left(\ln j + T\frac{\mathrm{d}\ln j}{\mathrm{d}T}\right)
$$ (agg_e_s0)

y

$$
\frac{S^{(x)}(T,N,\vert\mathbf{E}\vert)}{k_\mathrm{B}} = \ln(\xi N^3)+1 + \ln\left(1+\frac{N^2y^2}{6}\right) + \frac{2N^2y^2}{6+N^2y^2} \; .
$$ (agg_e_sx_tn)

Pues bien, al equiparar las ecuaciones {eq}`agg_e_stn` y {eq}`agg_elek_epsilon_k`, apreciaremos claramente que la mayoría de las contribuciones no lineales positivas a la entropía están relacionadas con los temas positivos del potencial de subdivisión, cada cual con el suyo.
```

$(c)$ Construye la magnitud $\overline{\vert\mathbf{p}\vert}$, pero **sin recurrir** a la aproximación que hemos usado en la ecuación {eq}`agg_e_approx`. Después, calcula la aproximación de la expresión obtenida, despreciando términos que vayan más allá del orden de magnitud $\mathscr{O}(\vert\mathbf{E}\vert^5)$.

```{dropdown} __Solución__

Para comenzar, recalcularemos $N\widehat{\mu}$. Así, utilizando la función $\sinh(Ny)$ tal cual, tendríamos 

$$
\frac{N\widehat{\mu}}{k_{\mathrm{B}}T} = -\ln Q = -N\ln j + (N-1) \frac{\epsilon}{k_{\mathrm{B}}T} - \ln(\xi N^3) - \frac{N\alpha \vert\mathbf{E}\vert^2}{2k_\mathrm{B}T} - \ln\left[\frac{\sinh (Ny)}{Ny}\right] \; .
$$ (agg_elek_muhatN)

De ahí,

$$
\overline{\vert\mathbf{p}\vert} := -\left[\frac{\partial (\widehat{\mu}N)}{\partial\vert\mathbf{E}\vert}\right]_{T,N} = N\left[\alpha\vert\mathbf{E}\vert + p_0 \coth(Ny) \right] - \frac{k_{\mathrm{B}}T}{\vert\mathbf{E}\vert} \; .
$$ (agg_elek_p0)

Así pues, la serie de Taylor de la función $\coth{Ny}$ será

$$
\coth(Ny) = \sum_{n=0}^{\infty} \frac{2^{2n}B_{2n}(Ny)^{2n-1}}{(2n)!} = \frac{1}{Ny} + \frac{Ny}{3} - \frac{(Ny)^3}{45} + \mathscr{O}[(Ny)^5] \quad,\quad 0 <\vert Ny\vert < \pi \; ,
$$

donde $B_{2n}$ denotan los números de Bernoulli.

Por ende, operando con la ecuación {eq}`agg_elek_p0`, alcanzaremos nuestro objetivo:

$$
\overline{\vert\mathbf{p}\vert} = N\alpha\vert\mathbf{E}\vert + \frac{1}{3}\frac{N^2p_0^2\vert\mathbf{E}\vert}{k_{\mathrm{B}}T} - \frac{1}{45}\frac{N^4p_0^4\vert\mathbf{E}\vert^3}{(k_{\mathrm{B}}T)^3} + \mathscr{O}(\vert\mathbf{E}\vert^5) \; .
$$ (agg_e_p_0_1)

```

**----------------------------------------------------**

##### Ejecicio suplementario: relaciones de Maxwell


$(a)$ Escribe, primero, las ecuaciones del sistema pequeño y, a partir de ahí, escribe la ecuación diferencial de $\mathrm {d} (\widehat {\mu} N) $. Construye después la relación de Maxwell correspondiente a la expresión $\left (\frac {\partial\mu} {\partial\vert\mathbf {E}\vert}\right) _ {T, N}$, y comprueba que ambas expresiones son equivalentes.


```{dropdown} __Solución__

Las variables originales de la energía interna del sistema son las extensivas: la entropía, el número de partículas y el momento dipolar eléctrico. Por ello,

$$
\overline{E}(S,N,\mathbf{p}) = TS+\widehat{\mu}N + \mathbf{E}\cdot\mathbf{p} \; ,
$$ (agg_e_E)

y,

$$
\mathrm{d}\overline{E}(S,N,\mathbf{p}) = T\mathrm{d}S+\mu\mathrm{d}N + \mathbf{E}\cdot\mathrm{d}\mathbf{p} \; .
$$ (agg_e_gibbs)


Mediante las dos ecuaciones anteriores,

$$
\mathrm{d}(\widehat{\mu}N)(T,N,\vert\mathbf{E}\vert) = -S\mathrm{d}T+\mu\mathrm{d}N - \vert\mathbf{p}\vert \mathrm{d}\vert\mathbf{E}\vert\; .
$$ (agg_e_dmuhat)

Se debe destacar que, al construir la función de partición canónica, hemos iniciado el grado eléctrico de libertad a través de la ecuación {eq}`agg_e_q_p0`. Pues bien, el resultado obtenido depende del módulo del campo $\mathbf {E}$. Por ello, podemos considerar el módulo como variable ambiental en lugar del propio vector, de modo que su conjugada sea el módulo del momento $\mathbf {p}$.

Desde allí construiremos la relación de Maxwell que se nos pide:

$$
\left(\frac{\partial \mu}{\partial \vert\mathbf{E}\vert}\right)_{T,N} = \frac{\partial}{\partial \vert\mathbf{E}\vert} \left(\frac{\partial (\widehat{\mu}N)}{\partial N}\right)_{T,\vert\mathbf{E}\vert} \equiv \frac{\partial}{\partial N} \left(\frac{\partial (\widehat{\mu}N)}{\partial \vert\mathbf{E}\vert}\right)_{T,N} = -\left(\frac{\partial \vert\mathbf{p}\vert}{\partial N}\right)_{T,\vert\mathbf{E}\vert} \; .
$$ (agg_elek_maxwell_1)

Ahora necesitamos la expresión exacta del potencial químico $\mu$. Así, por medio de la ecuación {eq}`agg_e_dmuhat`, 

$$
\frac{\mu}{k_{\mathrm{B}}T} = -\ln j + \frac{\epsilon}{k_{\mathrm{B}}T} - \frac{2}{N} - \frac{\alpha \vert\mathbf{E}\vert^2}{2k_\mathrm{B}T} - \frac{2Ny^2}{6+N^2y^2} - y\coth(Ny) \; .
$$ (agg_elek_mu_zehatz)

Operando ahora con el par de ecuaciones {eq}`agg_elek_p0` y {eq}`agg_elek_mu_zehatz`, verificaremos que se cumple la relación de Maxwell:

$$
\left(\frac{\partial \mu}{\partial \vert\mathbf{E}\vert}\right)_{T,N} = -\left(\frac{\partial \vert\mathbf{p}\vert}{\partial N}\right)_{T,\vert\mathbf{E}\vert} = -\alpha \vert\mathbf{E}\vert - p_0\coth(Ny) + Np_0\frac{y}{\sinh^2(Ny)} \; .
$$ (maxwell_1)


```

$(b)$ Haz lo mismo que en el apartado $(a)$ con la expresión $\left(\frac{\partial \overline{\vert\mathbf{p}\vert} }{\partial T}\right)_{\vert\mathbf{E}\vert, N}$.

```{dropdown} __Solución__

Para empezar, debemos conseguir la expresión exacta de la entropía $S(T, N, \vert\mathbf{E}\vert)$, con ayuda de la ecuación {eq}`agg_e_dmuhat`:

$$
\frac{S(T,N,\vert\mathbf{E}\vert)}{k_\mathrm{B}} = N\left(\ln j + T\frac{\mathrm{d}\ln j}{\mathrm{d}T}\right) + \ln(\xi N^3)+ 2 + \ln\left(\frac{\sinh(Ny)}{Ny}\right) -Ny\coth(Ny) \; .
$$ (agg_elek_S_zehatz)

Así, trabajando con las expresiones {eq}`agg_elek_p0` y {eq}`agg_elek_S_zehatz`,

$$
\left(\frac{\partial \overline{\vert\mathbf{p}\vert} }{\partial T}\right)_{\vert\mathbf{E}\vert, N} = \left(\frac{\partial S}{\partial \vert\mathbf{E}\vert}\right)_{T,N} = -\frac{k_{\mathrm{B}}}{\vert\mathbf{E}\vert} + N^2\frac{p_0}{T}\frac{y}{\sinh^2(Ny)} \; .
$$ (maxwell_2)


```


**----------------------------------------------------**

$$
\\
$$

En este ejercicio, como en otros anteriores, llevaremos el examen un paso más allá, sumergiéndonos en la **colectividad nanocanónica**. La función de partición generalizada la construiremos a partir de la función de partición {eq}`agg_q_tot`:

$$
\Upsilon(T,\mu,\vert\mathbf{E}\vert) := 1+ \sum_{N=1}^{\infty}Q(T,N,\vert\mathbf{E}\vert)\;e^{\mu N/k_{\mathrm{B}}T} = 1 +c(T)\left[\sum_{N=1}^{\infty}N^3x^N +\frac{y^2}{6}\sum_{N=1}^{\infty}N^5 x^N\right] \; ,
$$ (agg_e_upsilon)

donde, esta vez, tenemos que $x(T,\mu,\vert\mathbf{E}\vert) = j(T)\exp\left(\frac{-\epsilon + \mu }{k_{\mathrm{B}}T}\right)\exp\left(\frac{\alpha\vert\mathbf{E}\vert^2}{2k_{\mathrm{B}}T}\right)$.

Hay que recalcar que el hecho de recurrir a la aproximación de la función $\sinh (Ny) $ facilitará en gran medida el cálculo del sumatorio a través de la magnitud $N$. De hecho, observemos que en ambos sumatorios aparecen potencias de $N $. Esto permitirá llevar a cabo el desarrollo de la serie siguiendo las indicaciones que prosiguen a la ecuación {eq}`upsilontn`. Así las cosas,

$$
\boxed{\Upsilon = 1 + c(T)\left[\frac{x(x^2+4x+1)}{(x-1)^4} + \frac{y^2}{6}\frac{x^4+26x^3 + 66x^2+26x+1}{(x-1)^6}\right]}\quad, \quad \vert x\vert < 1 \; .
$$ (agg_e_upsilon_1)


Ademas, cabe mencionar que, al igual que en el {numref}`ejemplo {number} <mupt_linagg>`, la magnitud $x$ satisface la relación $x = e^{({\mu} - \mu^{(0)})/k_{\mathrm{B}}T}$.


`````{admonition} Sugerencia
:class: tip
Verifica lo mencionado en la frase anterior, empleando los potenciales $\mu$ y $\mu^{(0)}$ de la pareja de ecuaciones {eq}`agg_elek_mu` y la magnitud $x(T,\mu,\vert\mathbf{E}\vert) = j(T)\exp\left(\frac{-\epsilon + \mu }{k_{\mathrm{B}}T}\right)\exp\left(\frac{\alpha\vert\mathbf{E}\vert^2}{2k_{\mathrm{B}}T}\right)$.
`````

Dicho esto, como siempre, construiremos magnitudes termodinámicas en el conjunto nanocanónico a través de la función de partición {eq}`agg_e_upsilon_1`. Para empezar, definiremos la función probabilística $P (N) $, la cual abreviará las ecuaciones que prosiguen:


$$
P(N) = \frac{Q(T,N,\vert\mathbf{E}\vert)e^{\mu N/k_{\mathrm{B}}T}}{\Upsilon(T,\mu,\vert\mathbf{E}\vert)} \quad \Rightarrow \quad P(0) = \frac{1}{\Upsilon}
$$ (agg_e_pn)

Para compactar aún más las expresiones del momento medio dipolar y de la entropía, nos será muy beneficioso calcular primero el promedio del número de unidades, $\overline {N} $:

$$
\overline{N} := k_{\mathrm{B}}T\left(\frac{\partial\ln\Upsilon}{\partial \mu}\right)_{T,\vert\mathbf{E}\vert} = -cxP(0)\left[\frac{x^3+11x^2+11x+1}{(x-1)^5}+\frac{y^2}{6}\frac{x^5+57x^4+302(x^3+x^2)+57x+1}{(x-1)^7}\right]
$$ (agg_elek_nbar)


Pues bien, haciendo uso de esta ecuación, y operando (con suma atención), deberíamos llegar a la ecuación

$$
\overline{\vert\mathbf{p}\vert}(T,\mu,\vert\mathbf{E}\vert) := k_{\mathrm{B}}T\left(\frac{\partial\ln\Upsilon}{\partial \vert\mathbf{E}\vert}\right)_{T,\mu} = \overline{N}\alpha\vert\mathbf{E}\vert + c(T)P(0)\frac{p_0^2\vert\mathbf{E}\vert}{3k_{\mathrm{B}}T}\frac{x(x^4+26x^3+66x^2+26x+1)}{(x-1)^6} \; ,
$$ (agg_elek_p_bar)

para el momento dipolar, y a esta expresión elocuente para la entropía:

$$
\frac{S(T,\mu,\vert\mathbf{E}\vert)}{k_{\mathrm{B}}} := T\left(\frac{\partial\ln\Upsilon}{\partial T}\right)_{\mu,\vert\mathbf{E}\vert} = \overline{N}\left(\ln j + T\frac{1}{j}\frac{\mathrm{d}j}{\mathrm{d}T}\right)
$$
$$
+ \color{red}\left\{ \color{black} - \overline{N}\ln x - \ln P(0) + cP(0)\left(1-\frac{\epsilon}{k_{\mathrm{B}} T}\right)\frac{x(x^{2}+4x+1)}{(x-1)^{4}} \color{red} \right\} 
$$ 
$$
+ \color{red} \left\{ \color{black} cP(0)\left(\frac{p_0\vert\mathbf{E}\vert}{k_{\mathrm{B}} T}\right)^2 \left[\left(1-\frac{\epsilon}{k_{\mathrm{B}} T}\right)\frac{1}{6}-\frac{1}{3}\right]\frac{x(x^4+26x^3+66x^2+26x+1)}{(x-1)^6} \color{red} \right\} \color{black} \; .
$$ (agg_elek_s_nc)

Contemplemos la ecuación {eq}`agg_elek_s_nc`, término por término. Pues bien, si asumimos que $\overline {N} = N $, en la primera línea tendremos el término $S ^ {(0)}/k_ {\mathrm {B}} $. A partir de ahí, todas las contribuciones adicionales son de tamaño finito. Así, en la segunda línea, podemos detectar la aportación adicional adquirido en la ecuación {eq}`stmuagg`. Sin embargo, observemos que la variable $x $ que hemos definido en este ejemplo, al contrario de $ x(T,\mu)  =  je^{\left(\mu-\epsilon\right)/k_{\mathrm{B}}T}$, lleva en sí la contribución adicional $\exp\left(\frac{\alpha\vert\mathbf{E}\vert^2}{2k_{\mathrm{B}}T}\right)$, a causa de la polarizabilidad $\alpha$.


Para terminar, queda en evidencia que la tercera línea corresponde en su totalidad al aporte eléctrico. También es destacable que aparece el componente $\vert\mathbf {E}\vert ^ 2 $, por lo que, en el límite del campo eléctrico pequeño, esta aportación es esencialmente despreciable respecto a los términos de las dos líneas anteriores. En cualquier caso, observemos que si tomáramos $\epsilon\approx -2,3\cdot k_ {\mathrm {B}} T $, como hemos indicado en el {numref}`apartado {number} <mupt_linagg>`, el signo de este aporte sería positivo; es decir, el arranque del grado de libertad eléctrico en la región nanotermodinámica aumentará la entropía.


Finalmente, notemos que, si quitáramos el campo eléctrico, recobraríamos la ecuación original {eq}`stmuagg` del agregado lineal.




(ising)=
### Modelo de Ising

El sistema de espines magnéticos que nos ocupa en este ejemplo nos ofrecerá también una ocasión propicia para trabajar con los efectos de tamaño finito. Precisamente, trasladando las herramientas de la Nanotermodinámica a los sistemas magnéticos, nos enfrentaremos a la búsqueda del verdadero equilibrio térmico del modelo ilustrado en la {numref}`figura {number} <ising_geziak>`, el cual lo analizaremos en el colectivo estadístico microcanónico, canónico y, finalmente, nanocanónico. Atenderemos principalmente a la evolución de la entropía de colectividad en colectividad.

(ising_arrows)=
```{figure} ising_geziak.png
---
width: 650px
name: ising_geziak
---
 La cadena unidimensional de Ising está formada por $N $ espines inseparables. Solamente se pueden alinear en los sentidos $+\mathbf {u} _z $ y $-\mathbf {u} _z $. Para facilitar los desarrollos, solamente consideraremos la energía de interacción entre primeros vecinos, $\pm J $ ({numref}`figura {number} <ising_j>`).
```


Cada uno de los componentes del sistema de Ising genera dos aportaciones a la energía interna: por un lado, el término $\pm J$, según la alineación magnética entre dos espines; por otro lado, si asignáramos a cada uno de ellos el momento magnético $\mathbf {m} $, tendríamos también la interacción $-\mathbf {m}\cdot\mathbf {B} $ resultante del acople con el campo magnético externo $-\mathbf {B}$.

Cabe señalar que el análisis conjunto de ambos efectos no es una cuestión sencilla. De hecho, a la hora de construir la función de partición canónica tendremos que recurrir al método de la _matriz de transferencia_. Además, las expresiones largas obtenidas de ahí no son fáciles de utilizar. Pues bien, en lugar de esto, llevaremos a cabo el análisis en dos partes por separado. En primer lugar, en el {numref}`apartado {number} <b0jnot0>`, sólo tendremos en cuenta la interacción de alineación $\pm J $ entre dos primeros vecinos. A continuación, en el {numref}`apartado {number} <j0bnot0>`, haremos lo contrario: aplicaremos al sistema un campo magnético externo $\mathbf {B} $, y asumiremos que los espines no interaccionan entre ellos $(J = 0) $.


(b0jnot0)=
#### Cadena de Ising, bajo influencia de la interacción $J$ 

Atendamos a la {numref}`figura {number} <ising_j>`.

(ising_j)=
```{figure} ising_j.png
---
width: 650px
---
  Admitiremos que los espines de Ising favorecen la alineación magnética; es decir, esta configuración minimizará la energía magnética. Así, dos primeros vecinos apuntando al mismo sentido percibirán la energía de interacción $-J $, mientras que si mostraran direcciones opuestas, dicha energía pasaría a ser $+J $.
```

Siguiendo la aproximación descrita anteriormente, supongamos que el sistema se compone, en realidad, de $N+1 $ espines magnéticos, de forma que disponga de $N $ uniones en total (para aclarar esta última cuestión, obsérvese la imagen superior). De ellos, $n_+ $ son enlaces entre espines de sentido opuesto $(+J) $, y por tanto, quedarán $N-n_+ $ entre espines del mismo sentido $(-J) $. Por ejemplo, en el caso de la {numref}`figura {number} <ising_j>`, $N = 10 $ y $n_+ = 7 $. Por ello, la energía interna del sistema con las variables $N $ y $n_+ $ fijas en la **colectividad microcanónica** se puede escribir de la siguiente manera:

$$
  E(n_+, N) = n_+ J - (N-n_+)J = -(N-2n_+)J \; .
$$ (e_j)

El siguiente paso consiste en calcular el número de microestados compatibles con esa expresión de la energía total; es decir, en cuántas formas distintas podemos distribuir las $N $ uniones entre los espines indistinguibles que forman el sistema entre los grupos de energía alta $(n_+)$  y energía baja $(N-n_+)$. En este sentido, percatémonos de que la inversión de todas las flechas de la {numref}`figura {number} <ising_j>` no afectaría a la expresión {eq}`e_j`, ya que la magnitud $n_+ $ permanecería intacta; es decir, deberemos contar cada microestado dos veces. Así las cosas,


$$
\Omega(n_+,N) = 2\cdot \frac{N!}{n_+!\;(N-n_+)!} \;\;\;\; .
$$ (omega_nj)

A continuación, escribiremos la ecuación de la entropía, excluyendo todos los términos excepto los tres primeros de la serie $\ln (n!)$ de Stirling:

$$
\boxed{\frac{S(n_+,N)}{k_\mathrm{B}} = N\ln N - n_+\ln n_+ - (N-n_+)\ln(N-n_+) - \frac{1}{2}\ln\left[\frac{\pi}{2}n_+\left(1-\frac{n_+}{N}\right)\right]} \; .
$$ (s_ising_micro)

Según nos dice la ecuación {eq}`s_ising_micro`, la entropía tenderá a su máximo cuando $n_+ $ coincida con la mitad del número de enlaces, y por ende, cuando el sistema pierda la magnetización $(E = 0) $, es decir,

$$
S(n_+, N)_ {\text{max}} = S(N/2, N) = Nk_\mathrm{B}\ln 2 - \frac{1}{2}k_\mathrm{B}\ln\left(\frac{\pi}{8}N\right) \; .
$$ (s_max_micro)

Más adelante, a medida que vayamos iniciando grados de libertad, recalcularemos estas dos últimas expresiones para luego realizar comparaciones entre los resultados.

$$
\\
$$

Pasaremos ahora a la __colectividad canónica__. Para ello, introduciremos la energía $E (n_+) $ en el sumatorio, junto a su correspondiente conjunto de microestados, y, teniendo en cuenta el factor de Boltzmann, construiremos la función de partición:

$$
Q(T, N) = \sum_{n_+ = 0}^{N}\Omega(n_+,N)\;e^{-E(n_+, N)/k_\mathrm{B}T} \; .
$$ (qtn_ising_j)

Insertaremos las expresiones {eq}`e_j` y {eq}`omega_nj` de arriba en {eq}`qtn_ising_j`, y, tras realizar arreglos en las ecuaciones, llegaremos a

$$
Q(T, N) = 2 \sum_{n_+ = 0}^{N} \frac{N!}{n_+!\;(N-n_+)!}\left(e^{- J/k_\mathrm{B}T}\right)^{n_+}\left(e^{ J/k_\mathrm{B}T}\right)^{N-n_+} = 2\left(e^{- J/k_\mathrm{B}T} + e^{ J/k_\mathrm{B}T}\right)^N \; .
$$ (q_ising)

```{admonition} Nota
Para construir la última relación, hemos empleado la identidad del binomio:

$$
(x+y)^N = \sum_{k=0}^{N} \frac{N!}{k!\;(N-k)!}\; x^k\; y^{N-k} \; .
$$
```

Desde aquí, en primer lugar, calcularemos el promedio de la energía interna del sistema, siguiendo a la siguiente igualdad:

$$
\overline{E} = \frac{\sum_{n_+ = 0}^{N}E(n_+,N) \; \Omega(n_+,N) \;e^{-E(n_+,N)/k_\mathrm{B}T}}{\sum_{n_+ = 0}^{N}\Omega(n_+,N)\;e^{-E(n_+, N)/k_\mathrm{B}T}} = k_{\mathrm{B}}T^2\frac{\partial}{\partial T}\ln Q \; .
$$ (bar_E_def)

#####  Ejercicio

$(a)$ Calcula la expresión $\overline{E}$.

```{dropdown} __Solución__

$$
 \overline{E} = -NJ\tanh\frac{J}{k_{\mathrm{B}}T} 
$$ (bar_E)

```

$(b)$ A continuación, calcula la energía libre de Helmholtz.

```{dropdown} __Solución__

$$
A(T, N) = -Nk_{\mathrm{B}}T\left[\ln\left(2\cosh\frac{J}{k_{\mathrm{B}}T}\right) + \frac{1}{N}\ln 2\right] 
$$ (hehlmholtz_ising)

```

$(c)$ Utilizando las dos ecuaciones anteriores, construye la expresión $S (T, N) $ de la entropía. Luego, calcula su máximo y compara el resultado con la ecuación {eq}`s_max_micro`.

```{dropdown} __Solución__

Recordando que la entropía cumple la ecuación $S(T, N) =(\overline{E} - A)/T $ en el colectivo canónico, llegaremos a esta expresión:

$$
\boxed{S(T,N)
 = N\left[k_{\mathrm{B}}\ln\left(2\cosh\frac{J}{k_{\mathrm{B}}T}\right) - \frac{J}{T}\tanh\frac{J}{k_{\mathrm{B}}T}\right]  + k_{\mathrm{B}}\ln 2} \; .
$$ (s_ising_kan)

La entropía tiene un máximo cuando $\frac {J} {k_ {\mathrm {B}} T} = 0 $. Existen dos casos que pueden llevarnos a esta situación: por un lado, cuando $J = 0 $; es decir, al no existir interacciones entre los espines. Y, por otro lado, en el límite $T\rightarrow\infty $. Así las cosas, la entropía cumplirá la expresión

$$
S(T, N)_{\text{max}} = (N+1)k_{\mathrm{B}}\ln 2 \; .
$$ (s_max_kano)

Queda en evidencia que, en el límite macroscópico, tanto la expresión $(N\rightarrow\infty) $ como la ecuación {eq}`s_max_micro` tenderán al valor $Nk_ {\mathrm {B}}\ln 2 $. Sin embargo, si no descartáramos los efectos de tamaño finito en la región nanotermodinámica, se impondría $S (T, N) _ {\text {max}} $ frente a $S(n_+, N)_ {\text{max}}$ .
```

**----------------------------------------------------**

$$
\\
$$

Seguidamente, transcurriremos a la **colectividad nanocanónica**. 

#####  Ejercicio

$(a)$ Escribe la expresión de la función de partición nanocanónica, $\Upsilon(T,\mu)$, partiendo de la ecuación {eq}`q_ising`. No realices cálculos.


```{dropdown} __Solución__

Al construir la función de partición generalizada, recordemos que anteriormente hemos puntualizado que el sistema dispone de  $N $ uniones entre primeros vecinos, de manera que el número de espines del sistema es $N+1 $. Debido a eso, deberemos introducir $N+1 $ en el factor sumatorio de Boltzmann, por lo que la expresión a construir quedará como

$$
\Upsilon (T,\mu)= \sum_{N=0}^{\infty} Q(T,N)\; e^{\mu(N+1)/k_\mathrm{B}T} \; .
$$ (upsilon_ising)

```

$(b)$ Después, calcula la expresión de $\Upsilon(T,\mu)$ y el potencial de subdivisión.



```{dropdown} __Solución__

Desarrollando y arreglando la ecuación del apartado $(a)$,

$$
\Upsilon (T,\mu)= 2\lambda \sum_{N=0}^{\infty}\left[\left(e^{J/k_\mathrm{B}T} + e^{- J/k_\mathrm{B}T}\right)\lambda\right]^N = \left(\frac{1}{2\lambda} -\cosh\frac{J}{k_\mathrm{B}T}\right)^{-1} \; ,
$$ (upsilon_ising_1)

donde hemos sustituido $\lambda = e^{\mu/k_{\mathrm{B}}T}$. De ahí, la expresión del potencial de subdivisión resulta inmediata:

$$
\mathscr{E}(T,\mu) = k_\mathrm{B}T\ln\left(\frac{1}{2\lambda} -\cosh\frac{J}{k_\mathrm{B}T}\right)  \; .
$$(epsilon_ising)

```



$(c)$ De ahí, desarrolla las magnitudes $S(T,\mu)$ y $\overline{N}$. Seguidamente, remodela la ecuación de la entropía, para llegar a la expresión $S(T,\overline{N}(\mu))$, y maximiza esta última.

```{dropdown} __Solución__

Para comenzar,

$$
S(T,\mu) = -k_\mathrm{B}\ln\left(\frac{1}{2} e^{-\mu/k_{\mathrm{B}}T} -\cosh\frac{J}{k_\mathrm{B}T}\right) - \left(\frac{1}{2}\;\frac{\mu}{T}\;e^{-\mu/k_{\mathrm{B}}T} - \frac{J}{T}\;\sinh\frac{J}{k_\mathrm{B}T}\right)\cdot\left(\frac{1}{2} e^{-\mu/k_{\mathrm{B}}T} -\cosh\frac{J}{k_\mathrm{B}T}\right)^{-1} \; .
$$(s_tmu_ising)

A la hora de calcular el promedio del número de espines, debemos estar atentos, porque tendremos que introducir $\overline {N} + 1 $ en la expresión, es decir:

$$
\overline{N} + 1 = -\left(\frac{\partial \mathscr{E}}{\partial \mu}\right)_T =\frac{\frac{1}{2} e^{-\mu/k_{\mathrm{B}}T}}{ \frac{1}{2} e^{-\mu/k_{\mathrm{B}}T} -\cosh\frac{J}{k_\mathrm{B}T}} \; .
$$(bar_n_ising)


Por tanto, podemos reescribir la expresión de la entropía de la siguiente manera:

$$
\boxed{S(T,\overline{N}(\mu)) = \overline{N}\left[ k_{\mathrm{B}}\ln\left(2\;\frac{\overline{N}+1}{\overline{N}}\;\cosh\frac{J}{k_{\mathrm{B}}T}\right) - \frac{J}{T}\;\tanh\frac{J}{k_{\mathrm{B}}T}\right] + k_{\mathrm{B}}\ln\left[2(\overline{N}+1)\right]} \; .
$$ (s_tbarn_ising)

Esta función tiene tambíen un máximo en el punto $\frac{J}{k_{\mathrm{B}}T} = 0$:

$$
S(T, \overline{N}(\mu))_{\text{max}} = \overline{N}k_{\mathrm{B}}\ln \left(2\frac{\overline{N}+1}{\overline{N}}\right) + k_{\mathrm{B}}\ln\left[2(\overline{N}+1)\right] \; ,
$$ (s_max_nanokano)

cuyo límite macroscópico es, de nuevo, $\overline{N}k_{\mathrm{B}}\ln 2$.

```

**----------------------------------------------------**

Una vez calculados las tres expresiones $S(n_+, N)_{\mathrm{max}}$, $S(T, N)_{\mathrm{max}}$ y $S(T,\overline{N}(\mu))_{\mathrm{max}}$ resultará ilustrativo realizar una comparación entre ellas, atendiendo a su evolución en función del tamaño del sistema:

```{figure} ising_1_s.png
---
height: 350px
name: sn100
---
Entropía por unidad de enlace. Salta a la vista, por un lado, que cuando el sistema es pequeño, el conjunto nanocanónico nos devuelve una mayor entropía. Por otro, en los tres casos la magnitud $S/N $ no tiene carácter intensivo en la región nanotermodinámica. Sin embargo, en el límite macroscópico, las expresiones tenderán a unificarse, y se restablecerá la intensividad. Para construir las curvas hemos utilizado el valor $J/k_ {\mathrm {B}} T = 1,45 $ que se indica en el artículo {cite}`multiscale`.

```

Además, como hemos remarcado en varias ocasiones, la capacidad de subdivisión del conjunto en subsistemas pequeños es la clave del conjunto nanocanónico. En este sentido, podremos alcanzar el equilibrio térmico del sistema que nos ocupa en la nanoescala. En concreto, atendiendo al potencial de subdivisión, la implantación de $\mathscr {E} (T,\mu) = 0 $ garantizará que el conjunto totalmente abierto de subsistemas pequeños alcance sin impedimentos la situación de equilibrio correspondiente a la subdivisión. De hecho, en el camino hacia el equilibrio se producirán variaciones espontáneas en el número de réplicas, $\overline {\mathscr {N}} $.

Dicho lo dicho, estos son el promedio del número de partículas por réplica y la entropía en el estado de equilibrio:


$$
\overline{N}_{\mathrm{equilibrio}} = \cosh \frac{J}{k_{\mathrm{B}}T} \; ,
$$ (ising_nbar_equilibrio)

y,

$$
S(T,\overline{N}(\mu))_{\mathrm{equilibrio}} = \overline{N} k_{\mathrm{B}}\ln\left(2 + 2\cosh\frac{J}{k_{\mathrm{B}}T}\right) - \overline{N}\frac{J}{T}\;\tanh\frac{J}{k_{\mathrm{B}}T} \; .
$$ (ising_s_equilibrio)

Por lo tanto, recordemos la advertencia del final del {numref}`apartado {number} <stabeps>`. Ciertamente, debemos subrayar que el límite macroscópico de las entropías de las ecuaciones {eq}`s_ising_kan` y {eq}`s_tbarn_ising` no se corresponde con la expresión que aparece en la ecuación {eq}`ising_s_equilibrio`. En otras palabras, esta diferencia deja en evidencia que el estado de equilibrio alcanzado en el conjunto nanocanónico, en el que el potencial de subdivisión es estrictamente nulo, no se trata en absoluto del estado macroscópico del sistema. De hecho, si reescribimos la ecuación {eq}`epsilon_ising` con la ayuda de la expresión {eq}`bar_n_ising`, llegaremos a la igualdad

$$
\mathscr{E}(T,\mu) = -k_{\mathrm{B}}T \ln\left(\frac{\overline{N}}{\cosh\frac{J}{k_{\mathrm{B}}T}}\right) \; ,
$$ (ising_epsilon_1)

el cual indica claramente que en el límite $\overline{N} \rightarrow \infty$ el potencial de subdivisión no tenderá a cero, pese a que las aportaciones lineales macroscópicas recuperarán el predominio frente a él.


(j0bnot0)=
#### Spines libres, bajo influencia del campo externo $\mathbf{B}$ 

En esta reexaminación del mismo sistema, seguiremos el mismo procedimiento que en el apartado anterior. En cualquier caso, veremos que los resultados que obtendremos tienen una gran representatividad; por encima de todo, observaremos una evidente concomitancia con las expresiones construidas en el análisis del gas ideal del {numref}`ejemplo {number} <mupt_gi>`.

Así pues, atendamos a la {numref}`figura {number} <ising_b>`.

(ising_1)=
```{figure} ising_b.png
---
width: 700px
name: ising_b
---
Supongamos que los $N $ espines están interactuando solamente con el campo magnético externo $\mathbf {B} = B\mathbf {u_z} $. Por lo tanto, si asignamos a los espines el momento magnético $\mathbf{m} = \pm m \mathbf{u_z}$, la energía interna del sistema será $E = (N-2n_+) mB $, donde $n_+ $ es ahora el número de espines alineados en en el mismo sentido del campo $(+z) $.

```

Teniendo en cuenta las explicaciones de la figura, el número de microestados compatibles con el macroestado en el que está fijada la energía interna $E (n_+, N) $ en el **colectivo microcanónico** nos lo proporcionará, una vez más, el coeficiente binomial:

$$
\Omega(n_+,N) = \frac{N!}{n_+! (N-n_+)!} \; .
$$ (ising_b_omega)

Recurriendo a la aproximación $\ln N! \approx N\ln N - N + \frac{1}{2}\ln (2\pi N)$ de Stirling, solo mantendremos un único término no lineal en la entropía, el cual vendrá recogido en el potencial de subdivisión $\mathscr{E}(n_+, N)$. Así,

$$
\boxed{\frac{S(n_+,N)}{k_{\mathrm{B}}} \approx N\ln N - n_+ \ln n_+ - (N-n_+)\ln(N-n_+) - \frac{1}{2}\ln\left[2\pi n_+\left(1-\frac{n_+}{N}\right)\right]} \; ,
$$ (ising_b_s_mc)

y,

$$
\mathscr{E}(n_+, N) \approx \frac{1}{2} k_{\mathrm{B}}T \ln\left[2\pi n_+\left(1-\frac{n_+}{N}\right)\right] > 0 \; , \quad n_+ <N \; .
$$ (ising_b_epsilon_mc)


Tal y como se puede apreciar a través de las dos ecuaciones anteriores, el potencial de subdivisión positivo implica un descenso de la entropía. En efecto, recordando las explicaciones del {numref}`apartado {number} <stabeps>`, éste impide la subdivisión del conjunto microcanónico en subsistemas más pequeños, lo cual reduce el número de réplicas, y, por consiguiente, intensifica la indistinguibilidad de los espines constituyentes.


$$
\\
$$

Siguiendo adelante, pondremos los subsistemas en contacto térmico, y saltaremos así a la **colectividad canónica**. Para ello, al igual que en la sección precedente, debemos asumir que la magnitud $n_+ $ ya no se mantendrá constante. Así, ponderando cada conjunto de microestados con su correspondiente factor de Boltzmann $e ^ {-E (n_+, N)/k_ {\mathrm {B}} T} $, construiremos la función de partición canónica $Q (T, N) $:

$$
Q(T, N) = \sum_{n_+=0}^N \Omega(n_+,N)\;e^{-(N-2n_+)mB/k_{\mathrm{B}}T} = \left[2\cosh\frac{mB}{k_{\mathrm{B}}T}\right]^N \; .
$$ (ising_b_q)

De ahí, obtendremos las energías

$$
A(T,N) = -Nk_{\mathrm{B}}T\ln\left[2\cosh\frac{mB}{k_{\mathrm{B}}T}\right]
$$ (ising_b_A)

y 

$$
\overline{E} = -NmB\tanh\frac{mB}{k_{\mathrm{B}}T} \; .
$$ (ising_b_Ebar)

Mediante estas expresiones, la entropía será

$$
\boxed{S(T,N)
 = N\left[k_{\mathrm{B}}\ln\left(2\cosh\frac{mB}{k_{\mathrm{B}}T}\right) - \frac{mB}{T}\tanh\frac{mB}{k_{\mathrm{B}}T}\right]} \; .
$$ (ising_b_s_c)

En esta ocasión, todos los términos de la entropía son lineales respecto a la magnitud $N $. De hecho, al calcular el sumatorio a lo largo de todos los microestados en la ecuación {eq}`ising_b_q`, hemos eliminado los factoriales. Por lo tanto, la expresión de energía libre de Helmholtz $A (T, N)$ que hemos definido en la ecuación {eq}`ising_b_A` es una función Euler-homogénea de primer orden (estrictamente exacta), de forma que tendremos $\mathscr {E} (T, N) = 0 $.


$$
\\
$$

Para finalizar el análisis, pondremos en marcha el grado de libertad químico, y recalcularemos la entropía en el el **colectivo nanocanónico**. Así, sustituyendo $x (T,\mu) = 2\cosh\frac {mB} {k_ {\mathrm {B}} T}\; e ^ {\mu/k_ {\mathrm {B}} T} $, la función de partición generalizada obedecerá la expresión

$$
\Upsilon (T,\mu) = \sum_{N=0}^\infty x^N = \frac{1}{1-x} \;, \quad \vert x \vert < 1  \; .
$$ (ising_b_upsilon)

De ahí,

$$
\overline{N} = \frac{x}{1-x} \; ,
$$ (ising_b_nbar)


$$
\mathscr{E}(T,\mu) = k_{\mathrm{B}}T\ln(1-x) = -k_{\mathrm{B}}T\ln\left(\overline{N}+1\right) \; ,
$$ (ising_b_epsilon_tmu)

y,

$$
\boxed{S(T,\overline{N}(\mu)) = \overline{N}\left[ k_{\mathrm{B}}\ln\left(2\cosh\frac{mB}{k_{\mathrm{B}}T}\right) - \frac{mB}{T}\;\tanh\frac{mB}{k_{\mathrm{B}}T} + \ln\left(\frac{\overline{N}+1}{\overline{N}}\right)\right] + k_{\mathrm{B}}\ln\left(\overline{N}+1\right)} \; .
$$ (ising_b_s_tmu)


Pues bien, en comparación con la expresión $S (T, N) $ de la ecuación {eq}`ising_b_s_c`, el potencial de subdivisión $\mathscr {E} (T,\mu)$ negativo ha agregado una contribución positiva a la entropía (dado que $\overline {N} >0 $). A la vista de los resultados, es evidente la similitud entre el comportamiento del sistema bajo estudio formado por espines que no interaccionan y aquél del gas ideal presentado en el {numref}`apartado {number} <mupt_gi>`. Como en ese caso, la contribución negativa y no extensiva del potencial de subdivisión permitirá la maximización de la entropía por unidad de partícula en el límite $\overline {N}\rightarrow 0 $; es decir, a medida que aumente la subdivisión del colectivo (recordemos la ecuación {eq}`gi_tpmu_s_n`). Para ello, obviamente, los subsistemas deberán ser capaces de modificar su tamaño sin impedimento externo alguno. Este último requisito lo cumplirá únicamente la colectividad estadística nanocanónica.
