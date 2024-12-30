# Proyecto Backend con Tests de Operaciones CRUD para Cafés

Este proyecto incluye un servidor backend desarrollado con Express y un conjunto de pruebas utilizando Jest y Supertest para validar las operaciones CRUD relacionadas con cafés. Las pruebas verifican el correcto funcionamiento de las rutas y las respuestas esperadas.

## Instrucciones para Ejecutar el Proyecto

### Requisitos Previos

1. Tener instalado [Node.js](https://nodejs.org/) (versión 14 o superior).
2. Clonar el repositorio y ubicarse en la carpeta `backend`:

   ```bash
   cd backend
   ```
3. Instalar las dependencias necesarias ejecutando:

   ```bash
   npm install
   ```

### Ejecución de las Pruebas

Para ejecutar las pruebas, utiliza el siguiente comando:

```bash
npm run test
```

Este comando ejecuta las pruebas definidas en el archivo `server.spec.js` y valida las rutas del servidor.

---

## Tests Implementados

### Test 1: Ruta GET `/cafes`
Verifica que la ruta devuelva un código de estado 200 y que el tipo de dato recibido sea un arreglo con al menos un objeto.

### Test 2: Eliminar un café inexistente (ruta DELETE `/cafes/:id`)
Comprueba que al intentar eliminar un café con un ID inexistente, se obtenga un código de estado 404.

### Test 3: Agregar un café (ruta POST `/cafes`)
Verifica que la ruta permita agregar un nuevo café y devuelva un código de estado 201.

### Test 4: Actualizar un café con ID no coincidente (ruta PUT `/cafes/:id`)
Prueba que la ruta devuelva un código de estado 400 si el ID en los parámetros no coincide con el ID del payload enviado.

---

## Estructura del Proyecto

```
backend/
├── cafes.json          # Archivo con datos de ejemplo de cafés
├── index.js            # Servidor principal
├── server.spec.js      # Archivo con las pruebas de Jest y Supertest
├── package.json        # Configuración del proyecto y dependencias
├── jest.config.js      # Configuración de Jest
```

---

## Tecnologías Utilizadas
- **Express:** Framework para la creación del servidor.
- **Jest:** Librería para pruebas unitarias.
- **Supertest:** Herramienta para realizar peticiones HTTP y validar respuestas.

---

