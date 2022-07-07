
# GymAry V1
## INTRODUCTION
GymAry is an API to manage the activity of a gym.

## Errores
Cuando ocurre un código de error en cualquier petición se recibe un json con un campo **message** que explica el error.

## REFERENCE
### Members Resource
Gestiona lo relacionado con los miembros dados de alta en el gimnasio (listar, crear, eliminar y actualizar).

#### List All Members
Muestra todos los miembros dados de alta, toda su información y las actividades a las que están apuntados y sus horarios.

#### Get member
Muestra la información del miembro con el id dado.

#### Delete member
Elimina (da de baja) el miembro con el id dado.

#### Sign up a new member
Da de alta una persona. Se debe proporcionar:
  - Nombre: Nombre del cliente.
  - Apellidos: Apellidos del cliente.
  - DNI: Documento de identidad del cliente.
  - Dirección: Se divide en tres campos: dirección, ciudad y codigo postal.
  - Contacto: Email y telefono.
  - Actividades a las que el cliente desea apuntarse (puede ser ninguna).Tarifa mensual a pagar.

#### Update member
Acutaliza la información de un miembro dado. Se puede actualizar cualquier campo excepto el id y el DNI. También se actualizan las actividades (se inscribe al miembro en ella).

### Activities Resource
Gestiona las actividades del gimnasio, añadiendo, eliminando y actualizando.

#### List all activities
Muestra todas las actividades registradas que ofrece el gimnasio.

#### Inscribe new activity
Crea una nueva actividad.
Se debe proporcionar:
  - Nombre: Nombre de la actividad.
  - Horario: Dias en las que se imparte y horas. Pueden ser varios dias y varias horas por dia.

### Workers Resource
Gestiona los trabajadores del gimnasio.

#### Get worker
Muestra la información del trabajador con el id dado.

#### Sign up a new worker
Da de alta a un nuevo trabajador.
Se debe proporcionar:
  - Nombre: Nombre del trabajador.
  - Apellidos: Apellidos del trabajador.
  - NSS: Número de seguridad social.
  - Dirección: Se divide en tres campos: calle, ciudad y código postal.
  - Contacto: Número de teléfono y email.
  - Tipo: Tipo de trabajo a realizar (P. ej.: limpiador, monitor, recepcionista, etc.).Sueldo: Sueldo mensual a recibir.

### Material Resource
Gestiona las compras de material deportivo realizadas por el gimnasio.

#### Record new material purchase
Registra una compra de material. Se pueden comprar varios productos en una misma compra.
Se debe proporcionar la siguiente información sobre cada producto comprado:
  - Nombre del producto.
  - Cantidad solicitada de material.
  - Precio por unidad en euros.

Sobre la compra total se proporciona la siguiente información:
  - Precio total de la compra en euros.
