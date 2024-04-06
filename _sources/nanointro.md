(nanointro)=
## Introducción a la Nanotermodinámica

El reto de la Mecánica Estadística consiste en describir la Física de un sistema mediante sus componentes microscópicos; para este fin, se vale de colectividades estadísticas compuestas de réplicas (o copias) del propio sistema. Un gran número de réplicas garantiza que la colectividad sea estacionaria y que se encuentre en equilibrio estadístico. Además, los grados de libertad impuestos desde fuera le asignan un determinado carácter.


```{figure} multzoak.png
---
height: 500px
name: multzo
---
  Las colectividades microcanónica, canónica y macrocanónica resultan muy conocidas, y son ampliamente empleadas en la Termodinámica. No obstante, la colectividad nanocanónica puede parecer extraña a primera vista. Los paréntetsis contienen las variables de los susbsistemas que están bajo nuestro control. Los subsistemas son libres de intercambiar las magnitudes extensivas que se muestran junto a las flechas bidireccionales. Está claro, por tanto, que el conjunto nanocanónico es el más libre de los cuatro.

```

En primer lugar, la {numref}`figura {number}a <multzo>` muestra un conjunto de subsistemas completamente aislados entre sí, denominado colectividad **microcanónica**. En cada uno de los elementos que lo componen, todas las variables extensivas (la energía interna $E$, el volumen $V$ y el número de partículas $N$) permanecen invariables. Así, el punto de partida para el estudio del sistema consiste en _contar_ el número de _microestados_, $\Omega(E,V,N)$, compatibles con el _macroestado_ que se observa. A continuación, mediante la ecuación de Boltzmann obtendremos la entropía: $S(E,V,N) := k_{\mathrm{B}}\ln\Omega$. 

```{admonition} Nota
El signo $:=$ da a entender que dos expresiones son iguales por definición.
```

Al autorizar el intercambio de energía entre réplicas, transcurriremos a la colectividad **canónica** ({numref}`figura {number}b <multzo>`). La temperatura permanecerá bajo nuestro control, y realizando el sumatorio entre cada conjunto de microestados compatibles con cada energía accesible $E_{i}$, construiremos la función de partición canónica: $Q(T,V,N) := \sum_{E_{i}} \Omega(E_{i},V,N) e^{-E_{i}/k_{\mathrm{B}}T}\;$. A cada energía $E_{i}$ se le ha asignado su correspondiente factor de Boltzmann, el cual denota la probabilidad de que el sistema acceda a ese macroestado. Eso nos llevará a calcular la energía libre de Helmholtz (la energía útil de un sistema en contacto térmico con un reservorio de calor): $A(T,V,N) = -k_{\mathrm{B}}T\ln Q\;$.

```{admonition} __Aclaración importante__
A lo largo del trabajo mantendremos la notación que Hill emplea en su libro. Por lo tanto, designaremos los principales potenciales termodinámicos mediante las siguientes letras: Energía interna $\rightarrow E$ ; Energía libre de Helmholtz $\rightarrow A$ ; Entalpía $\rightarrow H$ ; Energía libre de Gibbs $\rightarrow F$.
```

Finalmente, el consentimiento de  la transferencia de materia entre subsistemas acarreará una colectividad de mayor libertad: la __macrocanónica__ ({numref}`figura {number}c <multzo>`). Aplicando la transformación de Legendre correspondiente al grado de libertad químico, obtendremos la función de partición macrocanónica: $\Xi (T, V, \mu) := \sum_{N_{i}} Q(T,V,N_{i})e^{\mu N_{i}/k_{\mathrm{B}}T}$, así como el denominado gran potencial:  $\Psi (T,V,\mu) = -k_{\mathrm{B}}T\ln \Xi$.

Considerando lo explicado previamente, las colectividades anteriores son las que figuran en los libros de Termodinámica. Es cierto que existen otras variantes, como la isotérmica-isobárica, caracterizada por las variables ambientales $(T,p,N)$. Más en adelante veremos que esta colectividad juega un gran papel en el análisis de los sistemas pequeños. Además, en sistemas de $n$ componentes diferentes es lícito construir la colectividad osmótica, designada por las variables $(T,p,N_1,\mu_2,...,\mu_n)$.

Pero lo que debemos remarcar es que, en las colectividades estudiadas por el momento, al menos una variable extensiva ha sido especificada por el contorno $(E$, $V$ o bien $N)$. Es más, atendiendo a la relación de **Gibbs-Duhem**, parece ser que no es posible fijar las tres variables intensivas a la vez a un sistema hidrostático macroscópico. Con el fin de aclarar la última frase, partiremos por escribir la **ecuación de Gibbs**:


$$
\mathrm{d}E(S,V,N) = T\mathrm{d}S - p\mathrm{d}V + \mu \mathrm{d}N \; .
$$ (gibbs)

Integrando, llegaremos a la expresión de la energía interna del sistema:

$$
E(S,V,N) = TS - pV + \mu N
$$ (E)
Calculando el diferencial total,

$$
\mathrm{d}E = T\mathrm{d}S + S\mathrm{d}T -p\mathrm{d}V - V\mathrm{d}p + \mu \mathrm{d}N + N \mathrm{d}\mu \; ,
$$

e igualándolo con la ecuación {eq}`gibbs`, obtendremos la esperada relación de Gibbs-Duhem:

$$
\boxed{N\mathrm{d}\mu = -S\mathrm{d}T + V\mathrm{d}p} \; .
$$ (gibbs-duhem)

La ecuación {eq}`gibbs-duhem` corrobora lo mencionado antes: el potencial químico $\mu$, la temperatura $T$ y la presión $p$ están ligados. Es decir, si escogemos dos de ellos, el tercero quedará especificado en función de los anteriores $[T(p,\mu),\; p(T,\mu)$ o bien, $\mu (T,p)]$. Pues bien, pese a que esta expresión parezca firme e inviolable, la figura a tratar muestra una colectividad estadística que de __ninguna manera sugiere lo mencionado hasta el momento__.

Obsérvese atentamente la __{numref}`figura {number}d <multzo>`__. A los subsistemas de un solo componente se les han iniciado todos los grados de libertad, por lo que tienen asignados $(T,p,\mu)$ como conjunto de variables de ambiente. Por consiguiente, ¡las réplicas intercambian energía, partículas y volumen sin impedimento externo alguno!

Al hilo de lo anterior, existen dos problemas que debemos afrontar. No obstante, para ese fin nos resultará imprescindible comenzar a sumergirnos en la Nanotermodinámica. Los motivos de preocupación son los siguientes: por un lado, queda de manifiesto que la __colectividad nanocanónica__ viola la condición impuesta por la ecuación {eq}`gibbs-duhem`. Por lo tanto, considerando lo explicado recientemente, no resulta factible emplearlo para la descripción de un sistema macroscópico; a lo que Hill replicaría: solamente debemos valernos de las variables $(T,p,\mu)$  para el estudio de __sistemas pequeños__ (de tamaño finito). El {numref}`apartado {number} <hillteo>` servirá como aclaración sobre el significado de que un sistema sea pequeño, desde el punto de vista de la Física y de las Matemáticas.

Por otro lado, para que las variables $(T,p,\mu)$ no queden ligadas, deberemos añadir otro grado de libertad al sistema pequeño. Así, junto a la variable suplementaria, el conjunto $(T,p,\mu)$ obedecerá una ecuación similar a la de Gibbs-Duhem{eq}`gibbs-duhem`, y la colectividad nanocanónica quedará bien definida. Resulta que Hill introdujo un grado de libertad especial, el cual lo asoció a la capacidad de la colectividad para variar el **número de réplicas** del sistema $(\mathscr{N})$. En otras palabras, la energía interna de la colectividad se verá afectada si ésta varía su distribución de subsistemas. En consecuencia, la ecuación {eq}`gibbs` de Gibbs deberá contener una contribución complementaria. La última frase nos conduce a definir el conjugado intensivo de la variable $\mathscr{N}$, el cual Hill denominó **POTENCIAL DE SUBDIVISIÓN**, o $\mathscr{E}$.


En el {numref}`apartado {number} <tpmu>` presentaremos las herramientas de la Física Estadística pertenecientes a la colectividad nanocanónica. Sin embargo, esta discusión la cerraremos mediante una reflexión cualitativa.

El potencial de subdivisión toma consideración de los efectos de superficie y de borde que emergen en la **región nanotermodinámica**, así como de la rotación o translación de los sistemas. En el caso de los sistemas pequeños, dichos agentes no se deben despreciar, puesto que ello infringiría la conservación de la energía, y, además, impediría la maximización de la entropía. Asimismo, estas correcciones redefinirán el carácter de las variables extensivas, puesto que no siempre resultará lícito afirmar que variarán linealmente con $N$. A veces, habremos de considerar relaciones como $\propto N^{2/3}$, $\propto N^{1/3}$, o bien $\propto \ln N$. Al mismo tiempo, sus variables conjugadas dejarán de ser intensivas; por ejemplo, aunque resulte extraño, la presión y la temperatura de un sistema pequeño dependerán del tamaño (ejemplo en la sección {numref}`sección {number} <fase>`), y solamente recobrarán la intensividad en el **límite macroscópico**.


Estos efectos acarrearán una consecuencia de gran peso: _las funciones termodinámicas de un sistema pequeño variarán según la colectividad_ que se emplee para su análisis. En ese mismo sentido, el cálculo de la entropía de un gas ideal mediante las variables de control adecuadas ofrece una solución innovadora a la paradoja de Gibbs {cite}`multiscale` ({numref}`apartado {number} <mupt_gi>`). Naturalmente, el potencial de subdivisión, el cual recoge todos los efectos de tamaño finito, pierde relevancia según crece el sistema. Así, progresivamente regresaremos a la Termodinámica Clásica, donde dicho potencial se volverá despreciable con respecto a otros términos de carácter macroscópico como, por ejemplo, la energía interna del sistema $(E \gg \mathscr{E})$.

$$
\\
$$

Los párrafos anteriores sintetizan la esencia de la teoría de Hill. En el próximo apartado, presentaremos su formalismo, y contemplaremos las transformaciones que les ocasionará a las relaciones termodinámicas.
