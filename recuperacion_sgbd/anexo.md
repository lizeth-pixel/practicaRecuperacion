<div style="display: flex; justify-content: space-between; align-items: center;"><img src="imagenes/logoitt.png"><img src="imagenes/logoitt2.png"></div>

<br>
<br>
<br>
<br>

# <center>**TECNOLÓGICO NACIONAL DE MÉXICO**
## <center>**INSTITUTO TECNOLÓGICO DE MILPA ALTA II**

<br>

### <center>INGENIERIA EN SISTEMAS  COMPUTACIONALES
### <center>SEMESTRE: 5

<br>

### <center>ADMINISTRACIÓN DE BASES DE DATOS
### <center>BOLLAS PAREDES DIEGO ALBERTO

<br>

#### <center><u>**ANEXO: INVESTIGACIÓN DE TÉRMINOS Y HERRAMIENTAS DESCONOCIDAS**</u>

<br>

#### <center> MARTINEZ VELASCO LIZETH
#### <center>NO.C. 241190035

<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>

<p style="text-align: right;">26/noviembre/2026</p>

<br>
<br>
<br>

---

<br>

**1. mariadb-dump**

Herramienta de MariaDB que permite exportar bases de datos a archivos SQL. Estos archivos contienen instrucciones para reconstruir las tablas y recuperar sus datos.

**2. Restauración**

Proceso de recuperar una base de datos utilizando un respaldo previamente generado.

**3. Binary Log (Binlog)**

Registro que almacena los cambios realizados en una base de datos, como inserciones, modificaciones y eliminaciones. Permite recuperar operaciones posteriores a un respaldo.

**4. mariadb-binlog**

Herramienta que permite leer y procesar los archivos binlog para reproducir los cambios registrados en MariaDB.

**5. PITR (Point In Time Recovery)**

Significa recuperación a un punto en el tiempo. Permite restaurar una base de datos hasta un momento específico, evitando incluir operaciones incorrectas.

**6. --single-transaction**

Opción de mariadb-dump que permite realizar un respaldo consistente de las tablas InnoDB mediante una transacción, sin bloquear las operaciones normales de lectura y escritura.

**7. --master-data=2**

Opción que agrega al respaldo información sobre el archivo y la posición del binlog. Es útil para realizar recuperaciones a un punto en el tiempo.