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

#### <center><u>**CUESTIONARIO: MIGRACIÓN DE BASES DE DATOS EN MARIADB**</u>

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

**1. ¿Por qué se hace un respaldo antes de migrar?**

Se realiza un respaldo para proteger la información original de la base de datos. Si ocurre algún error durante la migración, podemos recuperar los datos mediante la copia de seguridad y evitar perder información importante.

**2. ¿Para qué sirve la opción `--single-transaction`?**

Sirve para realizar una copia consistente de las tablas transaccionales, como las que utilizan InnoDB, mediante una sola transacción. Esto permite obtener los datos sin bloquear normalmente las operaciones de lectura y escritura durante el respaldo.

**3. ¿Qué diferencia hay entre exportar con y sin `--databases`?**

Cuando utilizamos `--databases`, el archivo SQL incluye instrucciones para crear y seleccionar la base de datos original.

Cuando no utilizamos esta opción, se exporta el contenido de la base de datos sin incluir esas instrucciones, lo que permite importarlo en otra base de datos previamente creada con un nombre diferente.

**4. ¿Qué dos pruebas permiten confirmar que los datos migraron sin pérdidas?**

Las dos pruebas principales son:

**1.** Comparación de registros: utilizar **`"SELECT COUNT(*)"`** para comprobar que la cantidad de registros de las tablas sea igual en el origen y en el destino.
**2.** Comparación de checksum: utilizar **`"CHECKSUM TABLE"`** para comparar los valores de comprobación de las tablas y verificar que coincidan.

**5. Si el destino estuviera en otro servidor, ¿qué paso adicional sería necesario?**

Sería necesario transferir el archivo SQL al servidor de destino mediante una herramienta de transferencia segura, como **"scp"**. Después, se tendría que importar el archivo en **`MariaDB`** del servidor destino, asegurándose de tener conectividad y permisos suficientes.

---