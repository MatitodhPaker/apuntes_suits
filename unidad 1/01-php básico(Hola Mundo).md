## Hola Mundo

Para hacer un hola con php se requiere primero iniciar los servicios de apache en **xampp** o de pendiendo de que servicio estés utilizando, ademas de crear una carpeta en el htdocs en este caso creamos la carpeta de php basico.
![[Pasted image 20230824072637.png]]
una vez creada la carpeta la abrimos con vscode para poder trabajar con cualquier archivo dentro de la carpeta
![[Pasted image 20230824073126.png]]
una vez creado el archivo creamos nustro tag de php para hacer codigo interpretado por php
```php
 <?php

        print('hola mundo')

    ?>
```

tenemos diferentes funciones de php para poder imprimir una respuesta
```php
	<?php
		print('hola');
		echo 'hola mundo';
	?>
```

**ademnas se puede insertar etiquetas html en el echo o el print y podremos agregar estilos css**
```php
	<?php

        print('hola mundo');

        echo '<br>';

        echo '<h1 style="color: blue">Hola mundo</h1>';

    ?>
```
las variables en php se declaran con el simbolo de '$' el cual nos permite crear variables el tipo de dato de las variables php lo infiere dependiendo su contenido
```php
	<?php
		 $nombre='parker';
		 $edad=25;
		 $soltero=false;
		var_dump($nombre);
		var_dump($edad);
		var_dump($soltero);
    ?>
```
algunas reglas para nombrar variables son:
1. Usar Unicamente careacteres y letras (0-9,a-z,A-Z) y guion bajo
2. No utilizar caracteres especiales
3. Si se puede utilizar con guion bajo al comienzo de la variable
4. el  nombre de la variable debera ser de significado semantico
5. tener en cuenta que se distinga entre nombres con mayuscula y miniscula
6. evitar el uso de palabras reservadas
Los comentarios en php se hacen con doble slash
## operadores aritmeticos
```php
<?php

    print(5*4);

    echo "<br>";

    print(5/4);

    echo "<br>";

    print(5-4);

    echo "<br>";

    print(5+4);

    echo "<br>";

    print(10%2);

?>
```
los operadores aritmeticos nos permiten hacer operaciones.

## operadores Logicos
```php
<?php

    var_dump(false and false);

    echo"<br>";

    var_dump(true and false);

    echo"<br>";

    var_dump(false && true);

    echo"<br>";

    var_dump(true && true);

    echo"<br>";

    //tabla de verdad del or

    var_dump(false or false);

    echo"<br>";

    var_dump(true or false);

    echo"<br>";

    var_dump(false | true);

    echo"<br>";

    var_dump(true | true);

    echo"<br>";

    //tabla de verdad del not

    var_dump( !false);

    echo"<br>";

    var_dump(!false);

?>
```
estos nos permiten hacer operaciones lógicas de verdadero o falso

| nombre | simbolo|
| -------| -------|
| and |&& o and
|or|l

## Operadores de comparacion

![[Pasted image 20230824082706.png]]

## Sentencia if

La sentencia if nos permite ejecutar un bloque de codigo si una condición se cumple
```ad-note
funciona con boleanos o con operaciones logicas
```

```php
	<?php

    $edad=35;

    if ($edad>=18 and $edad<30) {

        echo "eres mayo de edad";

    }else if($edad>=30 and $edad<60){

        echo "Eres un adulto joven";

    }else if ($edad>=60) {

        echo "Eres un adulto Mayor";

    }else{

        echo "eres menor de edad";

    }

?>
```

## Switch

Un switch es una estructura de control que ayuda a ejecutar un caso *dependiendo de si hace match o no* 
```php
<?php

    $opcion="HTML";

    switch ($opcion) {

        case 'HTML':

            print('Lenguaje de marcado');

            break;

        case 'CSS':

            print('hoja de estilos');

            break;

        case 'JS':

            print('Lenguaje de marcado');

            break;

        default:

            print('no se encuentra dentro de la opciones');

            break;

    }

?>
```

## while

es un bucle que se ejecuta si la condición sea cierta 
**ejemplo**
```php
	<?php

    $a=0;

    while ($a <= 10) {

        print($a);

        $a++;

    }

?>
```

## Do while

Es un bucle que se ejecuta una vez y después evalúa la condición

**ejemplo:**
```php
<?php

    $a=11;

    /* while ($a <= 10) {

        print($a);

        $a++;

    } */

    do {

        print($a);

    } while ($a <= 10);

?>
```

## Arreglos 

Los arreglos en php pueden guardar cualquier tipo de de dato sin problemas ademas de que guardan una cantidad de información

```php
	$calificaciones=[100,99,89,78,67,78];

    $arreglo=["hola mundo",24,true];

    echo "<pre>";

    print_r($arreglo);

    echo "</pre>";
```

```ad-note
 para mprimir objetos se usa el print r
```

## Arreglos Asociativos

son representados de diferente manera en php pero son objetos 
**ejemplo**
```php
<?php

    $persona=[

        "nombre"=>"fernando",

        "edad"=>29,

        "direccion"=>[

            "ciudad"=>"CDMX",

            "alcaldia"=>"Milpa Alta",

            "pueblo"=>"San Juan"

        ],

        "calificaciones"=>[1,2,3,4,5,6]

    ];

echo "<pre>";

print_r($persona);

print($persona["nombre"]);

echo"<br>";

print($persona["direccion"]["pueblo"]);

echo"<br>";

print($persona["calificaciones"][2]);

echo "</pre>";

?>
```
## bucle for
```ad-note
ES UNA OPERACION QUE NOS PERMITE CICLAR MIENTRAS LA CONDICION SE CUMPA
```
**ejemplo**
```php
<?php

    $calificaciones=[100,99,89,78,67,78];

    $arreglo=["hola mundo",24,true];

    for ($i=0; $i < count($arreglo) ; $i++) {

        print("iteracion".$i."valor: ".$arreglo[$i]);

        echo"<br>";

    }

    for ($i=0; $i < count($calificaciones) ; $i++) {

        print("iteracion".$i."valor: ".$calificaciones[$i]);

        echo"<br>";

    }

?>
```

## for each

 
