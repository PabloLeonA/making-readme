# Action For the Ocean

Action for the ocean es un proyecto realizado para el hackathon de LaunchX que ayudara a la conservación de playas y oceanos de México. 

## Server

Se levanta el server en express en el puerto `3000` donde pasaremos las rutas por medio del routerApi creado en `./routes`.

``` javascript
const express = require("express");
const routerApi = require("./routes");
const app = express();
const port = 3000;

app.use(express.json());

app.get("/", (req , res) => {
    res.send("Hello World!");
});

routerApi(app);

app.listen(port, () => {
    console.log(`app listening on port ${port}`);
});
```
