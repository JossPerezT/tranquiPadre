---
title: "Tutorial para una sitio wweb estático con GoHugo y los submódulos de Git "
date: 2022-08-17
tags:
- gohugo
- git
- submodulos
- web
thumbnailImagePosition: left
thumbnailImage: //d1u9biwaxjngwg.cloudfront.net/tag-plugins-showcase/car-6-140.jpg
---
# Go Hugo y Submódulos de Git
En esta primera publicación tendrmeo el tutorial sobre como crear un sitio web estático usando [GoHugo](https://gohugo.io/) y los submódulos de Git, enlazando repositorios entre sí. 
  ![image](https://user-images.githubusercontent.com/84040594/185272013-31c2dba5-d3dc-4464-b98c-dfab23713b8d.png)

## Paso 1 Instalar GoHugo 
Debemos [instalar](https://gohugo.io/getting-started/installing/) GoHugo en nuestro equipo según el Sistema Operativo que manejemos 

## Paso 2 Theme
Una vez instalado GoHugo escojemos un tema que nos interese para nuestro sitio web:
[![image](https://user-images.githubusercontent.com/84040594/185272407-4257f11d-9cfb-43b9-8081-a8c16444aebd.png)](https://themes.gohugo.io/)

- En nuestro ejemplo usaremos el theme [Tranquilpeak](https://themes.gohugo.io/themes/hugo-tranquilpeak-theme/), le dmaos en *DOWNLOAND*:
  ![image](https://user-images.githubusercontent.com/84040594/185272778-b98ff457-f5ff-49a0-847b-99a05171f1b3.png)
- Ingresmaos a su código fuente en GitHub
  ![image](https://user-images.githubusercontent.com/84040594/185273268-a5de4d72-26db-4f38-bd37-79bc0aaebf8c.png)
- Creamos un fork para hacer una copia para nosotros: 
  ![image](https://user-images.githubusercontent.com/84040594/185273552-be61517f-4980-4c5b-8721-5896b6838d30.png)
  ![image](https://user-images.githubusercontent.com/84040594/185273585-509db982-8c9a-4787-a376-c2e96932a6f5.png)

## Paso 3 Creación
Creamos el sitio web en nuestro equipo: 
- Ejecutamos el comando  `hugo new site <nombreDeTuRepoPadre>`
  ![image](https://user-images.githubusercontent.com/84040594/185274281-701a071a-1c82-4b91-b72b-f80d08f29d84.png)
- Ingresamos al repositorio del blog y lo versionamos:
  ![image](https://user-images.githubusercontent.com/84040594/185274613-4b4dd773-86f3-411f-b1a5-dc33d2cecafe.png)
- Creamos un nuevo repositorio en GitHub y lo vinculamos a nuestro proyecto padre con `git remote add <link del repo>`: 
  ![image](https://user-images.githubusercontent.com/84040594/185275351-625b3f79-279c-4eb5-b3b6-c95b57df6c5c.png)
  ![image](https://user-images.githubusercontent.com/84040594/185275386-67e42bbd-1d3b-485b-b622-8de4278b2898.png)
  ![image](https://user-images.githubusercontent.com/84040594/185275997-e91a2854-bd20-471e-8a42-7c8e8e01ebbd.png)
  ![image](https://user-images.githubusercontent.com/84040594/185276093-919bf4d2-c93e-4461-b3ef-78a149927169.png)

## Paso 4 Submódulos
Enalzamos nuestro repo Padre con nuestro repo del theme con `git submodule add <link del theme> theme/<nombreDelTheme>` y lo versionamos: 
  ![image](https://user-images.githubusercontent.com/84040594/185277930-37f079f9-7be1-4b20-bcda-9361358422c8.png)
Para corroborar que nuestro submódulo se creo correctamente podemos ver el enlace del archivo `.gitmodules`
  ![image](https://user-images.githubusercontent.com/84040594/185278136-5282e45c-3e13-4475-b0a8-c7042c872af9.png)

## Paso 5 Levantar el proyecto
- En cada repositorio del theme tenemos una carpeta o rama que se llama `exampleSite`, el contenido de esa carpeta debe ser copiado en el directorio raíz de nuestro repo Padre
  ![image](https://user-images.githubusercontent.com/84040594/185278720-e508efbc-1450-4b60-bd87-59ef5cd34ecd.png)
  ![image](https://user-images.githubusercontent.com/84040594/185278865-9f7edaab-3434-45a9-8344-6d10bc1bd6fd.png)
  ![image](https://user-images.githubusercontent.com/84040594/185278968-4a1016b3-6a99-4610-aa46-341069fc4588.png)
- Versionamos los archivos copiados y modificados. 
  ![image](https://user-images.githubusercontent.com/84040594/185279351-e26f69f6-7316-40e6-a35b-8d13ebc1f7e6.png) 
- Levantemos el proyecto con `hugo server`
  ![image](https://user-images.githubusercontent.com/84040594/185280054-169dbcea-332d-4b72-be5b-68d2418ac836.png)
  ![image](https://user-images.githubusercontent.com/84040594/185280214-581fda33-3359-466a-9d83-73dc7b2eed56.png)
LISTO, hemos creado nuestro blog de GoHugo. 

## Paso 6. Despliqgue 
Desplegaremos nuestro blog en GitHub Pages para tener nuestro link disponible en línea. 
- Creamos un repo vacio en GitHub (agregar un readme.md)
  
  

















