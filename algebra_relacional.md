# algebra relacional

## seleccion

- (sigma) condicion a cumplir(tabla)

  - que hace?
  
    - selecciona de una tabla las tuplas completas que cumplan con una condicion dada

  - consultar los datos d los carros modelo 2000

    - (sigma) modelo = 2000 (carro)

  - consultar los datos de los carros renault modelo 2012

    - (sigma) marca = "renault" ^ modelo = 2012 (carro)

## proyeccion

- (pi) atributo 1, atributo 2, ..., atributo n (tabla)

  - que hace?
  
    - selecciona los valores de los atributos especificados de una tabla

  - consultar placa y marca de todos los carros

    - (pi) placa, marca (carro)

  - consultar placa y modelo de los renault

    - (pi) placa, modelo ((sigma) marca = "Renault" (carro))

## renombramiento

- (ro) nuevo nombre (tabla)

  - que hace?

    - renombra a nivel logico la tabla

  - cambiar de nombre a la tabla carro por automovil

    - (ro) automovil (carro)

## union

- Tabla 1 (U) tabla 2

  - que hace?
  
    - Reune o junta las tuplas de la tabla 1 con las de la tabla 2 en un mismo resultado

  - consultar los datos de todos los automotores

    - ((pi) placa, marca (carro)) (U) ((pi) placa, marca (bus))

## diferencia

- Tabla 1 - Tabla 2

  - que hace?

    - selecciona las tuplas que estan en tabla 1 y no estan en tabla 2

  - seleccionar los estudiantes no becados de la tabla estudiantes

    - ((pi) cedula, nombre, edad (Todos_Estud)) - ((pi) cedula, nombre, edad (Est_Becados))

## interseccion

- Tabla 1 (n) Tabla 2

  - que hace?

    - selecciona las tuplas que estan el ambas tablas

  - consultar los datos de los estudiantes que tambien sean profesores

    - ((pi) cedula, nombre (profesor)) (n) ((pi) cedula, nombre (Estudiante))
