# Algoritmo-de-RSA

El algoritmo RSA que implementamos solo tiene un parametro "k", que es el número de bits que utilizaremos, luego generamos dos primos "p" y "q" de manera aleatoria tal que ambos números sean diferentes, para esto utilizaremos la función "PRIMO", para ello genearemos números aleatorios de K/2 bits y los pasamos por el test de Miller con "s" = 43 para que sea más preciso, para esto utilizaremos la función "COMPUESTO" para así descartarlos como primos, dentro de nuestra función COMPUESTO utilizaremos una función auxiliar para la exponenciación modular "EXPMOD". 


Definimos n como el producto de p y q, luego nuestra función fi y por último un bool seg para nuestro bucle, este bucle nos genera un número aleatorio e hasta que fi de n y e sean coprimos, para comprobarlo utilizaremos la funcion "EUCLIDES"


Luego hallamos d tal que d sea el inverso de e, para ello necesitamos la función "inverso", que esta a su vez utiliza "EUCLIDES" y "EUCLIDESEXT" 


Implementamos las funciones de cifrado y decifrado, para ambas utilizaremos la función EXPMOD, para cifrar la base sería M, el exponente e y el módulo n mientras que para decifrar la base sería C, el exponente d y el módulo n, donde m es el mensaje como texto plano y c el mensaje cifrado.


Por último llamamos a la función RSA para 64 bits y esta nos retorna n,e y d, generamos 10 números aleatorios desde 2 hasta n-1, los ciframos y deciframos, y los guardamos en listas para ver los resultados.
