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

A partir de la función de transferencia obtenida, se puede determinar la forma canónica controlable. En este proceso, se observa un cambio de signo en las variables del denominador (destacadas en verde).

![Figura de prueba](Forma_Canonica_Controlable.png)

Figura 1. Forma Canónica Controlable.

Para la salida se toman los valores del numerador sin cambiar el singo y se multipla por el vector de variables de estado.

![Figura de prueba](Forma_Canonica_Controlable_Salida.png)

Figura 2. Forma Canónica Controlable - Salida.

En la Figura 2 se observa que los ceros del sistema (numerador) aparecen en la ecuación de salida.

### Forma Canónica Observable
Este sistema es equivalente a la Forma Canónica Controlable.

$$G_{(z)} = \frac{b_{0}z^{n} + {\color{Blue}b_{1}}z^{n-1} + \cdots +{\color{Blue}b_{n-1}}z + {\color{Blue}b_{n}}}{z^{n} {\color{Green}+ a_{1}}z^{n-1} + \cdots {\color{Green}+ a_{n-1}}z {\color{Green}+ a_{n}}} $$

![Figura de prueba](Forma_Canonica_Observable.png)

Figura 3. Forma Canónica Observable.

En la Figura 3 se observa que los ceros del sistema (numerador) ya no aparecen en la ecuación de salida, sino en la ecuación de entrada.

![Figura de prueba](Forma_Canonica_Observable_Salida.png)

Figura 4. Forma Canónica Observable - Salida.


### Forma Canónica Diagonal
No se trabaja directamente con los coeficientes de la función de transferencia, sino que se determinan directamente los polos de la misma.

$$ P_1 = z_1; P_2 = z_2; \cdots ; P_n = z_n$$

![Figura de prueba](Forma_Canonica_Diagonal.png)

Figura 5. Forma Canónica Diagonal.

En la Figura 5, se observa que los polos deben ubicarse a lo largo de toda la diagonal. La matriz de entrada se completa con el valor 1.


![Figura de prueba](Forma_Canonica_Diagonal_Salida.png)

Figura 6. Forma Canónica Diagonal - Salida.

En la matriz de salida (Figura 6), se muestran los valores de las fracciones parciales, obtenidos a partir de la separación de los polos.

## Ejemplo
### Forma Canónica Controlable

$$G_{(z)} = \frac{z + 1}{z^{2} + 1.3z + 0.4}$$

![Figura de prueba](Forma_Canonica_Diagonal_Salida.png)


# Conclusiones
1. La forma canónica controlable y la forma observable son equivalentes en cuanto a su respuesta. Sus características, al estructurar las matrices, facilitan ciertos cálculos.
2. 

# Referencias
[1]. “ss - Modelo de espacio de estados - MATLAB - MathWorks América Latina”, Mathworks.com. [En línea]. Disponible en: https://la.mathworks.com/help/control/ref/ss.html. [Consultado: 02-nov-2024].

