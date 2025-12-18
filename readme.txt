README DE IVAN Y SERGIO     (enlace a github : https://github.com/sergiorodriguez-32/Trabajo-XML)

1. CONTENIDO ELEGIDO:

   Hemos escogido el sistema de reservas de un hotel.

2. Explicación breve sobre la estructura del xml: 

   La informacion esta organizada de forma logica, la raiz del XML es <hotel>, 
   la informacion se divide en tres elementos: (<clientes>, <empleados> y <distribuidores>).

   <clientes> con la etiqueta individual <cliente> y tiene el atributo obligatorio (id)  para identificar 
   al cliente de forma unica, guarda la informacion personal y bancaria; 
   (Nombre, Apellido, Genero, DNI, Numero de cuenta, Codigo postal y Codigo postal).

   <empleados> con la etiqueta individual <empleado> y tiene el atributo obligatorio (id)  para identificar 
   al empleado de forma unica, guarda la informacion pesonal, del puesto y el salario; (Nombre, Apellido, Puesto y Salario).

   <distribuidores> con la etiqueta individual <distribuidor> y tiene el atributo obligatorio (id) para identificar 
   al distribuidor de forma unica, guarda la informacion de la empresa; (Nombre de la empresa, Ciudad y Teléfono)

3. Que valida el dtd y el xsd:
      
   DTD;

   Solo valida el esqueleto del archivo: asegura , que el atributo id existan obligatorioramente y que no falten campos. 
   Trata todo el contenido (incluso números) como texto simple y establece con el comando #PCDATA que el contenido sean letras y numeros.
   Ademas estaable que las etiquetas clientes, empleados y distribuidores tengan que aparecer al menos una vez.

   XSD;

   Valida la calidad de la información: además de la estructura.
   Impone reglas matemáticas, asegurando que salario sea decimal y que telefono y codigo_postal sean números enteros,
   rechazando letras en esos campos. Tambien establece el orden de los atributos, el atributo (id) es obligatorio 
   y establece que cada etiqueta tiene que aparecer una vez minimo y sin limite.

4. Y las dificultades econtradas en el desarrollo;

   Como nos hemos divido el trabajo hemos tenido problemas en el orden de los atributos porque el compañero Sergio a realizado el archivo XML 
   y para validarlo con el archivo XSD hemos que ponernos de acuerdo con el orden para continuar.

   Tambien hemos tenido dificultades al darle un tipo de dato a lo que va a contener cada campo, ya que por ejemplo la etiqueta
   salario puede contener decimales.

5. Estructura
   
   hotel
│
├── clientes
│   ├── cliente
│   │   ├── nombre
│   │   ├── apellido
│   │   ├── genero
│   │   ├── dni
│   │   ├── numero_cuenta
│   │   ├── codigo_postal
│   │   └── ciudad
│   └── cliente 
│
├── empleados
│   ├── empleado 
│   │   ├── nombre
│   │   ├── apellido
│   │   ├── puesto
│   │   └── salario
│   └── empleado
│
└── distribuidores
    ├── distribuidor 
    │   ├── nombre
    │   ├── ciudad
    │   └── telefono
    └── distribuidor
