# ==========================================
# TALLER 7 - DICCIONARIOS EN PYTHON
# Lógica de Programación I
# ==========================================


# ==========================================
# ACTIVIDAD GUIADA 1: GESTIÓN DE INVENTARIO
# ==========================================

inventario = {
    "cuaderno": 12,
    "lapiz": 30,
    "borrador": 8
}

# 1. Tipo de datos
print("Tipo de claves:", type("cuaderno"))
print("Tipo de valores:", type(12))

# 2. Consulta segura
print("Cantidad de reglas:", inventario.get("regla", 0))

# 3. Agregar regla
inventario["regla"] = 10

# 4. Modificar cuadernos
inventario["cuaderno"] = 15

# 5. Sumar existencias
total = sum(inventario.values())

print("Inventario actualizado:", inventario)
print("Total de existencias:", total)


# ==========================================
# EJERCICIO 1: DIRECTORIO DE CONTACTOS
# ==========================================

contactos = {
    "Carlos": "3001234567",
    "Laura": "3012345678",
    "Andres": "3023456789",
    "Maria": "3034567890",
    "Juan": "3045678901"
}

nombre = input("Ingrese el nombre del contacto: ")

print("Número:", contactos.get(nombre, "Contacto no encontrado"))

# Actualizar o registrar contacto
nombre_nuevo = input("Ingrese el nombre para registrar o actualizar: ")
telefono = input("Ingrese el número de teléfono: ")

contactos.update({nombre_nuevo: telefono})

# Mostrar contactos
print("\nDIRECTORIO TELEFÓNICO")
for nombre, telefono in contactos.items():
    print(f"{nombre:<15} {telefono}")


# ==========================================
# EJERCICIO 2: FRECUENCIA DE PALABRAS
# ==========================================

parrafo = "python es versatil y python es legible y practico"

palabras = parrafo.split()

frecuencia = {}

for palabra in palabras:
    frecuencia[palabra] = frecuencia.get(palabra, 0) + 1

print("\nFRECUENCIA DE PALABRAS")

for palabra, cantidad in frecuencia.items():
    print(palabra, ":", cantidad)


# ==========================================
# EJERCICIO 3: REGISTRO DE CALIFICACIONES
# ==========================================

calificaciones = {
    "Carlos": [4.0, 3.5, 4.5],
    "Mariana": [4.8, 5.0, 4.7],
    "Andres": [3.0, 2.8, 3.5]
}

# 1. Calcular promedio
print("\nPROMEDIOS")

for estudiante, notas in calificaciones.items():
    promedio = sum(notas) / len(notas)
    print(estudiante, ":", round(promedio, 2))

# 2. Agregar nota a Carlos
calificaciones["Carlos"].append(4.0)

# 3. Estudiante con mayor promedio
promedios = {}

for estudiante, notas in calificaciones.items():
    promedios[estudiante] = sum(notas) / len(notas)

mejor_estudiante = max(promedios, key=promedios.get)

print("Mejor estudiante:", mejor_estudiante)
print("Promedio:", round(promedios[mejor_estudiante], 2))


# ==========================================
# PROYECTO INTEGRADOR: CATÁLOGO DE TIENDA
# ==========================================

catalogo = {
    "P01": {
        "nombre": "Cuaderno argollado",
        "precio": 6500,
        "stock": 20
    },
    "P02": {
        "nombre": "Caja de micropuntas",
        "precio": 18000,
        "stock": 12
    },
    "P03": {
        "nombre": "Resma de papel",
        "precio": 15000,
        "stock": 8
    }
}

# 1. Búsqueda segura
codigo = input("\nIngrese el código del producto: ")

producto = catalogo.get(codigo)

if producto:
    print("Nombre:", producto["nombre"])
    print("Precio:", producto["precio"])
    print("Stock:", producto["stock"])
else:
    print("Producto no encontrado")


# 2. Ingreso de existencias
codigo = input("Código del producto para aumentar stock: ")

if codigo in catalogo:
    cantidad = int(input("Cantidad a agregar: "))
    catalogo[codigo]["stock"] += cantidad
    print("Stock actualizado:", catalogo[codigo]["stock"])
else:
    print("Producto no encontrado")


# 3. Registro de producto nuevo
codigo = input("Ingrese código del nuevo producto: ")

if codigo in catalogo:
    print("El producto ya existe")
else:
    nombre = input("Nombre del producto: ")
    precio = float(input("Precio unitario: "))
    stock = int(input("Cantidad en bodega: "))

    catalogo[codigo] = {
        "nombre": nombre,
        "precio": precio,
        "stock": stock
    }

    print("Producto registrado correctamente")


# 4. Cálculo del valor total del inventario
total_inventario = 0

for codigo, producto in catalogo.items():
    valor = producto["precio"] * producto["stock"]
    total_inventario += valor

print("\nCATÁLOGO COMPLETO")

for codigo, producto in catalogo.items():
    print(codigo, producto)

print("Valor total del inventario:", total_inventario)
