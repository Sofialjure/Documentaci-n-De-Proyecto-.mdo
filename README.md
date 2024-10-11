# Desarrollo de un Sistema de Carrito de Compra #
### **Descripción:** 
#### Generar la documentación de un Sistema de Carrito de Compras. 
------
### **Requerimientos funcionales** 
----
#### **RF01:** Registro e Inicio de Sesión.     
#### **Descripción:**  Implementar el sistema para permitir el registro de usuarios y el inicio de sesión.
### **Entrada de datos:**
- #### **Registro de usuario:**
  -	Nombre 
  - Email
  - Contraseña
  - Teléfono
  - Dirección
- #### **Inicio de sesión:**
  - Email
  - Contraseña
### **Flujo normal:**
- El usuario accede al sistema.
- El usuario selecciona "Registrarse" e ingresa sus datos: nombre, email, contraseña, teléfono y dirección.
- Si el registro es exitoso, se guarda en la base de datos y se notifica al usuario.
- El usuario puede iniciar sesión ingresando su email y contraseña.
- Si las credenciales son correctas, el sistema lo redirige a la página principal.

### **Precondición:**
- El usuario no debe estar registrado para realizar el proceso de registro. Si está registrado, puede iniciar sesión directamente.
- Disponibilidad del sistema
- Acceso internet
### **Postcondición:**
- El usuario queda registrado en la base de datos o inicia sesión con éxito en el sistema.

![Registro / Inicio Sesión](out/Diagramas/RF_Diagramasrf01/RF01.png)

#### **RF02:** Catálogo de Productos.
#### **Descripción:** Mostrar una lista de productos.
### **Entrada de datos:**
- #### **Búsqueda de productos:**
	- nombre
	- categoría
- #### **Visualización de producto:**
    - nombre
    - descripción
    - precio
    - cantidad en stock

### **Flujo normal:**
- El usuario accede al catálogo de productos.
- El sistema muestra la lista de productos con nombre, descripción, precio y cantidad en stock.
- El usuario puede buscar productos por nombre o categoría.
- Los productos buscados se muestran con los detalles correspondientes.

### **Precondición:**
-  El sistema debe tener productos registrados en la base de datos.
### **Postcondición:**
-  El usuario visualiza los productos disponibles en el sistema.

![Busqueda / visualización](out/Diagramas/RF_Diagramasrf02/RF02.png)

#### **RF03:** Agregar Productos al Carrito.

#### **Descripción:** Añadir productos al carrito especificando cantidad.

### **Entrada de datos:**

- #### **Seleccionar producto:**
  - producto
  - cantidad 

### **Flujo normal:**
- El usuario selecciona un producto desde el catálogo.
- Elige la cantidad de productos que desea agregar.
- El sistema verifica la disponibilidad de stock.
- Si hay suficiente stock, el producto es agregado al carrito.

### **Precondición:**
-  El producto debe estar disponible en stock.
### **Postcondición:**
-  El producto seleccionado se agrega al carrito del usuario.
![Seleccionar Producto](out/Diagramas/RF_Diagramasrf03/RF03.png)

#### **RF04:** Gestión del Carrito de Compras.

#### **Descripción:** Permitir visualizar y modificar el carrito.
### **Entrada de datos:**

- #### **Modificar cantidad de producto en el carrito:**
   - producto
   - nueva cantidad
- #### **Eliminar producto del carrito:**
   - Producto
### **Flujo normal:**
- El usuario accede a su carrito de compras.
- El sistema muestra los productos agregados, permitiendo modificar la cantidad o eliminar productos.
- El usuario puede modificar la cantidad de productos o eliminarlos.
- El carrito se actualiza de acuerdo con los cambios.

### **Precondición:**
- El usuario debe haber agregado productos previamente al carrito.

### **Postcondición:**
- El carrito refleja los cambios hechos por el usuario.
![Modificar / Eliminar](out/Diagramas/RF_Diagramasrf04/RF04.png)

#### **RF05:** Generación de Factura

#### **Descripción:** Al confirmar la compra, el sistema debe generar una factura con los detalles de productos, cantidades, precios e impuestos.

### **Entrada de datos:**
- #### **Confirmación de compra:**
   - productos 
   - impuestos
   - precio total
- #### **Salida de la factura:**
   - productos comprados
   - precio subtotal
   - impuestos aplicados
   - precio total

### **Flujo normal:**
- El usuario confirma su compra desde el carrito.
- El sistema genera una factura con los productos, cantidades, impuestos, precio subtotal y total.
- El usuario puede descargar o ver la factura.

### **Precondición:**
- El usuario debe haber completado el proceso de agregar productos al carrito y estar listo para confirmar la compra.

### **Postcondición:**
- Se genera una factura y se asocia a la compra del usuario.
![Confirmación / Salida Factura](out/Diagramas/RF_Diagramasrf05/RF05.png)

