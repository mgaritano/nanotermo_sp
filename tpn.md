(tpn)=
## Colectividad isotérmica-isobárica: variables de entorno $(T,p,N)$ 

Antes de emprender con la Física de este capítulo, cabe remarcar lo siguiente: como veremos en la {numref}`sección {number} <tpmu>`, la transición a la colectividad nanocanónica $(T,p,\mu)$ la emprendemos desde la función de partición canónica $Q(T,V,N)$, aplicando transformaciones de Legendre. Si escogemos la colectividad macrocanónica $(T,V,\mu)$ como intermediaria, a veces el camino nos resultará escabroso. Así pues, si en lugar de calcular la integral en el volumen realizamos el sumatorio en el número de partículas $N$ partiendo del colectivo isotérmico-isobárico, el camino resultará más fácil. Por otra parte, mediante las variables $(T,p,N)$ es posible describir una macromolécula incompresible pero extensible. En este sentido, en el {numref}`apartado {number} <helix_coil>` presentaremos y trabajaremos el primer ejemplo, aún con aproximaciones especiales.


Así las cosas, merece la pena dedicar un análisis más profundo a la colectividad en cuestión.

(tpn_azter)=
### Estudio de la colectividad

Las variables extensivas de los sistemas pequeños serán $\overline{E}=E_{t}/\mathscr{N}$, $\overline{V}=V_{t}/\mathscr{N}$ y $N=N_{t}/\mathscr{N}$. 

##### Ejercicio

Teniendo en cuenta lo mencionado en la frase anterior, y siguiendo las explicaciones de la {numref}`sección {number} <hillsec>`,
construye las siguientes expresiones:

$(a)$ La ecuación de Hill-Gibbs asociada a la colectividad isotérmica-isobárica y la energía de réplica $X(T,p,N)$. Explica los resultados.

```{dropdown} __Solución__
$$
\mathrm{d}E_{t}(S_{t},V_{t},N,\mathscr{N}) = T\mathrm{d}S_{t} - p\mathrm{d}V_{t} + \mu \mathscr{N}\mathrm{d}N + (\mathscr{E}+\mu N)\mathrm{d}\mathscr{N}
$$ (dEttpn)

$$
X(T,p,N) = \mathscr{E} + \mu N := \left(\frac{\partial E_{t}}{\partial \mathscr{N}}\right)_{S_{t},V_{t},N} := \widehat{\mu}N \; .
$$ (xtpn)
```

```{dropdown} __Explicaciones__
En este caso, la variable $N$ debe aparecer en la ecuación, empleando la relación $\mathrm{d}N_{t} = \mathscr{N}\mathrm{d}N + N\mathrm{d}\mathscr{N}$. De esta forma, dejaremos de tener bajo control externo la variable $N_{t}$. 
Al mismo tiempo, la energía de réplica de la ecuación {eq}`xtpn` refleja la naturaleza de la colectividad. Al incluir una réplica, el volumen y la energía total se subdividirán, puesto que los sistemas pequeños pueden variar dichas variables con total libertad. Sin embargo, la magnitud $N$ debe permanecer invariable. En consecuencia, la energía interna total percibiría una aportación química caracterizada por el potencial $\widehat{\mu}$ a causa de la inclusión de un nuevo conjunto de $N$ partículas. En consecuencia, nos vemos obligados a modelar la contribución química antes mencionada insertando un potencial químico al nivel de la colectividad: $\widehat{\mu}$; éste no presentará el comportamiento del potencial $\mu$ asignado a los subsistemas, debido a la diferenciación ocasionada por los efectos de tamaño finito en la nanoescala.
```

$(b)$ La ecuación de Gibbs de los sistemas pequeños, y la energia interna.
```{dropdown} __Solución__
$$
\mathrm{d}\overline{E} = T\mathrm{d}S - p\mathrm{d}\overline{V} + \mu \mathrm{d}N
$$ (detpn)
$$
\overline{E} = TS - p\overline{V} + \widehat{\mu}N
$$ (etpn)
```
$(c)$ La energía libre de Gibbs, $F(T,p,N)$. Partiendo de ahí, escribe la expresión que relaciona la magnitud diferencial con la magnitud integral.

```{dropdown} __Solución__
$$
F(T,p,N) := \overline{E} - TS + p\overline{V} = \widehat{\mu}N
$$ (ftpn)
$$
\mathrm{d}F(T,p,N) = \mathrm{d}(\widehat{\mu}N) = -S\mathrm{d}T + \overline{V}\mathrm{d}p + \mu\mathrm{d}N \;
$$ (dftpn)
$$
\boxed {\mu := \left[\frac{\partial(\widehat{\mu}N)}{\partial N}\right]_{T, p} = \widehat{\mu} + N\left(\frac{\partial \widehat{\mu}}{\partial N}\right)_{T,p}}
$$ (mumuhat)
```

**----------------------------------------------------**

La ecuación {eq}`ftpn` muestra la relación entre la energía libre de Gibbs y el **potencial químico integral**: $F := \widehat{\mu}N$. Este último, junto al **potencial químico diferencial**, define el potencial de subdivisión: $\mathscr{E} =  (\widehat{\mu} - \mu)N$. Así, con las ecuaciones {eq}`xtpn` y {eq}`dftpn` escribiremos la expresión del potencial $\mathrm{d}\widehat{\mu}$:

$$
\boxed{\mathrm{d}\widehat{\mu} = -\frac{S}{N}\mathrm{d}T + \frac{\overline{V}}{N}\mathrm{d}p - \frac{\mathscr{E}}{N^2}\mathrm{d}N}
$$ (dmuhat)

Resultaría interesante asignar una expresión semejante al potencial $\mu$. Para este fin, primero debemos obtener las relaciones de Maxwell partiendo de {eq}`dftpn` y empleando las propiedades conmutativas de las derivadas. Por ejemplo,

$$
\left(\frac{\partial \mu}{\partial T}\right)_{p, N} := \frac{\partial}{\partial T}\left(\frac{\partial F}{\partial N}\right)_{T, p} =  \frac{\partial}{\partial N}\left(\frac{\partial F}{\partial T}\right)_{p, N} := -\left(\frac{\partial S}{\partial N}\right)_{T, p}  \; ,
$$ (dmuhatdT)

$$
\left(\frac{\partial \mu}{\partial p}\right)_{T, N} := \frac{\partial}{\partial p}\left(\frac{\partial F}{\partial N}\right)_{T, p} =  \frac{\partial}{\partial N}\left(\frac{\partial F}{\partial p}\right)_{T, N} := \left(\frac{\partial \overline{V}}{\partial N}\right)_{T, p} \; .
$$ (dmuhatdp)

También utilizaremos la expresión del potencial de subdivisión y el último término de la ecuación {eq}`dmuhat` para obtener

$$
\left(\frac{\partial \mu}{\partial N}\right)_{T, p} = \left(\frac{\partial \widehat{\mu}}{\partial N}\right)_{T, p} - \left[\frac{\partial (\mathscr{E}/N)}{\partial N}\right]_{T,p} = - \frac{1}{N}\left(\frac{\partial \mathscr{E}}{\partial N}\right)_{T,p} \; .
$$

Por lo tanto,

$$
\boxed{\mathrm{d}\mu = -\left(\frac{\partial S}{\partial N}\right)_{T,p}\mathrm{d}T + \left(\frac{\partial \overline{V}}{\partial N}\right)_{T,p}\mathrm{d}p - \frac{1}{N}\left(\frac{\partial \mathscr{E}}{\partial N}\right)_{T,p}\mathrm{d}N} \; .
$$ (dmu)

Las ecuaciones {eq}`dmuhat` y {eq}`dmu` han sacado a la luz la naturaleza integral y diferencial de los dos potenciales químicos, respectivamente. Igualmente, son reveladores de la no linealidad de las variables extensivas respecto a $N$. Finalmente, el último término de la ecuación {eq}`dmu` resulta ser igual a $\left(\partial \mu/\partial N\right)_{T,p}\mathrm{d}N$ por definición. Esto nos sugiere que el potencial químico $\mu$ generalmente no es intensivo, esto es, $\mu = \mu(T,p,N)$. En el límite macroscópico ambas ecuaciones coincidirán, precisamente con la relación {eq}`gibbs-duhem` (Hill-Gibbs-Duhem):

$$
\mathrm{d}\left[\left(\widehat{\mu}-\mu\right)N\right] = \mathrm{d}\mathscr{E} = -S\mathrm{d}T+\overline{V}\mathrm{d}p-N\mathrm{d}\mu \; .
$$ (depsilontpn)

Sin embargo, resultaría más apropiado que las variables $(T,p,N)$ sustituyeran a las variables $(T,p,\mu)$ que aparecen en la ecuación {eq}`depsilontpn`. Para este fin, introduciremos allí la expresión {eq}`dmu`, lo cual nos permitirá realizar una reescritura muy ilustrativa de la ecuación en cuestión:

$$
\boxed{\mathrm{d}\mathscr{E} = -\left[S-N\left(\frac{\partial S}{\partial N}\right)_{T,p}\right]\mathrm{d}T+\left[\overline{V}-N\left(\frac{\partial \overline{V}}{\partial N}\right)_{T,p}\right]\mathrm{d}p + \left(\frac{\partial \mathscr{E}}{\partial N}\right)_{T,p} \mathrm{d}N} \; .
$$ (depsilontpn2)

Antes de proseguir, trataremos de identificar los efectos de tamaño finito en las expresiones obtenidas hasta el momento, tales como las derivadas de magnitudes intensivas en el límite termodinámico (como $\widehat{\mu}$ y $\mu$) con respecto al tamaño, $N$. De hecho, las variables extensivas recobrarán el carácter homogéneo; es decir, prevalecerá la aportación lineal. Por ejemplo,

$$
\lim_{N\rightarrow \infty} \left(\frac{\partial \overline{V}}{\partial N}\right)_{T,p} = \frac{\overline{V}}{N} \; ,
$$ (barV_mak)

$$
\lim_{N\rightarrow \infty} \left[\frac{\partial (\widehat{\mu}N)}{\partial N}\right]_{T,p} = \frac{\widehat{\mu}N}{N} \quad \Rightarrow \quad \mu = \widehat{\mu} \; .
$$ (mu_mak)

Queda en evidencia, por consiguiente, que todos los términos de la ecuación {eq}`depsilontpn2` son _pequeños_, y relevantes solamente en la región nanotermodinámica. Ahondando en lo mencionado, examinemos el efecto de la variación de $N$ en las siguientes magnitudes intensivas: $S/N$, $\overline{V}/N$ y $N/\overline{V}$. De la ecuación {eq}`depsilontpn2` podemos construir fácilmente estas expresiones:

$$
\left[\frac{\partial \left(S/N\right)}{\partial N}\right]_{T,p} = \frac {1}{N^2}\left(\frac{\partial \mathscr{E}}{\partial T}\right)_{p,N} \, ,
$$ (dsdntp)

$$
\left[\frac{\partial (\overline{V}/N)}{\partial N}\right]_{T,p} = - \frac {1}{N^2}\left(\frac{\partial \mathscr{E}}{\partial p}\right)_{T,N} \; ,
$$ (dvdntp)

$$
\left[\frac{\partial (N/\overline{V})}{\partial N}\right]_{T,p} =  \frac {1}{\overline{V}^2}\left(\frac{\partial \mathscr{E}}{\partial p}\right)_{T,N} \; .
$$ (dndvtp)

Debemos remarcar que mediante la Termodinámica Clásica no alcanzaremos a lograr las últimas tres ecuaciones. Dicho de otra forma, la Nanotermodinámica, además de hacer aflorar los efectos de tamaño finito, nos abastecerá de relaciones que van más allá del alcance del límite termodinámico. A modo de comprobación, en el {numref}`ejemplo {number} <helix_coil>`, verificaremos que ambas partes de la ecuación {eq}`dvdntp` son coincidentes.

$$
\\
$$

Pero antes de concluir esta sección, erigiremos otro par de ecuaciones, también de cara al ejemplo que viene seguidamente. Recordando que la entalpía cumple la relación $H(S,p,N) := F(T,p,N) + TS := \widehat{\mu}N + TS$, transformaremos los potenciales químicos de esta manera:

$$
\widehat{\mu} =\frac{H}{N} - T\frac{S}{N} \; ,
$$ (muhat_H)

y,

$$
\mu := \left(\frac{\partial F}{\partial N}\right)_{T,p} = \left(\frac{\partial H}{\partial N}\right)_{T,p} - T\left(\frac{\partial S}{\partial N}\right)_{T,p} \; .
$$ (mu_H)

De ahí podemos obtener lo siguiente:

$$
 \left(\frac{\partial \widehat{\mu}/T}{\partial T}\right)_{p,N} = -\frac{1}{T^2}\frac{H}{N} \quad \pmb{\neq} \quad \left(\frac{\partial \mu/T}{\partial T}\right)_{p,N} = -\frac{1}{T^2}\left(\frac{\partial H}{\partial N}\right)_{T,p} \; .
$$ (mu_muhat_h)

Así pues, en la siguiente sección, tras calcular el par de potenciales $\widehat{\mu}$ y $\mu$ asociados a la cadena _hélice-ovillo_, observaremos la apariencia de los efectos de tamaño finito que diferencian las relaciones {eq}`mu_muhat_h`.


(helix_coil)=
### Ejemplo: transición hélice-ovillo

El sistema a tratar consiste en la cuerda o cadena unidimensional de la {numref}`figura {number} <heco>`. Ésta se compone de $n_{H}$ unidades de hélice y $n_{C}= N - n_{H}$ unidades de ovillo. Una fuente de calor establecerá la temperatura $T$, y mantendremos $N$ invariable. Así, emplearemos $(T,f,N)$ como variables de control, tomando $\overline{l}$, la longitud media de la cuerda, como la conjugada extensiva de la fuerza $f$.

```{figure} helix-coil.PNG
---
height: 200px
name: heco
---
La cadena _hélice-ovillo_ contiene unidades de hélice $(H)$ y unidades de ovillo $(C)$. En ambos extremos se ejercerá una fuerza $f$. En cuanto al número total de unidades, si prescindimos del límite asintótico $N\rightarrow\infty$, la cadena mostrará las particularidades de un sistema pequeño, las cuales afectarán significativamente a las variables de carácter intensivo en términos macroscópicos.
```

Para comenzar, supongamos que las unidades ovillo $(C)$ pueden colocarse únicamente en los extremos de la cuerda. En el caso de la figura, dispondríamos de las configuraciones $C\;H\;H\;H\;C$ , $C\;C\;H\;H\;H$ y $H\;H\;H\;C\;C$. Generalizando, esta condición impondría una degeneración $g(n_{H}) = N-n_{H}+1$ al sistema. En particular, si no hubiera unidades $H$, tendríamos $g=1$. Designaremos las funciones de partición de las unidades $C$ y $H$ $q_{H}(T)$ y $q_{C}(T)$, respectivamente. De esta forma, la función de partición canónica de la totalidad del sistema obedecería la relación $Q(T,l,N)=q_{C}^{n_{C}}q_{H}^{n_{H}}$. Partiendo de ahí, llegaremos a su homóloga isotérmica-isobárica, $\Delta(T,f,N)$:

$$
\Delta := \sum_{l} Q(T,l,N)e^{fl/k_{\mathrm{B}}T}
     = \sum_{n_{H}=0}^{N} g(n_{H})q_{C}^{N-n_{H}}q_{H}^{n_{H}}e^{\left[\left(N-n_{H}\right)l_{C} + n_{H}l_{H}\right]f/k_{\mathrm{B}}T} \; .
$$ (d)

En aras de la simplificación de cálculos posteriores, adoptaremos una aproximación un tanto cruda: el sistema puede consistir de solamente  unidades $H$, o bien de unidades $C$. En el ejemplo de la figura contaríamos con $H\;H\;H\;H\;H$ y $C\;C\;C\;C\;C$. De esta manera, extrayendo los términos $n_{H}=0$ y $n_{H}=N$ del sumatorio, abreviaremos la expresión de la función de partición:

$$
\Delta = q_{C}^Ne^{Nl_{C}f/k_{\mathrm{B}}T} + q_{H}^Ne^{Nl_{H}f/k_{\mathrm{B}}T} = r_{C}^N(1 + r^N)\; .
$$ (d_short)

Hemos sintetizado la ecuación reemplazando $r_{C,H}(T,f) = q_{C,H}(T)\exp(fl_{C,H}/k_{\mathrm{B}}T)$ y $r=r_{H}/r_{C}$. Es de mencionar que, a pesar de que el modelo sugerido por la función de partición simplificada {eq}`d_short` carece de realismo, no influirá en la finalidad didáctica del presente ejemplo.

Antes de nada, tomemos el límite $N\rightarrow \infty$:

$$
\Delta(T,f,N) =
    \begin{cases}
      r_{C}^N & \text{$r<1$ bada.}\Rightarrow N = n_{C} \\
      r_{H}^N & \text{$r>1$ bada.}\Rightarrow N = n_{H}
    \end{cases}  
$$

Salta a la vista que, en el caso $r=1$, en la cadena tendrá lugar una repentina **transición de fase** (en el límite termodinámico).

El siguiente paso consiste en describir la Termodinámica del sistema mediante la ecuación {eq}`d_short`. Para comenzar, la energía libre de Gibbs sigue la definición $F(T,f,N) := -k_{\mathrm{B}}T\ln\Delta$. 


##### Ejercicio

$(a)$ Calcula los potenciales $\widehat{\mu}$ y $\mu$. Después, construye el potencial de subdivisión, y analiza su evolución en función del tamaño del sistema. Emplea los valores  $r = 0,5 \; ;  \; r = 0,98$ y $r=1,05$.

```{dropdown} __Solución__
$$
\widehat{\mu} := \frac{F}{N} = -k_{\mathrm{B}}T\left[\ln r_{C} + \frac{1}{N}\ln(1+r^N)\right]
$$ (muhathelix)

$$
\mu := \left(\frac{\partial F}{\partial N}\right)_{T,f} = -k_{\mathrm{B}}T\left[\ln r_{C} + \frac{r^N\ln r}{1 + r^N}\right]
$$ (muhelix)

$$
\mathscr{E} = (\widehat{\mu}-\mu)N = -k_{\mathrm{B}}T\left[\ln(1+r^N) - N\frac{r^N\ln r}{1 + r^N}\right]
$$ (epsilonhelix)

```{figure} epsilon_tfn.PNG
---
height: 300px
name: epsilon_tfn
---
  La evolución de las contribuciones finitas se rige por medio del potencial de subdivisión. A medida que $N$ aumenta, $\mathscr{E}$ decrece, y junto a ello se restablecen las expresiones macroscópicas. Por otra parte, el ratio $r=r_{H}/r_{C}$ influye directamente sobre la extensión de la región nanotermodinámica. A medida que nos acercamos al punto donde acaece la transición de fase $(r \rightarrow 1)$, dicha región abarcará una mayor amplitud, y el potencial de subdivisión tenderá a la constante $\mathscr{E}\rightarrow\mathscr{E}_{0} = -k_{\mathrm{B}}T \ln 2$.
```


$(b)$ Partiendo de los potenciales químicos obtenidos en el apartado anterior, construye la pareja de {eq}`mu_muhat_h` y su límite macroscópico (considera la transición de $r<1$ a $r>1$). Examina, asimismo, las contribuciones que diferencian ambas expresiones, y relaciónalas con el potencial de subdivisión.


```{dropdown} __Solución__

$$
\left(\frac{\partial \widehat{\mu}/T}{\partial T}\right)_{f, N} = -k_{\mathrm{B}}\left(\frac{1}{r_{C}}\frac{\partial r_{C}}{\partial T} + \frac{r^{N-1}}{1 + r^{N}}\frac{\partial r}{\partial T}\right) \; ,
$$ (dmuhatT)

$$
\left(\frac{\partial \mu/T}{\partial T}\right)_{f, N} = -k_{\mathrm{B}}\left[\frac{1}{r_{C}}\frac{\partial r_{C}}{\partial T} + N\frac{r^{N-1}}{1 + r^{N}}\left(\frac{1}{N} + \ln r - \frac{r^{N}\ln r}{1 + r^N} \right)\frac{\partial r}{\partial T} \right] \; .
$$ (dmuT)

En el límite termodinámico,

$$
\left(\frac{\partial \widehat{\mu}/T}{\partial T}\right)_{f, N} = \left(\frac{\partial \mu/T}{\partial T}\right)_{f, N} = \begin{cases}
      -k_{\mathrm{B}}\left( \frac{1}{r_{C}} \frac{\partial r_{C}}{\partial T} + \frac{1}{r} \frac{\partial r}{\partial T} \right) & \text{si $r>1$.}\\
      -k_{\mathrm{B}}\frac{1}{r_{C}}\frac{\partial r_{C}}{\partial t}& \text{ si $r<1$.}
    \end{cases} 
$$ (dmuT_mak)

No obstante, considerando que el sistema es pequeño,

$$
\frac{1}{k_{\mathrm{B}}\; \partial r/\partial T}\left(\frac{\partial \mathscr{E}/NT}{\partial T}\right)_{f,N} = -N\frac{r^{N-1}}{1+r^N}\ln r \left(1-\frac{r^N}{1+r^N}\right) \; .
$$ (dmuT_epsilon)

```{figure} epsilon_mu_muhat.png
---
height: 300px
name: epsilon_mumuhat
---
  Podemos percibir que la expresión del potencial de subdivisión por unidad de partícula (ecuación {eq}`dmuT_epsilon`) sufre una transición más severa al límite macroscópico. Precisamente, a diferencia de la {numref}`figura {number} <epsilon_tfn>`, podemos afirmar que alrededor de la región $N=90-100$ el sistema muestra un comportamiento macroscópico; en consecuencia, a partir de ese punto, los efectos de tamaño finito no influenciarán significativamente a magnitudes intensivas como $l/N$. Tambiém podemos percibir que el signo de estas contribuciones se invierte tras la transición de fase; pasa de ser positibo en la región donde se cumple que $r<1$ $(N \rightarrow n_C)$ a ser negativo cuando $r>1$ $(N \rightarrow n_H)$.
```


**----------------------------------------------------**

$$
\\
$$

A propósito de estos resultados, emprenderemos con el aspecto de mayor relevancia de esta sección. Erigiremos el gráfico que mostrará la evolución de la fracción media de unidades de hélice del sistema $(\overline{n}_{H}/N)$ en función de la relación $r=r_{H}/r_{C}$. De ahora en adelante, añadiremos una barra a la magnitud $n_{H}$, lo cual especificará la longitud media de la cadena: 

$$
\overline{l}(\overline{n} _ {H}) = (N-\overline{n} _ {H})l_{C} + \overline{n} _ {H}l_{H} \; .
$$ (lbar)

Primeramente, deberemos adquirir la expresión de $\overline{n}_{H}$ mediante la función de partición. Extraeremos el término $n_{H}=0$ del sumatorio de la ecuación {eq}`d`, y reescribiremos $\Delta(T,f,N)$:

$$
\overline{n}_{H} := \frac{\sum _ {n _{H}} n _{H}Q(T,l(n _ {H}), N)e^{fl(n _{H})/k _{\mathrm{B}}T}}{\sum _ {n _{H}} Q(T,l(n _ {H}), N)e^{fl(n _{H})/k _{\mathrm{B}}T}} \equiv \frac{\sum _ {n _{H}} n _{H}Q(T,l(n _ {H}), N)e^{fl(n _{H})/k _{\mathrm{B}}T}}{\Delta(T,f,N)} \; .
$$ (nhdef)

Extraeremos el término $n_{H}=0$ del sumatorio de la ecuación {eq}`d`, y reescribiremos $\Delta(T,f,N)$:

$$
    \Delta = r_{C}^N\left[1+\sum_{n_{H}=1}^{N}\left(N-n_{H}+1\right)r^{n_{H}}\right]\; .
$$ (dnew)

Así, siguiendo la definición {eq}`nhdef`,

$$
\overline{n}_{H} := \frac{r_{C}^N\left[0+\sum_{n_{H}=1}^{N}n_{H}\left(N-n_{H}+1\right)r^{n_{H}}\right]}{\Delta} = r\frac{\partial}{\partial r}\ln \Delta \; .
$$ (nbar)

`````{admonition} Sugerencia
:class: tip
Verifica que ambas partes de la ecuación {eq}`nbar` son coincidentes.
`````

Así, sustituyendo la expresión {eq}`d_short` en la ecuación {eq}`nbar`, llegaremos, al fin, a nuestro destino:

$$
\boxed{\frac{\overline{n} _ {H}}{N} = \frac{r}{N}\frac{\partial}{\partial r}\ln\left[r_{C}^N(1 + r^N)\right] = \frac{r^N}{1+r^N}}\; .
$$(fraction_N)

Contemplemos, a continuación, el gráfico de la expresión {eq}`fraction_N`:

```{figure} hc_phase.PNG
---
height: 350px
name: hc_phase
---
  Las curvas representativas de la fracción media de unidades $H$ muestran una apariencia sospechosa. Ciertamente, resulta que la intensividad no es un concepto tan firme como parece.
```

Atendiendo a los resultados obtenidos, nos vemos obligados a realizar una parada inminente.

Acerquémonos, **con suma atención**, al conjunto de curvas de la {numref}`figura {number} <hc_phase>`. Bajo el punto de vista de la Termodinámica, una magnitud como la fracción media debería ser INTENSIVA por naturaleza. Pero, cuando $N$ varía, ¡la curva $\overline{n}_{H}/N$ cambia de forma! Esto sugiere que la magnitud en cuestión depende del tamaño del sistema, es decir, que es EXTENSIVA en realidad. Además, a medida que $N$ aumenta, disminuye el distanciamiento entre curvas. Tras estas peculiaridades yace la evolución del potencial de subdivisión representada en la {numref}`figura {number} <epsilon_tfn>`.

Por tanto, podríamos afirmar que, alrededor de $N=200$, la magnitud $\overline{n}_{H}/N$ ha recuperado su carácter intensivo, puesto que se puede apreciar la repentina transición de fase hélice-ovillo mencionada al principio del ejemplo. De cualquier forma, ciñéndonos a nuestro estricto criterio, solamente el límite $N \rightarrow \infty$ anulará completamente los efectos de tamaño finito, lo cual nos permitirá acceder al nivel macroscópico. De lo contrario, la cadena hélice-ovillo es un sistema pequeño.

$$
\\
$$

Dicho esto, en el {numref}`capítulo {number} <fase>`, donde trataremos las transiciones de fase en sistemas finitos, tendremos la ocasión de retornar a la {numref}`figura {number} <hc_phase>`. No obstante, antes de emprender con ese capítulo, vamos a retomar por unos instantes el hilo con el que hemos concluido la {numref}`sección {number} <tpn_azter>`.


(helix_ariketa_2)=
#### Ejercicio
La finalidad de este ejercicio suplementario consiste en demostrar que la cadena "hélice-ovillo" satisface la igualdad {eq}`dvdntp`. Antes de nada, debemos percatarnos de que el sistema a tratar es una cadena **unidimensional**; por lo tanto, hemos caracterizado la contribución mecánica a la energía interna por medio de la fuerza $f$ y su variable conjugada, $\overline{l}$. Debido a ello, primero tendremos que reescribir la ecuación en cuestión, adecuándola a las variables que disponemos. Así pues, emprenderemos la tarea paso a paso.

$(a)$ Escribe la ecuación de Gibbs del sistema pequeño. Partiendo de ahí, reconstruye la ecuación {eq}`depsilontpn2`, en base a las variables de control $(T,f,N)$. De ahí, extrae la expresión equivalente de la ecuación {eq}`dvdntp`. Pero antes de empezar, reflexiona acerca del signo de la contribución mecánica $f\overline{l}$; ¿debería ser positibo o negativo? 

```{dropdown} __Solución__
Considerando las explicaciones asociadas a la {numref}`figura {number} <heco>`, si en ambos extremos de la cadena aplicáramos una fuerza $f$ hacia el exterior $(f>0)$, su longitud aumentaría, con lo cual $\Delta l > 0$; por ende, el sistema percibiría un aporte energético $f \Delta l$, el cual incrementará su energía interna. Cabe remarcar que, en el caso de los sistemas hidrostáticos habituales, el comportamiento de la contribución mecánica es diferente. Consideremeos, como ejemplo, un gas confinado en un tanque bajo presión $p$ $(p>0)$. Si el gas comenzara a expandirse, el sistema aportaría trabajo al entorno. Entonces, el cambio positivo $\Delta V$ en el volumen que abarca el gas implicaría una pérdida de energía al sistema, $-p\Delta V$. Al contrario, si la presión $p$ fuera lo suficientemente elevada como para poder comprimir el gas, tendríamos que $\Delta V < 0$; y, siguiendo ese convenio, el proceso de compresión aportaría trabajo al sistema, aumentando de esta forma su energía interna.

Tomando consideración del razonamiento planteado, la ecuación de Gibbs perteneciente al sistema "hélice-ovillo" pequeño cumplirá 

$$
\mathrm{d}\overline{E} = T\mathrm{d}S + f\mathrm{d}\overline{l} + \mu\mathrm{d}N \; .
$$ (heco_gibbs)

Aplicando dos transformaciones de Legendre, la energía libre de Gibbs y el potencial cumplirán, respectivamente, las relaciones

$$
\mathrm{d}F(T,f,N) = -S\mathrm{d}T - \overline{l}\mathrm{d}f +\mu\mathrm{d}N
$$ (heco_gibss_aske)

y

$$
\mathrm{d}\mathscr{E} = -S\mathrm{d}T - \overline{l}\mathrm{d}f - N\mathrm{d}\mu \; .
$$ (heco_depsilon)

A continuación, siguiendo el procedimiento explicado en la {numref}`sección {number} <tpn_azter>`, reescribiremos la ecuación {eq}`heco_depsilon`:

$$
\mathrm{d}\mathscr{E} = -\left[S-N\left(\frac{\partial S}{\partial N}\right)_{T,f}\right]\mathrm{d}T+\left[\overline{l}-N\left(\frac{\partial \overline{l}}{\partial N}\right)_{T,f}\right]\mathrm{d}f + \left(\frac{\partial \mathscr{E}}{\partial N}\right)_{T,f} \mathrm{d}N \; .
$$ (heco_depsilon_1)

Consideremos ahora la ecuación {eq}`dvdntp`, y trasladémoslo a las variables de entorno $(T,f,N)$. Con ayuda de la relación {eq}`heco_depsilon_1`, concluiremos que se cumple esta igualdad:

$$
\left[\frac{\partial (\overline{l}/N)}{\partial N}\right]_{T,f} =  \frac {1}{N^2}\left(\frac{\partial \mathscr{E}}{\partial f}\right)_{T,N} \; .
$$ (heco_equality)


```


$(b)$ Comprueba que se cumple la relación {eq}`heco_equality` del apartado $(a)$, haciendo uso de las ecuaciones obtenidas a lo largo del desarrollo del ejemplo.

```{dropdown} __Solución__

La expresión de la parte izquierda la calcularemos mediante la ecuación {eq}`lbar`; la de la derecha, en cambio, con la ecuación {eq}`epsilonhelix`, y atendiendo a la relación $r(T,f)= r_H(T,f)/r_C(T,f)$. Tras realizar los cálculos necesarios, veremos que ambas partes coinciden en esta expresión:

$$
\left[\frac{\partial (\overline{l}/N)}{\partial N}\right]_{T,f} = \frac{r^N \ln r}{\left(1+r^N \right)^2} \left(l_H - l_C\right) = \frac {1}{N^2}\left(\frac{\partial \mathscr{E}}{\partial f}\right)_{T,N} 
$$ (heco_equality_1)

Es perceptible que la expresión {eq}`heco_equality_1` tenderá a cero en el límite macroscópico, independientemente de si $r < 1$ ó $r>1$. Junto a ello, la magnitud $\overline{l}/N$ recuperará el carácter intensivo.

```

**----------------------------------------------------**


(gitpn)=
### Ejemplo: gas ideal clásico, en la colectividad isotérmica-isobárica

El análisis del segundo sistema lo emprenderemos desde los resultados del [_apéndice C_](gitvn). Activando el grado de libertad mecánico a la ecuación {eq}`qtvngi`, transcurriremos a la colectividad isotérmica-isobárica, y calcularemos la nueva función de partición:

$$
\Delta(T,p,N) := \int_{0}^{\infty}\mathrm{d}\left(\frac{pV}{k_{\mathrm{B}}T}\right)\left[\frac{V^N}{N!\Lambda^{3N}}\right]\;e^{-pV/k_{\mathrm{B}}T} = \left(\frac{k_{\mathrm{B}}T}{p\Lambda^3}\right)^N \; .
$$ (dtpn_gi)

```{admonition} Nota
 $$
 \int_{0}^{\infty}\mathrm{d}x \; x^n e^{-ax} = \Gamma(n+1)a^{-n-1}
 $$
```

Cabe mencionar que $N!$ no figura en la nueva expresión. Lo que es más, al escribir la energía libre de Gibbs,

$$
F(T,p,N) = Nk_{\mathrm{B}}T\ln\left(\frac{p\Lambda^3}{k_{\mathrm{B}}T}\right) \; ,
$$ (ftpngi)

veremos que en todo momento muestra un comportamiento macroscópico, puesto que cumple una expresión estrictamente Euler-homogénea de primer orden. Por consiguiente, $\widehat{\mu}=\mu$, y

$$
\mathscr{E}(T,p,N)=0 \; .
$$ (gi_epsilon_tpn)

Se debe remarcar que en la colectividad canónica hemos concluido que $\mathscr{E}>0$ (ecuación {eq}`epsilon_tvn` del [_apéndice C_](gitvn)). Contemplemos la influencia que estos resultados tienen en la entropía:

$$
\boxed{S(T,p,N) := -\left(\frac{\partial F}{\partial T}\right)_{p,N}=Nk_{\mathrm{B}}\left[\ln\left(\frac{\overline{V}}{\Lambda^3N}\right) + \frac{5}{2}\right]} \; .
$$ (stpngi)

En comparación con la ecuación {eq}`stvngi` del [_apéndice C_](gitvn), (y asumiendo que  $Nk_{\mathrm{B}}T/p = \overline{V}=V$), notaremos que no figuran los términos negativos del final, pues hemos recuperado la expresión de Sackur-Tetrode; es decir, ¡al iniciar otro grado de libertad, el potencial de subdivisión ha pasado de ser negativo a cero, y, junto a ello, la entropía ha aumentado!

$$
\\
$$

En el {numref}`apartado {number} <tpmu>`, reexaminaremos el gas ideal en la colectividad nanocanónica compuesta por subsistemas totalmente libres. Los nuevos efectos que emergerán allí otorgarán una gran representatividad a la Nanotermodinámica en el estudio de sistemas pequeños.

