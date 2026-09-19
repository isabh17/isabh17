<img src="https://capsule-render.vercel.app/api?type=waving&color=0:FDEEF4,50:F0B8D8,100:C98FDB&height=200&section=header&text=Isabel%20Masaya&fontSize=52&fontColor=ffffff&fontAlignY=36&desc=software%20developer%20%C2%B7%20databases%20%26%20backend&descSize=17&descAlignY=56&animation=fadeIn" width="100%">

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Quicksand&weight=600&size=22&duration=3200&pause=900&color=C98FDB&center=true&vCenter=true&width=680&height=45&lines=model+the+problem+before+writing+tables;keep+the+query+fast+six+months+from+now;put+the+logic+where+it+belongs">
</p>

<p align="center">🎀 　 ୨୧ 　 🎀</p>

<p align="center">
  <img src="https://img.shields.io/badge/📍_Guatemala-C98FDB?style=flat-square">
  <img src="https://img.shields.io/badge/GMT–6_·_overlaps_US_Central-D4A0DC?style=flat-square">
  <img src="https://img.shields.io/badge/Open_to_remote-DDA8DC?style=flat-square">
  <img src="https://img.shields.io/badge/English_C1_·_Spanish_native-E6B0D8?style=flat-square">
</p>

<br>

I build **relational databases** and the **Python backends** that consume them.

What I enjoy most is the modeling: understanding the problem properly before
creating a single table. A badly designed schema doesn't hurt on day one — it
hurts six months later, in every query that drags.

I hold a degree in Computer Science and Systems Engineering from
**Universidad de San Carlos de Guatemala**, and I've been working as a
developer professionally since 2024.

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:FDEEF4,50:F0B8D8,100:C98FDB&height=3&section=footer" width="100%">

## 🌷 &nbsp;What I work with

<table>
<tr>
<td valign="top" width="33%">

**Databases**

<img src="https://img.shields.io/badge/MySQL-C98FDB?style=flat-square&logo=mysql&logoColor=white"><br>
<img src="https://img.shields.io/badge/Oracle-D4A0DC?style=flat-square&logo=oracle&logoColor=white"><br>
<img src="https://img.shields.io/badge/PL/SQL-DDA8DC?style=flat-square&logo=oracle&logoColor=white"><br>
<img src="https://img.shields.io/badge/Schema_design-E6B0D8?style=flat-square">

</td>
<td valign="top" width="33%">

**Backend**

<img src="https://img.shields.io/badge/Python-C98FDB?style=flat-square&logo=python&logoColor=white"><br>
<img src="https://img.shields.io/badge/Flask-D4A0DC?style=flat-square&logo=flask&logoColor=white"><br>
<img src="https://img.shields.io/badge/REST_APIs-DDA8DC?style=flat-square"><br>
<img src="https://img.shields.io/badge/Git-E6B0D8?style=flat-square&logo=git&logoColor=white">

</td>
<td valign="top" width="33%">

**Frontend & more**

<img src="https://img.shields.io/badge/React-C98FDB?style=flat-square&logo=react&logoColor=white"><br>
<img src="https://img.shields.io/badge/JavaScript-D4A0DC?style=flat-square&logo=javascript&logoColor=white"><br>
<img src="https://img.shields.io/badge/TensorFlow-DDA8DC?style=flat-square&logo=tensorflow&logoColor=white"><br>
<img src="https://img.shields.io/badge/HTML_/_CSS-E6B0D8?style=flat-square&logo=html5&logoColor=white">

</td>
</tr>
</table>

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:FDEEF4,50:F0B8D8,100:C98FDB&height=3&section=footer" width="100%">

## 🗄️ &nbsp;Relational databases in Oracle

[**→ Repository**](https://github.com/isabh17/bases-de-datos-oracle)

Two systems taken from conceptual model to a working implementation. Neither is
a syntax exercise: both required deciding how to split entities, where the
constraints belong, and which logic deserves to live inside the engine.

<details>
<summary><b>🛒 &nbsp;Commerce system — 7 tables + REST API</b></summary>

<br>

**The model**

| Entity | Purpose |
|---|---|
| `cliente` · `vendedor` · `pais` | Actors and their location |
| `producto` · `categoria` | The catalog |
| `orden_de_venta` | Sales order header |
| `detalle` | Resolves the many-to-many between orders and products |

**The hard part**

Bulk loading. Data arrives in six separate CSV files and can't be inserted
directly: it lands first in a temporary staging table, then gets distributed to
the final tables respecting foreign-key order. **20,000 customer records.**

On top of that: **25 business queries** and a Flask REST API with a web
interface.

`Oracle` · `Python` · `Flask` · `SQL`

</details>

<details>
<summary><b>🏦 &nbsp;Banking system — 13 tables, stored procedures, audit trail</b></summary>

<br>

The design decision here was to put transactional logic **inside the database**
rather than in the application. If a transfer has to be atomic, the engine is
the right place to guarantee it.

**10 stored procedures**

`registrarCliente` · `registrarCuenta` · `realizarDeposito` ·
`realizarDebito` · `realizarCompra` · `asignarTransaccion` ·
`crearProductoServicio` · `registrarTipoCliente` · `registrarTipoCuenta` ·
`registrarTipoTransaccion`

**Audit triggers**

Every table carries an `_audit` trigger that logs any change to a ledger. These
aren't isolated triggers — together they form a complete trail of who touched
what and when, which is exactly what a banking system needs to be able to prove.

**Entities**

`cuenta_bancaria` · `transaccion` · `deposito` · `debito` · `compra` ·
`historial` · `producto_servicio` · `cliente` · `tipo_cliente` ·
`tipo_cuenta` · `tip_trans` · `correo` · `telefono`

`Oracle` · `PL/SQL`

</details>

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:FDEEF4,50:F0B8D8,100:C98FDB&height=3&section=footer" width="100%">

## 🌸 &nbsp;A chatbot that runs in the browser

[**→ Repository**](https://github.com/isabh17/IA1_Proyecto_17.github.io) &nbsp;·&nbsp; [**✨ Live demo**](https://isabh17.github.io/IA1_Proyecto_17.github.io/)

A neural network trained with Keras that classifies **784 distinct intents**
from **2,075 training patterns**.

<details>
<summary><b>🧠 &nbsp;How it works under the hood</b></summary>

<br>

1. **Preprocessing** — NLTK tokenizes and lemmatizes each pattern, producing the
   model's vocabulary.
2. **Representation** — every phrase becomes a bag-of-words vector.
3. **Training** — a dense Keras network learns to map that vector to one of the
   784 intents.
4. **Deployment** — and here's the interesting part: the trained model is
   converted to TensorFlow.js. **There is no server.** The browser downloads the
   weights and runs inference locally, which is why the demo works on GitHub
   Pages, a static-file host.

`TensorFlow` · `Keras` · `NLTK` · `TensorFlow.js` · `JavaScript`

</details>

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:FDEEF4,50:F0B8D8,100:C98FDB&height=3&section=footer" width="100%">

## 💌 &nbsp;Beyond the code

I did the **design and layout** of
[**Revista ECYS**](https://issuu.com/revistaecys/docs/vigesimaoctava-revistadigital),
my school's digital magazine.

I don't see that as separate from engineering. Making something readable and
well presented isn't decoration — it's the same instinct that makes a schema
worth reading.

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:FDEEF4,50:F0B8D8,100:C98FDB&height=3&section=footer" width="100%">

## ✨ &nbsp;Currently

Open to **backend** and **database-focused** roles, remote or based in
Guatemala. I work comfortably in English and Spanish.

<p align="center">
  <a href="mailto:silverisa17@gmail.com"><img src="https://img.shields.io/badge/get_in_touch-C98FDB?style=for-the-badge&logo=gmail&logoColor=white"></a>
  &nbsp;
  <a href="https://isabh17.github.io/"><img src="https://img.shields.io/badge/my_résumé-E6B0D8?style=for-the-badge&logo=readthedocs&logoColor=white"></a>
</p>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:C98FDB,50:F0B8D8,100:FDEEF4&height=110&section=footer" width="100%">
