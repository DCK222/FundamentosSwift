# Fundamentos Swift
## Variables y Constantes:
```swift
var variable:String = "Hola"
let bienvenido = “Bienvenido, bienvenida”

let saludo2: String
saludo2 = "Bienvenido, Bienvenida”

let numero: Int
```
### Escritura del camello : 
### • Primera letra en minúsculas (excepto clases, estructuras y enumeraciones)
### • Primera letra del resto de palabras en mayusculas
```swift
var estaEsMiVariable = 1
```
## Operadores Aritmeticos :
```swift
var edad = 10
var edadNiña=20

var edadTotal = edadNiña-edad

edadTotal+=20

edadTotal+=20.0 (error)
edadTotal-=25
```
## Operadores Logicos :
```
==
!=
>
<
>=
<=
&&
||
```

```swift
let edadSeñora = 41
if edadSeñora == 40
{
print("La señora tiene 40 años")
}else{
print("La señora no tiene 40 años")
}
```
## Strings : 
```swift
let edadSeñora = 41
if edadSeñora == 40
{
print("La señora tiene 40 años")
}else{
print("La señora tiene \(edadSeñora) años")
}
var miNombre = "Ivan"
print("Hola que tal \(miNombre)?”)
let multilinea2 = """
Hola
caracola

}
```
###  Si ponemos 3 doble comilla al principio y final es una cadena multilenea
### print(multilinea2)rint("La señora no tiene 40 años")

## Strings : 
```swift
let edadSeñora = 41
if edadSeñora == 40
{
print("La señora tiene 40 años")
}else{
print("La señora no tiene 40 años")
}
```
## Operadores de rango
```swift
a...b
a..<b
for i in 1...5 {
print(i)
}
//operadores de rango
let r1 = 10 ... 40 //r1 almacena valores entre 10 y 40
let r2 = 10 ..< 40 //r2 almacena valores entre 10 y 39
let n1 = ...40
let n2 = ..<40
let n3 = 60 ...
Int.max
let z1 = "a"..."z" //rango desde A a Z
z1.contains("d")
z1.contains("D")
let aaa = 9223372036854775807 //numero maximo de un Int en un procesador de 64 bits
//let ccc = aaa + b //me dara error de ejecucion porque supera el maximo de Int
//con esto lo podemos controlar
let ddd = aaa.addingReportingOverflow(b) //funcion de desbordamiento
ddd.overflow //devuelve true si ha habido desbordamiento
//: [Next](@next)

```
## Condicional IF

```swift
if temperatura == 1{
print(“lo que pase en caso 1")
}
else if temperatura > 1 && temperatura <= 5{
print(“lo que pase en caso 2”)
}
else if temperatura > 16 && temperatura <= 25{
print(“lo que pase en caso 3")
}
else{
print (“lo que pase por defecto”)
}
```

## Bucles For :
```swift
for i in 1...10 {
if i%2 == 0{
print("Es par \(i)")
} else {
print("Es impar \(i)")
}
//para ir de 2 en 2
for i in stride(from: 1, through: 100, by: 2) {
print(i)
}
```

## Bucles While
```swift
var puntuacion = 0
while condition {
Código
break
}

var puntuacion = 0
while puntuacion < 15 {
puntuacion += 1
if puntuacion == 10 {
print("El estado de tu salud ha mejorado")
}
print("La puntuación es: \(puntuacion)")
}
```
## Bucles. Repeat-while:
```swift
numero = 25
repeat{
numero += 1
print("El valor de numero es \(numero)")
}
while numero<25

```
## Sentencia Switch
```swift
switch temperatura {
case 1:
print(“lo que pase en caso 1”)
fallthrough //si ponemos eso pasa al siguiente case SIN evaluarlo
case 2 ... 5:
print(“lo que pase en caso 2")
case 16 ... 25:
print(“lo que pase en caso 3")
default: //importante: siempre tiene que esta
print (“lo que pase por defecto”)
}
```
### Colecciones. Arrays
```swift
var miArray = [1,2,3,4,5,6]
Array vacio
var miArray2:Int = [] //error
var miArray3:[Int] = [] // array vacio
var miArray4 = [Int]() //array vacio
//añadir elementos de uno en uno
miArray.append(7)
miArray.append(8)
miArray += [9,10,11,12,13] //añadir varios elementos de golpe
//añadir elemento en una posicion
miArray.insert(0, at: 0)
print("mi array tiene \(miArray)”)
//otra opción
let array = Array(1...100)

c3.count //cantidad de elementos
c3.capacity //cantidad maxima de elenmentos que tiene reservados en memoria en
ese momento. Crece dinamicamente.
c3.reserveCapacity(12) //reserva en memoria la capacidad de para determinado
numero de elementos. Si se reserva la capacidad primero se ejecuta mas rapido
ya que se reserva la capacidad desde el principio, en vez de ir aumentando la
capacidad en tiempo real cada vez que se le inserte. A veces el reserva mas
espacio del que le decimos, si por ejemplo 10000 nos reserva a lo mejor 10000 o
10236 o 12284 (numero superior sin mas)
```

```swift
//contar elementos de un array
miArray.count
//saber si el array esta vacio
miArray.isEmpty
//eliminar elementos de un array
miArray.removeAll()
miArray.removeFirst()
miArray.removeLast()
miArray.remove(at: 5)
//iterar por un array
for elemento in miArray
{
print ("el elemento es \(elemento)")
}
print("mi array tiene \(miArray)")
```
## Colecciones. Diccionarios
```swift
var diccionario = [clave:valor,clave:valor,clave:valor...]
var diccionario = [“clave 1”:1,”clave 2”:2,”clave 3”:3]
var diccionarioVacio = [String:Int]() // si pulsamos alt u option y hacemos clic en el
diccionario (o cualquier variable) muestra su definición.
//acceder a un diccionario
diccionario ["clave 1"]
```
## Colecciones.Diccionarios. Excepción (String:Any)
### A priori debe ser del mismo tipo todo el diccionario
### pero podemos indicar que no será si
```swift
var diccionario = ["clave 1":1,"clave 2":2,"clave 3":"3"] as [String : Any]
```
## Colecciones.Diccionarios
```swift
Añadir elementos:
diccionario ["clave 4"] = 4
print ("El diccionario tiene los siguientes elementos \(diccionario)")
Eliminar elementos:
diccionario.removeValue(forKey: "clave 1") //borra un elemento de una clave
diccionario.removeAll() //borra tod
```
## Bucles 
```swift
for (clave, valor) in diccionario
{
print ("el valor es \(valor) y la clave es \(clave)")
}
```
## Colecciones.Set
```swift
Var miSet = set() //Error
Var miSet = Set<Int>() //para indicar el tipo
miSet.insert(4)
miSet.insert(4) //no da error pero no lo duplica
Print(“El Set tiene ahora: \(miSet)”
Se puede borrar:
miSet.remove(4) //ojo, 4 es el valor, no la posición

var conjunto1:Set = [1,2,3,4,5,6,7,1,2,5]
var conjunto2:Set = [4,1,0,11]
var conjunto3:Set = [2,7]
conjunto1.contains(6) //nos dice si tiene el 6
conjunto1.insert(10
```
## Alias de tipos de datos, typealias
```swift
Permite en cierta forma definir nuestros propios tipos de datos reutilizando los
existentes : 

typealias miTipoFloat = Float
var miVariableFloar: miTipoFloat
typealias miTipoUsuario = [String:String]
var miArray: [miTipoUsuario] = [miTipoUsuario]()
var miUsuario: miTipoUsuario = miTipoUsuario()
miUsuario["nombre"] = "Ivan"
miUsuario["apellido"] = "Alexis"
miArray.append(miUsuario)
print (miArray[0])
```
## Funciones
```swift
func miFuncion ()
{
//implementacion de la funcion
print("Soy una funcion simple")
}
miFuncion()
//funcion con parametros
func miFuncionConParametros(nombre: String)
{
print("se recibe \(nombre)")
}
miFuncionConParametros(nombre: "Ivan")
```
## Ejemplo :
```swift
//funcion que devuelve algo
func sumarNumero() -> Int
{
let numero1 = 1
let numero2 = 2
return numero1+numero2
}
let resultado = sumarNumero()
print(resultado)
//funcion que devuelve algo y requiere parametros
func sumarNumeros(numero1:Int, numero2: Int) -> Int
{
return numero1 + numero2
}
let resultado2 = sumarNumeros(numero1: 4,numero2: 6)
print(resultado2)
```
## Enumeraciones : 
```swift
enum GenerosCine{
case scifi, drama, comedia, infantil, fantasia, terror, anime
}
let genero1 = GenerosCine.comedia
if genero1 == .comedia
{
print("Es comedia")
}
//usar un switch con un enum genera por autocompletado todas las opciones y no requiere un default
switch genero1{
case .scifi:
print("Scifi")
case .drama:
print("Scifi")
case .comedia:
print("comedia")
case .infantil:
print("infantil")
case .fantasia:
print("fantasia")
case .terror:
print("Terror")
case .anime:
print("Anime")
}
```
## Opcionales
```swift
var cadena = "hola” //no es opcional, esta inicializada

var cadenaOpcional: String? 
//no esta inicializada la variable realmente,
tan solo esta preparada por si necesita que se inicie.

cadenaOpcional = cadena //asigna un valor a cadenaopcional
cadena = cadenaOpcional //falla
let edadSeñora = 41
if edadSeñora == 40
{
print("La señora tiene 40 años")
}else{
print("La señora tiene \(edadSeñora) años")
}
var miNombre = "Ivan"
print("Hola que tal \(miNombre)?”)
let multilinea2 = """
Hola
caracola

}
```

## Variables calculadas : 
```swift
Opción tipica:
var ancho: Intvar alto: Int
func centro() -> (x:Int, y:Int){
    (ancho/2, alto/2)
    }
    ancho = 1
    alto = 1
    centro()
    Opción con variantes calculadas:
    var ancho: Int
    var alto: Int
    ancho = 1a
    lto = 2
    var centro: (Int, Int) {
        (ancho/2 , alto/2)
        }
        
    centro
´´´

##Tuplas
```swift
una tupla es una agrupacion de datos
var peli1 = "Interstellar" 
//es una cadena
var peli2 = ("Interstellar", 2014, 9.8) //es una tupla, incluye titulo, año y puntuacion
peli2 // devuelve el primer componente
peli2.1 // devuelve el segundo componente
peli2.2 // devuelve el tercer componentevar 
peli3: (String, Int, Double)//Tambien podría ser peli3: (titulo:String, año: Int, puntuación: Double)
peli3 = ("Tenet", 2020, 9.7)//podemos etiquetar los componentesvar 
peli4: (titulo:String, año: Int, puntuacion: Double)peli4 = ("Star Wars", 1977, 9.7)peli4.titulo//se puede descomponerlet (pelicula, año, puntuacion) = peli3let (pelicula2, _, _) = peli3 //solo recojo el titulo

Mas ejemplos :
//se puede descomponer
let (pelicula, año, puntuacion) = movie3let (pelicula2, _, _) = movie3 //solo recojo el titulo
switch movie3 {
    case (_,2020,_):
    print("Peli de 2020")
    fallthrough //si ponemos eso pasa al siguiente case sin evaluarlo
    case (_, _, 9.7): 
    print ("tiene la puntuacion de 9.7")
    case (_,2020, let score) 
    where score > 9: //cojo el tercer dato y lo metoen una constante llamada score, y compruebo que sea mayor que 9print ("Es una peli de 2020 y puntuacion mayor que 9")
    
    default: ()}

Mas ejemplos :

//se iguala a un patron
if case(_, 2014, _) = movie2 {
    print("La peli es de 2014")
    }if case(_, 2020, let score) = movie3 , score > 9 {
        print("La peli es de 2020 con mas de 9")
        }let a = 1let b = 2let c = 3//es igual que
        var (d,e,f,g,h) = (4,5,6,7,8)//si quiero cambiar 2 valores por ejemplo 
        d = g y g = d(d,g) = (g,d)
```

## Protocolos
```swift
let cositas: [Any] = [1,2,"Hola","Adios", true]
//el protocolo Equatable en clases genera una funcion == , pero en struct por
defecto lo implementa sin añadirlo
struct Bicho: CustomStringConvertible, Equatable {
let nombre: String
let color: String
var description: String {
"Es un \(nombre) de color \(color)"
}
}
let bicho1 = Bicho(nombre: "Gamusino", color: "verde")
let bicho2 = Bicho(nombre: "Zargafilo", color: "amarillo")
let bicho3 = Bicho(nombre: "Gamusino", color: "verde")
print (bicho1)
bicho1 == bicho2
Protocolos
```
