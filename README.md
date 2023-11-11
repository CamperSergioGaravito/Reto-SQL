### Bloque 1

##### Consultas

1. Listar los nombres de los usuarios

   ```sql
   # SELECT nombre FROM tblUsuarios ORDER BY nombre;
   ```

2. Calcular el saldo máximo de los usuarios de sexo “Mujer”

     ```sql
      # SELECT saldo FROM tblUsuarios WHERE sexo="M" ORDER BY saldo DESC  LIMIT 1;
     ```

3. Listar nombre y teléfono de los usuarios con teléfono NOKIA, BLACKBERRY o SONY

     ```sql
      # SELECT nombre, telefono FROM tblUsuarios WHERE marca="nokia" OR marca="blackberry" OR marca="sony";
     ```

4. Contar los usuarios sin saldo o inactivos

     ```sql
      # SELECT COUNT(*) AS RESULTADO FROM tblUsuarios WHERE saldo=0 OR activo=0;
     ```

5. Listar el login de los usuarios con nivel 1, 2 o 3

     ```sql
      # SELECT usuario, nivel FROM tblUsuarios WHERE nivel BETWEEN 1 AND 3 ORDER BY nivel ASC;
     ```

6. Listar los números de teléfono con saldo menor o igual a 300

     ```sql
      # SELECT telefono FROM tblUsuarios WHERE saldo <= 300;
     ```

7. Calcular la suma de los saldos de los usuarios de la compañia telefónica NEXTEL

     ```sql
      # SELECT SUM(saldo) FROM tblUsuarios WHERE compañia="NEXTEL";
     ```

8. Contar el número de usuarios por compañía telefónica

     ```sql
      # SELECT compañia, COUNT(telefono) AS CANTIDAD FROM tblUsuarios GROUP BY compañia ORDER BY compañia ASC;
     ```

9. Contar el número de usuarios por nivel

     ```sql
      # SELECT nivel, COUNT(usuario) AS "CANTIDAD USUARIOS" FROM tblUsuarios GROUP BY nivel ORDER BY nivel ASC;
     ```

10. Listar el login de los usuarios con nivel 2

      ```sql
       # SELECT usuario, nivel FROM tblUsuarios WHERE nivel=2 ORDER BY usuario ASC;
      ```

11. Mostrar el email de los usuarios que usan gmail

      ```sql
       # SELECT email FROM tblUsuarios WHERE email LIKE "%gmail%";
      ```

12. Listar nombre y teléfono de los usuarios con teléfono LG, SAMSUNG o MOTOROLA

      ```sql
       # SELECT nombre, telefono FROM tblUsuarios WHERE marca="LG" OR marca="SAMSUNG" OR marca="MOTOROLA";
      ```

------

### Bloque 2

##### Consultas

1. Listar nombre y teléfono de los usuarios con teléfono que no sea de la marca LG o SAMSUNG

     ```sql
      # SELECT nombre, telefono, marca FROM tblUsuarios WHERE  marca != "LG" AND marca != "SAMSUNG";
     ```

2. Listar el login y teléfono de los usuarios con compañia telefónica IUSACELL

     ```sql
      # SELECT nombre, telefono, compañia FROM tblUsuarios WHERE compañia="IUSACELL";
     ```

3. Listar el login y teléfono de los usuarios con compañia telefónica que no sea TELCEL

     ```sql
      # SELECT nombre, telefono, compañia FROM tblUsuarios WHERE compañia != "TELCEL";
     ```

4. Calcular el saldo promedio de los usuarios que tienen teléfono marca NOKIA

     ```sql
      # SELECT AVG(saldo) AS "PROMEDIO SALDO" FROM tblUsuarios WHERE marca="NOKIA";
     ```

5. Listar el login y teléfono de los usuarios con compañia telefónica IUSACELL o AXEL

     ```sql
      # SELECT usuario, telefono FROM tblUsuarios WHERE compañia="IUSACELL" OR compañia="AXEL";
     ```

6. Mostrar el email de los usuarios que no usan yahoo

     ```sql
      # SELECT email FROM tblUsuarios WHERE email NOT  LIKE "%yahoo%" ORDER BY email ASC;
     ```

7. Listar el login y teléfono de los usuarios con compañia telefónica que no sea TELCEL o IUSACELL

     ```sql
      # SELECT usuario, telefono FROM tblUsuarios WHERE compañia!="TELCEL" AND compañia!="IUSACELL" ORDER BY usuario ASC;
     ```

8. Listar el login y teléfono de los usuarios con compañia telefónica UNEFON

     ```sql
      # SELECT usuario, telefono FROM tblUsuarios WHERE compañia="UNEFON" ORDER BY usuario;
     ```

9. Listar las diferentes marcas de celular en orden alfabético descendentemente

     ```sql
      # SELECT marca FROM tblUsuarios ORDER BY marca DESC;
     ```

10. Listar las diferentes compañias en orden alfabético aleatorio

      ```sql
       # SELECT compañia FROM tblUsuarios ORDER BY RAND();
      ```

11. Listar el login de los usuarios con nivel 0 o 2

      ```sql
       # SELECT usuario, nivel FROM tblUsuarios WHERE nivel=0 OR nivel=2 ORDER BY usuario;
      ```

12. Calcular el saldo promedio de los usuarios que tienen teléfono marca LG

      ```sql
       # SELECT AVG(saldo) FROM tblUsuarios WHERE marca="LG";
      ```

------

### Bloque 3

##### Consultas

1. Listar el login de los usuarios con nivel 1 o 3

     ```sql
      # SELECT usuario FROM tblUsuarios WHERE nivel=1 OR nivel=3 ORDER BY usuario;
     ```

2. Listar nombre y teléfono de los usuarios con teléfono que no sea de la marca BLACKBERRY

     ```sql
      # SELECT nombre, telefono FROM tblUsuarios WHERE marca!="BLACKBERRY" ORDER BY nombre;
     ```

3. Listar el login de los usuarios con nivel 3

     ```sql
      # SELECT usuario FROM tblUsuarios WHERE nivel=3 ORDER BY usuario;
     ```

4. Listar el login de los usuarios con nivel 0

     ```sql
      # SELECT usuario FROM tblUsuarios WHERE nivel=0 ORDER BY usuario;
     ```

5. Listar el login de los usuarios con nivel 1

     ```sql
      # SELECT usuario FROM tblUsuarios WHERE nivel=1 ORDER BY usuario;
     ```

6. Contar el número de usuarios por sexo

     ```sql
      # SELECT sexo, COUNT(sexo) AS cantidad FROM tblUsuarios GROUP BY sexo ORDER BY sexo ASC;
     ```

7. Listar el login y teléfono de los usuarios con compañia telefónica AT&T

     ```sql
      # SELECT usuario, telefono FROM tblUsuarios WHERE compañia="AT&T" ORDER BY usuario;
     ```

8. Listar las diferentes compañias en orden alfabético descendentemente

     ```sql
      # SELECT compañia FROM tblUsuarios ORDER BY compañia DESC;
     ```

9. Listar el logn de los usuarios inactivos

     ```sql
      # SELECT usuario FROM tblUsuarios WHERE activo=0 ORDER BY usuario;
     ```

10. Listar los números de teléfono sin saldo

      ```sql
       # SELECT telefono FROM tblUsuarios WHERE saldo=0 ORDER BY telefono ASC;
      ```

11. Calcular el saldo mínimo de los usuarios de sexo “Hombre”

      ```sql
       # SELECT MIN(saldo) AS "Saldo Min" FROM tblUsuarios  WHERE sexo="H" AND saldo!=0;
      ```

12. Listar los números de teléfono con saldo mayor a 300

      ```sql
       # SELECT telefono FROM tblUsuarios WHERE saldo > 300 ORDER BY telefono;
      ```

------

### Bloque 4

##### Consultas

1. Contar el número de usuarios por marca de teléfono

     ```sql
      # SELECT marca, COUNT(usuario) AS "Cant usuarios" FROM tblUsuarios GROUP BY marca ORDER BY marca ASC;
     ```

2. Listar nombre y teléfono de los usuarios con teléfono que no sea de la marca LG

     ```sql
      # SELECT nombre, telefono, marca FROM tblUsuarios WHERE marca!="LG" ORDER BY nombre;
     ```

3. Listar las diferentes compañias en orden alfabético ascendentemente

     ```sql
      # SELECT compañia FROM tblUsuarios ORDER BY compañia  ASC;
     ```

4. Calcular la suma de los saldos de los usuarios de la compañia telefónica UNEFON

     ```sql
      # SELECT compañia, SUM(saldo) AS "Total saldo" FROM tblUsuarios GROUP BY compañia HAVING compañia="UNEFON";
     ```

5. Mostrar el email de los usuarios que usan hotmail

     ```sql
      # SELECT email FROM tblUsuarios WHERE email LIKE "%hotmail%" ORDER BY email ASC;
     ```

6. Listar los nombres de los usuarios sin saldo o inactivos

     ```sql
      # SELECT nombre FROM tblUsuarios WHERE saldo=0 OR activo=0 ORDER BY nombre;
     ```

7. Listar el login y teléfono de los usuarios con compañia telefónicaIUSACELL o TELCEL

     ```sql
      # SELECT usuario, telefono FROM tblUsuarios WHERE compañia="IUSACELL" OR compañia="TELCEL" ORDER BY usuario ASC;
     ```

8. Listar las diferentes marcas de celular en orden alfabético ascendentemente

     ```sql
      # SELECT marca FROM tblUsuarios ORDER BY marca ASC;
     ```

9. Listar las diferentes marcas de celular en orden alfabético aleatorio

     ```sql
      # SELECT marca FROM tblUsuarios GROUP BY marca ORDER BY RAND();
     ```

10. Listar el login y teléfono de los usuarios con compañia telefónica IUSACELL o UNEFON

      ```sql
       # SELECT usuario, telefono FROM tblUsuarios WHERE compañia="IUSACELL" OR compañia="UNEFON" ORDER BY usuario ASC;
      ```

11. Listar nombre y teléfono de los usuarios con teléfono que no sea de la marca MOTOROLA o NOKIA

      ```sql
       # SELECT nombre, telefono FROM tblUsuarios WHERE marca!="MOTOROLA" AND marca!="NOKIA" ORDER BY nombre;
      ```

12. Calcular la suma de los saldos de los usuarios de la compañia telefónica TELCEL

      ```sql
       # SELECT compañia, SUM(saldo) AS "Saldo total" FROM tblUsuarios WHERE compañia="TELCEL";
      ```
