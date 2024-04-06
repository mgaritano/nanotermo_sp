```{epigraph}
$\huge \quad \quad \mathbf{\text{NANOTERMODINÁMICA}}$
```

```{epigraph}
_Classical thermodynamics... is the only physical theory of universal content which I am convinced that, within the framework of the applicability of its basic concepts, will never be overthrown._

-- Albert Einstein
```

(sarrera)=
## Introducción y objetivos

La Termodinámica, sin lugar a dudas, es actualmente la teoría de mayor aplicabilidad en la ciencia, ya que sus postulados se extienden a diversos campos; desde el interior de los átomos, hasta la inmensidad del universo. De hecho, junto a la Física Estadística, abastece a los científicos de las herramientas y aproximaciones necesarias para la correcta descripción del carácter térmico de la naturaleza. Como es bien sabido, dos de las leyes fundamentales de la Termodinámica rigen el comportamiento de un sistema cualquiera: la conservación de la energía y el incesante crecimiento de la entropía. A este último punto se le podría deber la solidez que Einstein muestra en su afirmación.

Al mismo tiempo, cabe remarcar que los análisis termodinámicos que se realizan en un sistema se fundamentan en dos aproximaciones principales; en considerar que el sistema en cuestión muestra un comportamiento macroscópico y homogéneo. Aún así, en la mayoría de los casos se han obtenido resultados de gran corrección y precisión.

Sin embargo, históricamente han acontecido sucesos que han hecho tambalear a criterios aparentemente firmes. Por ejemplo, a finales del siglo XIX, se observó que en las reacciones químicas se violaba la conservación de la energía. A raíz de ello, Gibbs introdujo una importante corrección: la contribución a la energía interna del sistema a causa del incremento en el número de partículas, la cual la caracterizó por medio del potencial químico, $\mu$ {cite}`nanointro`. Así, además de restablecer la primera ley, se logró propagar el campo de la Termodinámica. A comienzos del siglo XX, la creación y desarrollo de la teoría cuántica posibilitó el estudio de sistemas de menor tamaño. En consecuencia, emergieron nuevos factores como la _simetría local_ y los _efectos de tamaño finito_. No obstante, la Termodinámica Clásica no incluía explicación alguna para dichos fenómenos. De hecho, en algunos ensayos espectroscópicos se han observado distribuciones inhomogéneas de la temperatura {cite}`t_ez_hom`. Lo anterior, sin duda, desmiente el carácter homogéneo e intensivo que le asignan las leyes macroscópicas a la temperatura $T$.

Con el fin de dar solución a los problemas previos, se han creado herramientas que añaden correcciones a la teoría clásica, así como los teoremas de fluctuaciones y la Termodinámica Estocástica. Pero dichas teorías requieren que el sistema se encuentre en todo momento en contacto con una fuente de calor homogénea. En la mayoría de materiales (líquidos, cristales, polímeros...) no resulta factible hacer cumplir esta condición {cite}`multiscale`.


$$
\\
$$

De todas maneras, existe una teoría que considera los efectos mencionados bajo un punto de vista diferente, pero que, desafortunadamente, ha permanecido en desconocimiento en las últimas décadas. Esta teoría, objeto de estudio del presente trabajo, es denominada la **_Termodinámica de Sistemas Pequeños_**, y fue creada y desarrollada por el físico y biólogo __Terrell Leslie Hill__ (1917-2014) a comienzos de la década de 1960.


```{figure} hill.jpg
---
height: 200px
name: hill
---
T. L. Hill
```

En 1962, Hill publicó el artículo _Thermodynamics of Small Systems_ {cite}`hill_art`, y, a lo largo de los dos próximos años escribió un libro que lleva el mismo nombre {cite}`hill`. En él, presentó los fundamentos de la Nanotermodinámica y varias explicaciones.


```{admonition} Nota
Hill no emplea la palabra _Nanotermodinámica_ en sus trabajos. De hecho, en la década de 1960 sus ideas carecían de una robusta aplicabilidad en la mayoría de sistemas experimentales. Así las cosas, el autor introdujo este término posteriormente (en el año 2000).
```

A pesar de ello, al poco tiempo abandonó casi por completo la tarea, y se dedicó a investigar en el área de la biología molecular. Por desgracia, en décadas posteriores su trabajo ha permanecido postergado. Sin embargo, en 2020, un grupo de investigadores de la universidad NTNU de Noruega emprendió un proyecto denominado _Small Systems Thermodynamics_ {cite}`noruegos`, con el objeto de reflotar y propulsar la teoría de Hill. De hecho, además de publicar un libro que resume sus bases {cite}`nano`, lo han aplicado en experimentos y simulaciones moleculares, y han logrado adquirir resultados significativos; por ejemplo, en el caso de la adsorción {cite}`ads_t, ads`.

En resumidas cuentas, la teoría de Hill ofrece una generalización de la Termodinámica Clásica que posibilita la correcta descripción y caracterización de sistemas pequeños y heterogéneos. En otras palabras, modifica las ecuaciones clásicas añadiéndoles correcciones. El carácter e influencia de dichas adaptaciones resulta de suma importancia en el ámbito de los sistemas pequeños. Pero a medida que la escala aumenta, desvanece su influencia, con lo cual se restablecen las ecuaciones macroscópicas.


Al hilo de lo mencionado, esta unidad didáctica está especialmente destinada a la asignatura de Termodinámica y Física Estadística. Se presentarán explicaciones teóricas, las cuales se reforzarán a base de ejemplos de gran relevancia. Así, los alumnos tendrán la oportunidad de viajar más allá de la Termodinámica, y se percatarán de la influencia e importancia de la Nanotermodinámica en el estudio de sistemas pequeños. Lo anterior les supondrá un considerable avance en su aprendizaje.


Para comenzar, en el {numref}` apartado {number} <nanointro>` recordaremos los principios de la Mecánica Estadística {cite}`callen, hebreos, pathria` y consolidaremos su relación con la Nanotermodinámica. Habiendo establecido las ideas principales, en la {numref}`sección {number} <hillsec>` nos adentraremos en el formalismo de Hill {cite}`hill, nano`. Partiendo de ahí, en el {numref}`capítulo {number} <tpn>` estudiaremos los primeros ejemplos en la importante colectividad isotérmica-isobárica. Así, observaremos de cerca las particularidades de los efectos de tamaño finito. Seguidamente, en la {numref}`parte {number} <fase>` realizaremos una pausa para analizar las transiciones de fase en los sistemas pequeños. Para dar fin a la teoría, en el {numref}`apartado {number} <tpmu>`  retornaremos al hilo principal. Presentaremos una colectividad estadística que va más allá de los límites de la Termodinámica. Al mismo tiempo, reexaminaremos ejemplos concretos, y conseguiremos resultados muy representativos. Luego, en el {numref}`capítulo {number} <elek_mag>`, hablaremos de sistemas eléctricos y magnéticos; entre otras cosas, abordarémos un reanálisis del modelo de Ising. Además, la {numref}`sección {number} <osagarri>` complementaria contiene ejemplos adicionales importantes relacionados con el {numref}`tema {number} <tpmu>`. Para terminar, en la {numref}`sección {number} <app>` estudiaremos un ejemplo más elaborado, siguiendo el artículo {cite}`ads`. Éste servirá como claro indicador de la aplicabilidad actual de la teoría de Hill, así como una clara señal de que no quedará estancada en la década de 1960.

$$
\\
$$

Así las cosas, sin mayor demora, comenzaremos a cruzar el puente que nos trasladará de la Termodinámica convencional a la Nanotermodinámica. La {numref}`figura {number} <multzo>` del siguiente apartado es el punto de partida ideal para ello.


