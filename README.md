# demoFatsAPI
## Demo para practica de FastAPI

[https://fastapi.tiangolo.com/](https://fastapi.tiangolo.com/)

1. Intalar python

2. Instalar dependencias
```
$ python -m pip install "fastapi[all]"
```
3. Agregar el codigo de ejemplo en un archivo llamado test.py

```
from fastapi import FastAPI
app = FastAPI()

@app.get("/")
async def root():
    return {"message": "Hello Worlds"}


@app.get("/hola/{item_id}")
async def holaAmigo(item_id):
    return {"message": "Hola "+item_id}
```

4. Navegar al directorio donde se guardo test.py e iniciar Servidor uvicorn
```
$ python -m uvicorn test:app --reload
```
Despues de este punto ya es accesible la direccion como servicio 
[http://127.0.0.1:8000/](http://127.0.0.1:8000/)

- Al accesar debe mostrar la leyenda "Hello Worlds"

Otro ejemplo de controlador-parametro es la siguiente liga 
[http://127.0.0.1:8000/hola/Amigo](http://127.0.0.1:8000/hola/Amigo)

- Donde hola es un controlador-subdirectorio y la palabra "Amigo" es una variable de entrada, pueden cambiarla con su nombre o cualquier otra cosa y ver la salida
