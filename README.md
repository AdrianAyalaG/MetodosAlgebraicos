12/09/2024
# Metodos Algebraicos
## Igualación de coeficientes: 
> 🔑 ¿Qué se hace?: Se analizan los coeficientes del polinomio caracteristico.

Caracteristicas adicionales:
* Se conocen la ubicación de los polos que se desea, así que se busca la representación del polinomio caracteristico.
* Se puede obtener el C(z) Controlador que asegura el comportamiento deseado.
* Se hace una igualación coeficiente a coeficiente. 

# 💡Ejemplo 1
Si se tiene G(z) de la siguiente manera: 
$$G(z)= \frac{0.0043}{z^{2}-1.819z+0.8187}$$
Ahora bien, si se desea tener un controlador para ubicar los nuevos polos de la siguiente manera: 
$$p_{1}=0.91+0.23j; p_{2}=0.91-0.23j$$
Entonces el polinomio caracteristico, es decir, el que se desea en lazo cerrado es: 
$$(z-0.91+0.23j)(z-0.91-0.23j)= {\color{Red} z^{2}-1.82z+0.881}$$

Si en lazo cerrado $$G_{0}(z)= \frac{KG(z)}{1+KG(z)}$$, entonces se hacen los siguientes calculos: 
$$G_{0}(z)= \frac{K(\frac{0.0043}{z^{2}-1.819z+0.8187})}{1+K(\frac{0.0043}{z^{2}-1.819z+0.8187})}$$
$$G_{0}(z)=\frac{K(0.0043)}{z^{2}-1.819z+0.8187+K(0.0043)}$$

*Al igualar los coeficientes se puede observar que el termino que acompaña a las z a ambos lados del igual, son diferentes, por lo tanto no se puede realizar con acción proporcional.Entonces...

## Funciones causales(Propias) 
### Caracteristicas
* El controlador tiene que ser de un orden menor que el orden de la planta.
* Debe ser BIPROPIO.
* Se le debe agregar un polo y un zero.
* Este concepto no se aplica para funciones de primer orden.

$$G(z)=\frac{N(z)}{D(z)}; C(z)=\frac{B(z)}{A(z)}; G_{0}(z)=\frac{N_{0}(z)}{D_{0}(z)}$$
Si $$ G_{0}(z)=\frac{C(z)G(z)}{1+C(z)G(z)}\Rightarrow \frac{B(z)N(z)}{{\color{Orchid} A(z)D(z)}+{\color{Green} B(z)}N(z)}$$

*Donde A(z) y D(z) son los valores causantes de que se suba un orden. Y B(z) y A(z) son las variables a solucionar para hallar el controlador.

