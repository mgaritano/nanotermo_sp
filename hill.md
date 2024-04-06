(hillsec)=
## Termodinámica de sistemas pequeños

(hillteo)=
### Teoría de Hill

Siguiendo el método de Hill, construiremos una colectividad de $\mathscr{N}$ réplicas del sistema pequeño en cuestión como punto de partida de su análisis. Todos los subsistemas se considerarán equivalentes, distinguibles e independientes, es decir, no habrá ningún tipo de interacción entre ellos. De esa forma, si el número de réplicas es muy alto $\left(\mathscr{N}\rightarrow \infty\right)$, la propia colectividad mostrará un carácter macroscópico. Esta afirmación es de suma importancia, puesto que nos permite partir de la Termodinámica Clásica para examinar el macrosistema en su totalidad. Después, adquiriremos las propiedades de un solo sistema calculando los promedios por réplica.

```{admonition} Nota
La teoría de Hill mantiene la __ergodicidad__: el promedio en el tiempo de una propiedad concuerda con su promedio a través de la colectividad. Por otro lado, las magnitudes relacionadas con la colectividad se designarán mediante el subíndice $t$.
```

$$
\\
$$

Previo al estudio del conjunto, debemos recordar que disponemos de un cuarto grado de libertad en marcha. Por lo tanto, su energía interna cumple la relación $E_{t} = E_{t}(S_{t}, V_{t}, N_{t}, \mathscr{N})$. Así las cosas, añadiremos otro par de variables conjugadas a la ecuación {eq}`gibbs` para construir la **ecuación Hill-Gibbs**:

$$
 \mathrm{d}E_{t} = \left(\frac{\partial E_{t}}{\partial S_{t}}\right)_{V_{t}, N_{t}, \mathscr{N}}\mathrm{d}S_{t} + \left(\frac{\partial E_{t}}{\partial V_{t}}\right)_{S_{t}, N_{t}, \mathscr{N}}\mathrm{d}V_{t} + \left(\frac{\partial E_{t}}{\partial N_{t}}\right)_{S_{t},V_{t}, \mathscr{N}}\mathrm{d}N_{t} + \color{blue}{\left(\frac{\partial E_{t}}{\partial \mathscr{N}}\right)_{S_{t},V_{t}, N_{t}}}\color{red}{\mathrm{d}\mathscr{N}} \; .
$$

Sinteticemos la ecuación anterior:

$$
\mathrm{d}E_{t}(S_{t}, V_{t}, N_{t}, \mathscr{N}) = T\mathrm{d}S_{t} - p\mathrm{d}V_{t} + \mu \mathrm{d}N_{t} + \color{blue} {\mathscr{E}} \color{red}{\mathrm{d}\mathscr{N}} \; .
$$ (hill-gibbs)

Las dos expresiones han sacado a relucir la definición formal del potencial de subdivisión: 

$$
\boxed{\mathscr{E} := \left(\frac{\partial E_{t}}{\partial \mathscr{N}}\right)_{S_{t},V_{t}, N_{t}}} \; .
$$

Además, podrían servirnos de ayuda para aclarar la explicaciones un tanto difusas de la sección precedente. Como puede observarse, el potencial $\mathscr{E}$ se asemeja a la variable $\mu$, y, en cierto modo, lo podríamos tomar como un potencial químico relacionado con la adición de subsistemas {cite}`hill_diff_app`. Al incluir una réplica, las variables $S_{t}$, $V_{t}$ y $N_{t}$ permanecerán invariables, pero **se subdividirán**. Seguidamente, escribiremos la expresión de la energía interna, integrando la ecuación {eq}`hill-gibbs`:


$$
E_{t} \left(=\int \mathrm{d}E_{t} = T \int \mathrm{d}S_{t} - p \int \mathrm{d}V_{t} + \mu \int \mathrm{d}N_{t} + \mathscr{E} \int \mathrm{d}\mathscr{N}\right) = TS_{t} - pV_{t} + \mu N_{t} + \mathscr{E}\mathscr{N} \; .
$$ (pausoa)

Pese a que el cálculo parezca trivial, debemos advertir que tras este último paso yace una propiedad matemática primordial: _la homogeneidad de Euler_ (ver el [_apendíce A_](euler)). En concreto, las funciones $E_{t}, S_{t}, V_{t}, N_{t}$ y $\mathscr{N}$ son Euler-homogéneas de primer orden con respecto a la variable $N$. Es más, la temperatura $T$, la presión $p$ y el potencial químico $\mu$ son funciones de orden cero, es decir, estrictamente intensivas. Estas dos características permiten extraer el conjunto $(T, p, \mu,\mathscr{E})$ de las integrales, y, de esta forma, transcurrir de la ecuación {eq}`hill-gibbs` a {eq}`pausoa`. No obstante, enseguida nos percataremos de que en los sistemas pequeños lo anterior no se va a cumplir.

$$
\\
$$

Retomando el hilo principal, nuestro objetivo es llegar a las ecuaciones de un sistema pequeño, refiriéndonos a sus propiedades como promedios del colectivo. Por tanto, definiremos las siguientes variables: $\overline{E} \equiv E_{t}/\mathscr{N}$; $S \equiv S_{t}/\mathscr{N}$; $\overline{V} \equiv V_{t}/\mathscr{N}$; $\overline{N} \equiv N_{t}/\mathscr{N}$. De esta forma, cada subsistema de la colectividad obedecerá la siguiente ecuación:

$$
\boxed{\overline{E} = TS - p\overline{V} + \mu \overline{N} + \mathscr{E}} \; .
$$ (e_small)

A continuación, haciendo uso de la ecuación {eq}`e_small` e insertando las variables del sistema pequeño en la expresión {eq}`hill-gibbs`,

$$
\mathscr{N}\mathrm{d}\overline{E} + (TS-p\overline{V}+\mu \overline{N} + \mathscr{E})\mathrm{d}\mathscr{N} = T \mathrm{d}(\mathscr{N}S) - p \mathrm{d}(\mathscr{N}\overline{V}) + \mu \mathrm{d}(\mathscr{N}\overline{N}) + \mathscr{E}\mathrm{d}\mathscr{N} \; .
$$

Realizando cálculos y despejando, llegaremos a la ecuación de Gibbs de un sistema pequeño:

$$
\mathrm{d}\overline{E} = T\mathrm{d}S - p\mathrm{d}\overline{V} + \mu \mathrm{d}\overline{N} \; .
$$ (gibbs_small)

Ahora, calculando el diferencial total de la ecuación {eq}`e_small`, e igualándolo con {eq}`gibbs_small`, conseguiremos la ecuación __Hill-Gibbs-Duhem__:

$$
\boxed{\mathrm{d}\mathscr{E}(T,p,\mu) = -S\mathrm{d}T + \overline{V}\mathrm{d}p - \overline{N}\mathrm{d}\mu}\; .
$$ (h_g_d)

Esta ecuación corrobora matemáticamente lo mencionado en la {numref}`sección {number} <nanointro>`, puesto que queda en evidencia que el potencial de subdivisión iniciará un grado de libertad adicional. Así, nos será lícito especificar el conjunto $(T, p, \mu)$, y construir la colectividad nanocanónica. Ésta nos permitirá describir los sistemas pequeños con mayor detalle. Por otro lado, el aspecto de la ecuación {eq}`gibbs_small` podría dar a entender que hemos obtenido una expresión idéntica a {eq}`gibbs`. Pero debemos ser cautos, puesto que la inhomogeneidad de las variables no permite llevar a cabo las integrales que aparecen entre los paréntesis de {eq}`pausoa`; el término $\mathscr{E}$ de la ecuación {eq}`e_small` es indicador de lo anterior. Naturalmente, si el potencial de subdivisión resultara despreciable, las variables $S$, $\overline{V}$ y $\overline{N}$ y sus conjugadas recobrarían el carácter homogéneo. Esto haría desaparecer la colectividad nanocanónica, pues llevaría las ecuaciones del sistema pequeño al nivel macroscópico: {eq}`e_small` $\rightarrow$ {eq}`E`, {eq}`gibbs_small` $\rightarrow$ {eq}`gibbs` y {eq}`h_g_d` $\rightarrow$ {eq}`gibbs-duhem`.

Puede apreciarse que, mediante transformaciones de las ecuaciones ordinarias de la Termodinámica, hemos construido explicaciones más robustas y elaboradas para los conceptos cualitativos presentados previamente. De esta forma, estableceremos un riguroso criterio de clasificación entre sistemas: _Un sistema se considerará pequeño, si el potencial de subdivisión asociado a él es finito y no despreciable._

$$
\\
$$

Antes de seguir, debemos considerar una advertencia concerniente a la entropía. Al definir las variables de un sistema pequeño como promedios de la colectividad, hemos empleado la siguiente notación: $\overline{E}, S, \overline{V}$ y $\overline{N}$. Todos llevan una barra encima, excepto la variable $S = S_{t}/\mathscr{N}$. Cabe remarcar que esto no se ha debido a una errata inadvertida, sino que es más bien fruto del verdadero sentido de la entropía (ver [_apéndice B_](entropy)).

Para dar fin a este apartado, comenzaremos a examinar la manera en la que determinadas colectividades estadísticas influyen en el potencial de subdivisión. Esto dará paso a las secciones {numref}`{number} <tpn>`, {numref}`{number} <fase>` y {numref}`{number} <tpmu>`, así como a los ejemplos significativos incluidos en ellos. También comenzaremos a profundizar en el concepto más importante introducido en la parte anterior: las funciones termodinámicas sufren correcciones conforme a las variables ambientales empleadas para su análisis.

(replica_e)=
### Generalización de la ecuación Hill-Gibbs y energía de réplica

En el estudio del grado de libertad correspondiente a la subdivisión del colectivo realizado hasta el momento, al introducir una réplica, hemos mantenido todas las variables extensivas inalteradas $(S_{t}, V_{t}, N_{t})$. Así, hemos definido el potencial de subdivisión: la aportación a la energía total _únicamente_ a causa del cambio en el número de réplicas del sistema. Aún así, debemos advertir que la subdivisión de la colectividad afecta directamente a las variables de las réplicas, pues impide que $E$, $V$ y $N$ permanezcan intactos. En consecuencia, hemos tenido que asignarles necesariamente $(T, p, \mu)$ como variables de control; o, lo que es lo mismo, el desarrollo asociado a definir formalmente el potencial de subdivisión nos ha conducido directamente a la **colectividad nanocanónica**.

Obviamente, existirán circunstancias que no nos permitirán disponer del acceso a dichas variables. Esta frase nos conduce a generalizar la discusión precedente. En concreto, debemos definir la generalización del potencial de subdivisión ante variables de control cualesquiera $(A,B,C,...)$. Dicho potencial lo designaremos con la letra $X(A,B,C,...)$, y lo denominaremos **energía de réplica**. Por supuesto, en el caso de la colectividad nanocanónica, $X(T,p,\mu) = \mathscr{E}(T, p, \mu)$, pero en general, lo anterior no se cumplirá.

Como ejercicio aclaratorio, realizaremos el análisis de la sección {numref}`sección {number} <hillteo>` en la **colectividad macrocanónica**, esto es, las variables de un sistema pequeño pasarán a ser $(T,V,\mu)$. Así las cosas, las propiedades del colectivo serán definidas como $E_{t} = \mathscr{N}\overline{E}$, $S_{t} = \mathscr{N}S$, $V_{t} = \mathscr{N}V$ y $N_{t} = \mathscr{N}\overline{N}$. Es de mencionar que el volumen $V$ no es un promedio, sino una magnitud fija de cada subsistema de la colectividad. Seguidamente, reescribiremos la ecuación {eq}`hill-gibbs`, haciendo aparecer la variable $V$ $(\mathrm{d}V_{t} = \mathscr{N}\mathrm{d}V + V\mathrm{d}\mathscr{N})$:

$$
\mathrm{d}E_{t}(S_{t},V,N_{t},\mathscr{N}) = T\mathrm{d}S_{t} - p\mathscr{N}\mathrm{d}V + \mu \mathrm{d}N_{t} + (\mathscr{E}-pV)\mathrm{d}\mathscr{N} \; .
$$ (degc)

Partiendo de ahí, definiremos la energía de réplica:

$$
X(T,V,\mu) = \mathscr{E}-pV := \left(\frac{\partial E_{t}}{\partial \mathscr{N}}\right)_{S_{t},V,N_{t}} := -\widehat{p}\;V\;.
$$ (xgc)

Dicho lo dicho, si observamos la ecuación {eq}`xgc`, veremos que $X$ es una variable más adecuada que $\mathscr{E}$ en este entorno, puesto que lleva consigo el carácter innato de la colectividad macrocanónica. De hecho, al añadir una réplica, el volumen total $V_{t}$ del sistema también variará, lo cual posibilitará que el volumen $V$ de cada sistema pequeño permanezca inalterado. Así, la energía de réplica de la presente colectividad denota el trabajo mecánico que percibirá el colectivo, y que será caracterizado mediante la presión $\widehat{p}\;$: $-\widehat{p}\;V$. Cabe resaltar que $p\neq \widehat{p}$, puesto que las aportaciones a la energía de ambas presiones no son iguales: la primera está relacionada con cada uno de los sistemas pequeños, y, la segunda, con la totalidad de la colectividad. Debido a los efectos finitos, $p$ y $\widehat{p}$ solamente coincidirán en el límite macroscópico.

Siguiendo el procedimiento explicado anteriormente, y haciendo uso de la ecuación {eq}`xgc`, llegaremos a las siguientes expresiones:

$$
\overline{E} = TS - \widehat{p}\;V + \mu \overline{N} \; ,
$$ (e_small_gc)

$$
\mathrm{d}\overline{E} = T\mathrm{d}S - p\mathrm{d}V + \mu \mathrm{d}\overline{N} \; .
$$ (dE_small_gc)

Éstos dejan en evidencia que $\overline{E}$ no es una función homogénea, debido a la desigualdad entre las presiones $p$ y $\widehat{p}$. Acto seguido, aplicaremos dos transformaciones de Legendre a la ecuación {eq}`e_small_gc`:

$$
\mathrm{d}(-\widehat{p}\;V) := \mathrm{d}\Psi(T,V,\mu) = -S\mathrm{d}T - p\mathrm{d}V - \overline{N}\mathrm{d}\mu \; .
$$ (pot_gc)

De ahí, extraeremos dos expresiones que otorgarán gran representatividad a las explicaciones precedentes:

$$
\boxed {-\widehat{p} := \frac{-\widehat{p}\;V}{V} \quad \pmb{\neq} \quad -p := \left[\frac{\partial(-\widehat{p}\;V)}{\partial V}\right]_{T,\mu} \quad ; \quad \mathscr{E} = - (\widehat{p} - p)V} \; .
$$ (gc_summ)

Así las cosas, denominaremos **presión integral** a $\widehat{p}$ y **presión diferencial** a $p$. Salta a la vista que los efectos finitos y la no linealidad que los distingue quedan recogidos en el potencial de subdivisión.
