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
 
 Nos ayuda a recorrer un arreglo de manera mas sencilla otorgando el resultado.
 ``
 
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

    $calificaciones=[100,99,89,78,67,78];

    $arreglo=["hola mundo",24,true];

    /* foreach($calificaciones as $calificacion){

        print($calificacion);

        echo"<br>";

    }

    foreach($calificaciones as $calificacion):

        print($calificacion);

        echo"<br>";

    endforeach; */

    foreach($persona as $llave => $valor){

        /* print("llave".$llave."valor".$valor);

        echo"<br>"; */

        if (gettype($valor)=='array') {

            print_r($valor);

        }else {

            print("llave".$llave."valor".$valor);        

        }

        print(gettype($valor));

        echo "<br>";

    }

?>
```

## Funciones

Para hacer una funcion usamos la palabra funtion
```ad-note
 Las funciones solo deben ejecutar una tarea especifica 
```

```php
	<?php

    function saludar($nombre,$apellido){

        return "hola".$nombre." ".$apellido;

    }

    print(saludar("parker","perez"));

?>
```
  
## clases
 son clase de la cuales puden tener atributos y funciones de las cuale spodemos instarncar diversas cosas
 ```php
 <?php

    class Persona{

        public function __construct(public $nombre, public $apellido, public $edad){}

    }

    class Alumno{

        public $nombre;

        public $matricula;

        public $apellido;

        public $edad;

        public function __construct($matricula,$nombre,$edad,$apellido)

        {

            $this->$matricula=$matricula;

            $this->$nombre=$nombre;

            $this->$apellido=$apellido;

            $this->$edad=$edad;

        }

        function reprobaste ($materia,$calificacion) {

            return "Reprobaste ".$materia." con ".$calificacion;

        }

    }

    $nombre = new Persona("parker","perez",25);

    $alumno= new Alumno('181190076','parker',25,'perez');

    echo "<pre>";

        print_r($nombre);

        print_r($alumno);

        echo "<br>";

        print($alumno->reprobaste('poo',65));

    echo "</pre>";

?>
```

## Encapsulacion

Para encapsular los datos se utilizan las palabras resevadas de private o protected

```php
<?php

    class Producto{

        public function __construct(protected $nombre,private $precio,protected $caducidad){}

        public function obtenerProducto($nombre){

            if ($nombre === $this->nombre) {

                return 'Producto: '. $this->nombre .' precio: '. $this->precio .' caducidad '. $this->caducidad;

            }else{

                return 'El producto no existe';

            }

        }

        /* static public function obtenerProducto(){

            return "Accedimos al metodo estatico";

        } */

    }

    $galletas=new Producto('pincipe',20,'29/09/23');

    echo '<pre>';

        print_r($galletas->obtenerProducto('hola'));

        /* print_r(Producto::obtenerProducto()); */

    echo '</pre>';

?>
```

## funciones o atributos estaticos

```ad-note
	Para acceder a los metodos o atribotos estaticos dentro de la clase se usa self
```

Para acceder de manera estatica de una clase solo debes dar el nombre de clase y dos puntos 

```php
	<?php

  
  

    class Persona{

        public static $edad;

        protected static $nombre;

        protected static $apellido;

        public function __construct($edad,$apellido,$nombre){

            self::$edad=$edad;

            self::$apellido=$apellido;

            self::$nombre=$nombre;

        }

        public static function obtenerPersona(){

            return 'Nombre: '.self::$nombre.' Apellido '.self::$apellido.' edad '. self::$edad;

        }

    }

    $persona=new Persona(25,"Perez","Parker");

    print(Persona::obtenerPersona())

?>
```

```ad-note
	 para iniciar los datos primero debemos instanciar  las clases para de esa manera tener datos ya con valores 
```
