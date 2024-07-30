# Thermal-Diffusivity
Sobre los códigos del repositorio: 

  En difusion.py se encuentran los códigos para medir y graficar la difusión de calor en una barra de cobre, también la comunicación con el instrumental: multiplexor 34970A, generador de funciones Tektonix AFG 3021B y fuente HANTEK PPS2320A. En intrumetal-HANTEKPPS2320A.py se encuentran los métodos de la clase homónima. 

¿Que es la difusividad? 

En la ecuación de conducción de calor de Fourier se ve que la difusividad $\kappa$ es un índice que expresa la velocidad de cambio, y flujo de temperaturas, en un material hasta que alcanza el equilibrio térmico: 

$$ \frac{\partial^{2} T}{\partial x^{2}} \kappa= \frac{\partial T }{\partial t} $$ 

¿Como calcular $\kappa$?
Para el regimen estacionario se puede plantear una solucion de la pinta: 

$$ T(x,t)= T_{0}e^{-\epsilon x}cos(\omega (t-x/\nu)) $$

