[filmina teórica 1](https://docs.google.com/presentation/d/1FlhGIvC8bVVELO1vune0LqpluJsugZPYCM5Ejx6DzME/edit?slide=id.g1f3c798447e_0_0#slide=id.g1f3c798447e_0_0)
# Teoría
## ¿Qué es un algoritmo?

Es una secuencia finita de instrucciones o reglas que describen de modo preciso las operaciones que una computadora debe realizar para ejecutar una tarea en un tiempo determinado.

Pasos para desarrollar un algoritmo:****
1. entender el problema y la necesidad de solución es imprescindible para poder avanzar
2. definir los datos de entrada con los que vas a trabajar para lograr el resultado
3. plantear los procesos necesarios para pasar los datos de entrada a datos de salida transformados
4. validar el algoritmo

## Pseudocódigo

Estructura general:

```
Accion [nombre] es
	Ambiente
		var1 : [tipo de dato]
		... denominación y/o asignación de variables a utilizar
		Subacción [nombre](parámetros):
		FinSubacción
	Algoritmo
		... instrucciones
FinAcción
```

### Operadores

| concepto        | sintaxis       | tipo       |
| --------------- | -------------- | ---------- |
| igualdad        | A = B          | relacional |
| desigualdad     | A >< B         | relacional |
| menor a         | A < B          | relacional |
| menor o igual a | A <= B         | relacional |
| mayor a         | A > B          | relacional |
| mayor o igual a | A >= B         | relacional |
| o               | A o B          | lógico     |
| y               | A y B          | lógico     |
| negación        | No(A) \| No(B) | lógico     |
 
# Ejercicios

[Guía de ejercicios](https://aed-frre.github.io/practica/0)
## Datos y Estructuras
### 1.1.5.1
Escribir un programa que permita calcular el precio de un artículo para un año dado, considerando que la inflación es del 4 por 100 anual.

La fórmula del precio es: _P = C * (1 + R) ^ (N - A)_

C - Precio actual.  
N - Año futuro.  
R - Tasa de Inflación.  
A - Año actual.

```
Accion calcular_precio es
	Ambiente
		precio_act, precio_fut: real ó N(5, 2)
		año_act, año_fut: entero ó N(4)
		inflación_anual = 0.04
	Proceso
		Escribir("Este algoritmo calcula el precio ajustado por inflación de un
		producto en un lapso dado")
		Escribir("Ingrese el año actual y el futuro")
		Leer(año_act, año_fut)
		Escribir("Ingrese el precio actual del producto")
		Leer(precio_act)
		precio_fut := precio_ac * (1 + inflación_anual) ** (año_fut - año_act)
		Escribir("El precio del artículo para el año ", año_fut, " es de $", 
		precio_fut)
FinAcción	
```


### 1.1.5.2 
Las raíces de una ecuación de segundo grado $ax^2 + bx + c =0$ son reales si y sólo si el discriminante dado por $(b2−4ac)$ no es negativo. Se desea leer el valor de los coeficientes a, b, c e imprimir el resultado del discriminante. Realizar prueba de escritorio.

```
Accion calcular_discriminante es
	Ambiente
		a, b, c : real
		discriminante : real
	Proceso
		Escribir("Ingrese los coeficientes a, b y c de una función cuadrática")
		Leer(a, b, c)
		discriminante := b*2 - 4*a*c
		Escribir("El discriminante de la función es: ", discriminante)
FinAccion
```

| a   | b   | c   | discriminante |
| --- | --- | --- | ------------- |
| ?   | ?   | ?   | ?             |
| 4   | 2   | 8   | ?             |
| 4   | 2   | 8   | -124          |

### 1.1.5.3
Se desea comprar una PC y una impresora. Calcular el precio total: el cual está dado por la suma de los precios de costos, los porcentajes de ganancia del vendedor y un 21% de IVA. Supóngase una ganancia del vendedor del 12% por la PC y 7% por la impresora. Se leen los costos y se imprimen el precio total de ventas.

```
Acción calcular_total es
	Ambiente
		costo_pc, costo_impresora, precio_total : real
		precio_pc = 1.12
		precio_impresora = 1.07
		iva = 0.21
	Proceso
		Escribir("Este algoritmo calcula el precio final de una PC y una 
		impresora, añadiendo margen de ganancias y iva. Ingresar el costo de la 
		PC y luego el de la impresora")
		Leer(costo_pc, costo_impresora)
		precio_total := (costo_pc * precio_pc + costo_impresora * 
		precio_impresora) * (1 + iva)
		Escribir("El precio final por ambos productos es de: ", precio_total) 
FinAcción 
```

### 1.1.5.4
Se desea calcular la superficie de un trapecio, para la cual se ingresa la longitud de ambas bases y la altura. En base a la fórmula: `S=(Bmay+Bmen)×h2` $$S=\frac{(B_{may}+B_{men})×h}{2}$$Finalizando el proceso, emitir dicha superficie y los valores ingresados.

```
Acción superficie_trapecio es
	Ambiente
		base_may, base_men, altura, superficie : real
	Proceso
		Escribir("Este algoritmo calcula la superficie de un trapecio a partir 
		de los valores dados. Ingresar el número de su base mayor, base menor y 
		altura")
		Leer(base_may, base_men, altura)
		superficie := ((base_may + base_men) * h) / 2
		Escribir("La superficie de un trapecio con base mayor ", base_may, 
		", base menor ", base_men, " y altura de ", altura, " es de ", 
		superficie )
FinAcción
```

### 1.1.5.5
Se desea calcular el valor de la sección *(S)* de un conductor, la cual se determina en función de la corriente eléctrica *I* y de la conductividad *C* del material *(C=I/S)*. Además, a la sección así obtenida se le incrementa un 25% por razones de seguridad. 

```
Acción conductor_calcular_sección es
	Ambiente
		corr, conduc, seccion : real
		margen = 1.25
	Proceso
		Escribir("Este algoritmo calcula el valor de la sección S de un 
		conductor en función de su corriente eléctrica y conductividad. Ingrese
		el valor de la corriente y conductividad")
		Leer(corr, conduc)
		seccion := (corr / conduc) * margen
		Escribir("El valor de la sección S es de: ", seccion) 
FinAcción 
```

### 1.1.5.6
Realizar un programa que lea dos número complejos, *(a,b)* y *(c,d)*, y calcule su producto: *(a, b) ∗ (c, d) = (ac - db, ad + bc)* $$(a,b)∗(c,d)=(ac−db,ad+bc)$$
```
Acción calcular_producto es
	Ambiente
		a, b, c, d, primer_comp, segundo_comp : real
	Proceso
		Escribir("Este algoritmo devuelve el producto entre 2 pares de números")
		Escribir("Inserte los números del primer par")
		Leer(a, b)
		Escribir("Inserte los números del segundo par")
		Leer(c, d)
		primer_comp := a*c - d*b
		segundo_com := a*d + b*c
		Escribir("El resultado del producto es (", primer_comp, ", ", 
		segundo_comp, ")")
FinAcción
```

### 1.1.5.7
Escriba un algoritmo que halle la media geométrica de tres valores *X, Y, Z*. Este debe emitir los tres valores por separado y luego el valor medio. La media geométrica es igual a *(X × Y × Z) / 3*

```
Acción calcular_media_geo es
	Ambiente
		X, Y, Z, media : real
	Proceso
		Escribir("Este algoritmo calcula la media geométrica entre 3 medidas X, 
		Y y Z. Ingresar los valores respectivos")
		Leer(X, Y, Z)
		media := (X, Y, Z) / 3
		Escribir("La media geométrica para los valores dados: ")
		Escribir(X)
		Escribir(Y)
		Escribir(Z)
		Escribir("fue de: ", media)
FinAcción
```

## Estructuras condicionales y repetitivas

### 1.1.6
Escriba un algoritmo que permita ingresar 3 valores numéricos y determine cuál es el mayor, el medio y el menor. (era el 3 de los complementarios)