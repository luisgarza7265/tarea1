
with open("123", "r+") as archivo:
    file = archivo.read()
    resultado = False

def comparar_caracteres(palabra, caracter, tamaño, actual):
    if actual == tamaño:
        return True
    if palabra[actual] == file[caracter]:
        comparar_caracteres(palabra, caracter + 1, tamaño, actual + 1)
    else:
        return False


def buscar_palabra():
    palabra = input("Ingrese la palabra que desea buscar: ")
    tamaño = len(palabra)
    caracter = -1
    for letra in file:
        caracter += 1
        if palabra[0] == letra:
            try:
                resultado = comparar_caracteres(palabra, caracter + 1, tamaño, actual=1)
                if resultado:
                    break
            except:
                pass

    if resultado:
        return print(f"{palabra} se encuentra en la posicion {caracter - tamaño}")
    else:
        return print(f"{palabra} no se encuentra en el archivo")
        

    
    
    

with open("123", "w") as archivo:
    archivo.write("ndcnnciwjopcwoinjobn jnuchwiojcfvoikwmcvwcmonitortecladomouse")

buscar_palabra()
