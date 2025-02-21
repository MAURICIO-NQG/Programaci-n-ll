from datetime import datetime

class Cliente:
    def __init__(self, cedula, nombre, apellido, telefono, correo, direccion, fecha_nacimiento):
        self.cedula = cedula
        self.nombre = nombre
        self.apellido = apellido
        self.telefono = telefono
        self.correo = correo
        self.direccion = direccion
        self.fecha_nacimiento = fecha_nacimiento

    def obtener_datos(self):
        return (f"Cédula: {self.cedula}, Nombre: {self.nombre}, Apellido: {self.apellido}, "
                f"Teléfono: {self.telefono}, Correo: {self.correo}, Dirección: {self.direccion}, "
                f"Fecha de nacimiento: {self.fecha_nacimiento}")

    def calcular_edad(self):
        # Extraer el año de la fecha de nacimiento
        anio_nacimiento = int(self.fecha_nacimiento[:4])
        # Obtener el año actual
        anio_actual = datetime.now().year
        # Calcular la edad
        return anio_actual - anio_nacimiento

    def obtener_mensaje(self):
        edad = self.calcular_edad()
        return f"Mi nombre es {self.nombre} {self.apellido} y vivo en {self.direccion} y tengo {edad} años de edad."

# Crear una instancia de Cliente y mostrar el mensaje
cliente = Cliente(
    "02909237873",
    "MAURICIO",
    "ARRIETA",
    "98765331",
    "ARRIETAMAURO@example.com",
    "SAN JUAN  123",
    "1980/05/5"
)

print(cliente.obtener_mensaje())




