# Diccionario de Datos #

## Tabla del proveedor ##

| **Atributos**            |             **Tipo de datos** | **Descripción** |
|:-------------------------|:------------------------------|:----------------|
|id\_proveedor	            | int(5)                        |	Este atributo es la llave primaria del id del proveedor y su tipo es int |
|nombre\_empresa\_proveedor | varchar(60)                   | Nombre de la empresa de donde proviene el proveedor y su tipo es de varchar |
| direccion\_empresa       |	varchar(60)                   |	Este atributo es la direccion de la empresa y es por eso su tipo de varchar |
| nombre\_proveedor        |	varchar(60)                   | Nombre del proveedor y su tipo es varchar|
|tel\_empresa\_proveedor	  | varchar(10)                   |	Num del telefono de la empresa del proveedor y su tipo es varchar(10) |
| tel\_cel\_proveedor      |	varchar(13)                   | Num del celular del proveedor y el tipo es de varchar(13) los digitos del cel |

## Tabla de la clasificación de los artículos ##

|Atributos|	Tipo de datos|	Descripción|
|:--------|:-------------|:-----------|
|id\_clasificacion|	int(5)	      | Este atributo sera la llave primaria de la tabla y su tipo de datos es int|
|nombre\_clasificacion|	varchar(30)  |	Este atributo es el nombre de las clasificaciones de los articulos y su tipo varchar|


## Tabla de artículos ##


|Atributos|	Tipo de datos|	Descripción|
|:--------|:-------------|:-----------|
|id\_articulo|	int(10)      |	Este atributo es la llave primaria de la tabla "ARTICULOS" y su tipo es int|
|id\_proveedor2|	int(5)	      |Este atributo es la llave foranea  de la tabla "PROVEEDOR" y su tipo es int|
|id\_clasificacion2|	int(5)       |	Este atributo es la llave foranea de la tabla "CLASIFICACION" y su tipo es int|
|codigo\_articulo|	varchar(20)  |	Código de los articulos de identificacion unica  y su tipo es varchar|
|descripcion\_articulo|	varchar(50)  |	Descripción de los articulos y su tipo es varchar|
|presentacion\_articulo|	varchar(40)  |	Presentación(tamaño) del articulo y su tipo es varchar |
|medida   |	varchar(10)  |	Medidad de los articulos y su  tipo es varchar|
|precio\_articulo\_prov|	double(4,2)  |	Precio de los articulos de los proveedores y su tipo es double|
|precio\_articulo\_pub|	double(4,2)  |	Precio de los articulos a vender al publico en general y su tipo es double|
|existencia\_minima|	varchar(3)   |	Existencia minima de los articulos en inventario y su tipo es varchar|
|fecha\_caducidad\_articulo|	date         |	Fecha de caducidad del articulo y su tipo es date|
|fecha\_registro|	date	        |Fecha de registro del producto y su tipo es date|

## Tabla de nota\_venta ##


|Atributos	|Tipo de datos|	Descripción|
|:---------|:------------|:-----------|
|id\_nota	 |int(20)      |	Llave primaria de la tabla de "NOTA\_VENTA" y su tipo es int|
|id\_articulo2|	int(10)     |	llave foranea de la tabla de "ARTICULO" y su tipo es int|
|folio\_nota|	int(20)     |	folio de las notas expedida y su tipo es int|
|nota\_total|	double(4,2) |	Este atributo es el total a pagar en la compra y su tipo es double|
|nota\_pago\_con	|double(4,2)  |	Este atributo es la cantidad con la que pago el cliente y su tipo es double|
|nota\_cambio|	double(4,2) |	Este atributo es la cantidad a regresar al cliente y su tipo es double|

## Tabla de inventario ##

|Atributos	|Tipo de datos|	Descripción|
|:---------|:------------|:-----------|
|id\_inventario|	int(40)     |	llave primaria de la tabla "NOTA\_VENTA" y su tipo es int |
|id\_articulo3 int not null|	int(10)	    |llave foranea de la tabla "ARTICULO"  y su tipo es int|
|fecha\_inventario|	date	       |fecha del inventario de creación y su tipo es date|
|entrada\_producto	|varchar(4)   |	entrada de los articulos a inventario y su tipo es varchar|
|salida\_producto	|varchar(4)   |	salida de los articulos de inventario y su tipo es varchar|
|saldo\_producto|	double(5,2) |	saldo total de los articulos que se obtienen en inventario y su tipo es double|

## Tabla de corte\_caja ##


|Atributos|	Tipo de datos|	Descripción|
|:--------|:-------------|:-----------|
|id\_corte|	int(10)      |	llave primaria de la tabla "CORTE\_CAJA" y su tipo es int|
|fecha\_corte|	date         |	fecha del corte de caja que se realiza al dia y su tipo es date|
|inicio\_corte|	double(4,2)  |	ingresos que obtiene el sistema al inicio y su tipo es double|
|final\_corte|	double(4,2)  |	Cantidad que se vendio en el dia y su tipo es double|
|ganancia\_corte|	double(4,2)  |	ganancia que hubo en el dia de la venta y su tipo es double|