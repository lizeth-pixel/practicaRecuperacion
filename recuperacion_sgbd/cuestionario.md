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

#### <center><u>**CUESTIONARIO: RECUPERACIÓN DE UN SGBD**</u>

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

**1. ¿Qué datos se habrían perdido si solo hubieras usado el respaldo de la Parte A?**

Se habrían perdido los dos registros agregados después del respaldo: Pedro Nunez y Laura Vega. El respaldo inicial solamente contenía los cinco clientes originales.

**2. ¿Para qué sirve la opción "--master-data=2"?**

Sirve para guardar en el archivo de respaldo la información de la posición del binary log (binlog), incluyendo el nombre del archivo y la posición exacta desde donde se pueden reproducir los cambios posteriores al respaldo.

**3. ¿Por qué es necesario activar el binlog antes de que ocurra el error?**

Porque el binlog registra los cambios realizados en la base de datos. Si no está activado antes del incidente, no existiría un registro de las operaciones posteriores al respaldo y no sería posible recuperar esos cambios mediante este método.

**4. ¿Por qué se esperaron 5 segundos antes y después de anotar la hora?**

Para dejar una separación de tiempo entre la inserción de los nuevos registros y el borrado accidental. Esto facilita identificar las operaciones en el binlog y recuperar los datos hasta antes del error.