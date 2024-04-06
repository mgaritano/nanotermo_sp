(gitvn)=
## **_C_** _Gas ideal clásico, en la colectividad canónica_

El sistema a estudiar es un gas confinado en un volumen $V$, y compuesto por $N$ partículas monoatómicas libres e indistinguibles. Estas condiciones facilitarán significativamente nuestro trabajo, ya que la contribución a la energía será únicamente cinética: $H(q,p) = \sum_{i=1}^N \frac{p_{i}^2}{ 2m_{i} }$.

Iniciaremos el análisis en el espacio de fase; las coordenadas de posición y momento de una partícula son $(q_{i},p_{i})$. Considerando que la relación entre un estado cuántico y un elemento de volumen del espacio de fase es $\mathrm{d}^{3N}q\;\mathrm{d}^{3N}p/(N!h^{3N} )$ , construiremos la función de partición {cite}`pathria` y la energía libre de Helmholtz. Recordemos que la longitud de onda térmica sigue la definición $\Lambda = h/\sqrt{2\pi mk_{\mathrm{B}}T}$.

$$
Q(T, V, N)=\frac{1}{N ! h^{3 N}} \int \prod_{i=1}^{N} \mathrm{d}^{3} q_{i} \; \mathrm{d}^{3} p_{i} \; \exp\left({-\frac{1}{k_{\mathrm{B}}T} \frac{ p_{i}^2}{2 m}}\right)  = \frac{V^N}{N!\Lambda^{3N}}\; .
$$ (qtvngi)

Escribiremos la energía libre de Helmholtz:

$$
A(T,V,N) = k_{\mathrm{B}}T\left(N\ln\frac{\Lambda^3}{V} + \ln N!\right) \; .
$$ (atvngi)

Antes de continuar, observemos que la expresión contiene el término $N!$. Si bien en el límite termodinámico empleamos la aproximación $\ln N! \sim N\ln N - N$, en la Nanotermodinámica necesitaremos ir más allá. Escribamos la serie de Stirling:

$$
 \ln N! = N \ln N-N+ \ln \sqrt{2 \pi N}+\frac{1}{12 N}-\frac{1}{360 N^{3}}+\frac{1}{1260 N^{5}}-\frac{1}{1680 N^{7}}+\cdots \; .
$$ (stirling)

Cuando $N$ es pequeño, además de los dos primeros términos del lado derecho de la ecuación {eq}`stirling`, también debemos considerar el tercero y el cuarto, al menos. Reflejaremos la decisión tomada en entropía:

$$
\boxed{ S(T,V,N) = N k_{\mathrm{B}} \left[\ln \left(\frac{V}{\Lambda^{3} N}\right)+\frac{5}{2}\right]- k_{\mathrm{B}}\left[ \ln \sqrt{2 \pi N} + \frac{1}{12N}\right]} \; .
$$ (stvngi)

Las últimas dos contribuciones _pequeñas_ disminuirán la entropía, y tendrán un efecto considerable en la región nanotermodinámica. Calcularemos también el potencial de subdivisión. Aplicando dos transformaciones de Legendre a la energía $A(T,V,N)$, tenemos $\mathscr{E} = A +pV - \mu_{N} N$. El gas ideal cumple $pV=Nk_{\mathrm{B}}T$. Definiremos $\mu_{N}$ mediante una ecuación en diferencias: $ \mu_{N} = A_{N+1}-A_{N}$. En el caso de sistemas muy pequeños, es más adecuada que la ecuación diferencial.

```{admonition} Nota
Como explica Hill {cite}`hill`, $N$ debe considerarse como una variable discreta cuando $N< \mathscr{O }(50)$.

```

Usando la aproximación de Taylor $(N+1 \rightarrow N)$,


$$
\mu_{N} = -k_{\mathrm{B}}T\ln\left(\frac{1}{N+1}\frac{V}{\Lambda^3}\right) \approx -k_{\mathrm{B}}T\left[\ln\left(\frac{V}{\Lambda^3 N}\right) - \frac{1}{N} + \frac{1}{2N^2}\right] \; .
$$

Una vez establecido el potencial químico, construiremos el potencial de subdivisión:


$$
\mathscr{E} (T,V,N) \approx k_{\mathrm{B}}T\left[\ln\left(\frac{\sqrt{2\pi N}}{e}\right) + \frac{7}{12N}\right] > 0 \; .
$$ (epsilon_tvn)

Como veremos a lo largo de las próximas secciones, a medida que se inicien más grados de libertad, las contribuciones _pequeñas_ variarán (compárese la ecuación {eq}`epsilon_tvn` con las expresiones {eq}`gi_epsilon_tpn` de la {numref}`sección {number}. <tpn>`  y {eq}`epsilontpmugi` de la {numref}`sección {number} <tpmu>`). Esa última frase se basa en un postulado fundamental de la Nanotermodinámica: las ecuaciones termodinámicas cambiarán junto con las colectividades estadísticas que se utilizarán en los estudios.

