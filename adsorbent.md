(app)=
## Gas ideal y adsorbente esférico pequeño

En este apartado especial, repetiremos y analizaremos los resultados del artículo {cite}`ads`, por medio del lenguaje de programación Python.

### Estudio del sistema

```{figure} adsorbent.png
---
height: 350px
name: adsorbent
---
Una partícula libre del gas que se encuentra a una distancia $ r $ del centro detectará el efecto del adsorbente del radio $a $ por medio de la energía de interacción $U (a, r) $. Así, las partículas adsorbidas formarán una superficie de radio $R $. Pues bien, el potencial $U_{S} = U (a, R) $ en un estado de equilibrio dependerá del área $\Omega $ de la esfera, pero no de la temperatura $T $ o del potencial químico $\mu $.

```

La superficie de partículas adsorbidas será el sistema termodinámico que estudiaremos a partir de ahora. Su área es $\Omega$, y se encuentra en contacto con una fuente de calor a una temperatura $T$. Las partículas del gas forman una fuente química. Por lo tanto, las variables de entorno del sistema serán $ T, \Omega$ y $\mu $. Consideraremos al adsorbente como un agente externo. Siguiendo las explicaciones de la {numref}`figura {number} <adsorbent>`, y basándonos en la teoría de Hill ({numref}`sección {number} <hillteo>`), construiremos la colectividad macrocanónica formada por $\mathscr{N}$ réplicas. Sus variables son, por tanto, $ S_ {t} = \mathscr {N} S $, $ \Omega_ {t} = \mathscr {N} \Omega $ y $ N_ {t} = \mathscr {N} \overline {N}$. A través de ellos, obtendremos la ecuación de Hill-Gibbs correspondiente:


$$
\mathrm{d}E_{t}(S_{t},\Omega,N_{t},\mathscr{N}) = T\mathrm{d}S_{t} + \gamma\mathscr{N}\mathrm{d}\Omega + \mu \mathrm{d}N_{t} + \left(\mathscr{E}+ \gamma\Omega\right)\mathrm{d}\mathscr{N} ,
$$ (adseq)

La letra $\gamma$ representa **la tensión superficial diferencial**, es decir, el conjugado de $\Omega$, una magnitud intensiva en el límite macroscópico. Asimismo, definiremos la energía de réplica y el potencial de subdivisión por medio de la **tensión superficial integral** $ \widehat {\gamma} $:

$$
X(T,\Omega,\mu) = \mathscr{E} + \gamma\Omega  := \left(\frac{\partial E_{t}}{\partial \mathscr{N}}\right)_{S_{t},\Omega,N_{t}} := \widehat{\gamma}\Omega \; .
$$(adsx)

Transcurriendo a los sistemas pequeños, la energía interna cumplirá lo siguiente, poniendo de manifiesto la falta de homogeneidad de las variables:

$$
\mathrm{d}\bar{E} = T\mathrm{d}S + \gamma\mathrm{d}\Omega + \mu \mathrm{d}\bar{N} \; ,
$$ (adsde)
$$
\bar{E} = TS + \widehat{\gamma}\Omega + \mu \bar{N} \; .
$$ (adse)

De la pareja de ecuaciones, llegaremos a la relación Hill-Gibbs-Duhem:

$$
\mathrm{d}(\widehat{\gamma}\Omega) = -S\mathrm{d}T + \gamma \mathrm{d}\Omega - \bar{N} \mathrm{d}\mu \; .
$$ (adshgd)

Estableceremos la relación entre las tensiones superficiales (coinciden en el límite macroscópico):

$$
\gamma := \left[\frac{\partial(\widehat{\gamma}\Omega)}{\partial \Omega}\right]_ {T, \mu} = \widehat{\gamma} + \Omega\left(\frac{\partial \widehat{\gamma}}{\partial \Omega}\right)_{T,\mu} \; .
$$ (adsgandghat)

$$
\\
$$

A continuación, pasaremos a la Física Estadística. La función de partición canónica incluirá dos contribuciones: la correspondiente al gas ideal de la superficie $ \Omega $, y otra que toma en cuenta el efecto de la energía de interacción en equilibrio $ U_ {S} $. De este modo,

$$
Q(T,\Omega,N) = \frac{\Omega^N}{N!\Lambda^{2N}}\cdot e^{-NU_{S}/k_{\mathrm{B}}T} \; .
$$ (adsq)

Aplicando la transformación de Legendre al grado de libertad químico, escribimos la función de partición macrocanónica:

$$
\Xi(T,\Omega,\mu) = \sum_{N=0}^{\infty} \frac{\Omega^N}{N!\Lambda^{2N}} e^{N(\mu -U_{S})/k_{\mathrm{B}}T} = \exp\left[\frac{\Omega}{\Lambda^2}e^{(\mu -U_{S})/k_{\mathrm{B}}T}\right] \; .
$$ (adsxi)

A continuación, recordando que $\Psi (T,\Omega,\mu): =\widehat {\gamma}\Omega: = -k_{\mathrm{B}} T\ln \Xi $, las expresiones que emplearemos para la construcción de las gráficas  serán las siguientes:

$$
\boxed{\widehat{\gamma} = -\frac{k_{\mathrm{B}}T}{\Lambda^2}e^{(\mu -U_{S})/k_{\mathrm{B}}T}} \; ,
$$ (ghat)

$$
\boxed{\gamma=-\frac{k_{\mathrm{B}} T}{\Lambda^{2}} e^{(\mu -U_{S})/k_{\mathrm{B}}T}\left[1-\frac{ \Omega}{k_{\mathrm{B}}T}\left(\frac{\partial U_{S}}{\partial \Omega}\right)_{T, \mu}\right]} \; .
$$ (g)

```{admonition} Nota
Hemos calculado la tensión superficial diferencial con la ayuda de la ecuación {eq}`adsgandghat`.

```

Pero para hacer esto, primero necesitamos caracterizar la interacción entre el adsorbente y las partículas de gas, para así construir $ U (a, r)$ y llegar al potencial $ U_ {S} $.

### Potencial de interacción y resultados

El adsorbente es una esfera de densidad $\rho$. Caracterizaremos la interacción entre un elemento de volumen y una partícula de gas partiendo del potencial 12-6 de Lennard-Jones:

$$
u(r) = 4\epsilon\left[\left(\frac{\sigma}{r}\right)^{12} - \left(\frac{\sigma}{r}\right)^{6}\right] \; ,
$$ (lj)

donde $\sigma$ y $\epsilon$ son los parámetros de longitud y energía, respectivamente. Al integrarlo a través del volumen del adsorbente, adquiriremos el potencial $ U (a, r)$:

$$
U(a, r) =  \int_{\text{V}}\mathrm{d}^{3}\mathbf{r}\;u(r) = \frac{16 \pi \epsilon \rho \sigma^{3}}{3}\left[\frac{\left(15 a^{3} r^{6}+63 a^{5} r^{4}+45 a^{7} r^{2}+5 a^{9}\right) \sigma^{9}}{15\left(r^{2}-a^{2}\right)^{9}}-\frac{a^{3} \sigma^{3}}{\left(r^{2}-a^{2}\right)^{3}}\right] \; .
$$ (uar)

A continuación, minimizaremos la expresión {eq}`uar` para establecer la relación entre los radios $a$ y $R$, y también para lograr el potencial de equilibrio de $U_{S}$:

$$
U_{S} = U(a,r=R) = \mathrm{min}\left[U(a,r)\right] \; .
$$

Finalmente, necesitamos concretar la densidad. El artículo toma $\rho = 3/\left [4\pi (\sigma/2)^3\right]$. Así, en el conjunto de gráficos de la {numref}`figura {number} <plot1>` representaremos el par de ecuaciones {eq}`ghat` y {eq}`g` en función del tamaño del adsorbente, así como el potencial de subdivisión por unidad de área, usando $\mathscr{E}/\Omega = \widehat {\gamma} - \gamma $.

```{figure} plot1.PNG
---
height: 350px
name: plot1
---
Cuando el sistema es pequeño (por ejemplo, en la región $ a / \sigma <40 $), las tensiones superficiales son significativamente extensivas, y, además, las dos curvas se pueden diferenciar claramente. Sin embargo, a medida que aumenta el tamaño del adsorbente, el potencial de subdivisión se atenúa. Por lo tanto, las curvas $ \widehat {\gamma} $ y $ \gamma $ recuperarán gradualmente su carácter intensivo, y también tenderán a unificarse. En el punto $a/\sigma = 100$, el sistema ya se está aproximando a la transición a la región macroscópica.

```

```{figure} plot2.PNG
---
height: 350px
name: plot2
---
Las magnitudes por unidad de molécula de la fase adsorbida sufren una transición aún más rápida al nivel macroscópico $ (a / \sigma \approx 50)$. También se puede observar que la tensión superficial integral sigue la ley del gas ideal bidimensional, esto es, $ - \widehat {\gamma} \Omega = \overline {N} k _ {\mathrm {B}} T $.

```

Los parámetros empleados al construir las curvas pertenecen al gas de argon: $\Lambda_{\text{Ar}} = 16,7 \cdot 10^{-12} \; \mathrm{m}$ ; $\sigma_{\text{Ar}} = 3.4 \cdot 10^{-10} \; \mathrm{m}$ ; $\epsilon_{\text{Ar}} = 0,0104 \; \mathrm{eV}$.

Al construir las curvas de la {numref}`figura {number} <plot2>` hemos empleado esta relación, siguiendo a la ecuación {eq}`adshgd`:

$$
\bar{n} \equiv \frac{\bar{N}}{\Omega} = - \left(\frac{\partial \widehat{\gamma}}{\partial \mu}\right)_ {T,\Omega} = \frac{1}{\Lambda^2}e^{(\mu -U_{S})/k_{\mathrm{B}}T} \; .
$$ (nadsorb)

Para empezar, cabe señalar que, en el límite a cero del radio del adsorbente, hemos considerado éste como una partícula puntual. Por lo tanto, minimizando la ecuación {eq}`lj`, en este caso hemos usado $ R (a \rightarrow 0) = 2 ^ {1/6} \sigma $.

Por otro lado, siguiendo los comentarios de los gráficos, y mirando las ecuaciones {eq}`adsgandghat` y {eq}`g`, queda claro que en la escala de los sistemas pequeños, funciones termodinámicas como $\widehat {\gamma} \Omega $ presentan una dependencia no lineal con respecto a la superficie $ \Omega $ de la esfera. Como resultado, las tensiones superficiales tienen un comportamiento no intensivo, y la desviación entre ambas también es notable. En cualquier caso, el límite macroscópico restaurará la linealidad, de tal manera que recuperaremos la igualdad $\partial\left (\widehat {\gamma}\Omega\right)/\partial\Omega=(\widehat{\gamma}\Omega)/\Omega$. El potencial de subdivisión, de hecho, sigue la expresión

$$
\mathscr{E} = \widehat{\gamma}\Omega - \Omega \left[\frac{\partial (\widehat{\gamma}\Omega)}{\partial \Omega}\right]_{T,\mu} \; ,
$$ (epsilonads)
por lo que está al mando de las desviaciones con respecto al carácter lineal de las magnitudes.

En la misma línea, si iniciamos el grado de libertad mecánico al sistema, incluir una réplica al conjunto nanocanónico $( \mathscr {E} <0 )$ implicaría redistribuir el área total $ \Omega_ {t} $ del conjunto. Por tanto, el área $\Omega$ de los subsistemas con variables de entorno $(T,\gamma,\mu)$ disminuiría, y la curvatura de sus superficies aumentaría. Siguiendo el postulado de Hill, el potencial de subdivisión sería la única contribución a la energía interna del conjunto a causa de los efectos superficiales; esto es,


$$
\mathscr{E}(T,\gamma,\mu) := \left(\frac{\partial E_{t}}{\partial \mathscr{N}}\right)_ {S_{t},\Omega_{t},N_{t}} \; .
$$ (epsilonadsfree)

$$
\\
$$

Para concluir el análisis, es de mencionar que en esta aplicación hemos utilizado un modelo de adsorción simple basado en varias aproximaciones: por un lado, hemos considerado el gas como ideal, y, por otro, hemos aceptado que el potencial de equilibrio $ U_ {S} $ solo depende de la superficie del sistema. Sin embargo, ha resultado ser un ejemplo muy apropiado de cara a adaptar los conceptos de la Termodinámica de Sistemas Pequeños a la adsorción de una forma comprensible y didáctica.

