# Thermal-Diffusivity
Sobre los códigos del repositorio: 

  En difusion.py se encuentran los códigos para medir y graficar la difusión de calor en una barra de cobre, también la comunicación con el instrumental: multiplexor Agilent 34970A, generador de funciones Tektonix AFG 3021B y fuente HANTEK PPS2320A. En intrumetal-HANTEKPPS2320A.py se encuentran los métodos de la clase homónima. 

¿Que es la difusividad? 

En la ecuación de conducción de calor de Fourier se ve que la difusividad $\kappa$ es un índice que expresa la velocidad de cambio y flujo de temperaturas en un material hasta que alcanza el equilibrio térmico: 

$$ \frac{\partial^{2} T}{\partial x^{2}} \kappa= \frac{\partial T }{\partial t} $$ 

¿Como calcular $\kappa$?

Exitando la barra con una fuente armonica se puede obetener, para el regimen estacionario, una solucion de la pinta: 

$$ T(x,t)= T_{0}e^{-\epsilon x}cos(\omega (t-x/\nu)) $$

Donde $\epsilon$ es el coeficiente de decaimiento, $\nu$ es la velocidad de la onda termica, $\kappa$ = $\frac{\nu}{2 \epsilon}$. Finalemte $\nu$ se puede calcular partir del desfasaje
 de la onda en dos puntos: $\nu$ = $\frac{\Delta x}{\Delta t}$

Por otro lado, es posible también analizar el comportamiento del sistema en el período transitorio utilizando una fuente de potenciaconstante. Bajo estas condiciones, la temperatura se comporta de la siguiente manera: 

$$ T(x,t)= \frac{2F_{0}}{K} \left( \sqrt{\frac{\kappa t}{\pi}} e^{-\frac{x^{2}}{4\kappa t}} - \frac{x}{2} \text{erfc}\left( \frac{x}{2\sqrt{\kappa t}}  \right)  \right) $$ 

Arreglo Experimental

Se midió la temperatura a lo largo de toda una barra cobre utlizando un arreglo 7 termocuplas conectadas a un multiplexor Agilent 34970A. Se exitó uno de los extremos de la barra con pulso armonico y luego con un pulso constante para comparar los dos métodos arriba mencionados. 
![Esquema Experimental](https://github.com/hnatiuksanti/Thermal-Diffusivity/blob/main/imagenes/experimental.png)

