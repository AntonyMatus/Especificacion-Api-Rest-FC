# Especificaciones Api Rest FC OpenBootcamp

## Controller Login

* [POST] localhost:8080/api/user/register

Este Primer metodo hace un envio POST para registrar un nuevo usuario

**Representacion ejemplo**
```
    {
        "username":"LuisMiguel",
        "email": "luis_miguel@gmail.com",
        "password": "12345"
    }
```

* [POST] localhost:8080/api/user/login

Esta peticion hace un envio de los datos los cuales seran verificados desde una funcion llamada login()

**Representación ejemplo** 

``` 
    {
        "email":"luismi@gmail.com",
        "password": "auto_verde"
    }

```

**Listado de Peticiones HTTP Candidatos**

Metodo que recupera **Todos** los candidatos registrados de la DB 

* [GET] localhost:8080/api/candidatos/all


- Metodo que hace una filtracion de los candidatos por Nombre, Email, Etiqueta, Pais, Ciudad, traslado, 

* [POST] localhost:8080/api/candidatos/{palabra_clave}



**Represenciacion ejemplo**

```
    {
        "palabra_clave": "Juan"
    }
```

- Metodo para agregar un candidato 

* [POST] localhost:8080/api/candidatos/create

```
    {
        "nombre": "Antony",
        "pais": "México",
        "ciudad": "Cozumel",
        "telefono": "889032830",
        "email": "antony@gmail.com",
        "status_transfer": true,
        "status_face_to_face": "REMOTO"
    }
```

- Metodo para optener la informacion de un candidato por ID

[POST]localhost:8080/api/candidatos/{id}
