# kotlin


1: sirve para saber si un numero es primo o no, simplemente ponga en program arguments el numero que desea saber
fun esPrimo(n: Int): Boolean {
    if (n < 2) return false
    for (i in 2..Math.sqrt(n.toDouble()).toInt()) {
        if (n % i == 0) return false
    }
    return true
}

fun main(args: Array<String>) {
    if (args.isEmpty()) {
        println("Debes ingresar un número como argumento.")
        return
    }
    val n = args[0].toInt()
    println("¿Es primo? ${esPrimo(n)}")
}


2: este sirve para obtener el MCD entre 2 numeros usando el algoritmo de euclides, en program arguments ponga los 2 numero que va a usar
fun main(args: Array<String>) {
    if (args.size < 2) {
        println("Por favor ingresa dos números en Program arguments (ejemplo: 48 18)")
        return
    }

    val a = args[0].toInt()
    val b = args[1].toInt()

    println("El MCD de $a y $b es: ${mcd(a, b)}")
}
fun mcd(a: Int, b: Int): Int {
    return if (b == 0) a else mcd(b, a % b)
}


3: en este punto se va a necesitar un numero para saber su factorial, ingrese el numero del cual desea saber el factorial donde dice val number
fun factorialIterative(n: Int): Long {
    if (n < 0) {
        return -1 
    }
    var result: Long = 1
    for (i in 2..n) {
        result *= i
    }
    return result
}

fun main() {
    val number = "ponga un numero aca"
    println("El factorial de $number es: ${factorialIterative(number)}")
}


