<img src="https://capsule-render.vercel.app/api?type=waving&color=0:FDEEF4,50:F0B8D8,100:C98FDB&height=200&section=header&text=Isabel%20Masaya&fontSize=52&fontColor=ffffff&fontAlignY=36&desc=desarrolladora%20%C2%B7%20bases%20de%20datos%20%C2%B7%20guatemala&descSize=17&descAlignY=56&animation=fadeIn" width="100%">

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Quicksand&weight=600&size=22&duration=3200&pause=900&color=C98FDB&center=true&vCenter=true&width=620&height=45&lines=modelar+antes+de+escribir+tablas;que+la+consulta+siga+r%C3%A1pida+en+seis+meses;que+la+l%C3%B3gica+viva+donde+debe+vivir">
</p>

<p align="center">🎀 　 ୨୧ 　 🎀</p>

<br>

Trabajo sobre todo con **Python** y **bases de datos relacionales**.

Lo que más me gusta es la parte de modelar: entender bien el problema antes de
empezar a crear tablas. Un esquema mal pensado no se nota el primer día, se
nota seis meses después en cada consulta que se arrastra.

Estudié Ingeniería en Ciencias y Sistemas en la Universidad de San Carlos.

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:FDEEF4,50:F0B8D8,100:C98FDB&height=3&section=footer" width="100%">

## 🌷 &nbsp;Con qué trabajo

<table>
<tr>
<td valign="top" width="33%">

**Bases de datos**

<img src="https://img.shields.io/badge/MySQL-C98FDB?style=flat-square&logo=mysql&logoColor=white"><br>
<img src="https://img.shields.io/badge/Oracle-D4A0DC?style=flat-square&logo=oracle&logoColor=white"><br>
<img src="https://img.shields.io/badge/PL/SQL-DDA8DC?style=flat-square&logo=oracle&logoColor=white"><br>
<img src="https://img.shields.io/badge/PostgreSQL-E6B0D8?style=flat-square&logo=postgresql&logoColor=white">

</td>
<td valign="top" width="33%">

**Backend**

<img src="https://img.shields.io/badge/Python-C98FDB?style=flat-square&logo=python&logoColor=white"><br>
<img src="https://img.shields.io/badge/Flask-D4A0DC?style=flat-square&logo=flask&logoColor=white"><br>
<img src="https://img.shields.io/badge/REST_API-DDA8DC?style=flat-square&logo=fastapi&logoColor=white"><br>
<img src="https://img.shields.io/badge/Git-E6B0D8?style=flat-square&logo=git&logoColor=white">

</td>
<td valign="top" width="33%">

**También he usado**

<img src="https://img.shields.io/badge/TensorFlow-C98FDB?style=flat-square&logo=tensorflow&logoColor=white"><br>
<img src="https://img.shields.io/badge/JavaScript-D4A0DC?style=flat-square&logo=javascript&logoColor=black"><br>
<img src="https://img.shields.io/badge/Go-DDA8DC?style=flat-square&logo=go&logoColor=white"><br>
<img src="https://img.shields.io/badge/C++-E6B0D8?style=flat-square&logo=cplusplus&logoColor=white">

</td>
</tr>
</table>

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:FDEEF4,50:F0B8D8,100:C98FDB&height=3&section=footer" width="100%">

## 🗄️ &nbsp;Bases de datos en Oracle

[**→ Ver el repositorio**](https://github.com/isabh17/bases-de-datos-oracle)

Dos sistemas llevados desde el modelo conceptual hasta la implementación
funcionando. No son ejercicios de sintaxis: en los dos hubo que decidir cómo
partir las entidades, dónde poner las restricciones y qué lógica merecía vivir
dentro del motor.

<details>
<summary><b>🛒 &nbsp;Sistema de comercio — 7 tablas + API REST</b></summary>

<br>

Base de datos para un comercio de productos, con una API que la consume.

**El modelo**

| Entidad | Para qué |
|---|---|
| `cliente` · `vendedor` · `pais` | Los actores y su ubicación |
| `producto` · `categoria` | El catálogo |
| `orden_de_venta` | La cabecera de cada venta |
| `detalle` | Resuelve el muchos-a-muchos entre órdenes y productos |

**Lo que tuvo trabajo**

La carga masiva. Los datos llegan en seis CSV distintos y no se pueden insertar
directo: van primero a una tabla temporal de *staging*, y de ahí se reparten a
las tablas finales respetando el orden de las claves foráneas. Son 20 000
clientes.

Encima hay **25 consultas de negocio** y una API en Flask con interfaz web.

`Oracle` · `Python` · `Flask` · `SQL`

</details>

<details>
<summary><b>🏦 &nbsp;Sistema bancario — 13 tablas, procedimientos y auditoría</b></summary>

<br>

Aquí la decisión de diseño fue meter la lógica de las transacciones **dentro de
la base de datos**, no en la aplicación. Si una transferencia tiene que ser
atómica, el mejor lugar para garantizarlo es el motor.

**10 procedimientos almacenados**

`registrarCliente` · `registrarCuenta` · `realizarDeposito` ·
`realizarDebito` · `realizarCompra` · `asignarTransaccion` ·
`crearProductoServicio` · `registrarTipoCliente` · `registrarTipoCuenta` ·
`registrarTipoTransaccion`

**Triggers de auditoría**

Cada tabla tiene su trigger `_audit`, que registra en una bitácora cualquier
cambio sobre los datos. No son triggers sueltos: es un rastro completo de quién
tocó qué y cuándo, que es justo lo que un sistema bancario necesita poder
demostrar.

**Entidades**

`cuenta_bancaria` · `transaccion` · `deposito` · `debito` · `compra` ·
`historial` · `producto_servicio` · `cliente` · `tipo_cliente` ·
`tipo_cuenta` · `tip_trans` · `correo` · `telefono`

`Oracle` · `PL/SQL`

</details>

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:FDEEF4,50:F0B8D8,100:C98FDB&height=3&section=footer" width="100%">

## 🌸 &nbsp;Un chatbot que corre en el navegador

[**→ Ver el repositorio**](https://github.com/isabh17/IA1_Proyecto_17.github.io) &nbsp;·&nbsp; [**✨ Probar la demo**](https://isabh17.github.io/IA1_Proyecto_17.github.io/)

Una red neuronal entrenada con Keras que clasifica **784 intenciones**
distintas a partir de **2 075 patrones** de entrenamiento.

<details>
<summary><b>🧠 &nbsp;Cómo funciona por dentro</b></summary>

<br>

1. **Preprocesamiento** — NLTK tokeniza y lematiza cada patrón, y de ahí sale
   el vocabulario del modelo.
2. **Representación** — cada frase se convierte en un vector *bag-of-words*.
3. **Entrenamiento** — una red densa en Keras aprende a mapear ese vector a una
   de las 784 intenciones.
4. **Despliegue** — y aquí está lo interesante: el modelo entrenado se convierte
   a TensorFlow.js. **No hay servidor detrás.** El navegador descarga los pesos
   y hace la inferencia localmente, así que la demo funciona en GitHub Pages,
   que solo sirve archivos estáticos.

`TensorFlow` · `Keras` · `NLTK` · `TensorFlow.js` · `JavaScript`

</details>

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:FDEEF4,50:F0B8D8,100:C98FDB&height=3&section=footer" width="100%">

## 💌 &nbsp;Fuera del código

Hice el **diseño y la maquetación** de la
[**Revista ECYS**](https://issuu.com/revistaecys/docs/vigesimaoctava-revistadigital),
la revista digital de la Escuela de Ciencias y Sistemas.

Esa parte también me gusta, y no la veo separada de la otra: que algo se lea
bien y se vea bien no es un adorno.

<br>

<p align="center">
  <a href="mailto:silverisa17@gmail.com"><img src="https://img.shields.io/badge/escríbeme-C98FDB?style=for-the-badge&logo=gmail&logoColor=white"></a>
  &nbsp;
  <a href="https://isabh17.github.io/"><img src="https://img.shields.io/badge/mi_currículum-E6B0D8?style=for-the-badge&logo=readthedocs&logoColor=white"></a>
</p>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:C98FDB,50:F0B8D8,100:FDEEF4&height=110&section=footer" width="100%">
