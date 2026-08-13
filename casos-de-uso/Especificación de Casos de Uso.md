# Especificación de Casos de Uso

## 1. Introducción y Propósito

Este documento establece la versión final consolidada y afinada a partir de la Especificación de Casos de Uso. Se ha organizado e integrado de manera coherente con el Documento de Especificación de Requisitos del Software (SRS), funcionando como la línea base operativa y funcional que enlaza los requisitos de negocio con la arquitectura técnica y operativa del sistema.

Este entregable sirve como insumo de entrada directo para las siguientes fases del ciclo de vida del software:
* **Planificación y Gestión de Proyecto:** Permite la estimación de esfuerzo, la descomposición de tareas y la asignación de Historias de Usuario dentro de los Sprints de desarrollo.
* **Desarrollo y Arquitectura de Software:** Proporciona el flujo paso a paso, las reglas de negocio y los puntos de integración necesarios para la construcción de módulos y servicios backend/frontend.
* **Aseguramiento y Control de Calidad (QA):** Establece los criterios formales de aceptación, precondiciones y poscondiciones indispensables para el diseño de casos de prueba unitarios, de integración y de aceptación de usuario.

---

## 2. Matriz de Trazabilidad

### M-01 Seguridad y Perfiles

| CU | Nombre del Caso de Uso | Regla(s) de Negocio | RF asociado | RNF relevante(s) |
| :--- | :--- | :--- | :--- | :--- |
| **M01-CU1** | Presentar interfaz de inicio pública | RN-04 | | RNF26, RNF18, RNF19 |
| **M01-CU2** | Iniciar sesión (Generación de Token JWT) | RN-14 | RF3, RF2 | RNF9 |
| **M01-CU3** | Visualizar panel de control principal | RN-02 | RF2 | RNF33 |
| **M01-CU3.1** | Validar permisos y restricciones según el rol asignado | RN-02, RN-03, RN-14 | RF2 | RNF7 |
| **M01-CU4** | Cerrar sesión de usuario de forma segura | RN-02 | RF3 | RNF8 |
| **M01-CU5** | Gestionar recuperación de credenciales por correo | RN-04 | RF1 | RNF10 |

---

### M02 Inventario y Disponibilidad

| CU | Nombre del Caso de Uso | Regla(s) de Negocio | RF asociado | RNF relevante(s) |
| :--- | :--- | :--- | :--- | :--- |
| **M02-CU1** | Consultar calendario interactivo de disponibilidad global | RN-03, RN-07, RN-16 | RF6 | RNF29 |
| **M02-CU1.1** | Validar restricción técnica de fechas bloqueadas o pasadas | RN-06, RN-16 | RF6 | RNF5 |
| **M02-CU2** | Modificar estado físico de los inflables (Disponible/Mantenimiento) | RN-01, RN-03 | RF5 | RNF4 |
| **M02-CU3** | Consultar stock de insumos críticos en bodega | RN-03, RN-16 | RF5 | RNF30 |

---

### M03 Lógica de Costos y Logística

| CU | Nombre del Caso de Uso | Regla(s) de Negocio | RF asociado | RNF relevante(s) |
| :--- | :--- | :--- | :--- | :--- |
| **M03-CU1** | Calcular costo del evento | RN-01, RN-08 | RF11 | RNF13, RNF20 |
| **M03-CU2** | Calcular transporte | RN-07 | RF12 | RNF13 |
| **M03-CU3** | Generar presupuesto | RN-11 | RF11 | RNF6 |
| **M03-CU3.1** | Calcular costo del evento (subproceso) | RN-09 | RF11 | RNF13 |
| **M03-CU4** | Aplicar descuentos | RN-11 | | RNF20 |
| **M03-CU4.1** | Validar promociones y descuentos | RN-07, RN-09 | | RNF6 |
| **M03-CU5** | Estimar recursos necesarios | RN-10 | RF13 | RNF29 |

---

### M04 Inteligencia Artificial

| CU | Nombre del Caso de Uso | Regla(s) de Negocio | RF asociado | RNF relevante(s) |
| :--- | :--- | :--- | :--- | :--- |
| **M04-CU1** | Solicitar recomendación de servicio | RN-13 | RF9 | RNF11 |
| **M04-CU2** | Generar cotización automática | RN-13 | RF9, RF11 | RNF20 |
| **M04-CU2.1** | Calcular costos | RN-09, RN-17 | RF11 | RNF13 |
| **M04-CU3** | Analizar disponibilidad | RN-08, RN-10 | RF6, RF27 | RNF29 |
| **M04-CU4** | Generar sugerencias de paquetes | RN-07 | RF9 | RNF11 |
| **M04-CU4.1** | Analizar preferencias del cliente | RN-09 | RF9, RF22 | RNF11 |
| **M04-CU5** | Predecir necesidades logísticas | RN-07 | RF10 | RNF15 |

---

### M05 Administración y Documentos

| CU | Nombre del Caso de Uso | Regla(s) de Negocio | RF asociado | RNF relevante(s) |
| :--- | :--- | :--- | :--- | :--- |
| **M05-CU1** | Generar contrato | RN-04, RN-07 | RF14 | RNF4 |
| **M05-CU1.1** | Validar información del evento | RN-09, RN-13 | RF14 | RNF4 |
| **M05-CU2** | Consultar contrato | RN-02, RN-03, RN-07 | RF14 | RNF7 |
| **M05-CU2.1** | Buscar documento | RN-01, RN-09 | RF16 | RNF29 |
| **M05-CU3** | Descargar documento | RN-03 | RF14 | RNF7 |
| **M05-CU4** | Actualizar documento | RN-11, RN18 | RF14 | RNF33 |
| **M05-CU5** | Archivar documento | RN-11 | | RNF30 |

---

### M06 Gestión Financiera y Anticipos

| CU | Nombre del Caso de Uso | Regla(s) de Negocio | RF asociado | RNF relevante(s) |
| :--- | :--- | :--- | :--- | :--- |
| **M06-CU1** | Registrar anticipo | RN-02, RN-04 | RF17 | RNF22 |
| **M06-CU2** | Registrar pago | RN-02 | RF17 | RNF22 |
| **M06-CU2.1** | Validar pago | RN-04, RN-09 | RF18 | RNF24 |
| **M06-CU3** | Consultar saldo pendiente | RN-02, RN-07 | RF18 | RNF20 |
| **M06-CU4** | Generar reporte financiero | RN-02, RN-07 | RF19 | RNF20 |
| **M06-CU4.1** | Consolidar ingresos | RN-09, RN-17 | RF19 | RNF20 |

---

### M07 CRM y Fidelización

| CU | Nombre del Caso de Uso | Regla(s) de Negocio | RF asociado | RNF relevante(s) |
| :--- | :--- | :--- | :--- | :--- |
| **M07-CU1** | Registrar cliente | RN-01, RN-04, RN-05 | RF1 | RNF10 |
| **M07-CU2** | Consultar historial de eventos | RN-02 | RF21 | RNF7 |
| **M07-CU3** | Gestionar promociones | RN-02, RN-03 | | RNF6 |
| **M07-CU4** | Asignar beneficios | RN-07 | | RNF6 |
| **M07-CU4.1** | Verificar historial de compras | RN-01, RN-16 | RF21 | RNF17 |
| **M07-CU5** | Enviar campañas | RN-04 | | RNF31 |
| **M07-CU5.1** | Seleccionar clientes objetivo | RN-07, RN-09 | RF20 | RNF29 |

---

### M08 Notificaciones y Respuesta Inmediata

| CU | Nombre del Caso de Uso | Regla(s) de Negocio | RF asociado | RNF relevante(s) |
| :--- | :--- | :--- | :--- | :--- |
| **M08-CU1** | Enviar notificación | RN-04 | RF23 | RNF34 |
| **M08-CU2** | Recibir alerta | RN-02, RN-04 | RF23 | RNF34 |
| **M08-CU3** | Confirmar reserva | RN-11 | RF24 | RNF5 |
| **M08-CU3.1** | Enviar notificación (subproceso) | RN-09 | RF23 | RNF34 |
| **M08-CU4** | Recordar evento próximo | RN-16 | RF25 | RNF12 |
| **M08-CU4.1** | Consultar calendario | RN-07, RN-09 | RF6 | RNF29 |
| **M08-CU5** | Responder consulta automática | RN-13 | RF24, RF8 | RNF11 |

---

### M09 Digitalización de Operaciones (Paperless)

| CU | Nombre del Caso de Uso | Regla(s) de Negocio | RF asociado | RNF relevante(s) |
| :--- | :--- | :--- | :--- | :--- |
| **M09-CU1** | Registrar asistencia digital | RN-02, RN-06 | RF26 | RNF32 |
| **M09-CU2** | Adjuntar evidencia fotográfica | RN-03, RN-04, RN-05 | RF26 | RNF24 |
| **M09-CU3** | Firmar documento digitalmente | RN-20 | | RNF23 |
| **M09-CU4** | Generar acta digital | RN-07 | RF28 | RNF31 |
| **M09-CU4.1** | Registrar asistencia (subproceso) | RN-07, RN-09 | RF26 | RNF32 |
| **M09-CU4.2** | Adjuntar evidencia (subproceso) | RN-07, RN-09 | RF26 | RNF24 |
| **M09-CU5** | Consultar historial de operaciones | RN-07 | RF27 | RNF29 |

---

### M10 Administración Avanzada y Ajustes

| CU | Nombre del Caso de Uso | Regla(s) de Negocio | RF asociado | RNF relevante(s) |
| :--- | :--- | :--- | :--- | :--- |
| **M10-CU1** | Gestionar usuarios | RN-02, RN-03 | | RNF33 |
| **M10-CU1.1** | Crear usuario | RN-09, RN-19 | | RNF33 |
| **M10-CU1.2** | Modificar usuario | RN-09, RN-12 | | RNF33 |
| **M10-CU1.3** | Eliminar usuario | RN-09, RN-12 | | RNF33 |
| **M10-CU2** | Gestionar roles | RN-02, RN-03 | | RNF7 |
| **M10-CU2.1** | Asignar permisos | RN-03, RN-09 | | RNF7 |
| **M10-CU3** | Configurar parámetros del sistema | RN-02, RN-03 | RF29 | RNF33 |
| **M10-CU4** | Realizar copias de seguridad | RN-15, RN-16 | | RNF21 |
| **M10-CU5** | Restaurar respaldo | RN-15 | | RNF21, RNF35 |
| **M10-CU6** | Consultar auditoría | RN-03, RN-07 | RF31, RF4 | RNF17 |

---

## 3. Informe de Impacto del Refinamiento en el Desarrollo

### Impacto en el diseño
La matriz obliga a decidir, antes de modelar clases y diagramas de secuencia, si los 16 CU sin RF propio son parte del alcance formal del sistema o si requiere ampliar la ERS. En particular, el bloque de gestión de usuarios/roles de M10 (6 CU) representa un módulo de administración que el diagrama de clases debe reflejar como una entidad propia (Usuario, Rol, Permiso), aunque hoy no tenga un RF que lo respalde formalmente — de lo contrario el diseño quedaría desalineado con los requisitos documentados y sería difícil de justificar en la sustentación.

### Impacto en la programación
Las reglas de negocio centralizadas (RN-01 a RN-20) ahora funcionan como el contrato entre RF y CU: cada historia de usuario que se derive de un CU debe implementar las validaciones de su(s) RN asociada(s) como criterios de aceptación, y no como lógica dispersa. Esto reduce el riesgo de que dos desarrolladores implementen la misma validación (p. ej. pérdida de conexión a BD, RN-01) con criterios distintos, y facilita separar el backlog por RF con trazabilidad directa a los RN que debe cumplir cada endpoint.

### Impacto en las pruebas (QA)
La matriz se convierte en la base del plan de pruebas: cada RN mapeada a un CU es, como mínimo, un caso de prueba de validación de regla de negocio (caso negativo) más el flujo normal del CU (caso positivo). Los RF sin cobertura (RF7, RF15, RF30) deben marcarse como "pendientes de definición" en el plan de pruebas hasta que el equipo decida si se implementan en el alcance actual o se mueven a un backlog futuro, evitando que QA intente validar funcionalidad que no tiene CU ni criterios de aceptación definidos.

---

## 4. Próximos Pasos

* **Alineación con PO:** Decidir con el Product Owner si se amplía la ERS con un RF de administración de usuarios/roles o si se reclasifican esos 6 CU bajo RF2.
* **Definición de Alcance:** Definir si RF7, RF15 y RF30 entran al alcance del proyecto formativo o quedan como trabajo futuro documentado.
* **Fase 4 e Historias de Usuario:** Usar esta matriz como insumo directo para la Fase 4 (validación con stakeholder) y para la definición de historias de usuario.

* ## Módulo 1 - Seguridad y perfiles

### CU1: Presentar interfaz de inicio pública

* **Autores:** Luna Amézquita, Arantxa Leal, Alejandro Muñoz, Nicolas Giraldo
* **Descripción:** Hace referencia a la carga y visualización de la página principal pública del sitio web de Elmo Recreaciones. Esta interfaz es el primer punto de contacto de cualquier visitante con la plataforma; presenta la identidad visual de la empresa, los servicios destacados (shows recreativos, decoraciones temáticas, paquetes de eventos e inflables), y las opciones de navegación para iniciar sesión o registrarse. Se activa automáticamente al ingresar la URL del sistema en el navegador.
* **Actores:** Visitante (usuario no autenticado en la web)
* **Prioridad:** Alta
* **Precondiciones:** El servidor web de Elmo Recreaciones debe estar en funcionamiento y el dominio debe ser accesible desde internet. Los recursos estáticos del sitio (imágenes del catálogo, estilos, scripts) deben estar correctamente desplegados.

#### Flujo Normal
1. El visitante escribe la URL del sitio web de Elmo Recreaciones en su navegador o accede desde un enlace externo.
2. El servidor recibe la solicitud HTTP GET y verifica que el visitante no posee una sesión activa (sin token JWT).
3. El sistema carga la página de inicio con el banner principal de la empresa, los servicios destacados y el menú de navegación.
4. El sistema presenta las opciones: 'Ver catálogo', 'Iniciar sesión' y 'Registrarse'.
5. El visitante explora la interfaz, visualiza los servicios de recreación disponibles y decide su próxima acción.

#### Flujos Alternos
* **FA1 — Usuario con sesión activa:**
  * **2a.** El sistema detecta que el visitante ya posee un token JWT válido en su navegador.
  * **2b.** El sistema redirige automáticamente al panel de control principal según el rol del usuario (CU3), sin mostrar la interfaz pública.

#### Postcondición
La interfaz pública de Elmo Recreaciones se presenta correctamente al visitante, mostrando los servicios, el catálogo de paquetes y las opciones de acceso al sistema.

#### Excepciones
* **E1:** Si el servidor web no está disponible (caída del hosting), el navegador muestra un error HTTP 503 y el caso de uso no se ejecuta.
* **E2:** Si algún recurso estático (imagen de catálogo, script) falla al cargar, el sistema presenta la página con degradación visual pero sin interrumpir la navegación.
* **E3:** Si el certificado SSL ha expirado, el navegador advierte al visitante y bloquea el acceso por seguridad.

---

### CU2: Iniciar sesión en el sistema (Generación de Token JWT)

* **Autores:** Luna Amézquita, Arantxa Leal, Alejandro Muñoz, Nicolas Giraldo
* **Descripción:** Permite a un usuario registrado en el sistema de Elmo Recreaciones (Cliente, Recreador o Administrador) autenticarse mediante su correo electrónico y contraseña. Tras validar las credenciales, el sistema genera un Token JWT que contiene el identificador del usuario y su rol, habilitando el acceso a los módulos correspondientes. Este caso de uso incluye CU3 (Visualizar panel de control principal) al completarse exitosamente.
* **Actores:** Administrador, Recreador/Staff, Cliente
* **Prioridad:** Alta
* **Precondiciones:** El usuario debe estar previamente registrado en la base de datos de Elmo Recreaciones con estado 'activo'. La interfaz pública debe haberse cargado correctamente (CU1). El servicio de autenticación y generación de tokens JWT debe estar operativo en el servidor.

#### Flujo Normal
1. El usuario selecciona la opción 'Iniciar sesión' desde la interfaz pública de Elmo Recreaciones.
2. El sistema presenta el formulario de autenticación con campos: correo electrónico y contraseña. Además de un botón para recuperar credenciales: '¿Olvidó su contraseña?'.
3. El usuario ingresa su correo electrónico registrado (ej. cliente@email.com) y su contraseña.
4. El usuario presiona el botón 'Ingresar'.
5. El sistema valida que ambos campos estén diligenciados y con formato correcto.
6. El sistema verifica las credenciales contra la base de datos, comparando el hash de la contraseña.
7. El sistema confirma la identidad del usuario y recupera su rol (Administrador, Recreador o Cliente).
8. El sistema genera un Token JWT firmado que incluye: ID de usuario, rol, y tiempo de expiración.
9. El sistema almacena el token en el cliente (cookie segura o localStorage).
10. El sistema redirige al usuario al panel de control principal correspondiente a su rol (CU3).

#### Flujos Alternos
* **FA1 — Credenciales incorrectas:**
  * **6a.** El sistema detecta que el correo no existe o la contraseña no coincide con el hash almacenado.
  * **6b.** El sistema muestra el mensaje: 'Correo o contraseña incorrectos. Verifique sus datos e intente de nuevo.'
  * **6c.** El sistema incrementa el contador de intentos fallidos para ese usuario.
  * **6d.** El caso de uso regresa al paso 3.
* **FA2 — Recuperación de contraseña:**
  * **2a.** El usuario selecciona '¿Olvidó su contraseña?' en el formulario de login.
  * **2b.** El sistema redirige al flujo de recuperación de credenciales por correo (CU5).

#### Postcondición
El usuario queda autenticado en la plataforma de Elmo Recreaciones con un Token JWT válido. Es redirigido al panel de control principal adaptado a su rol (administración, agenda de recreador o perfil de cliente).

#### Excepciones
* **E1:** Si el usuario supera 3 intentos fallidos consecutivos, el sistema bloquea el acceso por 15 minutos y muestra un aviso.
* **E2:** Si el servicio de generación de JWT no responde, el sistema muestra: 'Servicio no disponible temporalmente. Intente más tarde.'
* **E3:** Si los campos del formulario están vacíos al presionar 'Ingresar', el sistema resalta los campos en rojo con el mensaje 'Campo requerido'.
* **E4:** Si la cuenta del usuario está desactivada por el administrador, el sistema muestra: 'Su cuenta ha sido suspendida. Contacte al administrador de Elmo Recreaciones.'

---

### CU3: Visualizar panel de control principal

* **Autores:** Luna Amézquita, Arantxa Leal, Alejandro Muñoz, Nicolas Giraldo
* **Descripción:** Presenta al usuario autenticado el panel de control principal de la plataforma de Elmo Recreaciones, adaptado dinámicamente al rol del usuario. El panel del Administrador muestra módulos de gestión de reservas, inventario, personal y reportes financieros. El panel del Recreador muestra su agenda y los contratos asignados. El panel del Cliente muestra sus reservas activas, historial y estado de pagos. Este caso de uso se activa automáticamente tras el login exitoso (CU2) e incluye la validación de permisos (CU3.1).
* **Actores:** Administrador, Recreador/Staff, Cliente
* **Prioridad:** Alta
* **Precondiciones:** El usuario debe haber completado el inicio de sesión exitosamente (CU2) y poseer un Token JWT válido y vigente. Los roles y permisos deben estar correctamente configurados en la base de datos del sistema. El servidor de la plataforma de Elmo Recreaciones debe estar disponible.

#### Flujo Normal
1. El sistema recibe la solicitud de acceso al panel de control con el Token JWT del usuario en el encabezado.
2. El sistema invoca la validación de permisos y restricciones según el rol (incluye CU3.1).
3. El sistema recupera la configuración del panel correspondiente al rol del usuario autenticado.
4. Renderizado según rol:
   * **4a. Administrador:** El sistema presenta módulos de gestión de reservas, inventario de inflables/disfraces, asignación de recreadores, catálogo de servicios y reportes financieros de Elmo Recreaciones.
   * **4b. Recreador/Staff:** El sistema presenta la agenda semanal de eventos asignados, especificaciones de contratos (dirección, temática, edades) y formulario de reporte de novedades.
   * **4c. Cliente:** El sistema presenta el estado de sus reservas activas, historial de eventos contratados con Elmo Recreaciones, cotizaciones pendientes y estado de cuenta de pagos.
5. El usuario navega e interactúa con los módulos habilitados según su rol.

#### Flujos Alternos
* **FA1 — Token JWT expirado:**
  * **1a.** El sistema detecta que el token ha superado su tiempo de expiración.
  * **1b.** El sistema elimina la sesión del cliente y muestra el mensaje: 'Su sesión ha expirado. Por favor inicie sesión nuevamente.'
  * **1c.** El sistema redirige al formulario de inicio de sesión (CU2).
* **FA2 — Visitante intenta acceder directamente al panel:**
  * **1a.** El sistema detecta ausencia de Token JWT en la solicitud.
  * **1b.** El sistema redirige al visitante a la interfaz pública de Elmo Recreaciones (CU1).

#### Postcondición
El usuario autenticado visualiza su panel de control personalizado en la plataforma de Elmo Recreaciones, con acceso únicamente a los módulos y funcionalidades autorizadas para su rol.

#### Excepciones
* **E1:** Si el Token JWT ha sido alterado o es inválido, el sistema invalida la sesión, registra el evento en el log de seguridad y redirige al inicio.
* **E2:** Si ocurre un error al consultar la base de datos para cargar el panel, el sistema muestra: 'No fue posible cargar el panel. Recargue la página.'
* **E3:** Si el usuario no tiene ningún módulo habilitado para su rol (configuración incompleta), el sistema muestra un panel vacío con mensaje de contacto al administrador.

---

### CU3.1: Validar permisos y restricciones según el rol asignado

* **Autores:** Luna Amézquita, Arantxa Leal, Alejandro Muñoz, Nicolas Giraldo
* **Descripción:** Sub-caso de uso incluido por CU3. Verifica automáticamente los permisos y restricciones del usuario autenticado en la plataforma de Elmo Recreaciones según su rol asignado. Determina qué módulos, acciones y datos puede visualizar o manipular: el Administrador tiene acceso CRUD total; el Recreador/Staff accede solo a su agenda y contratos asignados; el Cliente accede únicamente a su perfil, reservas y estado de cuenta. Este proceso es transparente para el usuario y se ejecuta en el servidor cada vez que se solicita el panel principal.
* **Actores:** Sistema (ejecutado internamente al invocar CU3). Involucra indirectamente a: Administrador, Recreador/Staff, Cliente.
* **Prioridad:** Alta
* **Precondiciones:** El usuario debe estar autenticado con un Token JWT válido generado por el sistema de Elmo Recreaciones (CU2). La matriz de roles y permisos debe estar correctamente definida y almacenada en la base de datos. El Token JWT debe contener el campo 'rol' con uno de los valores válidos: 'administrador', 'recreador', 'cliente'.

#### Flujo Normal
1. El sistema extrae el campo 'rol' y el ID del usuario desde el Token JWT recibido.
2. El sistema consulta la matriz de permisos en la base de datos para el rol extraído.
3. El sistema construye el perfil de acceso del usuario:
   * **Administrador:** Permisos CRUD en reservas, inventario, catálogo, personal y reportes financieros.
   * **Recreador/Staff:** Permiso de lectura en agenda y contratos asignados; escritura en reporte de novedades.
   * **Cliente:** Permiso de lectura en catálogo, reservas propias e historial; escritura en solicitud de reserva y pago.
4. El sistema aplica las restricciones de acceso, bloqueando los endpoints y módulos no autorizados.
5. El sistema retorna el perfil de permisos validado al proceso de CU3 para renderizar el panel correspondiente.

#### Flujos Alternos
* **FA1 — Rol no reconocido en el token:**
  * **2a.** El sistema detecta que el campo 'rol' del token no coincide con ninguno de los roles válidos del sistema.
  * **2b.** El sistema aplica automáticamente el perfil de permisos más restrictivo (equivalente a Cliente sin reservas).
  * **2c.** El sistema registra el evento como alerta en el log de seguridad de Elmo Recreaciones.
  * **2d.** El administrador puede revisar la alerta en el módulo de auditoría.

#### Postcondición
El sistema cuenta con el perfil de permisos validado y aplicado para el usuario de Elmo Recreaciones, garantizando que cada rol acceda únicamente a la información y funcionalidades que le corresponden.

#### Excepciones
* **E1:** Si el campo 'rol' del Token JWT está ausente, vacío o ha sido manipulado, el sistema deniega el acceso, cierra la sesión y redirige al login.
* **E2:** Si la consulta de la matriz de permisos falla por error de base de datos, el sistema bloquea el acceso al panel y muestra un error de servicio no disponible.
* **E3:** Si se detectan múltiples solicitudes anómalas desde el mismo token en un corto período, el sistema invalida el token como medida de seguridad.

---

### CU4: Cerrar sesión de usuario de forma segura

* **Autores:** Luna Amézquita, Arantxa Leal, Alejandro Muñoz, Nicolas Giraldo
* **Descripción:** Permite a cualquier usuario autenticado en la plataforma de Elmo Recreaciones (Administrador, Recreador o Cliente) finalizar su sesión de manera segura. Al ejecutarse, el sistema invalida el Token JWT activo agregándolo a una lista negra en el servidor, elimina los datos de sesión del navegador del cliente y redirige a la interfaz pública. Se activa cuando el usuario selecciona deliberadamente la opción de cerrar sesión desde el panel de control.
* **Actores:** Administrador, Recreador/Staff, Cliente
* **Prioridad:** Media
* **Precondiciones:** El usuario debe tener una sesión activa con un Token JWT válido en la plataforma de Elmo Recreaciones. El usuario debe estar navegando en cualquier módulo del panel de control que presente la opción 'Cerrar sesión'.

#### Flujo Normal
1. El usuario hace clic en su nombre o avatar en la esquina superior derecha del panel.
2. El sistema despliega el menú de perfil con la opción 'Cerrar sesión'.
3. El usuario selecciona 'Cerrar sesión'.
4. El sistema presenta un diálogo de confirmación: '¿Está seguro que desea cerrar sesión?'
5. El usuario confirma presionando el botón 'Sí, cerrar sesión'.
6. El sistema envía el Token JWT actual al servidor para agregarlo a la lista negra de tokens invalidados.
7. El sistema elimina el token de sesión del navegador del cliente (limpieza de cookies y localStorage).
8. El sistema registra el evento de cierre de sesión en el log de auditoría con: usuario, rol, fecha y hora.
9. El sistema redirige al usuario a la interfaz pública de inicio de Elmo Recreaciones (CU1).
10. El sistema muestra brevemente el mensaje: 'Ha cerrado sesión correctamente. ¡Hasta pronto!'

#### Flujos Alternos
* **FA1 — El usuario cancela la confirmación:**
  * **4a.** El usuario presiona 'Cancelar' en el diálogo de confirmación.
  * **4b.** El sistema cierra el diálogo y el usuario permanece en el módulo actual del panel sin ninguna alteración de sesión.

#### Postcondición
La sesión del usuario en Elmo Recreaciones es terminada de forma segura. El Token JWT queda invalidado en el servidor y los datos de sesión son eliminados del navegador. El usuario es redirigido a la interfaz pública sin posibilidad de acceder a módulos protegidos con el token anterior.

#### Excepciones
* **E1:** Si el Token JWT ya había expirado antes de ejecutar el cierre, el sistema de igual forma limpia los datos de sesión del cliente y redirige a la interfaz pública.
* **E2:** Si falla la comunicación con el servidor al intentar invalidar el token, el sistema limpia la sesión del lado del cliente de todas formas y registra la incidencia en el log para revisión del administrador.
* **E3:** Si el usuario cierra el navegador sin cerrar sesión explícitamente, el token permanecerá válido hasta su expiración natural definida en la configuración del sistema.

---

### CU5: Gestionar recuperación de credenciales por correo

* **Autores:** Luna Amézquita, Arantxa Leal, Alejandro Muñoz, Nicolas Giraldo
* **Descripción:** Permite a un usuario registrado en Elmo Recreaciones que ha olvidado su contraseña solicitar la recuperación mediante el correo electrónico asociado a su cuenta. El sistema genera un token de recuperación único y temporal, envía un enlace seguro al correo del usuario y permite establecer una nueva contraseña. Se activa desde el enlace '¿Olvidó su contraseña?' disponible en el formulario de inicio de sesión.
* **Actores:** Administrador, Recreador o Cliente, Servicio de correo electrónico (SMTP de Elmo Recreaciones)
* **Prioridad:** Media
* **Precondiciones:** El usuario debe tener un correo electrónico verificado y registrado en la base de datos de Elmo Recreaciones. El servicio SMTP configurado en la plataforma debe estar operativo para el envío de correos. La interfaz pública del sistema debe estar disponible (CU1).

#### Flujo Normal
1. El usuario selecciona '¿Olvidó su contraseña?' en el formulario de inicio de sesión de Elmo Recreaciones.
2. El sistema presenta un formulario con el campo: 'Ingrese su correo electrónico registrado'.
3. El usuario ingresa su correo electrónico (ej: maria.garcia@email.com) y presiona 'Enviar enlace de recuperación'.
4. El sistema valida el formato del correo y verifica su existencia en la base de datos.
5. El sistema genera un token de recuperación único, aleatorio y con vigencia de 30 minutos.
6. El sistema almacena el token en la base de datos vinculado al usuario y con marca de tiempo.
7. El sistema envía al correo del usuario un mensaje con el asunto 'Recuperación de contraseña – Elmo Recreaciones', incluyendo el enlace seguro de restablecimiento con el token embebido.
8. El sistema muestra el mensaje: 'Si el correo está registrado, recibirá instrucciones en los próximos minutos.'
9. El usuario abre su bandeja de entrada, localiza el correo de Elmo Recreaciones y hace clic en el enlace.
10. El sistema valida que el token sea correcto, esté vigente y no haya sido usado previamente.
11. El sistema presenta el formulario para establecer nueva contraseña con campos: 'Nueva contraseña' y 'Confirmar contraseña'.
12. El usuario ingresa su nueva contraseña cumpliendo los requisitos de seguridad (mínimo 8 caracteres, una mayúscula, un número).
13. El sistema actualiza el hash de la contraseña en la base de datos e invalida el token de recuperación.
14. El sistema muestra el mensaje: 'Contraseña actualizada exitosamente. Ya puede iniciar sesión.'
15. El sistema redirige al usuario al formulario de inicio de sesión (CU2).

#### Flujos Alternos
* **FA1 — Correo no registrado en el sistema:**
  * **4a.** El sistema no encuentra el correo en la base de datos de Elmo Recreaciones.
  * **4b.** Por razones de seguridad, el sistema muestra el mismo mensaje genérico del paso 8, sin confirmar si el correo existe o no, evitando enumeración de usuarios.
* **FA2 — Token de recuperación expirado (pasaron más de 30 minutos):**
  * **10a.** El sistema detecta que el token ha superado su tiempo de vigencia de 30 minutos.
  * **10b.** El sistema muestra el mensaje: 'El enlace de recuperación ha expirado. Por favor solicite uno nuevo.'
  * **10c.** El sistema presenta la opción 'Solicitar nuevo enlace', regresando al paso 2.
* **FA3 — Nueva contraseña no cumple los requisitos de seguridad:**
  * **12a.** El sistema detecta que la nueva contraseña no cumple los criterios mínimos.
  * **12b.** El sistema resalta el campo en rojo e indica los requisitos incumplidos.
  * **12c.** El usuario corrige la contraseña y reintenta (regresa al paso 12).

#### Postcondición
El usuario de Elmo Recreaciones ha restablecido su contraseña exitosamente. El token de recuperación queda invalidado en la base de datos y el usuario puede autenticarse con sus nuevas credenciales mediante CU2.

#### Excepciones
* **E1:** Si el servicio SMTP no está disponible al momento del envío, el sistema registra el error y muestra: "No fue posible enviar el correo. Intente nuevamente en unos minutos.".
* **E2:** Si el token ya fue utilizado previamente para restablecer la contraseña, el sistema lo marca como inválido y muestra: "Este enlace ya fue utilizado. Solicite un nuevo enlace de recuperación."
* **E3:** Si el usuario intenta acceder al enlace de recuperación desde un dispositivo diferente al que inició el proceso, el sistema valida únicamente el token, no el dispositivo, permitiendo el acceso.
* **E4:** Si la cuenta del usuario está desactivada por el administrador, el sistema no envía el correo de recuperación y muestra el mensaje genérico de confirmación por seguridad, sin revelar el estado de la cuenta.

## 📦 Módulo 2 - Inventario y Disponibilidad

### CU1: Consultar calendario interactivo de disponibilidad global

* **Descripción:** Permite al Administrador y al Operativo de Elmo Recreaciones consultar el calendario interactivo que muestra la disponibilidad global de todos los recursos de la empresa: inflables, disfraces, equipos de sonido y personal recreador. El calendario refleja en tiempo real las fechas ocupadas por eventos reservados, las fechas bloqueadas por mantenimiento o festivos, y las fechas disponibles para nuevas reservas. Este caso de uso incluye **CU1.1** (*Validar restricción técnica de fechas bloqueadas o pasadas*) al intentar interactuar con una fecha.
* **Actores:** Administrador, Operativo (Recreador / Staff)
* **Prioridad:** Alta

#### Precondiciones
1. El usuario debe estar autenticado en el sistema de Elmo Recreaciones con un Token JWT válido.
2. El usuario debe tener rol de Administrador u Operativo para acceder al módulo de inventario y disponibilidad.
3. La base de datos de reservas, eventos y mantenimientos debe estar actualizada y disponible.

#### Flujo Normal
1. El usuario autenticado accede al módulo **'Inventario y Disponibilidad'** desde el panel de control principal.
2. El sistema carga y presenta el calendario interactivo mensual con la disponibilidad global de recursos.
3. El calendario muestra con código de colores:
   * **Verde:** Fecha disponible
   * **Rojo:** Fecha ocupada por evento reservado
   * **Gris:** Fecha bloqueada por mantenimiento o festivo
   * **Amarillo:** Fecha con disponibilidad parcial de recursos
4. El usuario puede navegar entre meses usando los controles de avance y retroceso del calendario.
5. El usuario selecciona una fecha específica para consultar el detalle de disponibilidad.
6. El sistema ejecuta la validación técnica de la fecha seleccionada (incluye **CU1.1**).
7. El sistema muestra el detalle de la fecha: eventos programados, recursos ocupados, recursos disponibles (inflables libres, recreadores sin asignación, equipos disponibles) y observaciones registradas.
8. El usuario visualiza la información y puede filtrar por tipo de recurso (inflables, personal, equipos).

#### Flujos Alternos
* **FA1 — Filtrar por tipo de recurso:**
  * **2a.** El usuario selecciona un filtro específico: *'Solo inflables'*, *'Solo personal'* o *'Solo equipos de sonido'*.
  * **2b.** El sistema recarga el calendario mostrando únicamente la disponibilidad del recurso filtrado.
* **FA2 — Vista semanal:**
  * **2a.** El usuario cambia la vista del calendario de mensual a semanal.
  * **2b.** El sistema muestra los 7 días de la semana seleccionada con mayor detalle de eventos y recursos por día.
* **FA3 — Administrador bloquea una fecha:**
  * **7a.** El Administrador selecciona una fecha disponible y elige la opción *'Bloquear fecha'*.
  * **7b.** El sistema solicita el motivo del bloqueo (mantenimiento, festivo, evento interno).
  * **7c.** El sistema registra el bloqueo y actualiza el calendario mostrando la fecha en gris.

#### Postcondición
El usuario visualiza el calendario interactivo de disponibilidad global actualizado de Elmo Recreaciones, con información detallada de recursos disponibles y ocupados para la fecha o período consultado.

#### Excepciones
* **E1:** Si la base de datos de reservas no responde, el sistema muestra el mensaje: *"No fue posible cargar el calendario. Intente recargar la página."* y registra el error en el log.
* **E2:** Si el usuario intenta acceder al módulo sin los permisos de rol correspondientes, el sistema deniega el acceso y redirige al panel de control principal.
* **E3:** Si no existen registros de disponibilidad para el mes consultado, el sistema muestra el calendario vacío con todas las fechas en verde e indica: *"No hay eventos registrados para este período."*

---

### CU1.1: Validar restricción técnica de fechas bloqueadas o pasadas

* **Descripción:** Sub-caso de uso incluido por **CU1**. Valida automáticamente que la fecha seleccionada por el usuario en el calendario interactivo de Elmo Recreaciones sea técnicamente operable: no debe ser una fecha pasada, no debe estar bloqueada por mantenimiento programado, y no debe coincidir con un festivo marcado como no laborable por la empresa. Este proceso es transparente para el usuario y se ejecuta en el servidor cada vez que se selecciona o interactúa con una fecha del calendario.
* **Actores:** Sistema (ejecutado internamente al invocar CU1). Involucra indirectamente a: Administrador, Operativo.
* **Prioridad:** Alta

#### Precondiciones
1. El calendario interactivo debe haberse cargado correctamente (**CU1**).
2. La tabla de fechas bloqueadas y festivos debe estar actualizada en la base de datos de Elmo Recreaciones.
3. El servidor debe tener acceso a la fecha y hora actual del sistema para comparar fechas pasadas.

#### Flujo Normal
1. El usuario selecciona una fecha en el calendario interactivo de disponibilidad.
2. El sistema captura la fecha seleccionada y la compara con la fecha actual del servidor.
3. El sistema verifica si la fecha seleccionada está registrada en la tabla de fechas bloqueadas (mantenimiento programado, festivos no laborables o bloqueos manuales del administrador).
4. El sistema verifica que la fecha no tenga todos los recursos de Elmo Recreaciones ya ocupados.
5. Si la fecha pasa todas las validaciones, el sistema la marca como seleccionable y retorna el resultado a **CU1**.
6. **CU1** muestra el detalle de disponibilidad de la fecha validada.

#### Flujos Alternos
* **FA1 — Fecha pasada:**
  * **2a.** El sistema detecta que la fecha seleccionada es anterior a la fecha actual del servidor.
  * **2b.** El sistema bloquea la interacción con esa fecha y muestra el tooltip: *"No es posible seleccionar fechas pasadas."*
  * **2c.** El sistema solo permite la consulta de información histórica sin posibilidad de modificación.
* **FA2 — Fecha bloqueada por mantenimiento:**
  * **3a.** El sistema detecta que la fecha está registrada como bloqueada por mantenimiento de inflables o equipos.
  * **3b.** El sistema muestra el tooltip: *"Fecha no disponible: mantenimiento programado."* con el motivo registrado.
  * **3c.** Solo el Administrador puede desbloquear la fecha desde el módulo de gestión de calendario.
* **FA3 — Festivo no laborable:**
  * **3a.** El sistema detecta que la fecha corresponde a un festivo marcado como no laborable por Elmo Recreaciones.
  * **3b.** El sistema muestra el tooltip: *"Fecha no laborable: festivo."* y bloquea la selección para nuevas reservas.

#### Postcondición
El sistema retorna a **CU1** el resultado de la validación: la fecha es operable (disponible para consulta o reserva) o está restringida (pasada, bloqueada o festivo), permitiendo que el calendario muestre la información correcta al usuario.

#### Excepciones
* **E1:** Si la consulta a la tabla de fechas bloqueadas falla por error de base de datos, el sistema asume la fecha como potencialmente disponible, registra el error en el log y muestra una advertencia al usuario.
* **E2:** Si el reloj del servidor presenta una discrepancia con la hora real, las validaciones de fechas pasadas pueden verse afectadas; el sistema registra alertas de sincronización de tiempo en el log de auditoría.
* **E3:** Si una fecha tiene bloqueos parciales (algunos recursos disponibles y otros en mantenimiento), el sistema la marca como disponibilidad parcial (amarillo) y detalla cuáles recursos están restringidos.

---

### CU2: Modificar estado físico de los inflables (Disponible / Mantenimiento)

* **Descripción:** Permite al Administrador y al Operativo de Elmo Recreaciones actualizar el estado físico de los inflables del inventario entre los estados 'Disponible' y 'En mantenimiento'. Este caso de uso se utiliza cuando un recreador detecta daños en un inflable durante o después de un evento, o cuando el administrador programa un mantenimiento preventivo. El cambio de estado impacta directamente la disponibilidad mostrada en el calendario interactivo (**CU1**) y en el stock de insumos (**CU3**).
* **Actores:** Administrador, Operativo (Recreador / Staff)
* **Prioridad:** Alta

#### Precondiciones
1. El usuario debe estar autenticado con un Token JWT válido y con rol de Administrador u Operativo.
2. El inventario de inflables de Elmo Recreaciones debe estar registrado en el sistema con sus estados actuales.
3. El inflable al que se le modificará el estado debe existir en la base de datos del inventario.

#### Flujo Normal
1. El usuario accede al módulo **'Inventario y Disponibilidad'** y selecciona la sección **'Gestión de Inflables'**.
2. El sistema presenta el listado de inflables registrados con su estado actual: código, nombre (ej: *'Castillo inflable princesas'*, *'Tobogán doble'*), capacidad, estado y última actualización.
3. El usuario localiza el inflable que desea actualizar usando el buscador o filtro por estado.
4. El usuario selecciona el inflable y presiona el botón **'Cambiar estado'**.
5. El sistema presenta las opciones de estado: **'Disponible'** o **'En mantenimiento'**.
6. El usuario selecciona el nuevo estado e ingresa una observación obligatoria (ej: *"Daño en costura lateral detectado durante evento del 5 de junio"* o *"Mantenimiento preventivo mensual"*).
7. El usuario confirma el cambio presionando **'Guardar cambio de estado'**.
8. El sistema actualiza el estado del inflable en la base de datos con: nuevo estado, usuario responsable, fecha, hora y observación.
9. El sistema actualiza automáticamente la disponibilidad del recurso en el calendario interactivo (**CU1**).
10. El sistema muestra el mensaje: *"Estado del inflable actualizado correctamente."* y registra el cambio en el log de inventario.

#### Flujos Alternos
* **FA1 — Operativo reporta daño desde campo (evento en curso):**
  * **1a.** El Operativo accede al módulo desde su panel restringido durante la ejecución de un evento.
  * **1b.** El sistema presenta únicamente los inflables asignados al evento actual del recreador.
  * **1c.** El Operativo selecciona el inflable dañado, elige 'En mantenimiento' e ingresa la descripción del daño.
  * **1d.** El sistema notifica automáticamente al Administrador sobre el reporte de daño con los detalles del incidente.
  * **1e.** El flujo continúa desde el paso 8.
* **FA2 — Administrador programa mantenimiento preventivo:**
  * **4a.** El Administrador selecciona múltiples inflables simultáneamente usando casillas de selección.
  * **4b.** El sistema permite aplicar el cambio de estado 'En mantenimiento' de forma masiva.
  * **4c.** El Administrador define la fecha estimada de retorno al estado 'Disponible'.
  * **4d.** El sistema bloquea las fechas correspondientes en el calendario (**CU1**) durante el período de mantenimiento.

#### Postcondición
El estado físico del inflable queda actualizado en el inventario de Elmo Recreaciones. El calendario interactivo refleja el cambio de disponibilidad del recurso de forma inmediata, evitando que se asigne un inflable en mantenimiento a nuevas reservas de eventos.

#### Excepciones
* **E1:** Si el inflable seleccionado tiene eventos reservados pendientes para fechas futuras y se intenta pasar a 'En mantenimiento', el sistema advierte: *"Este inflable tiene N evento(s) reservado(s). ¿Desea continuar y notificar al administrador?"* Solo el Administrador puede confirmar el cambio en este caso.
* **E2:** Si el campo de observación queda vacío al intentar guardar, el sistema bloquea la acción y muestra: *"Debe ingresar una observación para registrar el cambio de estado."*
* **E3:** Si falla la conexión con la base de datos al guardar, el sistema muestra: *"No fue posible actualizar el estado. Intente nuevamente."* y no registra el cambio parcial.
* **E4:** Si el Operativo intenta cambiar el estado de un inflable que no le fue asignado en su evento actual, el sistema deniega la acción y muestra: *"No tiene permisos para modificar este recurso."*

---

### CU3: Consultar stock de insumos críticos en bodega

* **Descripción:** Permite al Administrador y al Operativo de Elmo Recreaciones consultar en tiempo real el stock disponible de insumos críticos almacenados en bodega: globos, pinturas para maquillaje, materiales de decoración, consumibles de sonido (pilas, cables de repuesto), implementos de shows recreativos y materiales de mantenimiento de inflables (parches, pegamentos). El sistema alerta automáticamente cuando algún insumo alcanza el nivel mínimo de stock definido por el administrador, facilitando la gestión de reabastecimiento oportuno.
* **Actores:** Administrador, Operativo (Recreador / Staff)
* **Prioridad:** Media

#### Precondiciones
1. El usuario debe estar autenticado con Token JWT válido y con rol de Administrador u Operativo.
2. El inventario de insumos críticos debe estar registrado en el sistema con sus cantidades y niveles mínimos.
3. Los niveles mínimos de alerta por insumo deben estar configurados por el Administrador.

#### Flujo Normal
1. El usuario accede al módulo **'Inventario y Disponibilidad'** y selecciona la sección **'Stock de Insumos en Bodega'**.
2. El sistema carga y presenta el listado de insumos críticos con: código de insumo, nombre, categoría (decoración, shows, mantenimiento, sonido), cantidad actual, nivel mínimo configurado, unidad de medida y estado de stock (Normal / Bajo / Crítico).
3. El sistema resalta visualmente los insumos con stock bajo (amarillo) o crítico (rojo) que requieren reabastecimiento.
4. El usuario puede filtrar el listado por categoría de insumo o por estado de stock.
5. El usuario selecciona un insumo específico para ver su detalle: historial de consumo por evento, fecha de último reabastecimiento, proveedor habitual y observaciones del almacenero.
6. El usuario visualiza la información y puede exportar el reporte de stock en formato PDF o Excel.

#### Flujos Alternos
* **FA1 — Administrador actualiza cantidad de stock (entrada de insumos):**
  * **5a.** El Administrador selecciona un insumo y presiona *'Registrar entrada de stock'*.
  * **5b.** El sistema solicita: cantidad ingresada, fecha de ingreso, proveedor y número de factura.
  * **5c.** El Administrador completa los datos y confirma.
  * **5d.** El sistema actualiza la cantidad en bodega, registra el movimiento en el historial y recalcula el estado de stock.
* **FA2 — Operativo consulta insumos antes de un evento:**
  * **1a.** El Operativo accede desde su panel y el sistema filtra automáticamente los insumos relevantes para los eventos asignados al recreador (según temática y tipo de show).
  * **1b.** El Operativo verifica que los materiales necesarios estén disponibles antes de preparar el kit del evento.
* **FA3 — Alerta automática de stock crítico:**
  * **3a.** El sistema detecta que un insumo ha alcanzado o superado su nivel crítico.
  * **3b.** El sistema envía una notificación automática al Administrador vía correo electrónico: *"Alerta de stock crítico: [nombre del insumo] – Cantidad actual: [N] unidades. Nivel mínimo: [M] unidades."*
  * **3c.** La alerta también aparece como notificación en el panel de control del Administrador.

#### Postcondición
El usuario visualiza el estado actualizado del stock de insumos críticos en bodega de Elmo Recreaciones, con identificación clara de los materiales que requieren reabastecimiento urgente para garantizar la operación continua de los eventos de recreación, decoración e inflables.

#### Excepciones
* **E1:** Si la base de datos de inventario no responde, el sistema muestra: *"No fue posible cargar el stock de insumos. Intente recargar la página."* y registra el error en el log del sistema.
* **E2:** Si el Operativo intenta registrar una entrada de stock (acción exclusiva del Administrador), el sistema deniega la acción mostrando: *"No tiene permisos para registrar movimientos de inventario."*
* **E3:** Si no hay insumos registrados en el sistema para la categoría consultada, el sistema muestra: *"No se encontraron insumos registrados para esta categoría. Contacte al administrador."*
* **E4:** Si el nivel mínimo de un insumo no ha sido configurado por el Administrador, el sistema no puede generar alertas para ese insumo y lo indica en el listado con la etiqueta *"Sin nivel mínimo configurado"*.

---

## 🤖 Módulo 3 - Inteligencia Artificial

### CU1: Solicitar recomendación de servicio

* **Descripción:** Permite al Cliente solicitar al sistema una recomendación de servicios de recreación, decoración o inflables, con base en sus preferencias y el tipo de evento que desea realizar.
* **Actores:** Cliente
* **Prioridad:** Media

#### Precondiciones
1. El Cliente debe haber ingresado datos básicos del evento (tipo de celebración, rango de edades, presupuesto aproximado).

#### Flujo Normal
1. El Cliente accede al módulo de recomendaciones e indica el tipo de evento y sus preferencias.
2. El sistema analiza el catálogo de servicios disponibles.
3. El sistema genera una recomendación de servicios acorde al perfil ingresado.
4. El sistema muestra las recomendaciones al Cliente, ordenadas por relevancia.
5. El Cliente puede seleccionar uno o varios servicios recomendados para continuar con su reserva.

#### Flujos Alternos
* **FA1 — El Cliente rechaza las recomendaciones:**
  * **4a.** El Cliente indica que ninguna recomendación se ajusta a sus necesidades.
  * **4b.** El sistema solicita información adicional (temática específica, presupuesto ajustado) y genera una nueva recomendación.
  * **4c.** El flujo continúa desde el paso 3.

#### Postcondición
El Cliente recibe una lista de servicios recomendados según sus preferencias, disponible para continuar con la cotización o reserva.

#### Excepciones
* **E1:** Si la información proporcionada es insuficiente, el sistema muestra *"Necesitamos más información para generar una recomendación precisa."* y solicita datos adicionales.
* **E2:** Si el catálogo no cuenta con servicios que se ajusten al perfil, el sistema muestra *"No encontramos servicios que coincidan con tus preferencias. Te mostramos las opciones más populares."*

---

### CU2: Generar cotización automática

* **Descripción:** Genera de forma automática una cotización con base en los servicios seleccionados por el Cliente o recomendados por el sistema (**CU1**), calculando el valor total mediante **CU2.1**.
* **Actores:** Cliente, Administrador
* **Prioridad:** Alta

#### Precondiciones
1. Deben existir servicios seleccionados por el Cliente o recomendados previamente por el sistema (**CU1**).

#### Flujo Normal
1. El usuario (Cliente o Administrador) solicita la generación de la cotización.
2. El sistema recopila los servicios a incluir.
3. El sistema ejecuta **CU2.1** (*Calcular costos*).
4. El sistema arma la cotización con los valores obtenidos, incluyendo desglose por servicio.
5. El sistema presenta la cotización al usuario.
6. El Cliente puede aceptar la cotización para continuar con el proceso de reserva.

#### Flujos Alternos
* **FA1 — Cotización generada por el Administrador para un cliente presencial:**
  * **1a.** El Administrador ingresa los servicios manualmente en representación del cliente.
  * **1b.** El flujo continúa desde el paso 2.

#### Postcondición
La cotización queda generada, almacenada con estado 'Pendiente' y disponible para ser revisada, ajustada o aceptada por el Cliente.

#### Excepciones
* **E1:** Si algún servicio no tiene precio configurado (según **CU2.1**), se excluye de la cotización y se notifica al Administrador.
* **E2:** Si no se selecciona ningún servicio, el sistema muestra *"Debe seleccionar al menos un servicio para generar la cotización."*

---

### CU2.1: Calcular costos

* **Descripción:** Subproceso interno, incluido por **CU2**, que calcula el costo correspondiente a cada servicio incluido en la cotización automática, aplicando tarifas vigentes y reglas de negocio de paquetes o combos.
* **Actores:** Cliente, Administrador (indirectamente, a través de **CU2**)
* **Prioridad:** Alta

#### Precondiciones
1. Los servicios y sus tarifas vigentes deben estar registrados en el sistema.

#### Flujo Normal
1. El sistema recibe la lista de servicios a cotizar.
2. El sistema consulta las tarifas vigentes de cada servicio.
3. El sistema suma los valores y aplica reglas de negocio (paquetes, combos, tarifas especiales).
4. El sistema retorna el costo total al proceso **CU2**.

#### Flujos Alternos
* **FA1 — Combo aplicable detectado:**
  * **3a.** El sistema detecta que los servicios seleccionados corresponden a un paquete/combo con tarifa preferencial.
  * **3b.** El sistema aplica automáticamente el valor del combo en lugar de la suma individual.
  * **3c.** El flujo continúa desde el paso 4.

#### Postcondición
El costo total de los servicios queda disponible para armar la cotización (**CU2**).

#### Excepciones
* **E1:** Si un servicio no tiene tarifa configurada, se marca como *'pendiente de definir precio'* y se excluye del total.

---

### CU3: Analizar disponibilidad

* **Descripción:** Analiza la disponibilidad de fechas, horarios, personal e inventario para atender un evento solicitado, consultando la agenda de recreadores y el inventario de inflables y equipos.
* **Actores:** Cliente, Administrador
* **Prioridad:** Alta

#### Precondiciones
1. Debe indicarse la fecha y hora tentativa del evento a consultar.

#### Flujo Normal
1. El usuario ingresa la fecha y hora deseada para el evento.
2. El sistema consulta la agenda de recreadores y el inventario disponible.
3. El sistema determina si existe disponibilidad para esa fecha y hora.
4. El sistema muestra el resultado: disponible, no disponible o disponibilidad parcial.
5. Si hay disponibilidad, el usuario puede continuar con la solicitud de reserva.

#### Flujos Alternos
* **FA1 — Disponibilidad parcial:**
  * **4a.** El sistema detecta que solo parte de los recursos solicitados están disponibles.
  * **4b.** El sistema indica qué recursos sí y cuáles no están disponibles.
  * **4c.** El flujo continúa desde el paso 5, si el usuario decide continuar con los recursos disponibles.

#### Postcondición
El resultado de disponibilidad queda registrado y disponible para continuar con la reserva o cotización.

#### Excepciones
* **E1:** Si no hay disponibilidad en la fecha solicitada, el sistema sugiere fechas alternas cercanas con recursos disponibles.
* **E2:** Si la fecha ingresada es anterior a la fecha actual, el sistema rechaza la consulta y muestra *"La fecha ingresada no es válida."*

---

### CU4: Generar sugerencias de paquetes

* **Descripción:** Sugiere paquetes de servicios combinados (shows, decoración, inflables) según el perfil y preferencias del Cliente, analizadas mediante **CU4.1**.
* **Actores:** Cliente, Administrador
* **Prioridad:** Media

#### Precondiciones
1. El sistema debe contar con historial de reservas o preferencias declaradas por el Cliente.

#### Flujo Normal
1. El usuario solicita la generación de sugerencias de paquetes.
2. El sistema ejecuta **CU4.1** (*Analizar preferencias del cliente*).
3. El sistema cruza las preferencias identificadas con el catálogo de paquetes disponibles.
4. El sistema presenta los paquetes sugeridos, ordenados por afinidad.
5. El Cliente puede seleccionar un paquete sugerido para continuar con la cotización.

#### Flujos Alternos
* **FA1 — Cliente sin historial suficiente:**
  * **2a.** El sistema detecta que el cliente no cuenta con historial previo.
  * **2b.** El sistema utiliza un perfil de preferencias genérico basado en los paquetes más populares.
  * **2c.** El flujo continúa desde el paso 3.

#### Postcondición
El Cliente o Administrador recibe una lista de paquetes sugeridos, disponible para su selección.

#### Excepciones
* **E1:** Si no existen paquetes configurados en el catálogo, el sistema muestra *"No hay paquetes disponibles en este momento."*

---

### CU4.1: Analizar preferencias del cliente

* **Descripción:** Subproceso interno, incluido por **CU4**, que analiza el historial de reservas y las preferencias declaradas del Cliente para personalizar las sugerencias de paquetes.
* **Actores:** Cliente, Administrador (indirectamente, a través de **CU4**)
* **Prioridad:** Media

#### Precondiciones
1. El Cliente debe estar registrado en el sistema, con o sin historial previo de reservas.

#### Flujo Normal
1. El sistema recopila el historial de reservas y preferencias del Cliente.
2. El sistema identifica patrones (tipo de evento, temática, rango de edad predominante).
3. El sistema retorna el perfil de preferencias al proceso **CU4**.

#### Flujos Alternos
* **FA1 — Cliente nuevo sin historial:**
  * **1a.** El sistema detecta que el cliente es nuevo y no cuenta con historial.
  * **1b.** El sistema utiliza un perfil de preferencias genérico por defecto.
  * **1c.** El flujo continúa desde el paso 3.

#### Postcondición
El perfil de preferencias del Cliente queda disponible para generar sugerencias de paquetes (**CU4**).

#### Excepciones
* **E1:** Si el historial del cliente está incompleto o corrupto, el sistema descarta los datos inválidos y utiliza únicamente la información confiable disponible.

---

### CU5: Predecir necesidades logísticas

* **Descripción:** Predice las necesidades logísticas futuras (inventario, personal, transporte) con base en el histórico de eventos y la estacionalidad, apoyando la planeación de recursos de Elmo Recreaciones.
* **Actores:** Administrador
* **Prioridad:** Media

#### Precondiciones
1. Debe existir un histórico de eventos registrados y datos de temporada suficientes para el análisis.

#### Flujo Normal
1. El Administrador solicita la predicción logística para un periodo determinado.
2. El sistema analiza el histórico de eventos y la estacionalidad.
3. El sistema proyecta la demanda de inventario y personal para el periodo.
4. El sistema presenta el reporte de predicción logística.
5. El Administrador utiliza el reporte para planear compras de inventario o contratación de personal.

#### Flujos Alternos
* **FA1 — Comparación entre periodos:**
  * **4a.** El Administrador solicita comparar la predicción con el mismo periodo del año anterior.
  * **4b.** El sistema muestra ambos reportes lado a lado.
  * **4c.** El flujo continúa desde el paso 5.

#### Postcondición
El reporte de predicción logística queda generado y disponible para la planeación de recursos.

#### Excepciones
* **E1:** Si los datos históricos son insuficientes, el sistema genera la predicción indicando un margen de error alto y lo advierte en el reporte.
* **E2:** Si no existe ningún histórico registrado, el sistema muestra *"No hay datos suficientes para generar una predicción."*

## 💰 Módulo 4 - Lógica de Costos y Logística

### CU1: Calcular costo del evento

* **Descripción:** Permite al Administrador calcular el costo total de un evento, sumando los valores de los servicios de recreación, decoración e inflables seleccionados, más los insumos y la mano de obra requerida (recreadores asignados). Este cálculo constituye la base para la generación del presupuesto (**CU3**).
* **Actores:** Administrador
* **Prioridad:** Alta

#### Precondiciones
1. El Administrador debe estar autenticado con un token JWT válido y con rol de Administrador.
2. Debe existir una solicitud de reserva o cotización con al menos un servicio seleccionado.
3. El catálogo de servicios debe tener tarifas configuradas.

#### Flujo Normal
1. El Administrador accede al módulo **'Lógica de Costos y Logística'** y selecciona la solicitud a costear.
2. El sistema muestra los servicios, paquetes y decoraciones seleccionados para el evento.
3. El sistema consulta las tarifas vigentes de cada servicio e insumo asociado.
4. El sistema suma el valor de servicios, insumos y mano de obra requerida.
5. El sistema calcula y muestra el costo total estimado del evento, con su desglose.
6. El Administrador revisa el desglose y puede ajustar manualmente algún valor.
7. El Administrador confirma presionando **'Guardar costo del evento'**.
8. El sistema almacena el costo calculado y lo deja disponible para **CU3** (*Generar presupuesto*).

#### Flujos Alternos
* **FA1 — Servicio sin tarifa configurada:**
  * **3a.** El sistema detecta que un servicio no tiene tarifa asignada.
  * **3b.** El sistema resalta el servicio y solicita al Administrador ingresar el valor manualmente.
  * **3c.** El flujo continúa desde el paso 4.
* **FA2 — Ajuste manual de valores:**
  * **6a.** El Administrador modifica el valor de uno o varios ítems del desglose.
  * **6b.** El sistema recalcula automáticamente el total con los nuevos valores.
  * **6c.** El flujo continúa desde el paso 7.

#### Postcondición
El costo del evento queda calculado, registrado y disponible como insumo para **CU3** (*Generar presupuesto*) y **CU3.1**.

#### Excepciones
* **E1:** Si la solicitud no tiene ningún servicio seleccionado, el sistema muestra *"No es posible calcular el costo: la solicitud no tiene servicios asociados."* y bloquea el cálculo.
* **E2:** Si falla la conexión con la base de datos al guardar, el sistema muestra *"No fue posible guardar el costo del evento. Intente nuevamente."* y no registra el cambio parcial.
* **E3:** Si el Administrador ingresa un valor negativo o no numérico en el ajuste manual, el sistema rechaza el dato y muestra *"El valor ingresado no es válido."*

---

### CU2: Calcular transporte

* **Descripción:** Calcula el costo de transporte del personal, inflables y equipos hacia el lugar del evento, según la dirección registrada y la tarifa por kilometraje o zona definida por Elmo Recreaciones. Puede ser invocado directamente por el Administrador o de forma automática por **CU3** (*Generar presupuesto*).
* **Actores:** Administrador
* **Prioridad:** Alta

#### Precondiciones
1. El Administrador debe estar autenticado con un token JWT válido (aplica solo en invocación directa).
2. La dirección del evento debe estar registrada en la solicitud.
3. Las tarifas de transporte por zona o kilometraje deben estar configuradas en el sistema.

#### Flujo Normal
1. El Administrador selecciona la solicitud sobre la cual calculará el transporte (u opcionalmente, **CU3** invoca este caso de uso automáticamente durante la generación del presupuesto).
2. El sistema toma la dirección registrada del evento.
3. El sistema calcula la distancia desde la bodega o base de operaciones hasta el sitio del evento.
4. El sistema aplica la tarifa correspondiente según kilometraje o zona.
5. El sistema muestra/retorna el costo de transporte estimado.
6. Si la invocación fue manual, el Administrador confirma presionando **"Guardar costo de transporte"**. Si fue automática (vía **CU3**), el paso se omite y el valor se retorna directamente al proceso invocador.
7. El sistema almacena el valor y lo deja disponible para **CU3** (*Generar presupuesto*).

#### Flujos Alternos
* **FA1 — Zona fuera de cobertura estándar:**
  * **3a.** El sistema detecta que la dirección se encuentra fuera del área de cobertura habitual.
  * **3b.** El sistema notifica que aplica una tarifa especial y solicita confirmación del Administrador (si es invocación manual) o registra la observación para revisión posterior (si es invocación automática).
  * **3c.** El flujo continúa desde el paso 4.
* **FA2 — Corrección manual de dirección:**
  * **2a.** El Administrador detecta que la dirección registrada es incorrecta y la actualiza.
  * **2b.** El sistema recalcula la distancia con la nueva dirección.
  * **2c.** El flujo continúa desde el paso 3.
* **FA3 — Invocación automática desde CU3:**
  * **1a.** **CU3** invoca este caso de uso durante la generación del presupuesto.
  * **1b.** Se omiten los pasos de selección manual (paso 1) y confirmación (paso 6).
  * **1c.** El flujo continúa desde el paso 2 y retorna el valor directamente a **CU3** al finalizar.

#### Postcondición
El costo de transporte queda calculado y disponible para integrarse en el presupuesto general del evento (**CU3**).

#### Excepciones
* **E1:** Si la dirección del evento no está registrada, el sistema muestra/retorna *"Debe registrar la dirección del evento antes de calcular el transporte."* y bloquea el cálculo.
* **E2:** Si no existe tarifa configurada para la zona, el sistema aplica una tarifa por defecto, guarda el cálculo como *"pendiente de revisión"* y notifica al Administrador para su ajuste posterior.
* **E3:** Si falla el servicio de geolocalización, el sistema muestra *"No fue posible calcular la distancia. Intente nuevamente."*

---

### CU3: Generar presupuesto

* **Descripción:** Genera el presupuesto completo del evento, integrando el costo del evento (**CU3.1**) y el costo de transporte (**CU3.2**) en un único documento consolidado para revisión y posterior envío al cliente.
* **Actores:** Administrador
* **Prioridad:** Alta

#### Precondiciones
1. El Administrador debe estar autenticado con rol de Administrador.
2. La solicitud de reserva debe estar registrada con los servicios seleccionados por el cliente.

#### Flujo Normal
1. El Administrador solicita la generación del presupuesto para una solicitud.
2. El sistema ejecuta **CU3.1** (*Calcular costo del evento*).
3. El sistema ejecuta **CU3.2** / **CU2** (*Calcular transporte*).
4. El sistema consolida ambos valores en un documento de presupuesto con su desglose.
5. El sistema presenta el presupuesto para revisión del Administrador.
6. El Administrador aprueba el presupuesto o solicita ajustes.
7. El sistema almacena el presupuesto con estado **'Generado'** y fecha de emisión.

#### Flujos Alternos
* **FA1 — Ajuste antes de aprobar:**
  * **6a.** El Administrador solicita modificar algún valor del presupuesto consolidado.
  * **6b.** El sistema permite editar el ítem correspondiente y recalcula el total.
  * **6c.** El flujo continúa desde el paso 7.

#### Postcondición
El presupuesto queda generado, almacenado con estado **'Generado'** y disponible para enviarse al cliente o para aplicar descuentos (**CU4**).

#### Excepciones
* **E1:** Si **CU3.1** o **CU3.2** falla por datos incompletos, el sistema detiene la generación y muestra *"No fue posible generar el presupuesto: falta información de costos o transporte."*
* **E2:** Si ya existe un presupuesto vigente para la misma solicitud, el sistema pregunta *"¿Desea generar una nueva versión del presupuesto?"* antes de continuar.

---

### CU3.1: Calcular costo del evento

* **Descripción:** Subproceso interno, incluido por **CU3**, que calcula el costo del evento (servicios, insumos y personal) de forma automática como parte de la generación del presupuesto.
* **Actores:** Administrador (indirectamente, a través de **CU3**)
* **Prioridad:** Alta

#### Precondiciones
1. **CU3** debe haber sido invocado.
2. La solicitud debe contar con servicios seleccionados.

#### Flujo Normal
1. El sistema recupera los servicios y paquetes de la solicitud.
2. El sistema calcula el costo de servicios, insumos y personal asociado.
3. El sistema retorna el valor total del costo del evento al proceso **CU3**.

#### Flujos Alternos
* **FA1 — Servicio sin tarifa:**
  * **2a.** El sistema detecta un servicio sin tarifa configurada.
  * **2b.** El sistema lo excluye del cálculo y lo marca como pendiente de definir precio.
  * **2c.** El flujo continúa desde el paso 3.

#### Postcondición
El valor del costo del evento queda disponible para ser consolidado en el presupuesto (**CU3**).

#### Excepciones
* **E1:** Si ningún servicio de la solicitud tiene tarifa configurada, el sistema retorna error a **CU3** indicando *"No fue posible calcular el costo del evento: sin tarifas disponibles."*

---

### CU4: Aplicar descuentos

* **Descripción:** Permite al Administrador aplicar descuentos o promociones vigentes a un presupuesto previamente generado, validando su vigencia mediante **CU4.1** antes de recalcular el valor total.
* **Actores:** Administrador
* **Prioridad:** Media

#### Precondiciones
1. Debe existir un presupuesto generado (**CU3**) con estado **'Generado'**.
2. El Administrador debe estar autenticado con rol de Administrador.

#### Flujo Normal
1. El Administrador selecciona el presupuesto sobre el cual aplicará el descuento.
2. El sistema ejecuta **CU4.1** (*Validar promociones y descuentos*).
3. El Administrador selecciona o ingresa el código de descuento aplicable.
4. El sistema recalcula el valor total del presupuesto con el descuento aplicado.
5. El sistema actualiza el presupuesto con el nuevo valor y registra el descuento aplicado.
6. El sistema muestra *"Descuento aplicado correctamente."*

#### Flujos Alternos
* **FA1 — Descuento por tipo de cliente frecuente:**
  * **3a.** El sistema detecta automáticamente que el cliente cumple condiciones de cliente frecuente.
  * **3b.** El sistema sugiere el descuento correspondiente antes de que el Administrador lo ingrese manualmente.
  * **3c.** El flujo continúa desde el paso 4.

#### Postcondición
El presupuesto queda actualizado con el descuento aplicado y listo para ser enviado al cliente.

#### Excepciones
* **E1:** Si el descuento no es válido o ha expirado (según **CU4.1**), el sistema rechaza la operación y muestra *"El descuento ingresado no es válido o se encuentra vencido."*
* **E2:** Si el descuento supera el porcentaje máximo permitido por política interna, el sistema bloquea la aplicación y notifica *"El descuento excede el límite permitido."*

---

### CU4.1: Validar promociones y descuentos

* **Descripción:** Subproceso interno, incluido por **CU4**, que verifica que la promoción o el código de descuento ingresado se encuentre vigente, cumpla las condiciones y no haya superado su límite de uso.
* **Actores:** Administrador (indirectamente, a través de **CU4**)
* **Prioridad:** Media

#### Precondiciones
1. Deben existir promociones o descuentos configurados previamente en el sistema.

#### Flujo Normal
1. El sistema recibe el código o tipo de descuento a validar.
2. El sistema verifica vigencia, condiciones de aplicación y límite de uso.
3. El sistema retorna el resultado de la validación (válido / no válido) al proceso **CU4**.

#### Flujos Alternos
* **FA1 — Descuento próximo a vencer:**
  * **2a.** El sistema detecta que el descuento vence en menos de 24 horas.
  * **2b.** El sistema marca el descuento como válido pero incluye una advertencia de vigencia próxima.
  * **2c.** El flujo continúa desde el paso 3.

#### Postcondición
El resultado de la validación queda disponible para que **CU4** decida si aplica o no el descuento.

#### Excepciones
* **E1:** Si el descuento ya fue utilizado por el cliente y no es acumulable, el sistema lo marca como *'no válido'* e indica el motivo.
* **E2:** Si el código de descuento no existe en el sistema, el sistema retorna *"Código de descuento no encontrado."*

---

### CU5: Estimar recursos necesarios

* **Descripción:** Estima el inventario (inflables, decoración, sonido) y el personal de recreadores necesarios para ejecutar un evento, con base en los servicios y paquetes contratados.
* **Actores:** Administrador
* **Prioridad:** Media

#### Precondiciones
1. Los servicios y paquetes contratados para el evento deben estar definidos.
2. El inventario y el personal deben estar registrados en el sistema.

#### Flujo Normal
1. El Administrador solicita la estimación de recursos para un evento.
2. El sistema revisa los servicios y paquetes contratados.
3. El sistema calcula las cantidades de inventario y personal requeridas según reglas predefinidas.
4. El sistema muestra la estimación de recursos necesarios (inflables, decoración, recreadores).
5. El Administrador confirma la estimación para proceder con la asignación de recursos.

#### Flujos Alternos
* **FA1 — Ajuste manual de cantidades:**
  * **4a.** El Administrador ajusta manualmente la cantidad de algún recurso estimado.
  * **4b.** El sistema registra el ajuste como observación en la estimación.
  * **4c.** El flujo continúa desde el paso 5.

#### Postcondición
La estimación de recursos queda registrada y disponible para la asignación de personal e inventario al evento.

#### Excepciones
* **E1:** Si el inventario disponible es insuficiente para la fecha solicitada, el sistema alerta *"Inventario insuficiente para cubrir el evento en la fecha indicada."*
* **E2:** Si no hay personal disponible suficiente, el sistema alerta *"No hay recreadores suficientes disponibles para esta fecha."*

## 📄 Módulo 5 - Administración y Documentos

### CU1: Generar contrato

* **Descripción:** Genera el contrato formal del evento con los datos del cliente, los servicios contratados y las condiciones del servicio, validando previamente la información mediante **CU1.1**.
* **Actores:** Administrador
* **Prioridad:** Alta

#### Precondiciones
1. Debe existir un presupuesto aprobado y aceptado por el Cliente.

#### Flujo Normal
1. El Administrador selecciona la reserva y solicita **'Generar contrato'**.
2. El sistema ejecuta **CU1.1** (*Validar información del evento*).
3. El sistema genera el documento de contrato con las cláusulas y datos del evento.
4. El sistema presenta el contrato para revisión del Administrador.
5. El Administrador aprueba y el sistema lo marca como **'Generado'**.

#### Flujos Alternos
* **FA1 — Datos incompletos detectados por CU1.1:**
  * **2a.** El sistema detecta información faltante en los datos del evento o del cliente.
  * **2b.** El Administrador completa la información faltante.
  * **2c.** El flujo continúa desde el paso 3.

#### Postcondición
El contrato queda generado y almacenado, disponible para consulta (**CU2**) o descarga (**CU3**).

#### Excepciones
* **E1:** Si no existe un presupuesto aprobado, el sistema bloquea la generación del contrato.
* **E2:** Si ocurre un error al generar el archivo PDF, el sistema notifica el error y permite reintentar.

---

### CU1.1: Validar información del evento

* **Descripción:** Subproceso interno, incluido por **CU1**, que verifica que todos los datos necesarios del evento y del cliente estén completos y sean consistentes antes de generar el contrato.
* **Actores:** Administrador (indirectamente, a través de **CU1**)
* **Prioridad:** Alta

#### Precondiciones
1. **CU1** debe haber sido invocado.

#### Flujo Normal
1. El sistema recopila los datos del cliente, el evento y el presupuesto asociado.
2. Verifica los campos obligatorios (dirección, fecha, servicios, valores).
3. Retorna el resultado de la validación al proceso **CU1**.

#### Flujos Alternos
* **FA1 — Inconsistencia de fecha detectada:**
  * **2a.** El sistema detecta que la fecha del evento es anterior a la fecha actual.
  * **2b.** El sistema marca la inconsistencia y detiene el flujo hasta que se corrija.

#### Postcondición
El resultado de la validación queda disponible para que **CU1** continúe o se detenga.

#### Excepciones
* **E1:** Si faltan datos obligatorios, el sistema retorna *'Información incompleta'* listando los campos faltantes.

---

### CU2: Consultar contrato

* **Descripción:** Permite consultar contratos previamente generados, utilizando un buscador de documentos (**CU2.1**) según distintos criterios.
* **Actores:** Administrador, Cliente
* **Prioridad:** Media

#### Precondiciones
1. El usuario debe estar autenticado, con permisos según su rol.

#### Flujo Normal
1. El usuario accede al módulo de documentos.
2. El sistema ejecuta **CU2.1** (*Buscar documento*) con los criterios ingresados.
3. El sistema muestra el o los contratos encontrados.
4. El usuario selecciona el contrato para visualizarlo.

#### Flujos Alternos
* **FA1 — Consulta del Cliente restringida a sus propios contratos:**
  * **1a.** El sistema detecta que el usuario autenticado tiene rol Cliente.
  * **1b.** El sistema filtra automáticamente los resultados por el cliente autenticado.
  * **1c.** El flujo continúa desde el paso 2.

#### Postcondición
El contrato solicitado queda mostrado al usuario.

#### Excepciones
* **E1:** Si no se encuentra ningún contrato con los criterios ingresados, el sistema muestra *"Sin resultados para la búsqueda realizada."*

---

### CU2.1: Buscar documento

* **Descripción:** Subproceso interno, incluido por **CU2**, que realiza la búsqueda de documentos en el repositorio según filtros como cliente, fecha o tipo de documento.
* **Actores:** Administrador, Cliente (indirectamente, a través de **CU2**)
* **Prioridad:** Media

#### Precondiciones
1. **CU2** debe haber sido invocado.

#### Flujo Normal
1. El sistema recibe los criterios de búsqueda ingresados.
2. Consulta el repositorio de documentos con dichos criterios.
3. Retorna los resultados coincidentes al proceso **CU2**.

#### Flujos Alternos
* **FA1 — Búsqueda por texto libre:**
  * **1a.** El usuario ingresa una palabra clave en lugar de filtros estructurados.
  * **1b.** El sistema busca coincidencias en el nombre y metadatos del documento.
  * **1c.** El flujo continúa desde el paso 2.

#### Postcondición
La lista de documentos coincidentes queda disponible para **CU2**.

#### Excepciones
* **E1:** Si el repositorio de documentos no está disponible, el sistema muestra *"Error temporal al buscar documentos. Intente nuevamente."*

---

### CU3: Descargar documento

* **Descripción:** Permite descargar un documento (contrato u otro archivo asociado a la reserva) en formato PDF, verificando previamente los permisos del usuario.
* **Actores:** Administrador, Cliente
* **Prioridad:** Media

#### Precondiciones
1. El documento debe existir y el usuario debe tener permisos sobre él.

#### Flujo Normal
1. El usuario selecciona el documento a descargar.
2. El sistema verifica los permisos del usuario sobre el documento.
3. El sistema genera o entrega el archivo en formato PDF.
4. El usuario descarga el archivo.

#### Flujos Alternos
* **FA1 — Descarga por el Cliente con versión no editable:**
  * **3a.** El sistema detecta que el usuario tiene rol Cliente.
  * **3b.** El sistema entrega el documento con marca de agua o en versión de solo lectura.

#### Postcondición
El documento queda descargado en el dispositivo del usuario.

#### Excepciones
* **E1:** Si el usuario no tiene permisos sobre el documento, el sistema deniega la descarga.
* **E2:** Si el archivo está corrupto o no disponible, el sistema notifica el error.

---

### CU4: Actualizar documento

* **Descripción:** Permite al Administrador actualizar o corregir un documento existente, por ejemplo cambios en cláusulas del contrato o en los datos del evento, conservando el historial de versiones.
* **Actores:** Administrador
* **Prioridad:** Media

#### Precondiciones
1. El documento debe existir y no encontrarse archivado.

#### Flujo Normal
1. El Administrador selecciona el documento a actualizar.
2. El sistema muestra el contenido editable del documento.
3. El Administrador realiza los cambios necesarios.
4. El sistema guarda una nueva versión del documento y conserva el historial de cambios.

#### Flujos Alternos
* **FA1 — Actualización de plantilla base:**
  * **1a.** El Administrador modifica la plantilla base en lugar de un documento individual.
  * **1b.** El sistema aplica el cambio únicamente a los documentos futuros, sin alterar los ya generados.

#### Postcondición
El documento queda actualizado, con una nueva versión registrada en el historial.

#### Excepciones
* **E1:** Si el documento se encuentra archivado, el sistema bloquea la edición y sugiere desarchivarlo primero.
* **E2:** Si se detecta edición simultánea por otro usuario, el sistema notifica el conflicto y solicita recargar la versión más reciente.

---

### CU5: Archivar documento

* **Descripción:** Permite archivar documentos de eventos finalizados o cancelados, para mantener organizado el repositorio activo sin eliminar la información histórica.
* **Actores:** Administrador
* **Prioridad:** Baja

#### Precondiciones
1. El documento debe corresponder a una reserva finalizada o cancelada.

#### Flujo Normal
1. El Administrador selecciona el documento y elige **'Archivar'**.
2. El sistema solicita confirmación de la acción.
3. El sistema cambia el estado del documento a **'Archivado'** y lo retira del listado activo.

#### Flujos Alternos
* **FA1 — Archivado automático programado:**
  * **1a.** El sistema identifica documentos de eventos finalizados hace más de un periodo definido (por ejemplo, 6 meses).
  * **1b.** El sistema los archiva automáticamente sin intervención del Administrador.

#### Postcondición
El documento queda archivado y disponible únicamente mediante búsqueda avanzada.

#### Excepciones
* **E1:** Si se intenta archivar un documento de una reserva activa, el sistema bloquea la acción y muestra *"No se puede archivar un documento de una reserva activa."*

---

## 💳 Módulo 6 - Gestión Financiera

### CU1: Registrar anticipo

* **Descripción:** Permite al Cliente registrar el pago de un anticipo (abono inicial) para asegurar la reserva de un evento con Elmo Recreaciones.
* **Actores:** Cliente
* **Prioridad:** Alta

#### Precondiciones
1. El Cliente debe estar autenticado.
2. Debe existir una solicitud de reserva aprobada con presupuesto definido.

#### Flujo Normal
1. El Cliente accede al módulo **'Gestión Financiera'** y selecciona la reserva a abonar.
2. El sistema muestra el valor total y el porcentaje mínimo de anticipo requerido.
3. El Cliente ingresa el monto del anticipo y selecciona el método de pago.
4. El sistema procesa el pago mediante la pasarela integrada.
5. El sistema registra el anticipo, actualiza el saldo pendiente y confirma al Cliente.

#### Flujos Alternos
* **FA1 — Pago con tarjeta rechazado:**
  * **4a.** La pasarela rechaza la transacción.
  * **4b.** El sistema notifica el error y permite reintentar u optar por otro método de pago.
* **FA2 — Anticipo menor al mínimo requerido:**
  * **3a.** El sistema detecta que el monto ingresado no cumple el mínimo requerido.
  * **3b.** El sistema advierte al Cliente y solicita ajustar el monto.

#### Postcondición
El anticipo queda registrado, el saldo pendiente actualizado y la reserva pasa a estado **'Anticipo pagado'**.

#### Excepciones
* **E1:** Si la pasarela de pago falla por completo, el sistema muestra *"No fue posible procesar el pago. Intente nuevamente."* y no registra el anticipo.
* **E2:** Si el monto ingresado es menor al mínimo permitido, el sistema bloquea el registro hasta que se corrija.

---

### CU2: Registrar pago

* **Descripción:** Permite al Cliente registrar pagos adicionales (abonos o pago total) sobre el saldo pendiente de su reserva, validando cada transacción mediante **CU2.1**.
* **Actores:** Cliente
* **Prioridad:** Alta

#### Precondiciones
1. El Cliente debe estar autenticado.
2. La reserva debe tener un saldo pendiente mayor a cero.

#### Flujo Normal
1. El Cliente selecciona la reserva y elige **'Registrar pago'**.
2. El sistema muestra el saldo pendiente actual.
3. El Cliente ingresa el monto a pagar y el método de pago.
4. El sistema ejecuta **CU2.1** (*Validar pago*).
5. El sistema registra el pago y actualiza el saldo pendiente.
6. El sistema envía confirmación al Cliente.

#### Flujos Alternos
* **FA1 — Pago total del saldo:**
  * **3a.** El Cliente paga el saldo restante en su totalidad.
  * **3b.** El sistema marca la reserva como **'Pagada en su totalidad'**.
  * **3c.** El flujo continúa desde el paso 4.

#### Postcondición
El pago queda registrado y el saldo pendiente de la reserva actualizado.

#### Excepciones
* **E1:** Si **CU2.1** determina que el pago no es válido, el sistema rechaza el registro y muestra el motivo.
* **E2:** Si el monto ingresado excede el saldo pendiente, el sistema alerta y sugiere ajustar el valor.

---

### CU2.1: Validar pago

* **Descripción:** Subproceso interno, incluido por **CU2**, que valida la transacción con la pasarela de pago y verifica que el monto coincida con lo solicitado antes de registrar el pago.
* **Actores:** Cliente (indirectamente, a través de **CU2**)
* **Prioridad:** Alta

#### Precondiciones
1. **CU2** debe haber sido invocado.

#### Flujo Normal
1. El sistema envía la transacción a la pasarela de pago.
2. La pasarela confirma la aprobación de la transacción.
3. El sistema verifica que el monto coincide con lo solicitado.
4. El sistema retorna el resultado de validación (válido / no válido) a **CU2**.

#### Flujos Alternos
* **FA1 — Confirmación demorada:**
  * **2a.** La pasarela no responde de inmediato.
  * **2b.** El sistema marca el pago como *'pendiente de confirmación'* y notifica al Cliente cuando se confirme.

#### Postcondición
El resultado de la validación queda disponible para que **CU2** registre o rechace el pago.

#### Excepciones
* **E1:** Si la pasarela rechaza la transacción, el sistema retorna *'no válido'* con el motivo del rechazo.
* **E2:** Si ocurre un timeout en la comunicación con la pasarela, el sistema marca el pago como *'pendiente de confirmación'*.

---

### CU3: Consultar saldo pendiente

* **Descripción:** Permite al Cliente y al Administrador consultar el saldo pendiente de pago de una o varias reservas.
* **Actores:** Cliente, Administrador
* **Prioridad:** Media

#### Precondiciones
1. El usuario debe estar autenticado.

#### Flujo Normal
1. El usuario accede al módulo y selecciona la reserva a consultar.
2. El sistema calcula el saldo pendiente (valor total menos pagos registrados).
3. El sistema muestra el saldo pendiente y el historial de pagos asociado.

#### Flujos Alternos
* **FA1 — Consulta consolidada por el Administrador:**
  * **1a.** El Administrador solicita ver los saldos pendientes de todos los clientes.
  * **1b.** El sistema muestra un listado consolidado con filtros por fecha o estado.
  * **1c.** El flujo continúa desde el paso 2, aplicado a cada registro del listado.

#### Postcondición
El saldo pendiente queda mostrado al usuario que realizó la consulta.

#### Excepciones
* **E1:** Si la reserva consultada no existe, el sistema muestra *"Reserva no encontrada."*

---

### CU4: Generar reporte financiero

* **Descripción:** Genera reportes financieros de ingresos, anticipos y saldos pendientes para un periodo determinado, consolidando la información mediante **CU4.1**.
* **Actores:** Administrador
* **Prioridad:** Media

#### Precondiciones
1. El Administrador debe estar autenticado.
2. Deben existir transacciones registradas en el sistema.

#### Flujo Normal
1. El Administrador selecciona el rango de fechas del reporte.
2. El sistema ejecuta **CU4.1** (*Consolidar ingresos*).
3. El sistema genera el reporte con ingresos totales, anticipos y saldos pendientes.
4. El sistema permite exportar el reporte en PDF o Excel.

#### Flujos Alternos
* **FA1 — Reporte filtrado por tipo de servicio:**
  * **1a.** El Administrador aplica un filtro adicional por categoría de servicio.
  * **1b.** El flujo continúa desde el paso 2, con el filtro aplicado.

#### Postcondición
El reporte financiero queda generado y disponible para descarga.

#### Excepciones
* **E1:** Si no existen transacciones en el rango seleccionado, el sistema muestra *"No hay datos para el periodo seleccionado."*

---

### CU4.1: Consolidar ingresos

* **Descripción:** Subproceso interno, incluido por **CU4**, que suma y clasifica todos los ingresos (anticipos, pagos, devoluciones) del periodo seleccionado.
* **Actores:** Administrador (indirectamente, a través de **CU4**)
* **Prioridad:** Media

#### Precondiciones
1. **CU4** debe haber sido invocado.

#### Flujo Normal
1. El sistema recopila todas las transacciones del periodo seleccionado.
2. Clasifica las transacciones por tipo (anticipo, pago).
3. Calcula los totales netos por categoría.
4. Retorna los datos consolidados al proceso **CU4**.

#### Flujos Alternos
* **FA1 — Transacciones con datos incompletos:**
  * **1a.** El sistema detecta una transacción con datos parcialmente registrados.
  * **1b.** La excluye del consolidado y la reporta como pendiente de revisión.

#### Postcondición
Los datos consolidados quedan disponibles para la generación del reporte (**CU4**).

#### Excepciones
* **E1:** Si una transacción presenta datos corruptos, se excluye del consolidado y se reporta al Administrador.

  ## 👥 Módulo 7 - CRM y Fidelización

### CU1: Registrar cliente

* **Descripción:** Permite capturar los datos personales y de contacto de un nuevo cliente en la base de datos de Elmo Recreaciones y vincularlo automáticamente al programa de fidelización (CRM). El registro puede iniciarlo el propio cliente desde la web pública o el Administrador de forma asistida durante un evento presencial.
* **Actores:** Cliente, Administrador
* **Prioridad:** Alta

#### Precondiciones
1. La interfaz pública debe estar disponible.
2. El formulario de registro debe estar habilitado en el sistema.

#### Flujo Normal
1. El cliente selecciona la opción **'Registrarme'** desde la interfaz pública de Elmo Recreaciones.
2. El sistema presenta el formulario con los campos: nombre completo, documento de identidad, correo electrónico y teléfono.
3. El cliente diligencia los datos solicitados y presiona **'Crear cuenta'**.
4. El sistema valida el formato de los campos y verifica que el correo no esté previamente registrado.
5. El sistema crea el registro del cliente en la base de datos y genera automáticamente su perfil CRM con saldo de puntos de fidelización en cero.
6. El sistema envía un correo electrónico de bienvenida con la confirmación del registro.
7. El sistema redirige al cliente a su panel principal (**CU3** del módulo M-01).

#### Flujos Alternos
* **FA1 — Registro asistido por Administrador:**
  * **1a.** El Administrador captura los datos del cliente durante un evento o llamada telefónica.
  * **1b.** El sistema marca el registro como *'creado por Administrador'* y envía las credenciales temporales al correo del cliente.
* **FA2 — Correo ya registrado:**
  * **4a.** El sistema detecta que el correo ingresado ya existe en la base de datos.
  * **4b.** El sistema muestra el mensaje: *"Este correo ya está registrado. Inicie sesión o recupere su contraseña."*

#### Postcondición
El cliente queda registrado en la base de datos de Elmo Recreaciones con un perfil CRM activo, listo para acumular beneficios y recibir campañas.

#### Excepciones
* **E1:** Si el correo tiene un formato inválido, el sistema resalta el campo y no permite continuar.
* **E2:** Si ocurre un error de conexión con la base de datos, el sistema muestra: *"No fue posible completar el registro. Intente nuevamente."*
* **E3:** Si el servicio de correo no está disponible, el registro se completa igualmente y el correo de bienvenida queda en cola de reenvío.

---

### CU2: Consultar historial de eventos

* **Descripción:** Permite al cliente visualizar el listado completo de los eventos, servicios y paquetes contratados previamente con Elmo Recreaciones, incluyendo fechas, montos pagados y estado de cada contrato.
* **Actores:** Cliente
* **Prioridad:** Media

#### Precondiciones
1. El cliente debe tener una sesión activa con Token JWT válido (**CU2** del módulo M-01).

#### Flujo Normal
1. El cliente accede a la opción **'Mi historial de eventos'** desde su panel principal.
2. El sistema consulta en la base de datos todos los contratos asociados al identificador del cliente.
3. El sistema presenta la información ordenada cronológicamente: fecha del evento, tipo de servicio, monto total y estado (finalizado, en curso, cancelado).
4. El cliente puede aplicar filtros por año o por tipo de servicio.
5. El cliente selecciona un evento específico para visualizar el detalle completo del contrato.

#### Flujos Alternos
* **FA1 — Cliente sin historial:**
  * **2a.** El sistema no encuentra contratos asociados al cliente.
  * **2b.** El sistema muestra el mensaje: *"Aún no tiene eventos registrados con Elmo Recreaciones."*

#### Postcondición
El cliente visualiza correctamente su historial de eventos contratados con Elmo Recreaciones.

#### Excepciones
* **E1:** Si ocurre un error al consultar la base de datos, el sistema muestra: *"No fue posible cargar su historial. Intente más tarde."*

---

### CU3: Gestionar promociones

* **Descripción:** Permite al Administrador crear, modificar, activar, desactivar o eliminar promociones y descuentos aplicables a los servicios y paquetes del catálogo de Elmo Recreaciones, con el fin de incentivar nuevas reservas.
* **Actores:** Administrador
* **Prioridad:** Media

#### Precondiciones
1. El Administrador debe contar con sesión activa y permisos CRUD (**CU3.1** del módulo M-01).

#### Flujo Normal
1. El Administrador accede al módulo **'Promociones'** desde su panel de control.
2. El sistema presenta el listado de promociones vigentes y vencidas.
3. El Administrador selecciona **'Nueva promoción'** e ingresa: nombre, porcentaje o valor de descuento, fecha de inicio, fecha de vencimiento y servicios aplicables.
4. El sistema valida que las fechas sean coherentes (inicio anterior a vencimiento).
5. El sistema guarda la promoción y la publica automáticamente en el catálogo web (M-03) mientras esté vigente.

#### Flujos Alternos
* **FA1 — Editar o desactivar promoción existente:**
  * **3a.** El Administrador selecciona una promoción del listado y modifica sus condiciones o la desactiva manualmente.
  * **3b.** El sistema actualiza el registro y refleja el cambio de inmediato en el catálogo público.

#### Postcondición
La promoción queda registrada y visible en el catálogo de Elmo Recreaciones durante el periodo de vigencia definido.

#### Excepciones
* **E1:** Si la fecha de inicio es posterior a la de vencimiento, el sistema rechaza el guardado y resalta los campos.
* **E2:** El sistema desactiva automáticamente cualquier promoción cuya fecha de vencimiento ya haya pasado.

---

### CU4: Asignar beneficios

* **Descripción:** Permite al Administrador otorgar beneficios de fidelización (puntos adicionales, descuentos VIP o regalos) a un cliente específico con base en su historial de compras. Este caso de uso incluye **CU4.1** (*Verificar historial de compras*) para determinar la elegibilidad del cliente.
* **Actores:** Administrador
* **Prioridad:** Media

#### Precondiciones
1. El cliente debe estar registrado en el sistema CRM de Elmo Recreaciones.

#### Flujo Normal
1. El Administrador busca al cliente por nombre, documento o correo electrónico.
2. El sistema invoca **CU4.1** (*Verificar historial de compras*) y presenta el resumen de eventos contratados y monto acumulado.
3. El Administrador selecciona el tipo de beneficio a otorgar: puntos extra, descuento porcentual o regalo especial.
4. El sistema registra el beneficio en el perfil CRM del cliente.
5. El sistema envía una notificación al cliente informando el beneficio asignado (integración con M-08).

#### Flujos Alternos
* **FA1 — Cliente no cumple el mínimo de compras:**
  * **2a.** El sistema advierte al Administrador que el cliente no alcanza el umbral configurado para el beneficio solicitado.
  * **2b.** El Administrador puede continuar de forma manual o cancelar la asignación.

#### Postcondición
El beneficio queda registrado en el perfil CRM del cliente y disponible para su próxima reserva.

#### Excepciones
* **E1:** Si el cliente no existe en la base de datos, el sistema muestra: *"Cliente no encontrado."*

---

### CU4.1: Verificar historial de compras

* **Descripción:** Sub-caso de uso incluido automáticamente por **CU4**. Consulta el historial completo de contratos y montos pagados por un cliente en Elmo Recreaciones para determinar su elegibilidad frente a los criterios de beneficios configurados (frecuencia, monto acumulado, antigüedad).
* **Actores:** Sistema (ejecutado internamente al invocar **CU4**).
* **Prioridad:** Media

#### Precondiciones
1. El cliente debe tener al menos un registro en la tabla de contratos.

#### Flujo Normal
1. El sistema recibe el identificador del cliente desde **CU4**.
2. El sistema consulta la totalidad de contratos asociados al cliente y suma los montos pagados.
3. El sistema calcula indicadores de elegibilidad: número de eventos, gasto total y antigüedad como cliente.
4. El sistema retorna el resultado a **CU4** para su presentación al Administrador.

#### Flujos Alternos
* *No aplica*.

#### Postcondición
El Administrador cuenta con la información necesaria para decidir sobre la asignación de beneficios.

#### Excepciones
* **E1:** Si ocurre un error de consulta a la base de datos, el sistema retorna un historial vacío y registra el incidente en el log.

---

### CU5: Enviar campañas

* **Descripción:** Permite al Administrador crear y enviar campañas de marketing y fidelización (correo electrónico o notificación) dirigidas a segmentos específicos de clientes de Elmo Recreaciones. Este caso de uso incluye **CU5.1** (*Seleccionar clientes objetivo*).
* **Actores:** Administrador
* **Prioridad:** Baja

#### Precondiciones
1. Debe existir al menos un cliente registrado en el sistema.
2. El servicio de envío de correos/notificaciones debe estar operativo.

#### Flujo Normal
1. El Administrador accede al módulo **'Campañas'** y selecciona **'Nueva campaña'**.
2. El Administrador redacta el asunto, contenido y adjunta imágenes promocionales si aplica.
3. El sistema invoca **CU5.1** para que el Administrador defina el segmento de clientes objetivo.
4. El Administrador confirma el envío inmediato o programa una fecha futura.
5. El sistema envía la campaña a los clientes seleccionados mediante correo o notificación push.
6. El sistema registra métricas básicas de envío (enviados, fallidos).

#### Flujos Alternos
* **FA1 — Envío programado:**
  * **4a.** El Administrador selecciona una fecha y hora futura para el envío.
  * **4b.** El sistema almacena la campaña en cola y la ejecuta automáticamente en el momento programado.

#### Postcondición
La campaña queda enviada o programada, y las métricas de envío quedan disponibles para el Administrador.

#### Excepciones
* **E1:** Si el segmento seleccionado no contiene clientes, el sistema impide el envío y muestra: *"No hay destinatarios seleccionados."*
* **E2:** Si el servicio de envío falla, el sistema reintenta y registra los correos no entregados.

---

### CU5.1: Seleccionar clientes objetivo

* **Descripción:** Sub-caso de uso incluido por **CU5**. Permite filtrar y segmentar la base de clientes de Elmo Recreaciones según criterios como frecuencia de compra, fecha del último evento, ubicación o proximidad de cumpleaños, con el fin de dirigir campañas personalizadas.
* **Actores:** Administrador
* **Prioridad:** Baja

#### Precondiciones
1. Debe existir información suficiente en el CRM para aplicar los filtros de segmentación.

#### Flujo Normal
1. El sistema presenta los filtros disponibles: frecuencia de compra, última fecha de contratación, ubicación y cumpleaños próximo.
2. El Administrador combina uno o varios filtros según el objetivo de la campaña.
3. El sistema calcula y muestra el número de clientes que cumplen los criterios.
4. El Administrador confirma la selección y el sistema retorna el listado a **CU5**.

#### Flujos Alternos
* *No aplica*.

#### Postcondición
El segmento de clientes objetivo queda definido para su uso en el envío de la campaña.

#### Excepciones
* **E1:** Si ningún cliente cumple los filtros aplicados, el sistema sugiere ampliar los criterios de búsqueda.

---

## 🔔 Módulo 8 - Notificaciones y Asistencia Automática

### CU1: Enviar notificación

* **Descripción:** Permite generar y despachar notificaciones (correo electrónico y/o push) hacia Clientes o Recreadores de Elmo Recreaciones, ya sea de forma manual por parte de un usuario autorizado o de forma automática desde otros procesos del sistema (confirmaciones, recordatorios, novedades).
* **Actores:** Cliente, Recreador
* **Prioridad:** Alta

#### Precondiciones
1. El destinatario debe tener un canal de contacto válido registrado (correo o dispositivo con notificaciones push habilitadas).

#### Flujo Normal
1. El sistema o el usuario que origina el evento solicita el envío de una notificación, indicando el destinatario, el tipo de mensaje y el contenido.
2. El sistema valida que el destinatario tenga un canal de contacto activo.
3. El sistema construye el mensaje según la plantilla correspondiente al tipo de notificación.
4. El sistema envía la notificación por el canal disponible (correo, push o ambos).
5. El sistema registra el envío en el log de notificaciones con fecha, hora y estado.

#### Flujos Alternos
* **FA1 — Envío múltiple (broadcast):**
  * **1a.** El origen de la solicitud indica una lista de destinatarios en lugar de uno solo.
  * **1b.** El sistema itera el envío para cada destinatario y consolida el resultado.

#### Postcondición
La notificación queda entregada al destinatario y registrada en el historial del sistema.

#### Excepciones
* **E1:** Si el destinatario no tiene canal de contacto válido, el sistema descarta el envío y registra la incidencia.
* **E2:** Si el servicio de correo o push falla, el sistema reintenta hasta 3 veces antes de marcar el envío como fallido.

---

### CU2: Recibir alerta

* **Descripción:** Permite a Clientes y Recreadores visualizar dentro de la plataforma las alertas y notificaciones que Elmo Recreaciones les ha enviado, tales como confirmaciones de reserva, recordatorios de eventos próximos o novedades operativas.
* **Actores:** Cliente, Recreador
* **Prioridad:** Alta

#### Precondiciones
1. El usuario debe tener sesión activa en la plataforma.

#### Flujo Normal
1. El usuario ingresa a su panel de control y visualiza el icono de campana con el contador de alertas nuevas.
2. El usuario selecciona el icono de alertas.
3. El sistema presenta el listado de notificaciones recibidas, ordenadas de la más reciente a la más antigua.
4. El usuario selecciona una alerta para ver su detalle y marcarla como leída.

#### Flujos Alternos
* **FA1 — Sin alertas pendientes:**
  * **3a.** El sistema muestra el mensaje: *"No tiene notificaciones nuevas por el momento."*

#### Postcondición
El usuario queda informado de las novedades relevantes de Elmo Recreaciones asociadas a su cuenta.

#### Excepciones
* **E1:** Si falla la carga del listado de alertas, el sistema muestra un mensaje de error y permite reintentar.

---

### CU3: Confirmar reserva

* **Descripción:** Permite al cliente confirmar de manera explícita una solicitud de reserva previamente aprobada por Elmo Recreaciones, garantizando su participación en el evento agendado. Este caso de uso incluye **CU3.1** (*Enviar notificación*) para avisar a las partes involucradas.
* **Actores:** Cliente
* **Prioridad:** Alta

#### Precondiciones
1. La reserva debe encontrarse en estado **'Aprobada'** y pendiente de confirmación por parte del cliente.

#### Flujo Normal
1. El cliente recibe una alerta indicando que su reserva está lista para confirmación.
2. El cliente accede al detalle de la reserva y revisa fecha, hora y servicios contratados.
3. El cliente presiona el botón **'Confirmar reserva'**.
4. El sistema actualiza el estado de la reserva a **'Confirmada'**.
5. El sistema invoca **CU3.1** para notificar al Recreador asignado y al Administrador sobre la confirmación.

#### Flujos Alternos
* **FA1 — Cliente no confirma dentro del plazo:**
  * **1a.** El sistema detecta que ha vencido el plazo establecido para confirmar.
  * **1b.** El sistema marca la reserva como *'Pendiente de revisión'* y notifica al Administrador.

#### Postcondición
La reserva queda formalmente confirmada y las partes involucradas notificadas.

#### Excepciones
* **E1:** Si la reserva ya fue cancelada previamente, el sistema no permite la confirmación y muestra el estado actual.

---

### CU3.1: Enviar notificación

* **Descripción:** Sub-caso de uso incluido por **CU3**. Envía automáticamente una notificación al Recreador asignado y al Administrador informando que el cliente confirmó su reserva en Elmo Recreaciones.
* **Actores:** Sistema (ejecutado internamente al invocar **CU3**).
* **Prioridad:** Alta

#### Precondiciones
1. La reserva debe haber cambiado a estado **'Confirmada'**.

#### Flujo Normal
1. El sistema recibe el identificador de la reserva confirmada desde **CU3**.
2. El sistema identifica al Recreador asignado y al Administrador responsable.
3. El sistema envía la notificación de confirmación a ambos destinatarios (reutilizando **CU1**).

#### Flujos Alternos
* *No aplica*.

#### Postcondición
El Recreador y el Administrador quedan informados de la confirmación de la reserva.

#### Excepciones
* **E1:** Si aún no se ha asignado un Recreador, la notificación se envía únicamente al Administrador.

---

### CU4: Recordar evento próximo

* **Descripción:** Genera de forma automática recordatorios para Recreadores y Administradores sobre los eventos próximos a realizarse, con el fin de asegurar la preparación logística oportuna. Este caso de uso incluye **CU4.1** (*Consultar calendario*).
* **Actores:** Recreador, Administrador
* **Prioridad:** Media

#### Precondiciones
1. Debe existir un proceso programado (tarea periódica) que revise los eventos próximos.

#### Flujo Normal
1. El sistema ejecuta la tarea programada diaria de revisión de eventos próximos.
2. El sistema invoca **CU4.1** para consultar el calendario de eventos dentro de las siguientes 48 horas.
3. El sistema identifica los eventos próximos y sus responsables (Recreador asignado, Administrador).
4. El sistema genera y envía un recordatorio a cada responsable con los detalles del evento (fecha, hora, dirección, temática).

#### Flujos Alternos
* **FA1 — Evento sin Recreador asignado:**
  * **3a.** El sistema detecta que el evento próximo no tiene Recreador asignado.
  * **3b.** El sistema envía una alerta prioritaria al Administrador para gestionar la asignación.

#### Postcondición
Los responsables de los eventos próximos quedan notificados con la anticipación configurada.

#### Excepciones
* **E1:** Si la tarea programada falla, el sistema registra el error en el log para revisión manual.

---

### CU4.1: Consultar calendario

* **Descripción:** Sub-caso de uso incluido por **CU4**. Consulta en la base de datos de Elmo Recreaciones los eventos programados dentro de un rango de fechas determinado, con sus responsables y detalles logísticos.
* **Actores:** Sistema (ejecutado internamente al invocar **CU4**).
* **Prioridad:** Media

#### Precondiciones
1. El módulo de agenda y calendario debe estar operativo.

#### Flujo Normal
1. El sistema recibe el rango de fechas a consultar desde **CU4**.
2. El sistema consulta los eventos programados dentro de dicho rango.
3. El sistema retorna el listado de eventos con su Recreador asignado, dirección y hora a **CU4**.

#### Flujos Alternos
* *No aplica*.

#### Postcondición
**CU4** dispone de la información necesaria para generar los recordatorios correspondientes.

#### Excepciones
* **E1:** Si no hay eventos en el rango consultado, el sistema retorna una lista vacía sin generar error.

---

### CU5: Responder consulta automática

* **Descripción:** Permite al sistema, bajo configuración del Administrador, responder de forma automática preguntas frecuentes de los clientes (horarios de atención, disponibilidad general, formas de pago) mediante un asistente de respuestas predefinidas.
* **Actores:** Administrador
* **Prioridad:** Baja

#### Precondiciones
1. El Administrador debe haber configurado previamente el catálogo de preguntas y respuestas frecuentes.

#### Flujo Normal
1. El cliente envía una consulta a través del canal habilitado (chat web o correo).
2. El sistema analiza el mensaje y lo compara contra el catálogo de preguntas frecuentes configurado.
3. El sistema identifica una coincidencia y responde automáticamente con la información predefinida.
4. El sistema registra la interacción para su posterior revisión por el Administrador.

#### Flujos Alternos
* **FA1 — Sin coincidencia encontrada:**
  * **2a.** El sistema no identifica una respuesta predefinida adecuada.
  * **2b.** El sistema informa al cliente que su consulta será atendida por un Administrador y genera un ticket de seguimiento.

#### Postcondición
El cliente recibe una respuesta inmediata o, en su defecto, su consulta queda registrada para atención manual.

#### Excepciones
* **E1:** Si el catálogo de preguntas frecuentes no está configurado, el sistema deriva automáticamente al Administrador.

  ## 📱 Módulo 9 - Digitalización de Operaciones (Paperless)

### CU1: Registrar asistencia digital

* **Descripción:** Permite al Recreador registrar digitalmente su llegada e inicio de actividades en el lugar del evento de Elmo Recreaciones, eliminando el uso de formatos físicos de asistencia.
* **Actores:** Recreador
* **Prioridad:** Alta

#### Precondiciones
1. El Recreador debe tener sesión activa y un evento asignado para la fecha en curso.

#### Flujo Normal
1. El Recreador accede a su agenda del día desde la aplicación móvil o web.
2. El Recreador selecciona el evento en curso y presiona **'Registrar llegada'**.
3. El sistema captura la geolocalización y la marca de tiempo del registro.
4. El sistema almacena el registro de asistencia asociado al contrato correspondiente.
5. El sistema confirma al Recreador: *"Asistencia registrada correctamente."*

#### Flujos Alternos
* **FA1 — Registro fuera del rango de ubicación esperado:**
  * **3a.** El sistema detecta que la geolocalización difiere significativamente de la dirección del evento.
  * **3b.** El sistema permite el registro, pero lo marca como *'observación de ubicación'* para revisión del Administrador.

#### Postcondición
La asistencia del Recreador queda registrada digitalmente y disponible dentro del acta del evento (**CU4**).

#### Excepciones
* **E1:** Si el dispositivo no tiene conexión a internet, el sistema almacena el registro localmente y lo sincroniza al recuperar la señal.

---

### CU2: Adjuntar evidencia fotográfica

* **Descripción:** Permite al Recreador capturar y adjuntar fotografías del montaje, desarrollo o finalización del evento, como evidencia digital del cumplimiento del servicio contratado con Elmo Recreaciones.
* **Actores:** Recreador
* **Prioridad:** Media

#### Precondiciones
1. El Recreador debe tener acceso al evento en curso y permisos de cámara/almacenamiento habilitados en su dispositivo.

#### Flujo Normal
1. El Recreador selecciona la opción **'Adjuntar evidencia'** dentro del evento en curso.
2. El Recreador captura una o varias fotografías desde la cámara del dispositivo o las selecciona de su galería.
3. El sistema comprime y sube las imágenes al servidor, asociándolas al contrato correspondiente.
4. El sistema confirma la carga exitosa de las imágenes.

#### Flujos Alternos
* **FA1 — Carga en segundo plano:**
  * **3a.** Si la conexión es lenta, el sistema continúa la carga en segundo plano mientras el Recreador sigue trabajando.

#### Postcondición
Las fotografías quedan almacenadas como evidencia del evento y disponibles para el acta digital (**CU4**).

#### Excepciones
* **E1:** Si el formato o tamaño de la imagen no es compatible, el sistema rechaza el archivo e indica el motivo.
* **E2:** Si falla la carga por pérdida de conexión, el sistema reintenta automáticamente al restablecerse la red.

---

### CU3: Firmar documento digitalmente

* **Descripción:** Permite al Recreador (y opcionalmente al cliente presente en el evento) firmar digitalmente el documento de conformidad del servicio prestado por Elmo Recreaciones, reemplazando la firma física en papel.
* **Actores:** Recreador
* **Prioridad:** Media

#### Precondiciones
1. El evento debe estar marcado como finalizado o próximo a finalizar.

#### Flujo Normal
1. El Recreador selecciona **'Firmar documento'** al concluir el servicio.
2. El sistema presenta el resumen del servicio prestado para revisión.
3. El Recreador y/o el cliente estampan su firma digital sobre la pantalla táctil del dispositivo.
4. El sistema almacena la firma junto con la fecha y hora de captura, vinculada al contrato.

#### Flujos Alternos
* **FA1 — Cliente no disponible para firmar:**
  * **3a.** El sistema permite continuar únicamente con la firma del Recreador y marca el documento como *'pendiente de firma del cliente'*.

#### Postcondición
El documento de conformidad queda firmado digitalmente y disponible dentro del acta del evento.

#### Excepciones
* **E1:** Si la firma capturada no cumple el mínimo de trazos requeridos, el sistema solicita repetir el proceso.

---

### CU4: Generar acta digital

* **Descripción:** Permite al Administrador consolidar en un acta digital única toda la información operativa de un evento de Elmo Recreaciones: asistencia del Recreador, evidencia fotográfica y firma de conformidad. Este caso de uso incluye **CU4.1** (*Registrar asistencia*) y **CU4.2** (*Adjuntar evidencia*).
* **Actores:** Administrador
* **Prioridad:** Alta

#### Precondiciones
1. El evento debe contar con al menos el registro de asistencia del Recreador asignado.

#### Flujo Normal
1. El Administrador selecciona el evento finalizado desde el módulo de operaciones.
2. El sistema invoca **CU4.1** para incorporar el registro de asistencia y **CU4.2** para incorporar la evidencia fotográfica.
3. El sistema compila automáticamente la información en un documento de acta digital (PDF), incluyendo la firma capturada en **CU3**.
4. El Administrador revisa el acta generada y la aprueba.
5. El sistema almacena el acta en el historial de operaciones del evento (**CU5**).

#### Flujos Alternos
* **FA1 — Información incompleta:**
  * **2a.** El sistema detecta que falta evidencia fotográfica o firma.
  * **2b.** El sistema genera el acta marcándola como *'incompleta'* y notifica al Administrador para su seguimiento.

#### Postcondición
El acta digital del evento queda generada, almacenada y disponible para consulta futura, eliminando el uso de papel.

#### Excepciones
* **E1:** Si el evento no tiene registros asociados, el sistema no permite generar el acta y muestra un mensaje informativo.

---

### CU4.1: Registrar asistencia

* **Descripción:** Sub-caso de uso incluido por **CU4**. Recupera el registro de asistencia digital previamente capturado por el Recreador (**CU1**) para incorporarlo al acta digital del evento.
* **Actores:** Sistema (ejecutado internamente al invocar **CU4**)
* **Prioridad:** Alta

#### Precondiciones
1. Debe existir un registro de asistencia previo asociado al evento.

#### Flujo Normal
1. El sistema consulta el registro de asistencia asociado al identificador del evento.
2. El sistema retorna la fecha, hora y geolocalización del registro a **CU4**.

#### Flujos Alternos
* *No aplica*.

#### Postcondición
El acta digital incorpora el registro de asistencia verificado.

#### Excepciones
* **E1:** Si no existe registro de asistencia, el sistema retorna un campo vacío y lo señala como pendiente.

---

### CU4.2: Adjuntar evidencia

* **Descripción:** Sub-caso de uso incluido por **CU4**. Recupera las fotografías previamente cargadas por el Recreador (**CU2**) para incorporarlas como anexos visuales del acta digital del evento.
* **Actores:** Sistema (ejecutado internamente al invocar **CU4**)
* **Prioridad:** Media

#### Precondiciones
1. Debe existir al menos una fotografía cargada asociada al evento.

#### Flujo Normal
1. El sistema consulta las imágenes almacenadas asociadas al identificador del evento.
2. El sistema incorpora las imágenes como anexos dentro del documento de acta digital generado por **CU4**.

#### Flujos Alternos
* *No aplica*.

#### Postcondición
El acta digital incorpora la evidencia fotográfica disponible del evento.

#### Excepciones
* **E1:** Si no existen fotografías cargadas, el sistema genera el acta sin anexos visuales y lo señala como pendiente.

---

### CU5: Consultar historial de operaciones

* **Descripción:** Permite al Administrador consultar y filtrar el historial completo de actas digitales generadas para los eventos realizados por Elmo Recreaciones, facilitando la trazabilidad operativa sin uso de archivos físicos.
* **Actores:** Administrador
* **Prioridad:** Media

#### Precondiciones
1. Debe existir al menos un acta digital generada en el sistema.

#### Flujo Normal
1. El Administrador accede al módulo **'Historial de operaciones'**.
2. El sistema presenta el listado de actas digitales generadas, ordenadas por fecha del evento.
3. El Administrador aplica filtros por Recreador, cliente, rango de fechas o estado del acta (completa/incompleta).
4. El Administrador selecciona un acta para visualizar o descargar el documento en PDF.

#### Flujos Alternos
* **FA1 — Exportación masiva:**
  * **3a.** El Administrador selecciona múltiples actas y solicita su exportación en un solo archivo comprimido.

#### Postcondición
El Administrador obtiene la información operativa histórica requerida para auditoría o análisis de calidad del servicio.

#### Excepciones
* **E1:** Si no existen actas que cumplan los filtros aplicados, el sistema muestra un listado vacío.

---

## ⚙️ Módulo 10 - Administración Avanzada y Ajustes

### CU1: Gestionar usuarios

* **Descripción:** Permite al Administrador administrar de forma centralizada las cuentas de usuario del sistema de Elmo Recreaciones (Clientes, Recreadores y Administradores). Este caso de uso incluye **CU1.1** (*Crear usuario*), **CU1.2** (*Modificar usuario*) y **CU1.3** (*Eliminar usuario*).
* **Actores:** Administrador
* **Prioridad:** Alta

#### Precondiciones
1. El Administrador debe contar con sesión activa y permisos CRUD globales.

#### Flujo Normal
1. El Administrador accede al módulo **'Gestión de usuarios'** desde su panel de control.
2. El sistema presenta el listado completo de usuarios con su rol y estado (activo/inactivo).
3. El Administrador selecciona la acción a realizar: crear (**CU1.1**), modificar (**CU1.2**) o eliminar (**CU1.3**) un usuario.
4. El sistema ejecuta el sub-caso de uso correspondiente y actualiza el listado general.

#### Flujos Alternos
* **FA1 — Búsqueda de usuario específico:**
  * **2a.** El Administrador utiliza el buscador para filtrar por nombre, correo o rol antes de seleccionar la acción.

#### Postcondición
El listado de usuarios de Elmo Recreaciones queda actualizado según la acción ejecutada.

#### Excepciones
* **E1:** Si ocurre un error al consultar la base de datos, el sistema muestra: *"No fue posible cargar el listado de usuarios."*

---

### CU1.1: Crear usuario

* **Descripción:** Sub-caso de uso incluido por **CU1**. Permite al Administrador registrar manualmente un nuevo usuario en el sistema (típicamente Recreador o Administrador adicional), asignándole rol y credenciales iniciales.
* **Actores:** Administrador
* **Prioridad:** Alta

#### Precondiciones
1. El correo electrónico del nuevo usuario no debe existir previamente en el sistema.

#### Flujo Normal
1. El Administrador presiona **'Nuevo usuario'** e ingresa nombre completo, correo electrónico y rol a asignar.
2. El sistema genera una contraseña temporal y valida que el correo no esté duplicado.
3. El sistema crea el registro del usuario con estado 'activo' y el rol seleccionado.
4. El sistema envía las credenciales de acceso al correo del nuevo usuario.

#### Flujos Alternos
* *No aplica*.

#### Postcondición
El nuevo usuario queda creado y habilitado para iniciar sesión en la plataforma de Elmo Recreaciones.

#### Excepciones
* **E1:** Si el correo ya está registrado, el sistema rechaza la creación y muestra el mensaje correspondiente.

---

### CU1.2: Modificar usuario

* **Descripción:** Sub-caso de uso incluido por **CU1**. Permite al Administrador editar los datos, el rol o el estado (activo/inactivo) de un usuario existente del sistema.
* **Actores:** Administrador
* **Prioridad:** Media

#### Precondiciones
1. El usuario a modificar debe existir en la base de datos.

#### Flujo Normal
1. El Administrador selecciona un usuario del listado y presiona **'Editar'**.
2. El sistema presenta el formulario precargado con los datos actuales del usuario.
3. El Administrador modifica los campos requeridos (datos de contacto, rol o estado).
4. El sistema valida y guarda los cambios, actualizando el registro en la base de datos.

#### Flujos Alternos
* **FA1 — Cambio de rol:**
  * **3a.** El Administrador cambia el rol asignado al usuario (por ejemplo, de Recreador a Administrador).
  * **3b.** El sistema invalida el Token JWT actual del usuario afectado, obligándolo a iniciar sesión nuevamente con el nuevo rol.

#### Postcondición
Los datos del usuario quedan actualizados en el sistema.

#### Excepciones
* **E1:** Si el usuario intenta desactivar su propia cuenta de Administrador, el sistema lo impide por seguridad.

---

### CU1.3: Eliminar usuario

* **Descripción:** Sub-caso de uso incluido por **CU1**. Permite al Administrador eliminar o desactivar de forma permanente una cuenta de usuario del sistema de Elmo Recreaciones.
* **Actores:** Administrador
* **Prioridad:** Media

#### Precondiciones
1. El usuario a eliminar debe existir y no debe ser la cuenta del Administrador que ejecuta la acción.

#### Flujo Normal
1. El Administrador selecciona un usuario del listado y presiona **'Eliminar'**.
2. El sistema solicita confirmación indicando las consecuencias de la acción.
3. El Administrador confirma la eliminación.
4. El sistema desactiva o elimina lógicamente el registro del usuario y revoca sus tokens de acceso activos.

#### Flujos Alternos
* **FA1 — Usuario con contratos vigentes:**
  * **2a.** El sistema detecta que el usuario (cliente) tiene contratos activos.
  * **2b.** El sistema desactiva la cuenta en lugar de eliminarla físicamente, preservando la integridad del historial.

#### Postcondición
El usuario queda eliminado o desactivado y no puede volver a iniciar sesión en el sistema.

#### Excepciones
* **E1:** Si el Administrador intenta eliminar su propia cuenta, el sistema rechaza la acción.

---

### CU2: Gestionar roles

* **Descripción:** Permite al Administrador definir y mantener los roles disponibles en el sistema de Elmo Recreaciones (Administrador, Recreador, Cliente) y sus características generales. Este caso de uso incluye **CU2.1** (*Asignar permisos*).
* **Actores:** Administrador
* **Prioridad:** Alta

#### Precondiciones
1. El Administrador debe contar con sesión activa y permisos CRUD globales.

#### Flujo Normal
1. El Administrador accede al módulo **'Gestión de roles'**.
2. El sistema presenta el listado de roles configurados en el sistema.
3. El Administrador crea un nuevo rol o selecciona uno existente para editarlo.
4. El sistema invoca **CU2.1** para definir o modificar los permisos asociados al rol.
5. El sistema guarda la configuración del rol.

#### Flujos Alternos
* *No aplica*.

#### Postcondición
Los roles del sistema quedan configurados y disponibles para su asignación a los usuarios.

#### Excepciones
* **E1:** Si se intenta eliminar un rol base del sistema (Administrador, Recreador o Cliente), el sistema lo impide.

---

### CU2.1: Asignar permisos

* **Descripción:** Sub-caso de uso incluido por **CU2**. Permite al Administrador definir, para cada rol, los módulos y acciones (lectura, escritura, actualización, eliminación) a los que tendrán acceso los usuarios asociados a dicho rol.
* **Actores:** Administrador
* **Prioridad:** Alta

#### Precondiciones
1. El rol al cual se le asignarán permisos debe existir previamente.

#### Flujo Normal
1. El sistema presenta la matriz de módulos disponibles junto con las acciones CRUD posibles para cada uno.
2. El Administrador marca o desmarca los permisos correspondientes al rol seleccionado.
3. El sistema valida la configuración y la guarda en la matriz de permisos de la base de datos.

#### Flujos Alternos
* *No aplica*.

#### Postcondición
La matriz de permisos del rol queda actualizada y será aplicada en la siguiente validación de acceso (**CU3.1** del módulo M-01).

#### Excepciones
* **E1:** Si se intenta remover todos los permisos del rol Administrador, el sistema lo impide para evitar bloquear la administración del sistema.

---

### CU3: Configurar parámetros del sistema

* **Descripción:** Permite al Administrador ajustar parámetros generales de operación de la plataforma de Elmo Recreaciones, tales como tiempos de expiración de sesión, porcentaje mínimo de abono, tiempos de vigencia de tokens de recuperación, y datos generales de la empresa.
* **Actores:** Administrador
* **Prioridad:** Media

#### Precondiciones
1. El Administrador debe contar con sesión activa y permisos CRUD globales.

#### Flujo Normal
1. El Administrador accede al módulo **'Configuración del sistema'**.
2. El sistema presenta los parámetros actuales organizados por categoría (seguridad, pagos, notificaciones, datos generales).
3. El Administrador modifica los valores requeridos.
4. El sistema valida los rangos permitidos para cada parámetro y guarda los cambios.
5. El sistema aplica la nueva configuración de forma inmediata en los módulos correspondientes.

#### Flujos Alternos
* *No aplica*.

#### Postcondición
Los parámetros generales del sistema quedan actualizados y vigentes para toda la plataforma.

#### Excepciones
* **E1:** Si un valor ingresado está fuera del rango permitido, el sistema rechaza el cambio e indica el rango válido.

---

### CU4: Realizar copias de seguridad

* **Descripción:** Permite al Administrador generar manualmente una copia de seguridad completa de la base de datos de Elmo Recreaciones, como complemento a las copias automáticas programadas del sistema.
* **Actores:** Administrador
* **Prioridad:** Alta

#### Precondiciones
1. El servicio de almacenamiento de respaldos debe estar disponible y con espacio suficiente.

#### Flujo Normal
1. El Administrador accede al módulo **'Copias de seguridad'** y selecciona **'Generar respaldo ahora'**.
2. El sistema solicita confirmación indicando el tamaño estimado del respaldo.
3. El Administrador confirma la acción.
4. El sistema genera el archivo de respaldo de la base de datos y lo almacena en el repositorio configurado.
5. El sistema notifica al Administrador la finalización exitosa del proceso, indicando fecha, hora y tamaño del archivo.

#### Flujos Alternos
* **FA1 — Respaldo automático programado:**
  * **1a.** El sistema ejecuta automáticamente el respaldo según la periodicidad configurada, sin intervención del Administrador.

#### Postcondición
Queda disponible un nuevo archivo de respaldo de la base de datos de Elmo Recreaciones para su eventual restauración (**CU5**).

#### Excepciones
* **E1:** Si no hay espacio suficiente en el repositorio de respaldos, el sistema cancela el proceso y notifica al Administrador.
* **E2:** Si el proceso se interrumpe, el sistema descarta el archivo parcial y registra el error en el log.

---

### CU5: Restaurar respaldo

* **Descripción:** Permite al Administrador restaurar la base de datos de Elmo Recreaciones a partir de un archivo de respaldo previamente generado, en caso de pérdida de información o fallo crítico del sistema.
* **Actores:** Administrador
* **Prioridad:** Alta

#### Precondiciones
1. Debe existir al menos un archivo de respaldo válido disponible en el repositorio.

#### Flujo Normal
1. El Administrador accede al módulo **'Copias de seguridad'** y selecciona **'Restaurar respaldo'**.
2. El sistema presenta el listado de respaldos disponibles con su fecha de generación.
3. El Administrador selecciona el respaldo deseado y confirma la restauración, aceptando la advertencia de sobrescritura de datos actuales.
4. El sistema pone la plataforma en modo mantenimiento y ejecuta el proceso de restauración.
5. El sistema confirma la finalización exitosa y reactiva el acceso normal a la plataforma.

#### Flujos Alternos
* *No aplica*.

#### Postcondición
La base de datos de Elmo Recreaciones queda restaurada al estado correspondiente al respaldo seleccionado.

#### Excepciones
* **E1:** Si el archivo de respaldo está corrupto o incompleto, el sistema cancela la restauración y conserva el estado anterior de la base de datos.
* **E2:** Si el proceso se interrumpe por fallo de energía o conexión, el sistema queda en modo mantenimiento hasta que el Administrador reintente la restauración.

---

### CU6: Consultar auditoría

* **Descripción:** Permite al Administrador consultar el registro histórico (log) de auditoría de las acciones críticas realizadas por los usuarios en el sistema de Elmo Recreaciones, tales como inicios de sesión, cambios de permisos, eliminaciones de usuarios y restauraciones de respaldo.
* **Actores:** Administrador
* **Prioridad:** Media

#### Precondiciones
1. El módulo de auditoría debe estar habilitado y registrando eventos del sistema.

#### Flujo Normal
1. El Administrador accede al módulo **'Auditoría'** desde su panel de control.
2. El sistema presenta el registro de eventos ordenados cronológicamente, indicando usuario, acción realizada, fecha y hora.
3. El Administrador aplica filtros por usuario, tipo de acción o rango de fechas.
4. El Administrador selecciona un evento para ver su detalle completo.

#### Flujos Alternos
* **FA1 — Exportar reporte de auditoría:**
  * **3a.** El Administrador solicita exportar el listado filtrado en formato PDF o Excel para fines de control interno.

#### Postcondición
El Administrador obtiene la trazabilidad completa de las acciones críticas realizadas en la plataforma.

#### Excepciones
* **E1:** Si no existen eventos que cumplan los filtros aplicados, el sistema muestra un listado vacío.

  ## 📜 Catálogo de Reglas de Negocio

| ID | Nombre | Descripción |
| :--- | :--- | :--- |
| **RN-01** | **Disponibilidad de conexión a base de datos / repositorio** | Si el sistema pierde la conexión con la base de datos o el repositorio durante una operación crítica (guardar, consultar, buscar), la operación se cancela sin dejar cambios parciales y se informa al usuario que debe reintentar. |
| **RN-02** | **Autenticación y sesión activa (Token JWT)** | Toda acción que module datos del negocio requiere que el usuario tenga una sesión activa con token JWT válido; si el token es inválido o expiró, el sistema exige reautenticación antes de continuar. |
| **RN-03** | **Validación de permisos según el rol asignado** | Cada acción del sistema se valida contra los permisos del rol del usuario autenticado (Cliente, Recreador, Administrador); si el rol no autoriza la acción, el sistema la bloquea y no expone datos ni funciones fuera de su alcance. |
| **RN-04** | **Indisponibilidad de servicios externos y reintento** | Cuando el sistema depende de un servicio externo (SMTP, pasarela de pago, hosting, generación de JWT) y este no responde, el sistema informa la indisponibilidad y, cuando aplica, reintenta automáticamente antes de marcar la operación como fallida. |
| **RN-05** | **Formato y tamaño válido de archivos adjuntos** | Todo archivo adjuntado al sistema (imagen, evidencia) debe cumplir con el formato y tamaño permitido; de lo contrario, se rechaza indicando el motivo. |
| **RN-06** | **Trabajo sin conexión y sincronización posterior** | Las acciones realizadas en campo sin conexión a internet se almacenan localmente en el dispositivo y se sincronizan automáticamente al recuperar la señal, sin pérdida de información. |
| **RN-07** | **Manejo de recurso o registro no encontrado** | Si una consulta o búsqueda no encuentra resultados (registro, historial, documento), el sistema retorna una respuesta vacía o informativa, sin generar un error bloqueante. |
| **RN-08** | **Validación de valores ingresados manualmente** | Todo valor ingresado manualmente por un usuario (montos, fechas, ajustes) se valida antes de procesarse; valores negativos, no numéricos o fechas inválidas se rechazan con un mensaje explicativo. |
| **RN-09** | **Integridad de subprocesos (`<<include>>`)** | Todo caso de uso que actúa como subproceso incluido por otro (`<<include>>`) debe reutilizar y complementar exclusivamente los datos o la lógica ya resuelta por su caso de uso base; no debe reimplementar cálculos, validaciones o reglas que ya existen en el proceso padre. |
| **RN-10** | **Verificación de disponibilidad de fecha, inventario y personal** | Antes de confirmar o estimar un evento, el sistema valida la disponibilidad real de fecha, inventario y personal de recreadores; si el recurso es insuficiente, informa al usuario y, cuando aplica, sugiere alternativas. |
| **RN-11** | **Restricción de acciones según el estado del registro** | Una acción sobre un registro (reserva, documento, presupuesto) se bloquea si su estado actual es incompatible con la acción solicitada (p. ej. reserva cancelada, documento archivado, descuento vencido). |
| **RN-12** | **Autoprotección de cuentas de Administrador** | El sistema impide que un Administrador elimine o desactive su propia cuenta, para evitar la pérdida accidental de acceso administrativo al sistema. |
| **RN-13** | **Completitud de datos obligatorios antes de procesar** | Antes de ejecutar una acción que dependa de datos de entrada (recomendación, cotización, contrato), el sistema valida que la información obligatoria esté completa; si falta información, la solicita explícitamente antes de continuar. |
| **RN-14** | **Bloqueo por intentos fallidos de autenticación** | Tras un número determinado de intentos fallidos de inicio de sesión, el sistema bloquea temporalmente el acceso a la cuenta, como medida de protección contra accesos no autorizados. |
| **RN-15** | **Integridad de copias de seguridad y restauración** | Toda copia de seguridad generada o utilizada para restaurar el sistema debe validarse (espacio disponible, archivo no corrupto) antes de ejecutar la operación; ante cualquier fallo, se conserva el estado anterior. |
| **RN-16** | **Registro de incidencias en log** | Todo error o incidencia relevante del sistema (fallos de tareas programadas, datos descartados, accesos denegados) debe quedar registrado en el log correspondiente para trazabilidad y revisión posterior. |
| **RN-17** | **Resiliencia ante datos corruptos o incompletos** | Cuando el sistema detecta datos corruptos o incompletos dentro de un conjunto mayor (transacciones, historial, tarifas), los excluye del resultado y continúa el proceso con los datos válidos restantes, dejando constancia del descarte. |
| **RN-18** | **Control de concurrencia en edición** | Si dos usuarios intentan editar el mismo registro de forma simultánea, el sistema detecta el conflicto y solicita recargar la versión más reciente antes de permitir guardar cambios. |
| **RN-19** | **Unicidad de identificadores** | El sistema no permite registrar dos usuarios con el mismo correo electrónico u otro identificador único; una solicitud duplicada se rechaza indicando el conflicto. |
| **RN-20** | **Validación de integridad de firma digital** | Toda firma digital capturada debe cumplir un mínimo de trazos/calidad definido para considerarse válida; si no lo cumple, el sistema solicita repetir el proceso. |

---

## 5. Reglas de negocio por caso de uso, agrupadas por módulo

### M01 — Seguridad y Perfiles

| Módulo | CU | Nombre del caso de uso | Regla(s) de negocio asociada(s) |
| :--- | :--- | :--- | :--- |
| **M01** | **CU1** | Presentar interfaz de inicio pública | RN-04 |
| **M01** | **CU2** | Iniciar sesión en el sistema (Generación de Token JWT) | RN-14 |
| **M01** | **CU3** | Visualizar panel de control principal | RN-02 |
| **M01** | **CU3.1** | Validar permisos y restricciones según el rol asignado | RN-02, RN-03, RN-14 |
| **M01** | **CU4** | Cerrar sesión de usuario de forma segura | RN-02 |
| **M01** | **CU5** | Gestionar recuperación de credenciales por correo | RN-04 |

---

### M02 — Inventario y Disponibilidad

| Módulo | CU | Nombre del caso de uso | Regla(s) de negocio asociada(s) |
| :--- | :--- | :--- | :--- |
| **M02** | **CU1** | Consultar calendario interactivo de disponibilidad global | RN-03, RN-07, RN-16 |
| **M02** | **CU1.1** | Validar restricción técnica de fechas bloqueadas o pasadas | RN-06, RN-16 |
| **M02** | **CU2** | Modificar estado físico de los inflables (Disponible / Mantenimiento) | RN-01, RN-03 |
| **M02** | **CU3** | Consultar stock de insumos críticos en bodega | RN-03, RN-16 |

---

### M03 — Lógica de Costos y Logística

| Módulo | CU | Nombre del caso de uso | Regla(s) de negocio asociada(s) |
| :--- | :--- | :--- | :--- |
| **M03** | **CU1** | Calcular costo del evento | RN-01, RN-08 |
| **M03** | **CU2** | Calcular transporte | RN-07 |
| **M03** | **CU3** | Generar presupuesto | RN-11 |
| **M03** | **CU3.1** | Calcular costo del evento | RN-09 |
| **M03** | **CU4** | Aplicar descuentos | RN-11 |
| **M03** | **CU4.1** | Validar promociones y descuentos | RN-07, RN-09 |
| **M03** | **CU5** | Estimar recursos necesarios | RN-10 |

---

### M04 — Inteligencia Artificial

| Módulo | CU | Nombre del caso de uso | Regla(s) de negocio asociada(s) |
| :--- | :--- | :--- | :--- |
| **M04** | **CU1** | Solicitar recomendación de servicio | RN-13 |
| **M04** | **CU2** | Generar cotización automática | RN-13 |
| **M04** | **CU2.1** | Calcular costos | RN-09, RN-17 |
| **M04** | **CU3** | Analizar disponibilidad | RN-08, RN-10 |
| **M04** | **CU4** | Generar sugerencias de paquetes | RN-07 |
| **M04** | **CU4.1** | Analizar preferencias del cliente | RN-09 |
| **M04** | **CU5** | Predecir necesidades logísticas | RN-07 |

---

### M05 — Administración y Documentos

| Módulo | CU | Nombre del caso de uso | Regla(s) de negocio asociada(s) |
| :--- | :--- | :--- | :--- |
| **M05** | **CU1** | Generar contrato | RN-04, RN-07 |
| **M05** | **CU1.1** | Validar información del evento | RN-09, RN-13 |
| **M05** | **CU2** | Consultar contrato | RN-02, RN-03, RN-07 |
| **M05** | **CU2.1** | Buscar documento | RN-01, RN-09 |
| **M05** | **CU3** | Descargar documento | RN-03 |
| **M05** | **CU4** | Actualizar documento | RN-11, RN-18 |
| **M05** | **CU5** | Archivar documento | RN-11 |

---

### M06 — Gestión Financiera y Anticipos

| Módulo | CU | Nombre del caso de uso | Regla(s) de negocio asociada(s) |
| :--- | :--- | :--- | :--- |
| **M06** | **CU1** | Registrar anticipo | RN-02, RN-04 |
| **M06** | **CU2** | Registrar pago | RN-02 |
| **M06** | **CU2.1** | Validar pago | RN-04, RN-09 |
| **M06** | **CU3** | Consultar saldo pendiente | RN-02, RN-07 |
| **M06** | **CU4** | Generar reporte financiero | RN-02, RN-07 |
| **M06** | **CU4.1** | Consolidar ingresos | RN-09, RN-17 |

---

### M07 — CRM y Fidelización

| Módulo | CU | Nombre del caso de uso | Regla(s) de negocio asociada(s) |
| :--- | :--- | :--- | :--- |
| **M07** | **CU1** | Registrar cliente | RN-01, RN-04, RN-05 |
| **M07** | **CU2** | Consultar historial de eventos | RN-02 |
| **M07** | **CU3** | Gestionar promociones | RN-02, RN-03 |
| **M07** | **CU4** | Asignar beneficios | RN-07 |
| **M07** | **CU4.1** | Verificar historial de compras | RN-01, RN-16 |
| **M07** | **CU5** | Enviar campañas | RN-04 |
| **M07** | **CU5.1** | Seleccionar clientes objetivo | RN-07, RN-09 |

---

### M08 — Notificaciones y Respuesta Inmediatas

| Módulo | CU | Nombre del caso de uso | Regla(s) de negocio asociada(s) |
| :--- | :--- | :--- | :--- |
| **M08** | **CU1** | Enviar notificación | RN-04 |
| **M08** | **CU2** | Recibir alerta | RN-02, RN-04 |
| **M08** | **CU3** | Confirmar reserva | RN-11 |
| **M08** | **CU3.1** | Enviar notificación | RN-09 |
| **M08** | **CU4** | Recordar evento próximo | RN-16 |
| **M08** | **CU4.1** | Consultar calendario | RN-07, RN-09 |
| **M08** | **CU5** | Responder consulta automática | RN-13 |

---

### M09 — Digitalización de Operaciones (Paperless)

| Módulo | CU | Nombre del caso de uso | Regla(s) de negocio asociada(s) |
| :--- | :--- | :--- | :--- |
| **M09** | **CU1** | Registrar asistencia digital | RN-02, RN-06 |
| **M09** | **CU2** | Adjuntar evidencia fotográfica | RN-03, RN-04, RN-05 |
| **M09** | **CU3** | Firmar documento digitalmente | RN-20 |
| **M09** | **CU4** | Generar acta digital | RN-07 |
| **M09** | **CU4.1** | Registrar asistencia | RN-07, RN-09 |
| **M09** | **CU4.2** | Adjuntar evidencia | RN-07, RN-09 |
| **M09** | **CU5** | Consultar historial de operaciones | RN-07 |

---

### M10 — Administración Avanzada y Ajustes

| Módulo | CU | Nombre del caso de uso | Regla(s) de negocio asociada(s) |
| :--- | :--- | :--- | :--- |
| **M10** | **CU1** | Gestionar usuarios | RN-02, RN-03 |
| **M10** | **CU1.1** | Crear usuario | RN-09, RN-19 |
| **M10** | **CU1.2** | Modificar usuario | RN-09, RN-12 |
| **M10** | **CU1.3** | Eliminar usuario | RN-09, RN-12 |
| **M10** | **CU2** | Gestionar roles | RN-02, RN-03 |
| **M10** | **CU2.1** | Asignar permisos | RN-03, RN-09 |
| **M10** | **CU3** | Configurar parámetros del sistema | RN-02, RN-03 |
| **M10** | **CU4** | Realizar copias de seguridad | RN-15, RN-16 |
| **M10** | **CU5** | Restaurar respaldo | RN-15 |
| **M10** | **CU6** | Consultar auditoría | RN-03, RN-07 |
