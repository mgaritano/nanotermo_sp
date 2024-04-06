(osagarri)=
## Ejemplos adicionales

(mupt_sphagg)=
### Agregado esférico

El análisis que presentaremos a continuación se asemeja al ejemplo de la {numref}`subsección {number} <mupt_linagg>`. No obstante, en lugar de en la rotación del sistema, en esta ocasión nos centraremos en el efecto de los efectos de superficie y de curvatura. Así las cosas, el sistema que nos ocupa es un agregado esférico incompresible compuesto por $N $ monómeros, de tal forma que no consideraremos el grado de libertad mecánico. Por ende, pondremos en marcha el estudio a través de las variables de entorno $(T, N) $. Asimismo, asignaremos a las unidades la función de partición intrínseca $j (T) $. Además, tendremos en cuenta el aporte de energía superficial libre $a (T) N ^ {2/3} $ $(a>0) $. Cabe destacar que la magnitud $a (T) $ es proporcional a la tensión superficial $\gamma $. Completaremos la formulación tomando consideración de la variación de la tensión superficial a causa de la curvatura de la superficie esférica. Este incluirá la aportación $b (T) N ^ {1/3} $ $(b>0) $. En el libro de Hill {cite}`hill` se trabaja este ejemplo en varias ocasiones. Pues bien, cabe destacar que en todos ellos se excluye el efecto de la curvatura. Nosotros lo consideraremos en este análisis como una pequeña corrección respecto al resto de aportaciones, tomando $b\rightarrow 0 ^ {+} $. Dicha asunción facilitará notoriamente el procedimiento del cálculo de la función de partición $\Upsilon (T,\mu) $.


Primero, construiremos la función de partición canónica $Q(T,N)$, sin aproximaciones.

$$
Q(T,N) = j(T)^N\;\exp\left[{\frac{-a(T)N^{2/3}}{k_{\mathrm{B}}T}}\right]\exp\left[{\frac{-b(T)N^{1/3}}{k_{\mathrm{B}}T}}\right]
$$ (qagg_sph)

De ahí, recordando la relación $Q=e^{-\widehat{\mu}N/k_{\mathrm{B}}T}$, calcularemos los potenciales químicos diferencial e integral, así como el potencial de subdivisión:

$$
\left.\begin{array}{l}
\widehat{\mu}=-k_{\mathrm{B}}T\ln j + N^{-1/3}\;a(T) + N^{-2/3}\;b(T)\\\\
\mu=-k_{\mathrm{B}}T\ln j +\frac{2}{3} N^{-1/3}\;a(T) + \frac{1}{3} N^{-2/3}\;b(T)
\end{array}\right\}\underset{(N \rightarrow \infty)}{\boldsymbol{\longrightarrow}} \; \mu^{(0)}(T) = -k_{\mathrm{B}}T\ln j \; ,
$$ (sph_agg_mu)

$$
\mathscr{E} (T,N) = N\left(\widehat{\mu}-\mu\right) = \frac{1}{3}N^{2/3}a(T) + \frac{2}{3}N^{1/3}b(T) > 0 \; .
$$ (sph_epsilon_c)

Junto a ellos, escribiremos las siguientes dos magnitudes, puesto que nos resultarán útiles más en adelante:

$$
\left.\begin{array}{l}
\widehat{\mu}^{(x)} = \widehat{\mu} - \mu^{(0)} = N^{-1/3}\;a(T) + N^{-2/3}\;b(T)\\\\
\mu^{(x)} = \mu - \mu^{(0)} = \frac{2}{3}N^{-1/3}\;a(T) + \frac{1}{3}N^{-2/3}\;b(T)
\end{array}\right\} \underset{(N \rightarrow \infty)}{\boldsymbol{\longrightarrow}} \; 0 \; .
$$ (excess_mu)

```{admonition} Nota
Hill denomina términos de exceso (_excess terms_) a las magnitudes $\widehat {\mu} ^ {(x)} $ y $\mu ^ {(x)} $. Son indicadores de efectos de tamaño finito de los potenciales químicos $\widehat {\mu} $ y $\mu $, respectivamente.
```

De las ecuaciones anteriores, calcularemos la entropía y el promedio de la energía interna, para luego poder realizar comparaciones con las expresiones $S (T,\mu) $ y $\overline {E} (T,\mu) $:

$$
\boxed{S(T,N) = -\left(\frac{\partial N\widehat{\mu}}{\partial T}\right)_{N} = Nk_{\mathrm{B}}\left(\ln j + T\frac{1}{j}\frac{\mathrm{d}j}{\mathrm{d}T}\right) - N^{2/3}\frac{\mathrm{d}a}{\mathrm{d}T} - N^{1/3}\frac{\mathrm{d}b}{\mathrm{d}T}} \; ,
$$ (s_sph_agg_tn)

$$
\overline{E}(T,N) = \widehat{\mu}N + TS = Nk_{\mathrm{B}}T^2\frac{1}{j}\frac{\mathrm{d}j}{\mathrm{d}T} + N^{2/3}\left(a -T\frac{\mathrm{d}a}{\mathrm{d}T}\right) + N^{1/3}\left(b -T\frac{\mathrm{d}b}{\mathrm{d}T}\right) \; .
$$(bar_e_tn_sph)

$$
\\
$$

Trasladaremos el análisis a la __colectividad nanocanónica__. Reescribiremos la definición de la función de partición nanocanónica a través del par de ecuaciones {eq}`excess_mu`, para poner a la vista las magnitudes $\widehat {\mu} ^ {(x)} $ y $\mu ^ {(x)} $.

$$
\Upsilon(T,\mu) = \sum_{N=0}^{\infty}e^{-\widehat{\mu}N/k_{\mathrm{B}}T}e^{{\mu}N/k_{\mathrm{B}}T} = \sum_{N=0}^{\infty}e^{-\widehat{\mu}^{(x)}N/k_{\mathrm{B}}T}e^{{\mu^{(x)}}N/k_{\mathrm{B}}T}
$$ (upsilon_sph)


Tengamos en cuenta que el hecho de que $\mu ^ {(x)} $ sea positivo en la ecuación {eq}`upsilon_sph` conllevaría la divergencia de la serie, ya que, para $N $ suficientemente grandes, dominaría el exponencial $e ^ {{\mu ^ {(x)}} N/k_ {\mathrm {B}} T}$. Por lo tanto, deberemos imponer $\mu ^ {(x)}\leq 0 $ para garantizar la convergencia (recordemos que $a $ y $b $ son positivos y, en consecuencia, $\widehat {\mu} ^ {(x)} $ también). De hecho, como veremos a continuación, la divergencia resultante de que $\mu ^ {(x)} > 0 $, o, lo que es lo mismo, $\mu > \mu^{(0)}(T)$, acarreará que $\overline {N} =\infty $. Cabe destacar que en este caso la variable $\mu $ no es la que figura en la ecuación {eq}`sph_agg_mu` calculada anteriormente, sino una constante asociada al sistema. Pues bien, como se explicará a continuación, para garantizar la convergencia de la serie, tendremos que imponer la condición $\mu\rightarrow\mu ^ {(0)}$. Antes de seguir adelante, es conveniente introducir la siguiente notación:

$$
\delta(T,\mu) = \frac{-\mu^{(x)}}{k_{\mathrm{B}}T} = \frac{\mu^{(0)}-\mu}{k_{\mathrm{B}}T} \quad , \quad \alpha(T) = \frac{a(T)}{k_{\mathrm{B}}T} \quad , \quad \beta(T) = \frac{b(T)}{k_{\mathrm{B}}T} \; .
$$

Así las cosas, antes de proceder a los cálculos, existen otras cuestiones que deberemos aclarar. De hecho, siguiendo las explicaciones del párrafo anterior, para que el tamaño del agregado bajo estudio sea razonable, tendremos que recurrir al límite $\delta\rightarrow 0 ^ {+} $, el cual nos mantendrá alejados de la divergencia. Por otro lado, la energia superficial $aN ^ {2/3} $ será realista solamente para valores de $N $ suficientemente grandes (por ejemplo, $N>20 $). Por ello, en la ecuación {eq}`upsilon_sph`, sustituiremos el sumatorio sobre $N$ por una integral. Hay que aclarar que, aunque este modelo es inadecuado para valores pequeños de $N $, para $\overline {N} $ medianamente grandes el error no será tan significativo. Por último, al hilo de lo dicho anteriormente sobre los efectos de curvatura, también nos es lícito utilizar el límite $\beta\rightarrow 0 ^ {+} $. Todo lo mencionado hasta ahora lo reflejaremos en la expresión de la función de partición que viene a continuación:

$$
\Upsilon (T,\mu) = \int_0^\infty \mathrm{d}N\;\left[1-\delta(T,\mu) N\right] \; e^{-\alpha(T) N^{2/3}}e^{-\beta(T) N^{1/3}} \approx \int_0^\infty \mathrm{d}N\;\left[1-\delta(T,\mu) N\right] \; e^{-\alpha(T) N^{2/3}}\left[1-\beta(T) N^{1/3}\right] \; .
$$ (upsilon_sph_int)

```{dropdown} __Instrucciones para el cálculo de la integral__

Estas relaciones nos resultarán de ayuda de cara a obtener la expresión {eq}`upsilon_sph_good`:

$$
\int_{0}^{\infty} \mathrm{d}x\; e^{-ax^b} = \frac{1}{b}a^{-1/b}\;\Gamma\left(\frac{1}{b}\right) \; ,
$$

$$
\int_{0}^{\infty} \mathrm{d}x\; x^ne^{-ax^b} = \frac{1}{b}a^{-(n+1)/b}\;\Gamma\left(\frac{n+1}{b}\right) \; ,
$$

y,

$$
\Gamma\left(\frac{1}{2} + n \right) = \frac{(2n)!}{4^n n!}\pi^{1/2} \; .
$$


```

El resultado de la integral definida es la siguiente:

$$
\Upsilon (T,\mu) = \frac{\pi^{1/2}\left(45\delta\beta+12\alpha^2\right)}{16\alpha^{7/2}} - \frac{3\beta}{2\alpha^2} - \frac{3\delta}{\alpha^3} \; \underset{(\delta \rightarrow 0^{+})}{\boldsymbol{\longrightarrow}} \; \frac{3\pi^{1/2}}{4\alpha^{3/2}} - \frac{3\beta}{2\alpha^2} \; .
$$ (upsilon_sph_good)

Desde ahí, para empezar, obtendremos el promedio $\overline {N} $. Para ello, notemos que deberemos derivar con respecto a la magnitud $\delta (T,\mu)$. Por lo tanto, tendremos que fijarnos en el lado izquierdo de la ecuación {eq}`upsilon_sph_good`; es decir,

$$
 \overline{N} := -\left(\frac{\partial \mathscr{E}(T,\mu)}{\partial\mu}\right)_T = \left(\frac{\partial\ln\Upsilon}{\partial\frac{\mu}{k_{\mathrm{B}}T}}\right)_T = \left(\frac{\partial\ln\Upsilon}{\partial\delta}\right)_{\alpha,\beta}\left(\frac{\partial\delta}{\partial\frac{\mu}{k_{\mathrm{B}}T}}\right)_T = \frac{48\alpha^{1/2}-45\pi^{1/2}\beta}{4\alpha^{3/2}(3\pi^{1/2}\alpha^{1/2}-6\beta)}\; .
$$ (bar_n_sph)

Es importante destacar que, puesto que trabajamos en el límite $\mu\rightarrow\mu ^ {(0)} (T) $, la magnitud $\overline {N} $ se ha convertido en una función dependiente solamente de la temperatura. Por otro lado, para escribir las expresiones de la entropía y laenergía interna, nos será útil obtener también los promedios $\overline {N ^ {2/3}} $ y $\overline {N ^ {1/3}} $. Por lo tanto, deberemos construir previamente la función probabilística $P(N)$:

$$
P(N)\;\mathrm{d}N = \frac{e^{-\alpha N^{2/3}}e^{-\beta N^{1/3}}}{\Upsilon} \mathrm{d}N \approx \frac{e^{-\alpha N^{2/3}}\left(1-\beta N^{1/3}\right)}{\Upsilon} \mathrm{d}N\; .
$$ (p_n_sph)

Hecho esto, llegaremos a los siguientes resultados:

$$
\overline{N^{2/3}} = \int_0^{\infty}\mathrm{d}NP(N)\;N^{2/3} = \frac{1}{\Upsilon}\left(\frac{9\pi^{1/2}}{8\alpha^{5/2}}-\frac{3\beta}{\alpha^3}\right) \; ,
$$ (bar_n23_sph)

$$
\overline{N^{1/3}} = \int_0^{\infty}\mathrm{d}NP(N)\;N^{1/3} = \frac{1}{\Upsilon}\left(\frac{3}{2\alpha^2}-\frac{9\pi^{1/2}\beta}{8\alpha^{5/2}}\right) \; .
$$ (bar_n13_sph)

Una vez obtenidas estas ecuaciones, la expresión del promedio de la energía interna es inmediata, si atendemos a su definición. Atendamos a la ecuación {eq}`bar_e_tmu_sph_def`.

$$
\overline{E}(T,\mu) =\frac{\sum_E\sum_N\Omega(E,N)\;e^{-E/k_{\mathrm{B}}T}e^{\mu N/k_{\mathrm{B}}T}}{\Upsilon(T,\mu)} = \frac{\sum_N \overline{E}(T,N)\;Q(T,N)\;e^{\mu N/k_{\mathrm{B}}T}}{\Upsilon(T,\mu)}
$$ (bar_e_tmu_sph_def)

Primero, debemos calcular el promedio de $E (S, N) $, utilizando la función $\Omega (E, N) $ obtenida del análisis en el colectivo microcanónico. Desde allí llegaremos la expresión $\overline {E} (T, N) $. Pues bien, su promedio a través de la magnitud $N $ nos devolverá la magnitud deseada, $\overline {E} (T,\mu) $. Así, sustituyendo las funciones $N $, $N ^ {2/3} $ y $N ^ {1/3} $ de la ecuación {eq}`bar_e_tmu_sph_def` en la parte derecha de la ecuación {eq}`bar_e_tmu_sph_def`, obtendremos sus respectivos promedios, de manera que la expresión del promedio de de energía interna quedará

$$
\overline{E}(T,\mu) = \overline{N}k_{\mathrm{B}}T^2\frac{1}{j}\frac{\mathrm{d}j}{\mathrm{d}T} + \overline{N^{2/3}}\left(a -T\frac{\mathrm{d}a}{\mathrm{d}T}\right) + \overline{N^{1/3}}\left(b -T\frac{\mathrm{d}b}{\mathrm{d}T}\right) \; .
$$ (bar_e_tmu_sph)

Una vez más, tal como indica el dúo {eq}`bar_e_tn_sph` y  {eq}`bar_e_tmu_sph`, las variables ambientales influyen a las propiedades de los sistemas pequeños. De hecho, aunque fijemos la relación $N =\overline {N} $, las dos expresiones de la energía interna no coincidirán, debido a las fluctuaciones en torno a las magnitudes $N ^ {2/3} $ y $N ^ {1/3} $. Debemos percatarnos de que $\overline{N}^{2/3}\neq \overline{N^{2/3}}$ y $\overline{N}^{1/3}\neq \overline{N^{1/3}}$.

También escribiremos la ecuación que obdecerá el potencial de subdivisión:

$$
\mathscr{E}(T,\mu) = -k_{\mathrm{B}}T\ln\left(\frac{3\pi^{1/2}}{4\alpha^{3/2}} - \frac{3\beta}{2\alpha^2}\right)\; .
$$ (sph_epsilon_nc)

Este es el último componente que necesitaremos para construir la entropía $S (T,\mu) $. De hecho, en este ejemplo en concreto, reescribiremos la ecuación {eq}`e_small` del sistema pequeño de esta forma: 

$$
\overline {E} = TS +\mu ^ {(0)} N +\mathscr {E} \; .
$$ (e_small_agg_es)

Recordemos que, por un lado, hemos descartado desde el principio la contribución del grado de libertad mecánico; por otro, el valor del potencial químico es el límite $\mu ^ {(0)} $. Por lo tanto, despejando la magnitud $S$ de la ecuación {eq}`e_small_agg_es`, la entropía que nos devolverá la colectividad nanocanónica es


$$
\boxed{S(T, \mu) =  \overline{N}k_{\mathrm{B}}\left(\ln j + T\frac{1}{j}\frac{\mathrm{d}j}{\mathrm{d}T}\right) - \overline{N^{2/3}}\frac{\mathrm{d}a}{\mathrm{d}T} - \overline{N^{1/3}}\frac{\mathrm{d}b}{\mathrm{d}T} + k_{\mathrm{B}}\ln\left[\frac{1}{\overline{N}}\left(\frac{3}{\alpha^3}-\frac{45\pi^{1/2}\beta}{16\alpha^{7/2}}\right)\right] + \overline{N^{2/3}}\frac{a}{T} + \overline{N^{1/3}}\frac{b}{T}} \; .
$$ (s_sph_agg_tmu)

Fijémonos en la expresión; y, al hilo de lo que hemos hecho en varias ocasiones anteriores, pongámoslo de par en par con la ecuación {eq}`s_sph_agg_tn`.

Pues bien, en la ecuación $S (T,\mu) $ aparecen tres términos adicionales. Es evidente que los dos últimos (positivos) son los responsables del aumento de la entropía debido a fluctuaciones en torno a las magnitudes $N ^ {2/3} $ y $N ^ {1/3} $. Sin embargo, el antepenúltimo término, relacionado con el potencial de subdivisión, requiere un análisis más profundo. De hecho, para que el logaritmo devuelva un valor positivo, debemos hacer cumplir los siguientes requisitos: $\alpha < 1 $ y $\alpha\gg\beta $. La segunda exigencia sí que es compatible con las condiciones anteriormente presentadas. En efecto, así podremos mantener solamente el primer término dentro de los paréntesis. Por tanto, nos es lícito prescindir de los efectos de curvatura.

Así, tomando el límite $\beta\rightarrow 0 $, reescribiremos la ecuación {eq}`bar_n_sph`, el potencial de subdivisión y el término de la entropía asociado a él. En primer lugar, sin embargo, adaptaremos la magnitud $\overline {N} $, partiendo de la ecuación {eq}`bar_n_sph`:

$$
\overline{N} \approx \frac{4}{\pi^{1/2}\alpha^{3/2}} \; ,
$$ (bar_n_sph_approx)

$$
\mathscr{E}(T,\mu) \approx -k_{\mathrm{B}}T\ln\left(\frac{3\pi^{1/2}}{4\alpha^{3/2}}\right) = -k_{\mathrm{B}}T\ln\left(\frac{3\pi\overline{N}}{16}\right) \; ,
$$ (sph_epsilon_nc_approx)

$$
k_{\mathrm{B}}\ln\left[\frac{1}{\overline{N}}\left(\frac{3}{\alpha^3}-\frac{45\pi^{1/2}\beta}{16\alpha^{7/2}}\right)\right] \approx k_{\mathrm{B}}\ln\left(\frac{3\pi\overline{N}}{16}\right) > 0 \; .
$$ (approx)

El límite utilizado pone de manifiesto la verdadera naturaleza de este término problemático; de hecho, en realidad, toma consideración de fluctuaciones en torno al número de partículas $N $, aumentando así la entropía.


Es destacable que, debido a que se cumple que $N \gg N^{2/3}, \; N^{1/3}$ y $\overline{N} \gg \overline{N^{2/3}}, \; \overline{N^{1/3}}, \; \ln \overline{N}$, las ecuaciones {eq}`s_sph_agg_tn` y {eq}`s_sph_agg_tmu` coinciden, en el límite macroscópico, con los resultados desarrollados en en la {numref}`subsección {number} <mupt_linagg>` con el agregado lineal, esto es,

$$
\boxed{\begin{gathered}
    (a) \quad S(T,\mu) > S(T,N) \\
    \\
   (b) \quad  \frac{S(T,\mu)}{\overline{N}k_{\mathrm{B}}}\equiv \frac{S(T,N)}{Nk_{\mathrm{B}}} = \frac{\mathrm{s}^{(0)}}{k_{\mathrm{B}}} = \ln j + T\frac{1}{j}\frac{\mathrm{d}j}{\mathrm{d}T} \quad (\overline{N},N\rightarrow\infty)\\
   \\
   (c) \quad \frac{\overline{E}(T,N)}{N} \equiv \frac{\overline{E}(T,\mu)}{\overline{N}} = \mathrm{e}^{(0)} = k_{\mathrm{B}}T^2\frac{1}{j}\frac{\mathrm{d}j}{\mathrm{d}T} \quad (\overline{N},N\rightarrow\infty)
\end{gathered}}
$$

```{admonition} Nota
En el caso del agregado lineal, a diferencia del presente ejemplo, tuvimos en cuenta la energía de interacción $\epsilon $ entre primeros vecinos. Por ello, la energía interna es, en realidad, $N\left (k_ {\mathrm {B}} T ^ 2\frac {1} {j}\frac {\mathrm {d} j} {\mathrm {d} T} +\epsilon\right) $.
```

Parece, por tanto, que, en el límite macroscópico, el hecho de que el agregado sea lineal o esférico no influye de ninguna manera en funciones termodinámicas como la energía interna y la entropía. Precisamente, para que afloren las aportaciones correspondientes a __la forma__ del sistema, resulta imprescindible recurrir a la Nanotermodinámica.


##### Ejercicio
El objetivo de este ejercicio consiste en trasladar el análisis general realizado hasta ahora al límite  $b (T) = 0 $. Así, descartando por completo los efectos de curvatura y considerando únicamente la aportación de superficie $a (T) N ^ {2/3} $, recuperaremos de paso los resultados del libro de Hill {cite}`hill`.


$(a)$ Ya hemos calculado la expresión que cumple el potencial de subdivisión en estas condiciones (ecuación {eq}`sph_epsilon_nc_approx`). Haz lo mismo con las magnitudes:

$$
\widehat{\mu},\;\mu,\; S(T,N),\;\overline{E}(T,N),\;\Upsilon(T,\mu),\;\overline{N},\;\overline{E}(T,\mu), \; S(T,\mu)
$$

$(b)$ Comprueba que la expresión $S (T,\mu) $ de la entropía del apartado $(a) $ también puede obtenerse recurriendo a su definición, esto es,

$$
S(T,\mu) := \frac{\partial}{\partial T}\left(k_{\mathrm{B}}T\ln\Upsilon\right)_\mu \; .
$$ (sph_agg_s_def)

Para ello, ten en cuenta la dependencia de la función de partición generalizada respecto a la variable $T$, es decir,
 $\Upsilon(T,\mu) = \Upsilon(\alpha(T),\delta(T,\mu))$.

**----------------------------------------------------**

##### Ejercicio
Esta vez, trasladamos el ejercicio anterior al límite contrario. De hecho, sólo trabajaremos con la aportación de la curvatura. Así, de paso, conseguiremos que emerja la influencia real de la propia curvatura en las funciones termodinámicas del sistema. De hecho, recordemos que, al hilo del aportación interna del logaritmo de la ecuación {eq}`s_sph_agg_tmu`, hemos tenido que imponer la condición $\beta = 0 $ para que este término tenga una contribución positiva a la entropía. De hecho, fijémonos en que el aumentar la magnitud $\beta $ asociada a la curvatura impediría lo anterior. Por ello, podríamos pensar que la incorporación de efectos de curvatura  bajaría la entropía del sistema.

Ante ello, debemos andar con cautela, dado que todas las expresiones utilizadas hasta ahora son solamente válidas en el límite $\beta\rightarrow 0 ^ + $. Este límite ha permitido, ante todo, eludir el cálculo escabroso de la integral de la ecuación {eq}`upsilon_sph_int`, ateniéndonos únicamente a los primeros dos términos de la serie de Taylor de la función $e^{-\beta N^{1/3}}$. Por consiguiente, no nos será lícito reconducir la reflexión presentada en el párrafo anterior a través de los resultados obtenidos previamente, ya que ello nos llevará por el camino equivocado.

Para esclarecer esta difusa situación, en este ejercicio reiniciaremos el análisis llevado a cabo a lo largo de todo el apartado, descartando por completo los efectos de superficie y centrando toda nuestra atención en las aportaciones derivadas de la curvatura. Por ello, el punto de partida es la función de partición canónica

$$
Q(T,N) = j(T)^N\;e^{-\beta(T)N^{1/3}} \; .
$$ (sph_agg_q_b)


$(a)$ Recalcula las siguientes magnitudes, partiendo de la ecuación {eq}`sph_agg_q_b`:

$$ 
\mu^{(x)}(T,N), \; S(T,N), \; \overline{E}(T,N), \; \Upsilon(T,\mu), \; P(N), \; \overline{N}, \; \mathscr{E}(T, \mu), \; \overline{N^{1/3}},\; \overline{E}(T,\mu), \; S(T,\mu) \; .
$$

```{dropdown} __Solución__

Primeramente, tenemos que

$$
\widehat{\mu}N = -Nk_{\mathrm{B}}T \ln j +  N^{1/3}b(T) \; .
$$ (sph_agg_nmu_b)

Desde ahí,

$$
S(T,N) = Nk_{\mathrm{B}} \ln j + Nk_{\mathrm{B}}T\frac{1}{j}\frac{\mathrm{d}j}{\mathrm{d}T} - N^{1/3}\frac{\mathrm{d}b}{\mathrm{d}T} 
$$ (sph_agg_stn_b)

y

$$
\overline{E}(T,N)  = Nk_{\mathrm{B}}T^2\frac{1}{j}\frac{\mathrm{d}j}{\mathrm{d}T}  + N^{1/3}\left(b -T\frac{\mathrm{d}b}{\mathrm{d}T}\right) \; .
$$ (sph_agg_ebar_b)

Pues bien, admitiremos que las explicaciones acerca de la tensión superficial $a (T) N ^ {2/3} $, expuestas ante la ecuación {eq}`upsilon_sph_int`, también son válidas en esta situación; es decir, la magnitud $N $ deberá ser lo suficientemente grande como para poder percibir el efecto de la tensión de curvatura $b (T) N ^ {1/3} $. Por ello, ahora también podremos calcular la función de partición generalizada $\Upsilon (T,\mu) $ mediante una integral:

$$
\Upsilon (T,\mu) \underset{(\delta \rightarrow 0^{+})}{\boldsymbol{\approx}} \int_0^\infty \mathrm{d}N\;\left(1-\delta N\right) \; e^{-\widehat{\mu}N/k_{\mathrm{B}}T} =\int_0^\infty \mathrm{d}N\;\left(1-\delta N\right) \; e^{-\beta N^{1/3}} = \frac{6}{\beta^3}-\frac{360\delta}{\beta^6}
$$ (upsilon_sph_agg_b)

La función de probabilidad modificada es

$$
P(N) \;\mathrm{d}N = \frac{e^{-\beta N^{1/3}}}{\Upsilon} \;\mathrm{d}N \underset{(\delta \rightarrow 0^{+})}{\boldsymbol{\approx}} \frac{6 e^{-\beta N^{1/3}}}{\beta^3} \;\mathrm{d}N \; .
$$ (agg_sph_pn_b)

Así, siguiendo a la ecuación {eq}`agg_sph_pn_b`,

$$
\overline{N} = \int_0^{\infty}\mathrm{d}NP(N)\;N = \frac{60}{\beta^3} \; .
$$ (agg_sph_barn_b)

Es conveniente reconstruir la magnitud $\overline {N} $ que acabamos de calcular recurriendo a su definición, al igual que en la ecuación anterior {eq}`bar_n_sph`, y verificar que ambos resultados coinciden. Por otra parte, al comparar las ecuaciones {eq}`upsilon_sph_agg_b` y {eq}`agg_sph_barn_b`, es evidente que $\Upsilon =\overline {N}/10 $. En consecuencia, podemos escribir el potencial de subdivisión como

$$
\mathscr{E}(T,\mu) = -k_{\mathrm{B}}T\ln\left(\frac{\overline{N}}{10}\right) < 0 \; .
$$ (agg_sph_epsilon_tmu_b)

Además de eso,

$$
\overline{N^{1/3}} = \int_0^{\infty}\mathrm{d}NP(N)\;N^{1/3} = \frac{3}{\beta} \; ,
$$ (agg_sph_barn13_b)

y, recurriendo de nuevo a la definición {eq}`bar_e_tmu_sph_def`, tendremos que el promedio de la energía interna es

$$
\overline{E}(T,\mu) = \overline{N}k_{\mathrm{B}}T^2\frac{1}{j}\frac{\mathrm{d}j}{\mathrm{d}T} + + \overline{N^{1/3}}\left(b -T\frac{\mathrm{d}b}{\mathrm{d}T}\right) \; ,
$$ (bar_e_tmu_sph_b)

y, empleando la expresión $S(T,\mu) = \frac{1}{T}\left[\overline{E}(T,\mu) - \mu^{(0)}N - \mathscr{E}(T,\mu)\right]$, llegaremos a esta ecuación para la entropía:

$$
\boxed{S(T, \mu) =  \overline{N}k_{\mathrm{B}}\left(\ln j + T\frac{1}{j}\frac{\mathrm{d}j}{\mathrm{d}T}\right)  - \overline{N^{1/3}}\frac{\mathrm{d}b}{\mathrm{d}T} + k_{\mathrm{B}}\ln\left(\frac{\overline{N}}{10}\right)  + \overline{N^{1/3}}\frac{b}{T}} \; .
$$ (s_sph_agg_tmu_b)

Pues bien, comparándola con la ecuación {eq}`sph_agg_stn_b`, podremos observar claramente que la nueva expresión tiene dos aportaciones positivas; una relacionada con el potencial de subdivisión negativo, y la otra con variaciones en torno a $N ^ {1/3} $. Ambas mantienen una estrecha relación, fundamentalmente, con las fluctuaciones asociadas al número de partículas $N $ en la región nanotermodinámica. En este concepto profundizaremos en el siguiente apartado del ejercicio.

```

$(b)$ Verifica, recurriendo a la expresión $P(N)\;\mathrm{d}N$ de la ecuación {eq}`agg_sph_pn_b`, que las aportaciones adicionales a la entropía que hemos obtenido en la colectividad nanocanónica, las cuales quedan recogidas en el término de exceso $S^{(x)}(T,\mu)$, son consecuencia de las fluctuaciones alrededor de la magnitud $N$.


```{dropdown} __Solución__

Dado que a lo largo de todo el apartado hemos considerado a $N$ como variable continua, la contribución a la entropía de las fluctuaciones en $N$ deberá cumplir la siguiente expresión:

$$
S^{(x)}(T,\mu) := -k_{\mathrm{B}}\int_0^\infty \mathrm{d}N\; P(N) \;\ln P(N)  \; .
$$ (s_x_sph_agg_b)

Así pues, desarrollemos la integral:

$$
\int_0^\infty \mathrm{d}N\; P(N) \;\ln P(N) = \frac{1}{\Upsilon}\left[-\ln\Upsilon\int_0^\infty \mathrm{d}N\;e^{-\beta N^{1/3}} -\int _0^\infty \mathrm{d}N\; N^{1/3}e^{-\beta N^{1/3}} \right] = \frac{10}{\overline{N}}\left[\ln\left(\frac{10}{\overline{N}}\right)\frac{6}{\beta^3}-\frac{18}{\beta^3}\right] \; .
$$

Reorganizaremos este resultado por medio de las expresiones {eq}`agg_sph_barn_b` y {eq}`agg_sph_barn13_b`:

$$
\int_0^\infty \mathrm{d}N\; P(N) \;\ln P(N) = \ln\left(\frac{10}{\overline{N}}\right) - \overline{N^{1/3}}\frac{b}{k_{\mathrm{B}}T} \; .
$$

Atendiendo a la ecuación {eq}`s_x_sph_agg_b` de arriba, podemos percibir facilmente que el término de exceso de la entropía cumple 

$$
S^{(x)}(T,\mu) = k_{\mathrm{B}}\ln\left(\frac{\overline{N}}{10}\right) + \overline{N^{1/3}}\frac{b}{T} \; .
$$ (s_x_sph_agg_b_1)

Hemos demostrado, por lo tanto, que para valores medianamente grandes de $\overline {N} $, el aumento en la entropía del sistema tiene una relación directa con las fluctuaciones de $N $ (observemos que el término correspondiente a la magnitud $b $ es la constante $3k_ {\mathrm {B}} $, por lo que, a medida que aumenta $\overline {N} $, se volverá despreciable con respecto al término $\ln\overline {N} $).


```

**----------------------------------------------------**

(mupt_id_lattice)=
### Gas en una red ideal

Este ejemplo se trabaja en varios apartados del libro {cite}`hill`. En efecto, analizaremos el mismo sistema en los colectivos microcanónico, isobárico, macrocanónico y  nanocanónico ({numref}`figura {number} <lattice_multzo>`); en particular, nos centraremos en la evolución de la entropía en función del potencial de subdivisión, como bien hicimos en varios ejemplos anteriores, por ejemplo, en la {numref}`subsección {number} <mupt_gi>`.

Dicho esto, el sistema que tenemos entre manos es una red constituida por $B$ celdas distinguibles. De ellas, $N $ celdas contienen una molécula, de modo que las $N$ moléculas (indistinguibles) componen el gas de la red cristalina. También descartaremos la energía de interacción y cualquier grado de libertad interno (rotación, vibración...), de forma que la única energía accesible del sistema es $E = 0 $. Así las cosas, solo tendremos en cuenta el aporte mecánico y químico a la energía del sistema. La variable extensiva que vamos a asignar a la primera es la magnitud $B $, por lo que el aporte mecánico a la energía será $-pB $. Tengamos en cuenta que, como $B $ es adimensional, las dimensiones de su variable conjugada $p $ corresponden a las de la energía. La contribución química, obviamente, vendrá determinada por el potencial químico y el número de moléculas: $\mu N $.

```{figure} lattice_1.png
---
height: 600px
name: lattice_multzo
---
Representación gráfica del sistema en los colectivos estadísticos que vamos a estudiar. En la colectividad microcanónica, los subsistemas no se ven entre ellos, y cada uno representa un microestado compatible con las condiciones $B = 25 $ y $N = 9 $. A medida que modificamos las variables de ambiente bajo nuestro control, otorgaremos a los subsistemas la libertad para intercambiar celdas y/o partículas. El colectivo nanocanónico dispone de ambos grados de libertad en marcha.
```

#### Colectividad microcanónica: variables de entorno $(B,N)$ 

Iniciaremos, pues, el análisis, en el **colectivo microcanónico**, el cual quedará especificado por las variables de control $(B, N) $. Dado que las moléculas son indistinguibles entre ellas, el número de microestados viene dado por

$$
\Omega(B,N) = \frac{B!}{N!\;(B-N)!} \; .
$$ (lattice_omega)

Al calcular la entropía, mantendremos los primeros cuatro términos de la serie de Stirling (ecuación {eq}`stirling` del [_apéndice C_](gitvn)). Así,

$$
\boxed{\frac{S(B,N)}{k_\mathrm{B}} = \ln\Omega = B\ln B-N\ln N-(B-N)\ln(B-N)-\frac{1}{2}\ln\left[2\pi\frac{(B-N)N}{B}\right] - \frac{1}{12}\left[\frac{1}{N}+\frac{1}{B-N}-\frac{1}{B}\right]} \; .
$$ (lattice_s_mc)


Para calcular el potencial de subdivisión, debemos tener en cuenta los desarrollos del {numref}`apartado {number} <hillteo>`. Comenzaremos escribiendo la ecuación del sistema pequeño y la ecuación de Gibbs:

$$
E = TS-pB+\mu N + \mathscr{E} \; ,
$$ (lattice_E)

$$
\mathrm{d}E = T\mathrm{d}S-p\mathrm{d}B+\mu \mathrm{d}N \; .
$$ (lattice_dE)

Por tanto, recordando que en las condiciones expuestas al principio tenemos que $E = 0 $, reescribiremos las ecuaciones {eq}`lattice_E` y {eq}`lattice_dE`:

$$
S = \frac{p}{T}B - \frac{\mu}{T}N - \frac{\mathscr{E}}{T} \; ,
$$ (lattice_S)

$$
\mathrm{d}S = \frac{p}{T}\mathrm{d}B - \frac{\mu}{T}\mathrm{d}N \; .
$$ (lattice_dS)

Siguiendo la última expresión, calcularemos las variables $p $ y $\mu $:

$$
p = T\left(\frac{\partial S}{\partial B}\right)_{N} = k_{\mathrm{B}}T\left\{\ln\left(\frac{B}{B-N}\right) - \frac{N}{2B(B-N)} + \frac{1}{12}\left[\frac{1}{(B-N)^2}-\frac{1}{B^2}\right]\right\} \; ,
$$ (lattice_p_mc)

$$
\mu = -T\left(\frac{\partial S}{\partial N}\right)_{B} = k_{\mathrm{B}}T\left\{\ln\left(\frac{N}{B-N}\right) + \frac{B-2N}{2N(B-N)} + \frac{1}{12}\left[\frac{1}{(B-N)^2}+\frac{1}{N^2}\right]\right\} \; .
$$ (lattice_mu_mc)

Así las cosas, empleando la relación $\mathscr{E} = -TS + pB -\mu N$,

$$
\mathscr{E} = k_{\mathrm{B}}T\left\{\frac{1}{2} + \frac{1}{2}\ln\left[2\pi\frac{(B-N)N}{B}\right]+\frac{1}{6}\left(\frac{1}{N}-\frac{1}{B}+\frac{1}{B-N}\right)\right\} \; .
$$ (lattice_epsilon_mc)


#### Colectividad isobárica: variables de entorno $(\frac{p}{T}, N)$

Arranquemos ahora el grado de libertad mecánico. Así, reanudaremos el análisis del sistema mediante las variables $\left (\frac {p} {T}, N\right) $ en el **colectivo isobárico**. Para empezar, la función de partición es

$$
\Delta \left(\frac{p}{T},N\right) = \sum_{{B=N}}^{{\infty}}\Omega(B,N)e^{-pB/k_{\mathrm{B}}T} = \frac{e^{-pN/k_{\mathrm{B}}T}}{\left(1-e^{-p/k_{\mathrm{B}}T}\right)^{N+1}} = \frac{x^N}{\left(1-x\right)^{N+1}} \; .
$$ (lattice_Delta)


En el último paso hemos insertado la variable $x = e ^ {p/k_ {\mathrm {B}} T} $. Percatémonos, además, de los límites del sumatorio. En concreto, a la hora de poner en marcha el grado de libertad mecánico, el límite inferior será fijado por la variable $N $ $(B=N)$, ya que la red cristalina deberá contar, al menos, con un mínimo numero de celdas para albergar los $N$ componentes moleculares del gas.


```{dropdown} __Desarrollo de la serie__

Hemos a continuación el procedimiento para calcular la serie de la ecuación {eq}`lattice_Delta`:


En primer lugar, modificaremos la expresión interna del sumatorio por medio de un cambio de variable:

$$
 \Delta = \frac{1}{N!}\sum_{{B=N}}^{{\infty}}\frac{B!}{(B-N)!}x^{B} \underset{(M=B-N)}{=} \frac{1}{N!}\sum_{{M=0}}^{{\infty}}\frac{(M+N)!}{N!}x^{M+N}
$$

A continuación fijémonos en la siguiente igualdad:

$$
\frac{\mathrm{d}^{N}}{\mathrm{d}x^{N}}\;x^{N+M} = \frac{(M+N)!}{N!}x^{M} \; .
$$

Con ayuda de la última expresión, reescribiremos el contenido del sumatorio de esta forma:

$$
\frac{1}{N!}\sum_{{M=0}}^{{\infty}}\frac{(M+N)!}{N!}x^{M+N} =   \frac{1}{N!}\;\frac{\mathrm{d}^{N}}{\mathrm{d}x^{N}}\left[x^{N}\sum_{{M=0}}^{{\infty}}x^{M}\right]\underset{\vert x\vert < 1}{=} \frac{1}{N!}\frac{\mathrm{d}^{N}}{\mathrm{d}x^{N}} \left[\frac{x^N}{1-x}\right] = \frac{1}{N!}\left[\frac{N!\; x^N}{(1-x)^{N+1}}\right]
$$

Hecho esto, hemos llegado a nuestro objetivo:

$$
\boxed{\Delta = \frac{x^N}{\left(1-x\right)^{N+1}}} \; .
$$


```

Seguidamente, de la relación $\Delta = e^{-F/k_{\mathrm{B}}T}$, extraeremos la energía libre de Gibbs:

$$
F\left(\frac{p}{T}, N\right) = N\widehat{\mu} = k_{\mathrm{B}}T\left[-N\ln x + (N+1)\ln(1-x)\right] \; .
$$ (lattice_F)

Con esta ecuación, llegaremos a las expresiones de los potenciales químicos integral y diferencial, así como al potencial de subdivisión:

$$
\widehat{\mu} = k_{\mathrm{B}}T\left[-\ln x + \frac{N+1}{N}\ln(1-x)\right] \; ,
$$ (lattice_muhat_iso)

$$
\mu = k_{\mathrm{B}}T\ln\left(\frac{1-x}{x}\right) \; ,
$$ (lattice_mu_iso)

$$
\mathscr{E} = k_{\mathrm{B}}T\ln\left(1-x\right) \; .
$$ (lattice_epsilon_iso)

Reparemos en que $\mu^{(x)} = 0$; en consecuencia, en el límite macroscópico tendremos que $\widehat{\mu} = \mu^{(0)} \equiv \mu$.

Además, calcularemos el promedio del número de celdas:

$$
\overline{B} = \frac{\sum_B B \;\Omega(B,N)e^{-pB/k_{\mathrm{B}}T}}{\sum_B \Omega(B,N)e^{-pB/k_{\mathrm{B}}T}} = -k_{\mathrm{B}}T\;\frac{\partial }{\partial p}\ln \Delta = k_{\mathrm{B}}T\frac{\partial(F/ k_{\mathrm{B}}T)}{\partial p} = \frac{N+x}{1-x} \; .
$$ (lattice_bbar)

Reorganizando la expresión podemos escribir también la ecuación de estado del sistema:

$$
\frac{p}{k_{\mathrm{B}}T} = \ln\left(\frac{1+\overline{B}}{\overline{B}-N}\right) \underset{(\overline{B},\; N \; \rightarrow\; \infty)}{=} -\ln\left(1-\frac{N}{\overline{B}}\right) \; .
$$ (lattice_eq_state)


Finalmente, construimos la expresión $S\left (\frac {p} {T}, N\right) $. Para ello, escribamos en primer lugar la función probabilística correspondiente al presente colectivo estadístico:

$$
P(B) = \frac{e^{-pB/ k_{\mathrm{B}}T}}{\Delta} \; .
$$ (lattice_pb)

De este modo, atendiendo a la definición de la entropía (ecuación {eq}`entropy_def` del [_apéndice B_](entropy)), y con la ayuda de la ecuación {eq}`lattice_bbar`, llegaremos a

$$
S\left(\frac{p}{T}, N\right) = -k_{\mathrm{B}}\sum_BP(B)\;\ln P(B) = \frac{p\overline{B}}{T} + k_{\mathrm{B}}\ln\Delta = \frac{p\overline{B}}{T} - \frac{\widehat{\mu}N}{T} \; .
$$ (lattice_s_iso_def)

Sustituyendo las magnitudes $\overline{B}$ y $\widehat{\mu}$ previamente calculadas,

$$
\boxed{\frac{S\left(\frac{p}{T}, N\right) }{k_\mathrm{B}} =  (\overline{B}+1)\ln (\overline{B}+1) -(N+1)\ln (N+1)-(\overline{B}-N)\ln(\overline{B}-N)} \; .
$$ (lattice_s_iso)

La expresión obtenida es absolutamente exacta, es decir, no hemos recurrido a la aproximación de Stirling. Por ello, es válido para sistemas tan pequeños como se desee (incluso para el caso de $N = 1 $). En este sentido, resultará interesante analizar el mismo sistema en el colectivo macrocanónico, y comparar la ecuación de la entropía $S\left(B, \frac{\mu}{T}\right)$ con la expresión que acabamos de construir, contemplando, ante todo, a las correcciones de tamaño finito en ambos casos. De hecho, fijémonos en que las colectividades macrocanónica e isobárica son equivalentes (_semiabiertas_), ya que en ambas disponen de un único grado de libertad en marcha.

#### Colectividad macrocanónica: variables de entorno $(B, \frac{\mu}{T})$ 

Pongamos en marcha solamente el grado de libertad químico, para construir la función de partición macrocanónica:

$$
\Xi\left(B,\frac{\mu}{T}\right) = \sum_{{N=0}}^{{B}}\;\Omega(B,N)\;e^{\mu N/k_{\mathrm{B}}T} = \sum_{N=0}^B \frac{B!}{N!(B-N)!}\;\lambda^N = (1+\lambda)^B \; ,
$$ (lattice_xi)

donde, al igual que en ocasiones anteriores, hemos sustituido $\lambda = e^{\mu/k_{\mathrm{B}}T}$. En cuanto al cálculo del sumatorio, al lector puede resultarle útil la nota que sigue a la ecuación {eq}`q_ising`.

Ahora, teniendo en cuenta las explicaciones del {numref}`apartado {number} <replica_e>`, asumiremos que la magnitud integral $\widehat {p} $ satisfará la igualdad $\xi = e ^ {\widehat {p} B/k_ {\mathrm {B}} T} $, ya que ésta fijará la contribución mecánica al nivel del colectivo estadístico. Así las cosas, observando la ecuación {eq}`lattice_xi`, veremos que la variable diferencial $p $ coincide con la integral $\widehat{p}$, es decir:

$$
p =\left[\frac{\partial (\widehat{p}B)}{\partial B}\right]_{T,\mu} = k_{\mathrm{B}}T\ln \left(1+\lambda\right) = \widehat{p} \; .
$$ (lattice_p_phat)


Por tanto, dado que el potencial de subdivisión engloba las aportaciones que diferencian ambas variables, se cumplirá que

$$
\mathscr{E} = -(\widehat{p}-p)B = 0 \; .
$$ (lattice_epsilon_gc)


```{admonition} Nota

Debido a los resultados anteriores, los términos de exceso son nulos, es decir $\widehat {p} ^ {(x)} = p ^ {(x)} = 0 $. En otras palabras, ambas presiones cumplirán $\widehat {p} = p = p ^ {(0)} $ en el límite macroscópico.

```

En lo que respecta al promedio del número de partículas,

$$
\overline{N} = \left[\frac{\partial (\widehat{p}B)}{\partial \mu}\right]_{T,B} = \frac{B\lambda}{1+\lambda} \; .
$$ (lattice_nbar)

Por consiguiente,

$$
\widehat{p} = p = -k_{\mathrm{B}}T\ln\left(1-\frac{\overline{N}}{B}\right) \; .
$$ (lattice_p_phat_new)

Construyamos ahora la expresión de la entropía.


##### Ejercicio

Escribe la distribución probabilística correspondiente a la presente colectividad estadística. A través de ella, escribe la ecuación que deberá cumplir la entropía. Por último, adapta la expresión para que en ella figuren las variables $B $ y $\overline {N} $.

```{dropdown} __Solución__

$$
P(N) = \frac{e^{\mu N/k_{\mathrm{B}}T}}{\Xi}
$$ (lattice_pn)

Así las cosas, la entropía abarcará las fluctuaciones relativas a la magnitud $N $, es decir,

$$
S\left(B,\frac{\mu}{T}\right) = -k_{\mathrm{B}}\sum_N P(N)\ln P(N) = k_{\mathrm{B}}\ln\Xi -\frac{\mu\overline{N}} {T}  = \frac{\widehat{p}B} {T} - \frac{\mu\overline{N}} {T} \; .
$$ (lattice_s_gc_def)

Deberemos modificar esta expresión por medio de las ecuacioens {eq}`lattice_nbar` y {eq}`lattice_p_phat_new`.

```

**----------------------------------------------------**

Desarrollando la igualdad obtenida en el ejercicio anterior,

$$
\boxed{\frac{S\left(B,\frac{\mu}{T}\right) }{k_\mathrm{B}} =  B\ln B -\overline{N}\ln\overline{N} -(B-\overline{N})\ln (B-\overline{N})} \; .
$$ (lattice_s_gc)

La ecuación {eq}`lattice_s_gc` de la entropía también es exacta. Asimismo, cabe destacar que al transcurrir al límite macroscópico, esta expresión se mantendrá invariable; es decir, en este caso, el colectivo macrocanónico tampoco ha incorporado ninguna corrección de tamaño finito. Un claro indicador de ello es el potencial de subdivisión estrictamente nulo obtenido anteriormente (ecuación {eq}`lattice_epsilon_gc`).

Asimismo, comparándola con la ecuación {eq}`lattice_s_iso`, y aceptando que $\overline {B} = B$ y $\overline {N} = N $, se puede percibir un descenso en la entropía. De todas maneras, las correcciones son muy pequeñas, es decir, del orden $\mathscr {O} (1) $ con respecto a las variables $N $ y $B $.


La recta final consiste en abordar la reexaminación del sistema en la colectividad totalmente libre.


#### Colectividad nanocanónica: variables de entorno $(\frac{p}{T}, \frac{\mu}{T})$

La definición de la función de partición generalizada es la siguiente:

$$
\Upsilon\left(\frac{p}{T},\frac{\mu}{T}\right) = \sum_{B=0}^\infty\;\sum_{N=0}^B \; \Omega(B,N)\;e^{-pB/k_{\mathrm{B}}T}e^{\mu N/k_{\mathrm{B}}T} \; .
$$ (lattice_upsilon)

Para compactar las ecuaciones, desde ahora sustituiremos $\varphi = p/k_ {\mathrm {B}} T $ y $m =\mu/k_ {\mathrm {B}} T $. Además, es conveniente calcular primero el sumatorio a través de la variable $N $. Por lo tanto,

$$
\Upsilon = \sum_{B=0}^\infty\left[\sum_{N=0}^B \; \frac{B!}{N!(B-N)!}e^{mN}\right]e^{-\varphi B} = \sum_{B=0}^\infty\; (1+e^m)^B\; e^{-\varphi B} = \sum_{B=0}^\infty\; \Xi\left(B,\frac{\mu}{T}\right)\; e^{-\varphi B}\; .
$$ (lattice_upsilon_1)

Teniendo en cuenta la igualdad a la derecha de la ecuación superior, podemos adaptar la expresión interna del sumatorio de la siguiente manera:

$$
(1+e^m)^B = \Xi = e^{\widehat{p}B/k_{\mathrm{B}}T} = e^{p^{(0)}B/k_{\mathrm{B}}T} = e^{\varphi^{(0)}B}
$$ (lattice_moldatu)

Así, desarrollaremos la expresión de la función de partición nanocanónica:

$$
\Upsilon = \sum_{B=0}^\infty e^{(\varphi^{(0)}-\varphi) B} = \frac{1}{1-e^{\varphi^{(0)}-\varphi}} \; , \quad \varphi > \varphi^{(0)}(m)\; ,
$$ (lattice_upsilon_2)

donde, atendiendo a la ecuación {eq}`lattice_moldatu`, tenemos que $\varphi^{(0)}(m) = \ln(1+e^m)$. Esta reescritura nos servirá, por ejemplo, para calcular el promedio $\overline {N} (\varphi, m) $.

##### Ejercicio
$(a)$ Calcula $\overline{B}(\varphi, m)$. Al hacer esto, adapta la función de partición $\Upsilon $, para que dependa de la variable $\overline {B} $. Aparte de eso, reescribe la expresión $\overline {B} $ en el límite $\varphi -\varphi ^ {(0)}\ll 1 $.


```{dropdown} __Solución__

$$
\overline{B}(\varphi, m) = -k_{\mathrm{B}}T\left(\frac{\partial \ln \Upsilon}{\partial p}\right)_{\mu} \equiv -\left(\frac{\partial \ln \Upsilon}{\partial \varphi}\right)_{m} = \frac{e^{\varphi^{(0)}-\varphi}}{1-e^{\varphi^{(0)}-\varphi}}
$$ (lattice_bbar_nc)

Por tanto, $\Upsilon =\overline {B} + 1 $. Por otro lado, la ecuación {eq}`lattice_bbar_nc` nos dice que el límite mencionado en el enunciado garantizará que la magnitud $\overline {B} $ permanezca suficientemente elevada. Pues bien, considerando esto, de aquí en adelante emplearemos

$$
\overline{B} \approx \frac{1}{\varphi - \varphi^{(0)}} \; .
$$ (lattice_bbar_approx)

```

$(b)$ Construye ahora la magnitud $\overline{N} (\varphi, m)$, y, a través de los resultados obtenidos anteriormente, reescribe la expresión para que sólo aparezca bajo dependencia de $\overline {B} $ y $\varphi ^ {(0)} $.


```{dropdown} __Solución__

$$
\overline{N}(\varphi, m) = k_{\mathrm{B}}T\left(\frac{\partial \ln \Upsilon}{\partial \mu}\right)_{p} \equiv \left(\frac{\partial \ln \Upsilon}{\partial m}\right)_{\varphi} = \left(\frac{\partial \ln \Upsilon}{\partial \varphi^{(0)}}\right)_{\varphi} \frac{\mathrm{d}\varphi^{(0)}}{\mathrm{d}m} = \overline{B}\frac{e^m}{1+e^m} = \overline{B}\left(1-e^{-\varphi^{(0)}}\right)
$$ (lattice_nbar_nc)

```

**----------------------------------------------------**

Hay que destacar que la relación $\overline {N} /\overline {B} $ se mantiene invariable en el límite macroscópico. Esta última idea sugiere implícitamente que, cualquiera que sea el conjunto estadístico que utilicemos en el estudio, recuperaremos el mismo resultado en el límite termodinámico.
 

`````{admonition} Sugerencia
:class: tip
Para comprobar lo mencionado en la última frase, demuestra que las expresiones $N /\overline {B} $ del colectivo isobárico, $\overline {N}/B $ del colectivo macrocanónico y $\overline {N} /\overline {B} $ del colectivo nanocanónico cumplen la siguiente expresión en el límite termodinámico:

$$
\frac{N}{\overline{B}} = \frac{\overline{N}}{B} =\frac{\overline{N}}{\overline{B}} = \frac{e^{\mu/k_{\mathrm{B}}T}}{1+e^{\mu/k_{\mathrm{B}}T}}
$$

Para ese fin, emplea las siguientes ecuaciones: {eq}`lattice_mu_iso` y {eq}`lattice_eq_state` ; {eq}`lattice_nbar` ;  {eq}`lattice_nbar_nc`.

`````

Siguiendo el procedimiento utilizado en las dos subsecciones previas, la función probabilística perteneciente a la colectividad nanocanónica es

$$
P(B,N) = \frac{e^{-pB/k_{\mathrm{B}}T}e^{\mu N/k_{\mathrm{B}}T}}{\Upsilon} \; .
$$ (lattice_p_nc)

La entropía, por ende, cumplirá la siguiente expresión:

$$
S\left(\frac{p}{T},\frac{\mu}{T}\right) = -k_{\mathrm{B}}\sum_{B,\;N} P(B,N) \; \ln P(B,N) = \frac{p\overline{B}}{T} - \frac{\mu\overline{N}}{T} - \frac{\mathscr{E}}{T} \; ,
$$ (lattice_s_nc)

donde, por cierto, el potencial de subdivisión cumple la ecuación

$$
\mathscr{E} = -k_{\mathrm{B}}T\ln \Upsilon = -k_{\mathrm{B}}T\ln(\overline{B} + 1) \; .
$$ (lattice_epsilon_nc_def)

Por tanto,

$$
\boxed{\frac{S\left(\frac{p}{T},\frac{\mu}{T}\right) }{k_\mathrm{B}} =  (\overline{B}+1)\ln (\overline{B}+1) - \overline{N}\ln\overline{N} -(\overline{B}-\overline{N})\ln (\overline{B}-\overline{N})} \; .
$$ (lattice_s_gc)

La entropía ha vuelto a aumentar. Así las cosas, para terminar con el análisis que tenemos en marcha, resultará ilustrativo recoger todos los resultados obtenidos hasta el momento en la siguiente tabla:

```{list-table} Evolución del potencial de subdivisión, y consiguiente aumento de la entropía, a través de las diferentes colectividades.
:header-rows: 1
:name: taula_s_lattice

* - Variables
  - Potencial de subdivisión
  - Entropía
* - $\left(B,N\right)$
  - $\frac{\mathscr{E}}{k_{\mathrm{B}}T} \approx \frac{1}{2} + \frac{1}{2}\ln\left[2\pi\frac{(B-N)N}{B}\right] > 0$
  - $\frac{S}{k_\mathrm{B}} \approx B\ln B-N\ln N-(B-N)\ln(B-N)-\frac{1}{2}\ln\left[2\pi\frac{(B-N)N}{B}\right]$
* - $\left(B,\frac{\mu}{T}\right)$
  - $\mathscr{E} = 0$
  - $\frac{S}{k_{\mathrm{B}}} =  B\ln B -\overline{N}\ln\overline{N} -(B-\overline{N})\ln (B-\overline{N})$
* - $\left(\frac{p}{T},N\right)$
  - $\frac{\mathscr{E}}{k_{\mathrm{B}}T} = \ln\left(1-e^{-p/k_{\mathrm{B}}T}\right) < 0$
  - $\frac{S}{k_{\mathrm{B}}} =  (\overline{B}+1)\ln (\overline{B}+1) -(N+1)\ln (N+1)-(\overline{B}-N)\ln(\overline{B}-N)$
* - $\left(\frac{p}{T},\frac{\mu}{T}\right)$
  - $\frac{\mathscr{E}}{k_{\mathrm{B}}T} = - \ln(\overline{B} + 1) < 0$
  - $\frac{S}{k_{\mathrm{B}}} = (\overline{B}+1)\ln (\overline{B}+1) -\overline{N}\ln\overline{N} -(\overline{B}-\overline{N})\ln (\overline{B}-\overline{N})$

```

Repasemos, una a una, las expresiones de la {numref}`tabla {number} <taula_s_lattice>`. En el colectivo microcanónico (totalmente cerrado), a medida que añadimos términos de la serie de Stirling, los efectos de tamaño finito refuerzan el potencial de subdivisión y, con ello, añaden contribuciones negativas a la entropía. En comparación, en el conjunto macrocanónico (semiabierto) ya no hemos tenido que recurrir a la aproximación de Stirling. Esta última, por un lado, ha hecho desaparecer las aportaciones negativas y, por otro, nos ha devuelto una expresión estrictamente exacta de la entropía que, a medida que transcurrimos al límite macroscópico, se mantendrá intacta. Al saltar al conjunto isobárico (semiabierto), el potencial de subdivisión se ha vuelto negativo, lo que ha provocado un ligero aumento de la entropía, ya que las correcciones son del orden $\mathscr {O} (1) $. Finalmente, como era de esperar, en el conjunto nanocanónico (totalmente abierto) hemos conseguido maximizar la entropía. En esta ocasión, las nuevas correcciones a las expresiones anteriores son también del orden $\mathscr {O} (1) $.

Dicho esto, representaremos la evolución de la entropía en el gráfico de la {numref}`figura {number} <lattice_s_graph>`.

```{figure} lattice_s_comp.png
---
height: 350px
name: lattice_s_graph
---
Al construir las curvas, hemos mantenido constante número de celdas en el valor $B = 40 $. Así, hemos cambiado el tamaño del sistema desde transcurriendo desde $N = 1 $ al límite superior $N = B $. Lo que muestra el gráfico refuerza las explicaciones expuestas en el párrafo anterior.

```

Es destacable que, en cuanto al aumento de la entropía en función de la evolución del potencial de subdivisión, los resultados obtenidos en este ejemplo coinciden con las conclusiones desarrolladas en el {numref}`apartado {number} <mupt_gi>` perteneciente al gas ideal.

Finalmente, para redondear el análisis, analizaremos las fluctuaciones en torno a las magnitudes $\overline {B} $ y $\overline {N} $ en el colectivo nanocanónico.

##### Ejercicio

Considerando que el promedio de una variable $X $ en el colectivo nanocanónico sigue la definición

$$
\overline{X} = \frac{\sum_{B, N}\; X \; \Omega(B,N)\;e^{-\varphi B}e^{mN}}{\sum_{B, N}\; \Omega(B,N)\;e^{-\varphi B}e^{mN}} \; ,
$$ (bar_x)

verifica que se cumplen las siguientes igualdades:

$$
\overline{B^2} - \overline{B}^2 = -\left(\frac{\partial \overline{B}}{\partial \varphi}\right)_m  \; ,
$$ (lattice_b_fluc)

$$
\overline{N^2} - \overline{N}^2 = \left(\frac{\partial \overline{N}}{\partial m}\right)_{\varphi} \; .
$$ (lattice_n_fluc)

Emplea las ecuaciones {eq}`lattice_bbar_nc` y {eq}`lattice_nbar_nc`.

**----------------------------------------------------**


Desarrollando la parte derecha de la ecuación {eq}`lattice_b_fluc`,

$$
\overline{B^2} - \overline{B}^2 = \frac{e^{\varphi^{(0)}-\varphi}(1-e^{\varphi^{(0)}-\varphi}) + e^{2(\varphi^{(0)}-\varphi)}}{(1-e^{\varphi^{(0)}-\varphi})^2} \underset{(\varphi-\varphi^{(0)}\ll 1)}{\approx} \frac{1}{\left(\varphi-\varphi^{(0)}\right)^2} + \frac{1}{\varphi-\varphi^{(0)}} \; ,
$$ (lattice_b_fluc_1)

y,

$$
\overline{N^2} - \overline{N}^2 \underset{(\varphi-\varphi^{(0)}\ll 1)}{\approx}\frac{e^{\varphi^{(0)}}-1}{e^{\varphi^{(0)}}}\left[\frac{1}{\left(\varphi-\varphi^{(0)}\right)^2} +\frac{e^{\varphi^{(0)}}}{\varphi-\varphi^{(0)}}\right] \; .
$$ (lattice_n_fluc_1)


Como se ve, ambas magnitudes presentan fluctuaciones significativas, ya que, al menos en la primera aproximación, éstas son del orden $\overline {B} ^ 2 +\overline {B} $.





