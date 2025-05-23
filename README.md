<div align=center>

# API-REST

</div>

## **💡 Acerca de este repositorio**

Este repositorio contiene una API REST (Transferencia de Estado Representacional) utilizada para gestionar la base de datos en un contexto universitario.

Esta API fue solicitada como parte de un proyecto universitario. Puedes consultar las condiciones e instrucciones en el documento:  `Proyecto_apirest.pdf`.

Puedes clonar este repositorio para usarlo como guía si intentas crear una API de tipo REST:

```bash
git clone https://github.com/JS-Bej/API-REST.git
```

---

</br>

## **🔍 ¿Cómo funciona?**

Las APIs (Interfaz de Programación de Aplicaciones) se utilizan para habilitar la comunicación entre máquinas o software.  
Puedes encontrarlas tanto en sitios web como en aplicaciones. Por ejemplo:  
La API de **Google Maps** nos permite usar Google Maps en nuestro sitio web o aplicación.

</br>

Existen varios tipos de APIs, como **Rest, Soap, Web Socket, Webhook, etc...**. Sin embargo, nos enfocaremos en **Rest**, que es comúnmente utilizada en aplicaciones web con microservicios, como los sistemas de e-commerce. Este tipo de API se caracteriza por usar únicamente **métodos HTTP**:

- `GET`: Para obtener recursos.

- `POST`: Para crear nuevos recursos.

- `PUT`: Para actualizar recursos existentes.

- `DELETE`: Para eliminar recursos.

---

> _Esta API fue creada con TypeScript y frameworks como Node.js, Express.js, etc. Recuerda que el directorio `dist` contiene los archivos JS que TypeScript tradujo para que nuestro navegador pueda utilizarlos._

---

</br>

## **🛠️ Src**

En este directorio encontrarás:

- `models`: Define la estructura adecuada de cada entidad para que un recurso pueda almacenarse correctamente en la base de datos.

- `controllers`: Define las posibles acciones para cada entidad (_Recuerda que, como API REST, solo utilizaremos métodos HTTP_).

- `routes`: Define las rutas para acceder, agregar, actualizar y eliminar recursos para cada entidad.

---

</br>

## **⚙️ .env**

En este archivo se encuentran las credenciales que se usaran para la conexión con la base de datos.

---

</br>

## **🗂️ db.ts & app.ts 🚀**

Con `db.ts`, podemos crear la conexión a la base de datos proporcionando las credenciales necesarias para una base de datos MySQL. Por ejemplo:  
Usando *host: process.env.DB_HOST*, indicamos que el host de la base de datos se encuentra en una variable *DB_HOST* en el archivo `.env`.

> [!NOTA]  
> _El archivo *.env* está incluido en el repositorio para que puedas usar este proyecto como guía, sin embargo, en un caso profesional no debes incluir este archivo ya que se encuentran las credenciales de la base de datos._

Es importante inicializar la base de datos y conectarla a la aplicación antes de realizar cualquier solicitud. En el archivo `package.json`, encontrarás scripts que simplifican este proceso. Para establecer la conexión, ejecuta este comando en la terminal **bash** y no la cierres:

```bash
npm run dev
```