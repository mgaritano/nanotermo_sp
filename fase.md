(fase)=
## Transiciones de fase en sistemas pequeños

En esta apartado adicional, examinaremos las peculiaridades que los efectos de tamaño finito aportan al comportamiento de la transición de fase entre dos estados de equilibrio.

(itzul)=
### Reversibilidad y condiciones de equilibrio

Siguiendo la teoría de Hill, examinaremos un conjunto macroscópico de $ \mathscr{N} (\rightarrow \infty) $ réplicas. No iniciaremos ningún grado de libertad a los subsistemas, es decir, están completamente aislados. Por tanto, les asignaremos las variables $(E,V,N)$. De acuerdo con el segundo principio de la Termodinámica {cite}`st`, el sistema, en su camino desde el primer estado de equilibrio al segundo, pasará por procesos infinitesimales irreversibles. Éstos generarán contribuciones positivas a la entropía  $(\mathrm{d}S_{t}>0)$ hasta que se restablezca el equilibrio $(\mathrm{d}S_{t}=0)$. Cualquier cambio posterior será reversible, ya que el sistema se mantendrá en el nuevo estado de equilibrio.

En general, un proceso espontáneo se puede modelar mediante el sistema de la {numref}`figura {number} <esp>`. Inicialmente, el sistema se encuentra bajo la influencia de una barrera externa. Como resultado, solo estarán disponibles algunos de todos los estados cuánticos posibles: $ \Omega_ {i} (E, V, N) $. Eliminar esta prohibición externa cambiará el estado del sistema. De hecho, las réplicas también tendrán acceso a estados que han sido previamente prohibidos, por lo que al final tenemos $\Omega_{f} (E,V,N)>\Omega_{i}(E,V,N)$. Este proceso se puede lograr reduciendo la energía de activación o minimizando un potencial. Al hilo de la discusión inicial, maximizar la entropía acarreará minimizar la energía libre.


```{figure} esp.PNG
---
height: 200px
name: esp
---
  Modelización del proceso espontáneo. La pared divisoria evita que el gas se desplace hacia la parte derecha de la caja. No hay pared al final, y como resultado, el gas se ha extendido a todo el volumen, de forma espontánea. De principio a fin, la entropía ha aumentado.
```

Dado que la entropía satisface $ S_ {t} = \mathscr{N}k_{\mathrm{B}} \ln \Omega $, cuando se completa el proceso finito y espontáneo,

$$
\Delta S_{t} = S_{f}^{t} - S_{i}^{t} = \mathscr{N}k_{\mathrm{B}}\ln\left(\frac{\Omega_f}{\Omega_i}\right) > 0 \; .
$$ (sesp)

Esta ecuación ilustra el significado de una de las leyes más importantes de la Termodinámica. De hecho, si ocurriera espontáneamente el proceso contrario, tendríamos $ \Delta S_ {t} <0 $, lo cual iría en contra del segundo principio. Sin embargo, como hemos aceptado $\mathscr{N}\rightarrow\infty$, la probabilidad de que esto suceda en la **totalidad del colectivo**, es decir, en todos y cada uno de los sistemas, es casi cero, es decir,

$$
 P_{f \rightarrow i}^{t} := \frac{\Omega_{i}}{\Omega_{f}} = \exp\left(-\frac{\Delta S_{t}}{\mathscr{N}k_{\mathrm{B}}}\right) \rightarrow 0 \; .
 $$ (probcont)

Sin embargo, en los **subsistemas**  tendríamos $N$ en lugar de $\mathscr{N}$, y por tanto $P_{f\rightarrow i}\propto e^{- N}$. Así, la magnitud de $ N $ no tiene que  por qué ser lo suficientemente grande como para descartar el valor de $P_{f\rightarrow i}$. Por lo tanto, si $ N $ es demasiado pequeño, cabría la posibilidad de observar espontáneamente un proceso que viola el segundo principio $(\Delta S < 0)$ en ciertos sistemas pequeños. En cualquier caso, recordemos que la teoría de Hill consiste en inferir del conjunto las propiedades de las variables. Entonces, para empezar, necesitamos ver la variación de la entropía de todo el colectivo, y de ahí pasar a los sistemas pequeños, considerando que se cumple $ \Delta S = \Delta S_ {t} / \mathscr{N} $.

A propósito de esta discusión, en la {numref}`sección {number} <stabeps>`  examinaremos el proceso de subdivisión del conjunto de sistemas pequeños. Asimismo, observaremos el efecto del potencial de subdivisión $ \mathscr {E} $ sobre la reversibilidad de dicho proceso.


(fase1order)=
### Transiciones de fase de primer orden, en sistemas $(T,p,N)$ pequeños

Supongamos que deseamos llevar un sistema macroscópico de un estado de la fase inicial a otro final. En el primer estado, su ecuación de estado es una función continua y derivable, es decir, está correctamente definida. Sin embargo, en algún momento sufrirá un cambio repentino a la segunda fase, por lo que sufrirá discontinuidades; es decir, ocurrirá una transición de fase de primer orden en el sistema ({numref}`figura {number}a <faseirudi>`).


```{figure} faseirudi.PNG
---
height: 250px
name: faseirudi
---
$\text{(a)}$ En el límite termodinámico, en la transición de fase de primer orden, el sistema sigue la __curva isotérmica__ $ p- \overline {V} $, pasando directamente del estado $ A $ al estado $B$. De hecho, la **curva discontinua** va en contra de la estabilidad, dado que la compresibilidad es negativa, es decir, $ \kappa_ {T} = - \left (\partial p / \partial V \right) _ {T} <0 $. $\text{(b)}$ **En el caso de los sistemas pequeños**, los estados $ A $ y $ B $ estarán presentes en la zona  $ \Delta p $ al mismo tiempo. En el límite macroscópico, está claro que se cumplirá $ \Delta p \rightarrow p_ {0} $.
```

En cambio, si el sistema fuera pequeño, la transición sería menos pronunciada, como se puede ver en la {numref}`figura {number}b <faseirudi>`. Como veremos enseguida, la extensión del rango de presión $ \Delta p $ está directamente relacionada con el tamaño del sistema $( N )$. Pero antes de entrar en ello, hay otra cuestión que necesita ser aclarada. De hecho, como bien indica la imagen {numref}`figura {number} <prob>`, las fluctuaciones que emergen alrededor de los volúmenes $\overline{V}_{A}$ y $\overline{V}_{B}$ son perceptibles. En otras palabras, la probabilidad de $ P (V) $ se alejará ligeramente a los alrededores de los volúmenes $ \overline {V} _ {A} $ y $ \overline {V} _ {B} $.

```{figure} prob.PNG
---
height: 250px
name: prob
---
En el límite termodinámico, la probabilidad satisface $ P (V) = \delta (V- \overline {V} _ {A}) + \delta (V- \overline {V} _ {B}) $. En el caso de un sistema pequeño, en cambio, las curvas muestran una **mayor dispersión**. Por lo tanto, no seguirá estrictamente a la denominada _aproximación de dos estados_. En cualquier caso, $ P (\overline {V} _ {0}) $ es despreciable en cualquier volumen $ \overline {V} _ {0} $ intermedio. Por todo esto, es lícito afirmar que el área de la transición de fase se compone de una combinación de los estados $A$ y $B$.
```

Retomando el hilo anterior, partiendo de la función de partición canónica $ Q (T, V, N) $, definiremos la probabilidad de que el sistema tenga el volumen $ V_ {i} $:

$$
P(V_{i}) := \frac{Q(T,V_{i},N)e^{- pV_{i}/k_{\mathrm{B}}T}}{\sum_{V_{i}}Q(T,V_{i},N)e^{-pV_{i}/k_{\mathrm{B}}T}} = \frac{Q(T,V_{i},N)e^{-pV_{i}/k_{\mathrm{B}}T}}{\Delta(T,p,N)}\;.
$$ (pvi)

Ahora, siguiendo los comentarios de la {numref}`figura {number} <prob>`, calcularemos la relación $ P (\overline {V} _ {A, B}) / P (\overline {V} _ {0}) $, que servirá como claro indicador de la legitimidad del empleo de la _aproximación de dos estados_. Encauzaremos el análisis desde la Física Estadística con la ayuda del libro {cite}`sm`. La cuestión es que en un estado intermedio los estados originales $A$ y $B$, ambos también estarán presentes, separados por una superficie divisoria. El número de moléculas que contenga será de aproximadamente $ N ^ {2/3} $, por lo que las interacciones entre estas moléculas aportarán una contribución a la energía  $ A (T, V, N) $ del orden $ N ^ { 2/3} k _ {\mathrm {B}} T $. La función de partición alrededor de este punto, por tanto, satisfará la expresión

$$
Q(T,\overline{V}_{0},N) = e^{-A(T,V,N)/k_{\mathrm{B}}T-N^{2/3}} = Q(T,V,N)e^{-N^{2/3}} \; .
$$ (q_fase_puntu)

Como esta ecuación es proporcional a la probabilidad (teniendo en cuenta la expresión  {eq}`pvi`), se cumplirá lo siguiente, excepto en torno a un punto crítico:

$$
\frac{P(\overline{V}_{A,B})}{P(\overline{V}_{0})} \propto e^{N^{2/3}}  \; .
$$

Por lo tanto, excluyendo los puntos críticos, si el sistema no es demasiado pequeño, las únicas contribuciones a la distribución de probabilidad serán las de los estados $ A $ y $ B $, y la aproximación será correcta.

$$
\\
$$

Así las cosas, empleemos ahora un razonamiento basado en las herramientas de la Termodinámica de Sistemas Pequeños para corroborar los resultados obtenidos. Construyamos un conjunto isotérmico-isobárico de $\mathscr{N}$ réplicas. Los estados $A$ y $B$ contienen, respectivamente, $\mathscr{N}_{A}$ y $\mathscr{N}_{B}$ subsistemas. De la {numref}`sección {number} <tpn_azter>`, recordando que la energía libre de Gibbs se define como $ F_ {A, B}: = N \widehat {\mu} _ {A, B} $, y considerando la contribución de todas las distribuciones posibles (entropía configuracional), la energía total será

$$
F_{t} = \mathscr{N}_ {A}\left(N\;\widehat{\mu}_ {A}\right) +  \mathscr{N}_ {B}\left(N\;\widehat{\mu}_ {B}\right) - k_{\mathrm{B}}T\ln\left(\frac{\mathscr{N}!}{\mathscr{N}_ {A}!\;\mathscr{N}_{B}!}\right) \; .
$$ (gibbstot)

Nuestro objetivo es reparar en la fracción $ \mathscr {N} _ {A} / \mathscr {N} _ {B} $ en un estado de equilibrio. De ahí obtendremos la información necesaria para este segundo análisis. Dado que el conjunto en sí es macroscópico, podremos hacer uso de la aproximación de Stirling; esto es, partiremos de la expresión $ \ln \mathscr {N}! \approx\mathscr{N}\ln\mathscr{N}-\mathscr{N}$. Así, fijando la magnitud $\mathscr {N} _ {A} $ perteneciente al estado de equilibrio, y escribiendo $\mathscr {N} _ {B} = \mathscr {N} - \mathscr {N} _ { A} $, impondremos la condición 

$$
\left(\frac{\partial F_{t}}{\partial \mathscr{N}_ {A}}\right)_{T,p,N,\mathscr{N}} = 0 \; ,
$$ (fase_oreka)

y, de esta forma, llegaremos a esta expresión:

$$
\frac{\mathscr{N}_ {A}}{\mathscr{N}_ {B}} = \left(\exp\frac{\widehat{\mu}_ {B} - \widehat{\mu}_ {A}}{k_{\mathrm{B}}T}\right)^N \; .
$$ (fracnanb)

Por lo general, siguiendo las explicaciones de la sección {numref}`sección {number} <tpn_azter>`, el potencial químico integral es una función de las variables ambientales, es decir, $ \widehat {\mu} _ {A, B} = \widehat {\mu } _ {A, B } (T, p, N) $. Por lo tanto, podemos fijar la presión $ p $ de tal forma que los dos potenciales coincidan $( \widehat {\mu} _ {A} = \widehat {\mu} _ {B} )$. Este valor corresponde a la presión $ p_ {0} $ de la {numref}`figura {number}b <faseirudi>`. Además, según la ecuación {eq}`fracnanb`, se cumplirá que $\mathscr{N} _ {A} = \mathscr {N} _ {B} $. Pero, si la presión se desviara ligeramente del valor de $ p_ {0} $, tal que $ \widehat {\mu} _ {A} \gtrsim \widehat {\mu} _ {B} $ o $ \widehat {\mu} _ {B} \gtrsim \widehat {\mu} _ {A} $, en el límite $ N \rightarrow \infty $ casi todos los sistemas saltarían a los estados $ B $ y $ A $, respectivamente, y se cumpliría que $ \mathscr { N} _ {B} \gg \mathscr {N} _ {A} $ o $ \mathscr {N} _ {A} \gg \mathscr {N} _ {B} $. En otras palabras, el límite macroscópico de la ecuación {eq}`fracnanb` es compatible con la _aproximación de dos estados_. En cualquier caso, si $ N $ no fuera lo suficientemente grande, la presión se debería alejar considerablemente del punto $ p_ {0} $ para observar lo anterior. Por lo tanto, en un rango de presión $ \Delta p $  bastante amplio, $ \mathscr {N} _ {B} \gtrsim \mathscr {N} _ {A} $ o bien $ \mathscr {N} _ {A} \gtrsim \mathscr {N} _ {B} $. El salto de un estado a otro sería más suave. 

$$
\\
$$

Para concluir el análisis de las transiciones de fase, se debe tener en cuenta que en el punto $p = p_{0}$ las variables $(T,p,N)$ de entorno deben permanecer constantes. Entonces, para mantener la igualdad, las variaciones alrededor de estos valores deben cumplir $ \mathrm {d} \widehat {\mu} _ {A} = \mathrm {d} \widehat {\mu} _ {B}$. Usando esta condición y la ecuación {eq}`dmuhat`, llegamos a

$$
\frac{S_{A}-S_{B}}{N}\;\mathrm{d}T + \frac{V_{B}-V_{A}}{N}\;\mathrm{d}p + \frac{(\mu_{B}-\mu_{A}) + (\widehat{\mu} _ {A} - \widehat{\mu}_{B})}{N}\;\mathrm{d}N = 0 \; .
$$ (sasb)

Por supuesto, el punto de estudio satisface $ \Delta \widehat {\mu} = \widehat {\mu} _ {B} - \widehat {\mu} _ {A} = 0 $. Con esto en mente, obtendremos las siguientes relaciones con las variaciones de las demás magnitudes:

$$
\boxed{\left(\frac{\partial p}{\partial T}\right)_ {N} = \frac{\Delta S}{\Delta V}\quad ; \quad \left(\frac{\partial T}{\partial N}\right)_ {p} = \frac{\Delta \mu}{N\Delta \mathrm{s}}\quad ; \quad \left(\frac{\partial p}{\partial N}\right)_{T} = -\frac{\Delta \mu}{N\Delta \mathrm{v}}} \quad ,
$$ (neweq)

donde $\mathrm{v} = V/N$ y $\mathrm{s}=S/N$. La segunda y tercera relaciones (las cuales no son alcanzables por medio de la Termodinámica Clásica) sugieren claramente que la temperatura y la presión generalmente no son magnitudes intensivas. Así las cosas, y a modo de avance, en el {numref}`ejemplo {number} <cryst_melt>` obtendremos una expresión de la temperatura que dependiente del tamaño.

(fase_simple)=
#### Ejemplo sencillo

El propósito de este ejemplo es expresar cuantitativamente la validez de _la aproximación de dos estados_. Consideremos que los volúmenes $ \overline {\mathrm {v}} _ {A} $ y $ \overline {\mathrm {v}} _ {B} $ de los estados $ A $ y $ B $ son independientes de las variables $ p $ y $ N$. De manera similar, escribiremos $ \widehat {\mu} = \widehat {\mu} _ {A, B} (p = p_ {0}) $. Así, extrayendo la relación  $\partial\widehat {\mu}_{A,B}/\partial p=\overline{V}_{A,B}/N=\overline{\mathrm { v}} _ {A, B} $  de la {eq}`dmuhat` e integrando, tendremos que

$$
\widehat{\mu}_ {A,B} = \widehat{\mu} + \overline{\mathrm{v}}_ {A,B}\left(p-p_{0}\right) \; .
$$ (muhatab)

Mediante esta ecuación reescribiremos la relación {eq}`fracnanb`:

$$
\frac{\mathscr{N}_ {A}}{\mathscr{N}_ {B}} = \exp\left[-N\frac{\left(\overline{\mathrm{v}}_ {A} - \overline{\mathrm{v}}_ {B}\right)\left(p-p_{0}\right)}{k_{\mathrm{B}}T}\right]\; .
$$ (nanbex)

La expresión del volumen total es

$$
\left(\frac{\partial F}{\partial p}\right)_{T,N
} := \overline{V} = \frac{\mathscr{N}_ {A}}{\mathscr{N}}\overline{V}_ {A} + \frac{\mathscr{N}_ {B}}{\mathscr{N}}\overline{V}_ {B}\equiv P_{A}\overline{V}_ {A} +  P_{B}\overline{V}_{B} \; ,
$$ (vtotex)

Considerando que $P_{A} = (\overline{\mathrm{v}} - \overline{\mathrm{v}}_ {B}) / (\overline{\mathrm{v}}_ {A} - \overline{\mathrm{v}}_ {B})$ eta $P_{B}=1-P_{A}$, llegaremos a 

$$
\frac{(\overline{\mathrm{v}}_ {A} - \overline{\mathrm{v}}_ {B})(p-p_{0})}{k_{\mathrm{B}}T} = -\frac{1}{N}\ln\left[\frac{(\overline{\mathrm{v}} - \overline{\mathrm{v}}_ {B})/(\overline{\mathrm{v}}_ {A} - \overline{\mathrm{v}}_ {B})}{1-(\overline{\mathrm{v}} - \overline{\mathrm{v}}_ {B})/(\overline{\mathrm{v}}_ {A} - \overline{\mathrm{v}}_{B})}\right] \; .
$$ (fasesimplegraph)

Erijamos la representación gráfica de la ecuación {eq}`fasesimplegraph`:

```{figure} faseplot.PNG
---
height: 350px
name: faseplot
---
Este modelo simple de transiciones de fase en sistemas pequeños pone de manifiesto que la coexistencia de los estados $ A $ y $ B $ abarca un rango de presión considerable en el caso de $ N <40 $. Además, la curva de $ N = 200 $ tiende a asemejarse con el gráfico de la {numref}`figura {number}a <faseirudi>`.
```

Obsérvese la {numref}`figura {number} <faseplot>`. Si el gráfico se rota $90 ^ \circ $ hacia la izquierda, coincidirá con las curvas de la {numref}`figura {number} <hc_phase>` del ejemplo "hélice-ovillo". En otras palabras, podemos confirmar con mayor rigurosidad que en el límite macroscópico se producirá una transición de fase entre los estados hélice y ovillo.


(cryst_melt)=
#### Fusión del cristalito

En este segundo ejemplo, examinaremos el efecto del tamaño de un cristalito esférico sobre su temperatura de fusión. Entonces, siguiendo la  _aproximación de dos estados_, denominaremos $ A $ al estado sólido $(S)$ y $ B $ al estado líquido $(L)$. La energía libre de Gibbs de los sistemas pequeños contendrá no sólo la contribución __lineal macroscópica__ $(\propto N)$, sino también las correspondientes a  __efectos de superficie__ $(\propto N^{2/3})$ y la __rotación__ $(\propto\ln N)$; es decir,

$$
F(T,p,N) := N\widehat{\mu} = Nf(T,p) + N^{2/3}a(T,p) + \ln N \; b(T) \; .
$$ (fklasto)

De esta forma, centraremos nuestro análisis en la zona de coexistencia de los dos estados. Denominaremos $ T _ {\infty} $ y $ p _ {\infty} $ la temperatura y la presión del límite macroscópico. En concreto, calcularemos las desviaciones que el tamaño del sistema ocasiona en la temperatura en este estado de equilibrio, manteniendo constante la presión. Siguiendo las explicaciones del apartado {numref}`apartado {number} <fase1order>`, se cumplirá que $ \Delta \widehat {\mu} = \widehat {\mu} _ {L} - \widehat {\mu} _ {S} = 0 $. Usando esta condición y la ecuación {eq}`fklasto`, tendremos

$$
\Delta \widehat{\mu}(T,p_{\infty},N) = \Delta f(T,p_{\infty}) + N^{-1/3}\Delta a(T,p_{\infty}) + \frac{\ln N}{N}\Delta b(T) = 0 \; .
$$ (muhatklasto)

Para hacer aparecer la variable $ T $, calcularemos la aproximación de Taylor en los puntos $ T = T _ {\infty} $ de las funciones $ \Delta f $ y $ \Delta a $, e incluiremos solamente el primer término no nulo:

$$
\Delta f(T,p_{\infty}) \approx \left(\frac{\partial \Delta f}{\partial T}\right)_ {T_{\infty}}\left(T-T_{\infty}\right) = -\Delta \mathrm{s}_ {\infty}(T-T_{\infty})
$$
$$
\Delta a(T,p_{\infty}) \approx \Delta a(T_{\infty},p_{\infty}) \; .
$$

```{admonition} Nota
 Los términos macroscópicos de los estados $ f_ {S} (T, p) $ y $ f_ {L} (T, p) $ coinciden en la región de coexistencia. De hecho, esto es lo que observamos en el límite termodinámico: un salto repentino de una fase a otra. Las desviaciones que allí aparecen se deben únicamente a contribuciones pequeñas. Por lo tanto, debemos aceptar que $\Delta f(T_{\infty}, p_{\infty})=0$.
```

Al introducir estas expresiones en la ecuación {eq}`muhatklasto`, veremos que la temperatura obedecerá esta expresión:

$$
\boxed{T = T_{\infty} + N^{-1/3}\frac{\Delta a (T_{\infty},p_{\infty})}{\Delta \mathrm{s}_ {\infty}} + \frac{\ln N}{N}\frac{\Delta b(T_{\infty})}{\Delta \mathrm{s}_{\infty}}} \; .
$$ (t_ez_int)

Está claro que las pequeñas contribuciones inhomogéneas que hemos añadido a la temperatura $T_{\infty}$ son de carácter extensivo.

$$
\\
$$

Los comentarios sobre las transiciones de fase que hemos realizado a lo largo de este capítulo han reforzado lo predicho en la {numref}`sección {number} <tpn_azter>`. Ante todo, nos han ayudado a establecer $\color{teal}{\text{la naturaleza propia del potencial químico integral} \; \widehat {\mu} }$, pues ha quedado de manifiesto que que es un indicador de los cambios que experimenta el conjunto de subsistemas (ecuación {eq}`fracnanb`); es decir, toma consideración de las $\color{teal}{\text{propiedades de la colectividad}}$. Por el contrario, el $\color{red}{\text{potencial químico diferencial} \; \mu} $ tiene en cuenta las variaciones en las moléculas individuales de $\color{red}{\text{un solo sistema pequeño}}$. La Nanotermodinámica diferencia estrictamente estos dos efectos.
