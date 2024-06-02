# Living in the dark: Satelites that never see the light

## Objetivo
La finalidad de estre proyecto es la de demostrar la posibilidad de existencia de satélites que siempre estarían escondidos tras el planeta que orbitan a usando para ello un desarrollo matemático en el cual se pondrán en juego las interacciones de distintas leyes físicas.

## Habilidades adquiridas
- Razonamiento matemático
- Fenómenos físicos aplicados a la astrofísica
- Desarrollo de pensamiento crítico y resolución de problemas

## Demostración matemática
La interacción de los distintos cuerpos en un sistema solar depende, en exclusiva, de las fuerzas de gravitación, las cuales dependen del producto de las masas de los cuerpos y el cuadrado las distancias entre estos. Dicho equilibrio se pueude ver alterado al mover uno solo de los cuerpos, por lo que, en un escenario real, un sistema solar es un sistema muy complejo de estudiar. Por este mismo motivo, se va a simplificar el problema forzando una serie de condiciones:
1. El sistema estará compuesto de tan solo 3 cuerpos: una estrella, un planeta y un satélite.
2. Las órbitas descritas tanto por el planeta como por el satélite son perfectamente circulares.
3. La masa del satélite es despreciable frente a las masas del planeta (m) y la estrella (M).

Con restricciones impuestas, se puede demostrar que un satélite orbitando un planeta nunca ve la luz de la estrella de su sistema solar si se iguala el periodo orbital (T) del satélite tiene el mismo valor que el periodo orbital del planeta. Esto es:

$$\ T_{planeta}=T_{satélite}	\to 	\frac{2\pi}{\omega_{planeta}}=\frac{2\pi}{\omega_{satélite}}$$

donde 

$$\ \omega=\tau/\theta$$

Como T debe tener el mismo valor para ambos astros, no queda más remedio que ambas $\ \omega$ sean iguales y, por extensión, ambas $\ \theta$, que es el ángulo de giro del cuerpo desde la posición inicial, han de ser iguales. Esto se puede ver mejor de forma gráfica en la figura 1, donde se ha dibujado un círculo con puntos representando el movimiento que hace el satélite desde el punto de vista de la estrella.

![image](https://github.com/JoseManuelMdlV/Living-in-the-dark-Satelites-that-never-see-the-light/assets/83475119/27a3e18f-db59-46f0-8137-3097790f51ef)

<b>Fig 1.</b> Esquema del sistema solar donde se describen las distintas órbitas.

Una vez hemos visto bajo qué condiciones las órbitas de los astros son circulares, podemos pasar a la demostración de que, efectivamente, el satélite estará en oscuridad perpetua. Para ello, nos tenemos que atener a las leyes de Newton, las cuales nos dicen que, para que un cuerpo describa una órbita alrededor de otro, la fuerza que lo atrae (debido a la atracción gravitatoria de la masa M) es igual en valor que la fuerza que lo está expulsando (debido a la velocidad del cuerpo en movimiento)

$$ F_g=F_c \to G\frac{Mm}{R^2}=m\frac{v^2}{R}$$

$$\ v=\omega r 	\to	G\frac{Mm}{R^2}=m(\frac{2\pi}{T})^2R$$

Si ordenamos la igualdad para resolver $T^2$, nos queda que

$$ T^2=\frac{4\pi^2}{GM}R^3 $$

De esta expresión, que no es si no la 3ª ley de Kepler, se puede denotar que la masa del planeta (m) no interviene en el periodo, siendo solo la masa central y la distancia del astro con respecto a esta las únicas variables que entran en juego. Para el satélite, hacemos un razonamiento análogo teniendo en cuenta que la masa central será la del planeta, no la estrella. 

Si tomamos esta última expresión y la sustituímos en la primera igualdad, tras simplificar un poco las expresiones nos queda que

$$ \sqrt{\frac{R}{F_{g_1}}}=\sqrt{\frac{R}{F_{g_2}}} \to \frac{R}{F_{g_1}}=\frac{R}{F_{g_2}} $$

$$ r'=R\frac{F_{g_1}}{F_{g_2}} $$

Sustituyendo ahora los valores de $\ F_g$

$$ r'=R\sqrt[3]{\frac{M}{m}} $$

El ratio entre las masas siempre será mayor que la unidad, por lo que r', que es la distnacia entre la estrella y el satélite, siempre será mayor que R, dando a entender que el satélite siempre estará por detrás del planeta desde el punto de vista de la estrella. Sin embargo, esto no prueba que el satélite esté en penumbra permanente, pues existen una serie de ángulos y distancias para los cuales ciertas partes del satélite estarían iluminadas mientras aún se cumple que r'>R. 

![image](https://github.com/JoseManuelMdlV/Living-in-the-dark-Satelites-that-never-see-the-light/assets/83475119/e087f1f7-b89b-4de0-8f66-7dd7c9be9288)

<b>Fig 2.</b> Representación del cono de sombra y las situaciones en las que el satélite no está en penumbra completa.

Para poder cerciorarnos que el satélite se haya dentro de la sombra proyectada por el planeta, es necesario conocer el volumen de dicho cono de sombra[1]. Para ello, basta con calcular el volumen de revolución de un triángulo, de tal modo que:

$$ V=\int_0^d \int_0^{r^2=(r-d)^2} 2\pi\ \mathrm{d}r\ \mathrm{d}d = \pi \int_0^d (r-d)^2\ \mathrm{d}d =  -\frac{1}{3}\pi (r-d_{max})^3|^{d}_{0} $$

Si sustituimos en la expresión por los límites de integración y reordenamos un poco los términos, nos queda que el volumen del cono de sombra proyectado por el planeta es

$$ V=\frac{1}{3}\pi[r^3-(r-d_{max})^3] $$

Dentro de dicho volumen, el satélite siempre estaría a oscuras, opacado por el planeta que orbita, demostrando así la existencia teórica de dichos cuerpos celestes. 

[1] Es de notar, que la distanca $\ d_{max}$ es la altura total del cono, desde la base hasta su pico. Eso significa que es necesario que el satélite esté a una distancia d menor que $\ d_{max}$ para asegurarnos que no hay zonas iluminadas. No obstante, en la realidad, dicha distancia sería demasiado grande como para considerar que el satélite estuviese orbitando el planeta en lugar de la estrella.
