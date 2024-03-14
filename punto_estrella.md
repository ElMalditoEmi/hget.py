# El problema
Cuando se intenta acceder a una URL en internet que no esta formada por todos caracteres del set de ascii, estos no pueden ser enviados de forma 'cruda' a traves de internet usando
los estandares y protocolos que son utilizados normalmente.

# Url encoding
Para solucionar esto existe el 'URL encoding'; que a caracteres que no pertenecen al set ascii se les asigna un numero hexadecimal de 2 digitos (o una combinacion de varios numeros) 
que lo representan. Este numero en hexa es obviamente representable con letras y numeros que estan en el set de ascii, por lo que usando el simbolo '%' por delante del valor en hexa
podemos castear su valor en una url para usarlos.

## Ejemplo
Por ejemplo algo como el caracter: '文' viajaria a traves de internet como: '%E6%96%87' que es una cadena formada unicamente por caracteres ascii.
Con esta [herramineta](https://www.urlencoder.org/es/) se puede probar el encoding de links y caracteres.

Tambien podemos ver este comportamiento si googleamos el caracter '@', que al apretar enter el navegador entra a: 'https://www.google.com/search?client=firefox-b-d&q=%40'
vemos que no esta el arroba por ningun lado... solo que esta encodeado como '%40' su representacion hexadecimal con el '%' casteandolo.

