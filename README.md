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
import requests

# Función para obtener datos de una API y extraer pares clave: valor
def obtener_datos_api(url):
    response = requests.get(url)
    
    if response.status_code == 200:  # Verificar si la petición fue exitosa
        datos = response.json()  # Convertir la respuesta a JSON
        print(f"\nDatos de la API ({url}):\n", datos)  # Imprimir el JSON completo
        print("\nPares clave: valor extraídos:\n")
        
        # Imprimir los pares clave-valor de forma organizada
        for clave, valor in datos.items():
            print(f"{clave}: {valor}")
        
        return datos
    else:
        print(f"Error al conectar con la API: {url}")
        return None

# URLs de 3 APIs públicas
apis = [
    "https://api.coindesk.com/v1/bpi/currentprice.json",  # Precio actual de Bitcoin
    "https://dog.ceo/api/breeds/image/random",           # Imagen aleatoria de un perro
    "https://api.agify.io/?name=michael"                # Predicción de edad según nombre
]

# Conectarse a cada API e imprimir los resultados
for url in apis:
    obtener_datos_api(url)
    print("=" * 50)  # Separador visual
```
