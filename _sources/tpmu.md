(tpmu)=
## Colectividad nanocanónica: variables de entorno $(T,p,\mu)$ 

En este capítulo acometeremos el área más significativa perteneciente a la teoría. Supongamos que el sistema en cuestión es un polímero agregado compuesto por $N$ monómeros, y que se encuentra a una temperatura $T$ y una presión $p$. Si las fuerzas de unión entre las moléculas no fueran lo suficientemente fuertes, el número de moléculas $ N $ no se mantendría fijo por largo tiempo, ya que estaría sujeto a fluctuaciones. Por lo tanto, deberemos asignar al sistema el potencial químico $\mu$ como tercera variable ambiental; es decir, el análisis debe realizarse necesariamente por medio de una colectividad nanocanónica compuesta por subsistemas con variables $ (T, p, \mu) $.

Pero tengamos en cuenta lo mencionado en el {numref}`apartado {number} <nanointro>`: a nivel macroscópico no podremos definir tal conjunto, ya que sólo dos de las tres variables intensivas del sistema pueden ser libres (relación de Gibbs-Duhem). En este sentido, hemos aceptado que los sistemas pequeños disponen de un grado de libertad especial que se caracteriza por el potencial de subdivisión $\mathscr{E}$. Así, ahora el tamaño del sistema afectará a las variables intensivas. Esto permite, precisamente, la construcción de la colectividad nanocanónica. Sin embargo, como hemos visto, a medida que incrementa el tamaño del sistema, el gradual predominio de las contribuciones macroscópicas eliminará paulatinamente este grado de libertad.


```{admonition} Nota
En su libro, Hill emplea el apelativo _colectividad generalizada_ ("generalized ensemble"), en lugar de colectividad _nanocanónica_. 

```

$$
\\
$$

Con motivo de profundizar en lo anterior, iniciaremos todos los grados de libertad a los sistemas de los ejemplos {numref}`{number} <mupt_linagg>`  y {numref}`{number} <mupt_gi>`, y, particularmente, estudiaremos su efecto en la __entropía__. También comprobaremos que los resultados obtenidos en el límite macroscópico son compatibles con los del resto de colectividades estadísticas. Pero, primero, presentaremos brevemente las herramientas necesarias para el análisis.


(mupt_azter)=
### Estudio de la colectividad

Es de mencionar que la mayoría de las expresiones que pertenecen a este conjunto se han construido en la sección {numref}`sección {number} <hillteo>`, puesto que ofrece un punto de partida adecuado para el abordaje de la teoría de Hill. Recuperemos la ecuación {eq}`h_g_d` (relación de Hill-Gibbs-Duhem), y reescribámosla para construir las relaciones que cumplirán la entropía $S$, el volumen $ \overline {V} $ y el número de partículas $ \overline {N} $:

$$
\mathrm{d}\mathscr{E}(T,p,\mu) = \color{red}{ \left(\frac{\partial \mathscr{E}}{\partial T}\right)_ {p,\mu}}\color{black}{\mathrm{d}T} + \color{blue}{\left(\frac{\partial \mathscr{E}}{\partial p}\right)_ {T,\mu}}\color{black}{\mathrm{d}p} + \color{teal}{\left(\frac{\partial \mathscr{E}}{\partial \mu}\right)_{T,p}}\color{black}{\mathrm{d}\mu} = \color{red}{ -S}\color{black}{\mathrm{d}T} \; \color{blue}{+\overline{V}}\color{black}{\mathrm{d}p}  \; \color{teal}{-\overline{N}}\color{black}{\mathrm{d}\mu}\; .
 $$ (depsilonnew)

Como el potencial de subdivisión es una función del conjunto de variables $(T,p,\mu)$, ellos determinarán las magnitudes extensivas $(S,\overline{V},\overline{N})$ de un sistema pequeño de un solo componente, como bien indica la ecuación {eq}`depsilonnew`. No obstante, en el límite termodinámico la situación será diferente; en efecto, solamente podremos definir dos variables intensivas libres, y éstas no especificarán el tamaño del sistema. 

De la misma forma, la ecuación {eq}`depsilonnew` nos abastecerá de las relaciones de Maxwell propias de la colectividad nanocanónica; entre ellas, 

$$
\left(\frac{\partial S}{\partial p}\right)_{T,\mu} =- \left(\frac{\partial \overline{V}}{\partial T}\right)_{p,\mu} \quad ; \quad \left(\frac{\partial S}{\partial \mu}\right)_{T,p} = \left(\frac{\partial \overline{N}}{\partial T}\right)_{p,\mu} \quad ; \quad \left(\frac{\partial \overline{V}}{\partial \mu}\right)_{T,p} = - \left(\frac{\partial \overline{N}}{\partial p}\right)_{T,\mu} \; .
$$ (maxwell_nc)

Nótese que en el límite macroscópico todas las derivadas tenderán a infinito; de hecho, sus expresiones recíprocas (derivadas de magnitudes intensivas con respecto al tamaño) se volverán cero. Así pues, mediante las magnitudes que calcularemos en la segunda reexaminación del gas ideal clásico ({numref}`subsección {number} <mupt_gi>`), confirmaremos la veracidad de las relaciones {eq}`maxwell_nc`.

Ahora, de cara a establecer el vínculo con la Física Estadística, escribiremos la relación entre la __función de partición nanocanónica__, $\Upsilon (T , p, \mu)$, y el potencial de subdivisión: 

$$
  \mathscr{E}(T,p,\mu) := -k_{\mathrm{B}}T\ln \Upsilon \; .
$$ (epspf)

Calcularemos la función de partición generalizada aplicando las transformaciones de Legendre correspondientes. Por ejemplo, a partir del conjunto isotérmico-isobárico, tendríamos 

$$
\Upsilon(T,p,\mu) := \sum_{E,V,N}\Omega(E,V,N)e^{-E/k_{\mathrm{B}}T}e^{-pV/k_{\mathrm{B}}T}e^{\mu N/k_{\mathrm{B}}T} \equiv \sum_{N}\Delta(T,p,N)e^{\mu N/k_{\mathrm{B}}T} \; .
$$ (upsilon_def)

(mupt_linagg)=
### Ejemplo: agregado lineal

El sistema pequeño de este ejemplo se muestra en la {numref}`figura {number} <agg>`. Aceptaremos que el conjunto macroscópico es un gas diluido compuesto por sistemas distinguibles. Así, las interacciones entre réplicas se considerarán despreciables. Por otro lado, no se tendrá en cuenta el grado de libertad mecánico.

```{figure} aggregate.PNG
---
height: 225px
name: agg
---
Un agregado lineal es una vara larga que se constituye de $N$ monómeros. Por tanto, su masa es $ Nm $ y su longitud $ Na $.  Las unidades tienen una función de partición $ j (T) $ asociada con movimientos internos; la energía de interacción negativa entre primeros vecinos es $\epsilon$ ($N-1$ contribuciones). Asimismo, la barra puede girar alrededor del eje que pasa por su centro. El momento de inercia es $I = \frac {1} {12} N ^ {3} ma ^ {2} $.
```

Primero, analizaremos el sistema en la __colectividad canónica__. Por una parte, la función de partición asociada a la rotación del agregado es

$$
Q_{\mathrm{rot}}(T,N) := \frac{4\pi^2}{h^2}I(N)k_{\mathrm{B}}T = \xi(T)N^3 \; .
$$ (qrot)


```{admonition} Nota
Ver el capítulo 6 del libro {cite}`pathria`. De ahora en adelante usaremos la abreviación $\xi(T) = \frac{\pi^2ma^2}{3h^2}k_{\mathrm{B}}T$.
```

Combinando la influencia de la rotación con la contribución intrínseca de las unidades y las interacciones entre ellas, construiremos la función de partición canónica. Para abreviar las ecuaciones, definiremos $c(T) = \xi(T) e^{\epsilon/k_{\mathrm{B}}T}$. Así las cosas,

$$
\boxed{Q(T,N) := j(T)^{N} \cdot Q_{\mathrm{rot}}(T,N) \cdot e^{-(N-1)\epsilon/k_{\mathrm{B}}T} = c(T)\;N^3j(T)^N\;e^{-N\epsilon/k_{\mathrm{B}}T}} \quad (N\geq1)\; .
$$ (qagg)

Cuando $N=0$, no habrá contribuciones de la rotación ni de la energía de interacción a la función de partición del sistema. Por lo tanto, teniendo en cuenta la función de partición intrínseca, se cumplirá que $Q(T,0)=j(T)^0=1$.

##### Ejercicio

$(a)$ Calcular los potenciales químicos $\widehat{\mu}$ y $\mu$, su forma cuando $N\rightarrow \infty$ y el potencial $\mathscr{E}(T,N)$.

```{dropdown} __Solución__

Haciendo uso de la función de partición canónica (ecuación {eq}`qagg`), y recordando la relación $N\widehat{\mu} = -k_{\mathrm{B}}T\ln Q(T,N)$,

$$
\left.\begin{array}{l}
\widehat{\mu}=-k_{\mathrm{B}}T\ln j + \frac{N-1}{N} \epsilon - \frac{\ln(\xi N^3)}{N}k_{\mathrm{B}}T \\\\
\mu=-k_{\mathrm{B}}T\ln j + \epsilon -\frac{3}{N}k_{\mathrm{B}} T
\end{array}\right\}\underset{(N \rightarrow \infty)}{\boldsymbol{\longrightarrow}} \; \mu^{(0)} = -k_{\mathrm{B}}T\ln j + \epsilon
\\
$$ (muagg)

$$
\frac{\mathscr{E}(T,N)}{k_\mathrm{B}T} = \frac{N(\widehat{\mu}-\mu)}{k_\mathrm{B}T} = -\frac{\epsilon}{k_\mathrm{B}T} + 3  -\ln(\xi N^3)
$$ (eps_agg_tn)

```

$(b)$ Construir la expresión $S(T,N)/k_{\mathrm{B}}$. Analizar lo que ocurre en el límite macroscópico.

```{dropdown} __Solución__

$$
\frac{S(T,N)}{k_{\mathrm{B}}} := -\frac{1}{k_{\mathrm{B}}}\left(\frac{\partial N\widehat{\mu}}{\partial T}\right)_{N} = N\left(\ln j + T\frac{1}{j}\frac{\mathrm{d}j}{\mathrm{d}T}\right) +\color{red} \{ \color{black} 1 + \ln\left(\xi N^3\right)\color{red} \}
$$ (stnagg)

Las llaves rojas contienen contribuciones ligadas a la rotación, y son de tamaño finito, puesto que en el límite termodinámico prevalecerán los primeros dos términos de la expresión (lineales con respecto a $N$). Por ende, parece ser que el sistema macroscópico no percibirá la influencia de la rotación, ni siquiera de la energía de interacción entre las unidades $(\epsilon)$.
```

**----------------------------------------------------**

$$
\\
$$

Así las cosas, iniciaremos el grado de libertad químico, y pasaremos a la  __colectividad nanocanónica__. Sustituyendo la expresión $ x = je ^ {\left (\mu- \epsilon \right) / k _ {\mathrm {B}} T} $, e introduciendo la ecuación {eq}`qagg` en la definición {eq}`upsilon_def`, calcularemos la función de partición generalizada:

$$
\boxed{\Upsilon(T,\mu) = 1 + c\sum_{N=1}^{\infty}  N^{3}\;x^N = 1 +  c \left[\frac{6x^2}{(x-1)^4} + \frac{x}{(x-1)^2}\right]}\; , \; \vert x \vert < 1 \; .
$$ (upsilontn)


```{dropdown} __Desarrollo de la serie__

Partiremos de la siguiente serie geométrica, ya conocida:

$$
\sum_{N=1}^{\infty}x^N = \frac{1}{1-x} \; , \; \vert x \vert < 1 \; .
$$

Derivaremos ambas partes de la ecuación con respecto a $x$, y tras ello, multiplicaremos por $x$:

$$
\sum_{N=1}^{\infty}Nx^N = \frac{x}{(x-1)^2}
$$

Siguiendo el mismo procedimiento, calcularemos primero $\sum_{N=1}^{\infty}N^2x^N$, y, a continuación, la expresión requerida, $\sum_{N=1}^{\infty}N^3x^N$:

$$
\sum_{N=1}^{\infty}N^3x^N = \frac{6x^2}{(x-1)^4} + \frac{x}{(x-1)^2} \; .
$$

```

Hecho esto, escribiremos el potencial de subdivisión, atendiendo a la definición {eq}`epspf`:

$$
\mathscr{E}(T,\mu) = -k_{\mathrm{B}}T\ln \left\{1 + c\left[\frac{6x^2}{(x-1)^4} + \frac{x}{(x-1)^2}\right]\right\} \;.
$$ (epsagg_tmu)

Considerando el potencial químico $ \mu ^ {(0)} $ de la ecuación {eq}`muagg`, podemos reescribir $ x = e ^ {({\mu} - \mu ^ {(0)}) / k_ { \mathrm {B}} T} $. Por lo tanto, en el límite macroscópico se cumplirá $ x \rightarrow 1 $. Efectivamente, si calculamos el número medio de partículas,

$$
\overline{N} := -\left(\frac{\partial \mathscr{E}}{\partial \mu}\right)_{T} = c \; x \; P(0)\left[\frac{12 x(x-1)-24 x^{2}}{(x-1)^{5}}-\frac{x+1}{(x-1)^{3}}\right] \; ,
$$ (barnagg)

veremos que  $ \overline {N} (x \rightarrow 1) \rightarrow \infty $. Construiremos la expresión de la entropía en función de las variables $(T,\mu)$, y la abreviaremos con la ayuda de la ecuación {eq}`barnagg`:

$$
\frac{S(T,\mu)}{k_{\mathrm{B}}} := -\frac{1}{k_{\mathrm{B}}} \left(\frac{\partial \mathscr{E}}{\partial T}\right)_ {\mu}  = \overline{N}\left(\ln j + T\frac{1}{j}\frac{\mathrm{d}j}{\mathrm{d}T}\right)
$$
$$ + \color{red} \left\{ \color{black} - \overline{N}\ln x - \ln P(0) + cP(0)\left(1-\frac{\epsilon}{k_{\mathrm{B}} T}\right)\frac{x(x^{2}+4x+1)}{(x-1)^{4}} \color{red} \right\} \; \color{black} .
$$(stmuagg) 

Observemos que la función $ P (0) $ que aparece en las dos ecuaciones anteriores la hemos extraído de la probabilidad $P(N)$ (o $P(\overline{N}=N)$), el cual denota la probabilidad de que el sistema contenga $N$ partículas:

$$
P(N) := \frac{Q(T,N)e^{N\mu/k_{\mathrm{B}}T}}{\Upsilon} \; .
$$(probagg)

Como $Q(T,0) = 1$, se cumplirá que $P(0) = 1/\Upsilon$.

$$
\\
$$

Llegados a este punto, comparemos las ecuaciones {eq}`stnagg` y {eq}`stmuagg`. Parece que los dos primeros términos muestran la misma apariencia. Sin embargo, debemos tener cuidado, ya que en la primera expresión aparece la variable $ N $, y, en la segunda, el promedio $\overline{N}$. En aras de mayor claridad, construyamos la representación gráfica de la magnitud $ P (N) $: 


```{figure} pn_plot.PNG
---
height: 300px
name: pn_plot
---
En la región de los sistemas pequeños $( x \ll 1 )$, la distribución de probabilidad tiene un máximo bien definido en el punto $ N = \overline {N} $, como puede comprobarse mediante la ecuación {eq}`barnagg`. Pero a medida que aumenta el tamaño del sistema, la ubicación del máximo se difuminará, y no se cumplirá que $ \mathrm{max} [P (N)] = P (\overline {N}) $.
```

Ahora sí, siguiendo las explicaciones de la {numref}`figura {number} <pn_plot>`, podemos estimar que los primeros dos términos en las ecuaciones {eq}`stnagg` y {eq}`stmuagg` coinciden cuando el sistema es pequeño. Habiendo aclarado esto, retomemos el hilo de la discusión. Observemos las contribuciones de tamaño finito que contienen las llaves rojas. En el caso de la ecuación de la colectividad canónica {eq}`stnagg`, estas contribuciones se deben únicamente al grado de libertad correspondiente a la rotación. En contraste, la expresión {eq}`stmuagg` de la colectividad nanocanónica muestra más términos, todos los cuales son positivos. De hecho, además de la rotación, las fluctuaciones en el número de partículas $ N $ aumentarán aún más la entropía.


```{admonition} Oharra
Nótese que en la ecuación {eq}`stmuagg` se cumple que $ \epsilon <0 $ y $ x, P ( 0) \leq1 $. Por otro lado, en agregados lineales comunes se cumple que $e^{\epsilon/k_{\mathrm{B}}T} = 0.1$ {cite}`hill`. Entonces, la energía de interacción será $\epsilon \approx -2,3 \cdot k_{\mathrm{B}}T < 0$.
```

$$
\\
$$

El siguiente cuadro resume las principales conclusiones de este ejemplo: $(a)$ el aumento de entropía que se produce en un sistema completamente libre, y $(b)$ la compatibilidad entre la Nanotermodinámica y la Termodinámica.

$$
\boxed{\begin{gathered}
    (a) \quad S(T,\mu) > S(T,N) \\
    \\
   (b) \quad  \frac{S(T,\mu)}{\overline{N}k_{\mathrm{B}}}\equiv \frac{S(T,N)}{Nk_{\mathrm{B}}} = \frac{\mathrm{s}^{(0)}}{k_{\mathrm{B}}} = \ln j + T\frac{1}{j}\frac{\mathrm{d}j}{\mathrm{d}T} \quad (\overline{N},N\rightarrow\infty)
\end{gathered}}
$$


##### Ejercicio

Hill no considera la rotación en el ejemplo del libro {cite}`hill`. Por lo tanto, en ese caso el aumento de entropía está directamente relacionado con las fluctuaciones, puesto que obedece lo siguiente:

$$
S(T,\mu)-S^{(0)} \equiv S^{(x)}(T,\mu) = -k_{\mathrm{B}}\sum_{N}P(N)\ln P(N)\; .
$$ (agg_sx)

El objetivo de este ejercicio es, precisamente, llegar a la ecuación {eq}`agg_sx`. Como no vamos a considerar el efecto de la rotación, la función de partición de la ecuación {eq}`qagg` quedará resumida:

$$
Q(T,N) = c(T)j(T)^N\;e^{-N\epsilon/k_{\mathrm{B}}T} \quad (N\geq1)\; ,
$$ (agg_q_summ)

donde $c(T) = e^{\epsilon/k_{\mathrm{B}}T}$, y $Q(T,0) = 1$.

Dicho esto, dividiremos la tarea de este ejercicio en las siguientes partes: 

$(a)$ Partiendo de la función de partición {eq}`agg_q_summ`, recalcular las magnitudes contempladas entre las ecuaciones {eq}`muagg` y {eq}`probagg`; esto es,

$$
\widehat{\mu}, \; \mu, \; \mu^{(0)}, \mathscr{E}(T,N), \; S(T,N), \; \Upsilon(T,\mu), \; \mathscr{E}(T,\mu), \; \overline{N}, \; P(N) \; \text{eta} \; S(T,\mu) \; .
$$


```{dropdown} __Solución__

Éstos son los resultados a obtener:

$$
\left.\begin{array}{l}
\widehat{\mu}=-k_{\mathrm{B}}T\ln j + \frac{N-1}{N} \epsilon \\\\
\mu=-k_{\mathrm{B}}T\ln j + \epsilon 
\end{array}\right\}\underset{(N \rightarrow \infty)}{\boldsymbol{\longrightarrow}} \; \mu^{(0)} = -k_{\mathrm{B}}T\ln j + \epsilon \; ,
$$ (muagg_short)

$$
\mathscr{E}(T,N) = -\epsilon > 0 \; ,
$$ (epstn_agg_short)

$$
S(T, N) = N k_\mathrm{B} \left(\ln j + T\frac{1}{j}\frac{\mathrm{d}j}{\mathrm{d}T}\right) \equiv S^{(0)} \; .
$$ (stn_agg_short)

Por tanto, tenemos que $S^{(x)}(T,N) = 0$.

$$
\Upsilon(T,\mu) = \frac{1-x+cx}{1-x} \quad (x < 1) \; ,
$$ (upsilon_agg_short)

donde el término $x(T,\mu)  =  j(T)e^{\left(\mu-\epsilon\right)/k_{\mathrm{B}}T}$ permanece inalterado, y, $c = e^{\epsilon/k_{\mathrm{B}}T}$.

$$
\mathscr{E}(T,\mu) = - k_{\mathrm{B}}T\ln\left(\frac{1-x+cx}{1-x}\right) < 0
$$ (epstmu_agg_short)

$$
\overline{N} = \frac{cx}{(1-x)(1-x+cx)}
$$ (nbar_agg_short)

$$
P(N) = \begin{cases}\frac{1-x}{1-x+cx} & , \quad N = 0\\\frac{x^Nc(1-x)}{1-x+cx} & , \quad N  \geq 1\end{cases}
$$ (pn_agg_short)

$$
S(T,\mu) = \overline{N} k_\mathrm{B} \left(\ln j + T\frac{1}{j}\frac{\mathrm{d}j}{\mathrm{d}T}\right)  + \color{red} \left\{ \color{black} - \overline{N}k_\mathrm{B}\ln x - k_\mathrm{B}\ln P(0) - \left[1-P(0)\right]\frac{\epsilon}{T} \color{red} \right\} \color{black} = S^{(0)} + \color{red}S^{(x)} (T,\mu)
$$ (stmu_agg_short)

```

$(b)$ Verificar que se cumple la igualdad {eq}`agg_sx`.

```{dropdown} __Solución__

Empleando la función $P(N)$ de la ecuación {eq}`pn_agg_short`,

$$
-k_{\mathrm{B}}\sum_{N=0}^{\infty}P(N)\ln P(N) = -k_\mathrm{B}\ln P(0) - k_\mathrm{B}\frac{c(1-x)}{1-x+cx} \left\{\ln x\sum_{N=1}^{\infty}N x^N +\ln\left[\frac{c(1-x)}{1-x+cx}\right]\sum_{N=1}^{\infty} x^N\right\} \; .
$$ (pn_aux)

Desarrollando los sumatorios,

$$
\sum_{N=1}^{\infty}N x^N = \frac{x}{(x-1)^2} \;\; (x < 1) \quad , \quad  \sum_{N=1}^{\infty} x^N = \frac{x}{1-x} \;\; (x < 1) \; .
$$

Reescribiremos la ecuación {eq}`pn_aux` de esta manera:

$$
-k_{\mathrm{B}}\sum_{N=0}^{\infty}P(N)\ln P(N) = -k_\mathrm{B}\ln P(0) - k_\mathrm{B}\left\{\frac{cx\ln x}{(1-x)(1-x+cx)}  + \frac{cx}{1-x+cx}\left[ \ln c + \ln\left(\frac{1-x}{1-x+cx}\right)\right]\right\}
$$

Teniendo en cuenta las expresiones de las magnitudes {eq}`nbar_agg_short`,  $P(0)$ y $c$,

$$
-k_{\mathrm{B}}\sum_{N=0}^{\infty}P(N)\ln P(N) = -k_\mathrm{B}\ln P(0) - k_\mathrm{B}\left\{\overline{N}\ln x  + \left[1-P(0)\right]\left[ \frac{\epsilon}{k_\mathrm{B}T} + \ln P(0)\right]\right\} \; .
$$

Reordenando la ecuación, llegaremos a la meta:

$$
\boxed{-k_{\mathrm{B}}\sum_{N=0}^{\infty}P(N)\ln P(N) = -\overline{N}k_{\mathrm{B}}\ln x - k_\mathrm{B}\ln P(0) - \left[1-P(0)\right]\frac{\epsilon}{T}}
$$ (pnlnpn_def)

Pongamos las ecuaciones {eq}`stn_agg_short` , {eq}`stmu_agg_short` y {eq}`pnlnpn_def` frente a frente. Una vez realizada esta observación, es evidente que el aumento de entropía causado por la transición del conjunto canónico al nanocanónico es asociable a las fluctuaciones relacionadas con el número de partículas $N$ . Además, podemos percibir que en la región nanotermodinámica $(\overline{N} \not \to \infty)$, dichas fluctuaciones alrededor de $N$ serán significativas con respecto a los términos lineales. Este último resultado ha revelado una vez más que el conjunto nanocanónico es indispensable para garantizar la maximización de la entropía de los sistemas pequeños.

```

**----------------------------------------------------**

Más en adelante, en concreto en el {numref}`ejemplo {number} <agg_elek>`, sumergiremos el agregado lineal en un campo eléctrico, y examinaremos la influencia que esto acarreará a las magnitudes calculadas a lo largo del presente análisis. 


(mupt_gi)=
### Ejemplo: Gas ideal clásico, en la colectividad nanocanónica

El punto de partida para el segundo análisis de este sistema es la ecuación {eq}`dtpn_gi` del {numref}`ejemplo {number} <gitpn>`.

##### Ejercicio
Calcula estas expresiones: la función de partición $\Upsilon(T,p,\mu)$, el potencial de subdivisión $\mathscr{E}(T,p,\mu)$ y la entropía $S(T,p,\mu)$. A continuación, construye las magnitudes $\overline{N}$ y $\overline{V}$, y reescribe la entropía en función de ellas; esto es, $S(T,\overline{V},\overline{N})$.

```{dropdown} __Solución__

Aplicando a la función de partición $\Delta(T,p,N)$ la transformación de Legendre asociada a la activación del grado de libertad químico, construiremos la función de partición generalizada:

$$
\Upsilon(T,p,\mu) = \sum_{N=0}^{\infty} \left(\frac{k_{\mathrm{B}}T\lambda}{p\Lambda^3}\right)^{N} = \frac{1}{1 - k_{\mathrm{B}}T\lambda/(p\Lambda^3)} \; , \; \left| \frac{k_{\mathrm{B}}T\lambda}{p\Lambda^3} \right| < 1 \; ,
$$ (upsilongi)

en donde hemos sustituido la expresión $\lambda = e^{\mu/k_{\mathrm{B}}T}$. Por tanto,

$$
\mathscr{E}(T,p,\mu) = k_{\mathrm{B}}T \ln\left(1- \frac{k_{\mathrm{B}}T\lambda}{p\Lambda^3}\right) = -k_{\mathrm{B}}T \ln(\overline{N} + 1) < 0 \; .
$$ (epsilontpmugi)

El lado derecho de la ecuación la hemos reescrito con ayuda del par de expresiones de {eq}`barnbarvtpmugi`:

$$
 \overline{N} = \frac{1}{p\Lambda^3/(k_{\mathrm{B}}T\lambda) - 1} \quad , \quad \overline{V} = \frac{\overline{N}k_{\mathrm{B}}T}{p} \; .
$$(barnbarvtpmugi)

De esta forma, obtendremos la tercera expresión de la entropía:

$$
\boxed{S(T,p,\mu) =  \overline{N}k_{\mathrm{B}}\left[\ln\left(\frac{\overline{V}}{\Lambda^3}\frac{\overline{N}+1}{\overline{N}^2}\right) + \frac{5}{2}\right] + k_{\mathrm{B}}\ln(\overline{N} + 1)}
$$ (stpmugi)
```
**----------------------------------------------------**

Examinemos la ecuación {eq}`stpmugi` de la entropía obtenida por medio de la colectividad nanocanónica. Recordemos también las expresiones {eq}`stvngi` del [_apéndice C_](gitvn) y {eq}`stpngi`, y coloquémoslas frente a frente ({numref}`tabla {number} <taula_s_gi>` y {numref}`figura {number} <sn100>`). En todas ellas, la contribución principal es la expresión de Sackur-Tetrode _extensiva_ $( S_ {0} )$. Pero, en comparación con los dos primeros, en la ecuación {eq}`stpmugi` se puede apreciar otro término _positivo_, y, por lo tanto, en sistemas pequeños predominará $S(T,p, \mu)$.


```{list-table} Entropía y potencial de subdivisión del gas ideal, en cuatro colectividades estadísticas.
:header-rows: 1
:name: taula_s_gi

* - Variables
  - Potencial de subdivisión
  - Entropía
* - $\left(T, V,N\right)$
  - $\frac{\mathscr{E}}{k_{\mathrm{B}}T} \approx \ln\left(\frac{\sqrt{2\pi N}}{e}\right) + \frac{7}{12N} > 0$
  - $\frac{S}{k_\mathrm{B}} \approx N \left[\ln \left(\frac{V}{\Lambda^{3} N}\right)+\frac{5}{2}\right]-  \ln \sqrt{2 \pi N} - \frac{1}{12N}$
* - $\left(T,p,N\right)$
  - $\mathscr{E} = 0$
  - $\frac{S}{k_{\mathrm{B}}} =  N\left[\ln\left(\frac{\overline{V}}{\Lambda^3N}\right) + \frac{5}{2}\right]$
* - $\left(T,V,\mu\right)$
  - $\mathscr{E} = 0$
  - $\frac{S}{k_{\mathrm{B}}} =  \overline{N}\left[\ln\left(\frac{V}{\Lambda^3 \overline{N}}\right) + \frac{5}{2}\right]$
* - $\left(T,p,\mu\right)$
  - $\frac{\mathscr{E}}{k_{\mathrm{B}}T} = - \ln(\overline{N} + 1) < 0$
  - $\frac{S}{k_{\mathrm{B}}} = \overline{N}\left[\ln\left(\frac{\overline{V}}{\Lambda^3}\frac{\overline{N}+1}{\overline{N}^2}\right) + \frac{5}{2}\right] + \ln(\overline{N} + 1)$

```

```{figure} sn100.PNG
---
height: 350px
name: sn100
---
Para erigir las curvas, se han empleado los datos pertenecientes al gas $\text{Ar}$ $(1 \; \text{mol})$: $\Lambda = 16,7 \; \mathrm{pm}$ ; $T=273,15 \; \mathrm{K}$ ; $N/V = 2,687\cdot10^{25}\; \mathrm{at/m^3}$. Salta a la vista, por una parte, que a medida que vamos activando grados de libertad, los efectos de tamaño finito aumentan la entropía en la región nanotermodinámica. Por otra, la magnitud $S/Nk_{\mathrm{B}}$ se ha tornado extensiva.

```

Además, el lado derecho de la ecuación {eq}`epsilontpmugi` nos dice que este aumento en la entropía se debe a la contribución _negativa_ y _no extensiva_ del potencial de subdivisión, esto es,


$$
S(T,p,\mu) = S_{0}(T,p,\mu) - \frac{\mathscr{E}(T,p,\mu)}{T} \;.
$$ (stpmuginew)

En la sección {numref}`sección {number} <stabeps>` que viene a continuación, veremos que $\mathscr {E} <0 $ conduce al aumento en el número de réplicas dentro de la colectividad ({numref}`figura {number} <gisub>`).


```{figure} gibbsparadox.PNG
---
height: 300px
name: gisub
---
En el conjunto nanocanónico, el __aumento de la subdivisión reforzará la distinguibilidad__. Al principio, las partículas de cada una de las dos réplicas eran indistinguibles precisamente por pertenecer al mismo subsistema. Pero al final, las paredes divisorias entre los subsistemas las han vuelto distinguibles. Como resultado, la entropía ha aumentado.

```

Considerando la imagen y la ecuación {eq}`stpmugi`, las contribuciones resultantes de la subdivisión del conjunto incrementarán la variación de entropía, puesto que se cumple que $ \Delta S = k _ {\mathrm {B}} \ln (\overline {N} +1) $. Al llegar a un estado de equilibrio en términos de la subdivisión del colectivo, tendremos que $\overline{N} \rightarrow 0$, y, de ahí, $\Delta S_{\text{equilibrio}}=0$. Sin embargo, maximizaremos la entropía por número de partícula: 

$$
\lim_{\overline{N} \rightarrow 0}\frac{\Delta S/k_{\mathrm{B}}}{\overline{N}} = 1 \; .
$$ (gi_tpmu_s_n)

Cabe señalar que las explicaciones asociadas a la {numref}`figura {number} <gisub>` son extremadamente importantes, ya que otorgan un significado especial a la colectividad nanocanónica. Por ejemplo, supongamos que dos conjuntos macroscópicos contienen el mismo gas, y que hemos colocado una pared de separación entre ellos. Al eliminar la pared, los dos conjuntos se unificarán. Si nos basáramos de la Termodinámica, argumentaríamos de la siguiente manera: como los gases no se pueden diferenciar, el proceso deberá haber sido reversible, lo cual significa que $ \Delta S = 0 $. Sin embargo, si seguimos por este camino, nos encontraremos con la **paradoja de Gibbs**, ya que la entropía sufrirá, en realidad, una variación positiva. Para afrontar esto, impondremos la indistinguibilidad de las partículas, y parece ser que el factor _ad hoc_ $1/N!$ de Gibbs soluciona el problema... 

Por el contrario, si fuéramos más allá de lo que dice la Termodinámica, y siguiéramos el razonamiento basado en la Nanotermodinámica, procederíamos de esta forma: al combinar los dos sistemas, la colectividad nanocanónica comenzará a subdividirse, acrecentando la distinguibilidad de las partículas. Por tanto, aunque los dos gases sean iguales, en la región nanotermodinámica se _entremezclarán_ **irreversiblemente**, y la colectividad  reflejará este fenómeno en el aumento de la entropía, llegando así a maximizarla. Así, al intensificar la distinguibilidad dentro de la colectividad nanocanónica, eludiremos la paradoja de Gibbs en los sistemas pequeños {cite}`nanointro, multiscale`.

Los efectos de tamaño finito que yacen detrás de esta solución innovadora están bajo la dirección del potencial $ \mathscr {E} $. Le dedicaremos la última sección perteneciente a la teoría en su totalidad, profundizando en el papel que juega en el equilibrio asociado a la subdivisión.

##### Ejercicio: Gas ideal clásico, en la colectividad macrocanónica $\left(T,V,\mu\right)$

Calcula los resultados de la tercera fila de la {numref}`tabla {number} <taula_s_gi>`.

```{dropdown} __Solución__

Para empezar, la función de partición nanocanónica es

$$
\Xi (T,V,\mu) = \sum_{N=0}^{\infty}\; Q(T,V,N)\;e^{\mu N/k_{\mathrm{B}}T} = \sum_{N=0}^{\infty}\;\frac{1}{N!}\left(\frac{V\lambda}{\Lambda^3}\right)^N = e^{V\lambda/\Lambda^3} := e^{\widehat{p}V/k_{\mathrm{B}}T} \; .
$$ (gi_xi)

De ahí, nos percataremos de que la presión integral $\widehat{p}$ coincide con la presión diferencial $p$; de hecho, la expresión

$$
\widehat{p}V = -\frac{k_{\mathrm{B}}T  \lambda}{\Lambda^3}V
$$ (gi_widehatp_v)

es una función Euler-homogénea de primer orden. Por consiguiente, tenemos que $\mathscr{E} = 0$. Al mismo tiempo,

$$
\overline{N} = \left[\frac{\partial \left(\widehat{p}V\right)}{\partial \mu}\right]_{T,V} = \frac{\lambda V}{\Lambda^3} \; ,
$$ (gi_barn_makro)

y, sustituyendo esa expresión en la ecuación {eq}`gi_widehatp_v` obtendremos la entropía:

$$
\boxed{S(T,V,\mu) = \left[\frac{\partial \left(\widehat{p}V\right)}{\partial T}\right]_{V,\mu} = \overline{N}k_{\mathrm{B}}\left[\ln\left(\frac{V}{\Lambda^3 \overline{N}}\right) + \frac{5}{2}\right]} \; .
$$ (gi_s_makro)

```

(stabeps)=
### Potencial de subdivisión y estabilidad

Para empezar, recordemos la definición del potencial $\mathscr{E}$: la contribución a la energía total de la colectividad a causa de influenciar en su número de réplicas, manteniendo constantes el resto de las variables ambientales respectivas, es decir,

$$
\mathscr{E} := \left(\frac{\partial E_{t}}{\partial \mathscr{N}}\right)_ {S_{t},V_{t}, N_{t}} \equiv \left(\frac{\partial A_{t}}{\partial \mathscr{N}}\right)_ {T,V_{t}, N_{t}} \equiv \left(\frac{\partial F_{t}}{\partial \mathscr{N}}\right)_ {T,p, N_ {t}} \; .
$$ (epsilonnewdef)

En otras palabras, en el caso de la colectividad nanocanónica, representa el trabajo que se le debe realizar al conjunto para crear una nueva réplica.

$$
\\
$$

En este sentido, en la presente sección discutiremos la naturaleza espontánea de las variaciones en el número promedio de réplicas, $ \overline{\mathscr {N}} $. Supondremos que los subsistemas del conjunto son completamente libres, pero deberán contener al menos una partícula ($ N \geq 1 $). El conjunto de variables de entorno de la colectividad será $(T,p,N_ {t})$, donde $N_{t} = \overline{\mathscr{N}}\;\overline{N}$.

Así las cosas, en el camino hacia el equilibrio a través del proceso espontáneo, la energía libre $ F_ {t} (T, p, N_ {t}) $ tenderá a su valor mínimo, y, por lo tanto, $ \mathrm {d} F_ {t} <0 $. Si el conjunto se mantiene aislado durante el proceso, todas las variables excepto $ \overline {\mathscr {N}} $ permanecerán invariables. En consecuencia, considerando la parte derecha de la ecuación {eq}`epsilonnewdef`,


$$
\mathrm{d}F_{t}=\mathscr{E}\mathrm{d}\overline{\mathscr{N}}<0\; .
$$ (dft)

Esta expresión nos sugiere que cuando el potencial de subdivisión es positivo, disminuirá el número de réplicas, y, cuando es negativo, se intensificará la subdivisión de la colectividad, creando subsistemas más pequeños (recordemos la {numref}`figura {number} <gisub>`). Además, como al alcanzar el equilibrio la energía se encontrará en un mínimo, se cumplirá asimismo que

$$
\left(\frac{\partial^2 F_{t}}{\partial \overline{\mathscr{N}}^2}\right)_{T,p, N_{t}} = \left(\frac{\partial \mathscr{E}}{\partial \overline{\mathscr{N}}}\right)_{T,p, N_{t}} > 0 \; .
$$ (d2f)

Resulta evidente que $\mathrm{d}\mathscr{E}$ y $\mathrm{d}\overline{\mathscr{N}}$ son del mismo signo. Además de eso, considerando la ecuación {eq}`dft`, se cumplirá  $\mathscr{E}\cdot\mathrm{d}\mathscr{E} <0$. Esta significativa conclusión nos ayudará a completar la explicación del {numref}`ejemplo {number} <mupt_gi>`: dado que $\mathscr{E}$ y $\mathrm{d}\mathscr{E}$ son de signos opuestos, a medida que $\overline{\mathscr {N}} $ aumenta, el potencial $ \mathscr {E} $ tenderá a cero, hasta alcanzar el equilibrio. **Un estado de equilibrio correspondiente a la subdivisión** debe satisfacer la condición $ \mathscr {E} = 0 $.

Debido a esta última frase, necesitamos aclarar un última asunto. Para llegar a ello, retomaremos el ejemplo del gas ideal. Antes de nada, tengamos en cuenta que a los sistemas pequeños les hemos establecido la condición $ N \geq 1 $. Por ende, necesitaremos extraer el término $ N = 0 $ de la ecuación {eq}`upsilongi`. Reemplazando $ x = k _ {\mathrm {B}} T \lambda / (p \Lambda ^ 3) $, la nueva función de partición será

$$
 \Upsilon = \frac{x}{1-x}
$$ (upsilonginew)

De ahí volveremos a calcular las magnitudes $\mathscr{E}$ y $\overline{N}$:

$$
\mathscr{E} = -k_{\mathrm{B}}T\ln\left(\frac{x}{1-x}\right) = -k_{\mathrm{B}}T\ln\left(\overline{N}-1\right) \; ,
$$ (epsginew)

$$
 \overline{N} = \frac{1}{1-x} = 1 + e^{-\mathscr{E}/k_{\mathrm{B}}T} \; .
$$ (barnginew)


Supongamos que ahora iniciamos un proceso espontáneo que cambiará el número de subsistemas $ \overline {\mathscr {N}} $, manteniendo $ T $ y $ p $ constantes. Durante la subdivisión ($\mathrm{d}\overline{\mathscr{N}} <0$ o $\mathrm{d}\overline{\mathscr{N}}>0$), la entropía sufrirá la variación $\Delta S =  \pm k _ {\mathrm {B}} \ln (\overline {N} / 2)$. Cuando se alcance el equilibrio,

$$
\mathscr{E}_ {\text{equilibrio}} = 0 \quad \Rightarrow \quad \overline{N}_ {\text{equilibrio}}=2 \quad \text{y} \quad \Delta S_{\text{equilibrio}}=0 \; .
$$

Recordemos que antes, al insertar el término $ N = 0 $ en la función de partición, la condición $ \overline {N} \rightarrow 0 $ nos llevaba al equilibrio, lo que podría dar a entender que la subdivisión es incesante. Por el contrario, parece que los resultados obtenidos ahora son de mayor sentido y significado físico.

$$
\\
$$

Finalmente, abordaremos el aspecto que ha quedado por aclarar. Como hemos ido mencionando en varias secciones anteriores, en el límite macroscópico, las contribuciones que cumplen una relación lineal con la variable $ \overline {N} $ prevalecerán fuertemente sobre el potencial de subdivisión, y por lo tanto $ \mathscr {E} $ se considerará despreciable. Pues bien, esta última frase puede resultar engañosa, puesto que nos puede conducir hacia una argumentación errónea. De hecho, podría sugerirnos que, dado que el sistema macroscópico percibe que $ \mathscr {E} \approx 0 $, _el límite macroscópico es en sí un estado de equilibrio_. 

De hecho, debemos actuar con cautela ante ese concepto. Por ejemplo, en el caso del gas ideal, el límite macroscópico ($\overline{N}\rightarrow\infty$) de la ecuación {eq}`epsginew` viene a ser

$$
\mathscr{E} = -k_{\mathrm{B}}T\ln \overline{N} \; .
$$ (epslimgi)

Como resultado, el potencial de subdivisión aumentará en módulo, aunque sea más lentamente que otras funciones de carácter lineal. Es cierto que las expresiones obtenidas en otros casos (por ejemplo, en las secciones {numref}`{number} <helix_coil>` y {numref}`{number} <app>`) sí que cumplen $\mathscr{E}\rightarrow 0$ en el límite macroscópico, pero la ecuación {eq}`epslimgi` deja en claro que en general esto no sucederá. Además, cabe destacar que el significado de este límite a cero del potencial de subdivisión no corresponde a la estricta condición $ \mathscr {E} = 0 $ requerida por un estado de equilibrio. Por lo tanto, generalmente no es lícito afirmar que el estado macroscópico es equivalente a un estado de equilibrio.


$$
**********
$$

Estos comentarios esclarecedores darán el cierre a la parte de la teoría correspondiente a la Termodinámica de Sistemas Pequeños. Al final, ({numref}`capítulo {number} <app>`) saltaremos de la década de 1960 al año 2021, y nos sumergiremos en una importante aplicación actual de la teoría de Hill.

Pero antes, los siguientes dos apartados ({numref}`{number} <elek_mag>` y {numref}`{number} <osagarri>`) están destinados a presentar nuevos ejemplos. Asimismo, se modificarán varios sistemas ya trabajados (el agregado lineal, entre otros) incorporando nuevas contribuciones a las magnitudes más relevantes. Hay que decir que éstos nos resultarán fructíferos y representativos, a fin de completar la teoría de Hill y establecer el punto de partida para su extensión a aplicaciones importantes.

