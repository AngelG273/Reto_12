# Reto_12

- Ejercicio 1:
```Python
# Se define el diccionario
dict_1 = { 22:"nube", 44:"sol", 55:"tierra", 66:"luna" }
#Se utiliza el operador sorted, este se puede usar porque el .values devuelve una lista que sorted puede ordenar
sorted(dict_1.values())
```

- Ejercicio 2:
```Python
def mezclar_diccionarios(dic1, dic2):

    diccionario_mezclado = dic2.copy()  # Copiar el segundo diccionario
    diccionario_mezclado.update(dic1)  # Actualizar con el primer diccionario (sobrescribe si hay claves repetidas)
    
    return diccionario_mezclado

if __name__ == "__main__":
#Se definen los diccionarios
diccionario1 = {'a': 1, 'b': 2, 'c': 3}
diccionario2 = {'b': 10, 'c': 20, 'd': 30}
#Se llama la funcion
resultado = mezclar_diccionarios(diccionario1, diccionario2)
print(resultado)  # Salida: {'b': 2, 'c': 3, 'd': 30, 'a': 1}

```
- Ejerccio 3:
```Python

```
- Ejerccio 4:
```Python

```
- Ejercicio 5:
```Python

```
