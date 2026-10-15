## PEP 8

No se debe dejar espaciones en funciones con argumentos por defecto 
```python
def my_function(arg1=8):
	return 8;
```

## modulo collections

Define nuevos tipos de datos con funcionalidades compuestas para reemplazar tipos tradicionales como tuplas, listas, diccionarios.

- Chain Map 
	- Agrupacion de diccionarios
- Counter
	- Cuenta el numero de ocurrencias dentro de un string, objecto. Como el numero de letras s en "redes"
- defaultdict


## List comprehensions

Forma de crear listas de manera rapida

```python
square_number = [x**2 for x in range(12) if x >= 4]
```

## Iteracion Multiple

Forma de iterar sobre varias listas/tuplas a la vez, como al recorrer una matriz, en python se usa el metodo zip() para mayor legibilidad

## Generadores

Se utiliza el operador **yield**, retorna en valor actual de la iteracion, pero almacenando el estado global dentro del rango establecido.


## OOP 
factory methods = Metodos que manipulan el estado de la clase
@classmethod = metodo de clase, recibe como parametro
	- Constructores alternativos

@staticmethod = funciones que no reciben ni la instancia, ni la clase, agrupacion logica de funciones que no dependen del estado de la clase2

@abstracmethod -- interfaz que  las clases derivadas deben implementar

Mixin -- Añadir metodos/atributos adicionales a una clase a traves de herencia multiple, heredar de dos clases a la vez, la primera que hereda el comportamiento y la segunda como metodos adicionales no estrictamente necesarios.

```python
class Usuario(Persona, SerializableMixin):
```

### MRO (Method resolution order)

Algoritmo que determina el orden de ejecuacion de los metodos cuando se sobreescriben por herencia multiple.

