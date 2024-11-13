# Operaciones con Espacios de Estados

Un modelo de espacios de estados es una forma matemática de representar un sistema físico utilizando un conjunto de variables de entrada, salida y estados, las cuales están conectadas a través de ecuaciones diferenciales de primer orden. Las variables de estado determinan los valores de las variables de salida del sistema [1].

## Espacio de estados a partir de una Función de transferencia

Se considera una función de transferencia si tiene la siguiente estructura:

$$G_{(z)} = \frac{b_{0}z^{n} + b_{1}z^{n-1} + \cdots + b_{n-1}z + b_{n}}{z^{n} + a_{1}z^{n-1} + \cdots + a_{n-1}z + a_{n}}$$

A partir de esta aclaración, es posible representar una función de transferencia en diferentes formas clásicas de espacio de estados. Algunas de estas formas facilitan el análisis y el diseño de sistemas y controladores.


## Formas de Espacio de Estados 
### Forma Canónica Controlable
* El orden del polinomio caracteristico corresponde al número de ecuaciones del sistema.
* En la matriz, los signo de los términos cambian y se organizan desde el término independiente hasta el mayor grado.

$$y_{k} = [Numerador][X_{n}(k)]$$

* Si se tiene la función:

$$ G_{(z)} = \frac{b_{0}z^{n} {\color{Green}+ b_{1}}z^{n-1} + \cdots {\color{Green}+ b_{n-1}}z {\color{Green}+ b_{n}}}{z^{n} {\color{Green}+ a_{1}}z^{n-1} + \cdots {\color{Green}+ a_{n-1}}z {\color{Green}+ a_{n}}} $$

A partir de la función de transferencia previamente obtenida, se puede determinar la forma canónica controlable de la siguiente manera:

![Figura de prueba](Forma_Canonica_Controlable.png)

Figura 1. Forma Canonica Controlable.

![Figura de prueba](Forma_Canonica_Controlable_Salida.png)

Figura 2. Forma Canonica Controlable - Salida.



![Figura de prueba](Forma_Canonica_Observable.png)

Figura 3. Forma Canonica Observable.

![Figura de prueba](Forma_Canonica_Observable_Salida.png)

Figura 4. Forma Canonica Observable - Salida.


![Figura de prueba](Forma_Canonica_Diagonal.png)

Figura 3. Forma Canonica Diagonal.

![Figura de prueba](Forma_Canonica_Diagonal_Salida.png)

Figura 4. Forma Canonica Diagonal - Salida.






# Referencias
[1]. “ss - Modelo de espacio de estados - MATLAB - MathWorks América Latina”, Mathworks.com. [En línea]. Disponible en: https://la.mathworks.com/help/control/ref/ss.html. [Consultado: 02-nov-2024].

