### Tareas Parametrizadas

Permiten lanzar una ejecución pasando uno o varios parámetros.

Estos parámetros están disponibles durante la ejecución de la tarea como **variables de entorno**.

^^^^^^

#### Tareas Parametrizadas

En la sección "General" de la configuración de la tarea, seleccionamos la opción "Esta ejecución debe parametrizarse".

![parameterized builds](/slides/images/parameterized_build_1.png)<!-- .element: class="plain" -->


^^^^^^

#### Tareas Parametrizadas

Seleccionamos el tipo de parámetro y rellenamos los valores que ese parámetro necesita.

![parameterized builds](/slides/images/parameterized_build_2.png)<!-- .element: class="plain" -->


^^^^^^

#### Tareas Parametrizadas

Cuando lancemos la ejecución manualmente, debemos rellenar los parámetros.

![parameterized builds](/slides/images/parameterized_build_3.png)<!-- .element: class="plain" -->


^^^^^^

#### Tareas Parametrizadas

* Los plugins pueden definir sus propios tipos de parámetros
* Cuando se utiliza un disparador de ejecución **no es posible pasar parámetros** 
  (se usa el valor por defecto)
* Si se usa una URL como disparador, es posible pasar los parámetros por URL

```
http://server/job/myjob/buildWithParameters?PARAMETER=Value
```

notes:

Algunos de los disparadores que no permiten el uso de parámetros son SCM polling, downstream builds y ejecuciones programadas.
En estos casos se utilizará el valor por defecto definido al configurar el parámetro.

Los parámetros que se pasan por URL diferencian mayúsculas de minúsculas por lo que no 
es lo mismo

```
http://server/job/myjob/buildWithParameters?PARAMETER=Value
```

que

```
http://server/job/myjob/buildWithParameters?Parameter=Value
```
