# Product Backlog

**Producto:** sistema de costos y rentabilidad por unidad de negocio.

**Visión:** que los dueños y contadores de la empresa sepan cuánto gana cada unidad de negocio y cada
producto, cuál es su punto de equilibrio y cuánto les cuesta cada decisión de inversión, para decidir
con números y no a ojo.

**Usuarios:**
- **Dueño / directivo:** consulta resultados y toma decisiones.
- **Contador / administrativo:** carga y valida los datos de ventas y costos.
- **Administrador del sistema:** gestiona usuarios y configuración.

## Convenciones

- **Prioridad (MoSCoW):** Must (imprescindible), Should (importante), Could (deseable), Won't (fuera de alcance por ahora).
- **Estimación:** story points en escala Fibonacci (1, 2, 3, 5, 8, 13). Son **tentativas** y se
  ajustan con Planning Poker en el equipo y con lo que surja de la reunión con el cliente.
- Las historias se escriben con el formato *Como [usuario], quiero [acción], para [beneficio]*.

## Resumen por épica

| Épica | Descripción | Historias | Puntos |
|---|---|---|---|
| E1 | Estructura de la empresa | HU-01 a HU-03 | 8 |
| E2 | Carga de datos | HU-04 a HU-08 | 26 |
| E3 | Reparto de costos indirectos | HU-09 | 8 |
| E4 | Cálculos de rentabilidad | HU-10 a HU-13 | 21 |
| E5 | Reportes y tablero | HU-14 a HU-16 | 18 |
| E6 | Evaluación de inversiones y stock | HU-17 a HU-18 | 13 |
| E7 | Usuarios y seguridad | HU-19 a HU-20 | 8 |
| | **Total** | **20 historias** | **102** |

## Backlog priorizado

| ID | Épica | Historia de usuario | Prioridad | SP |
|---|---|---|---|---|
| HU-01 | E1 | Como administrador, quiero dar de alta las unidades de negocio, para poder analizar cada una por separado. | Must | 2 |
| HU-02 | E1 | Como contador, quiero registrar los productos o servicios de cada unidad, para conocer la rentabilidad por producto. | Must | 3 |
| HU-03 | E1 | Como contador, quiero asignar los empleados a una unidad de negocio (o a la estructura central), para imputar correctamente los sueldos. | Must | 3 |
| HU-04 | E2 | Como contador, quiero cargar las ventas por unidad y producto en un período, para tener los ingresos de cada unidad. | Must | 5 |
| HU-05 | E2 | Como contador, quiero cargar los costos clasificándolos en fijos o variables y directos o indirectos, para poder calcular márgenes. | Must | 5 |
| HU-06 | E2 | Como contador, quiero importar ventas y costos desde una planilla Excel, para no cargar todo a mano. | Should | 8 |
| HU-07 | E2 | Como contador, quiero ver y corregir los datos cargados de un período, para asegurarme de que los cálculos sean correctos. | Must | 3 |
| HU-08 | E2 | Como contador, quiero cerrar un período, para que los resultados de ese mes no cambien una vez validados. | Could | 5 |
| HU-09 | E3 | Como contador, quiero definir el criterio para repartir cada costo indirecto (ventas, empleados, m², horas), para que cada unidad cargue la parte que le corresponde. | Must | 8 |
| HU-10 | E4 | Como dueño, quiero ver el margen de contribución de cada unidad de negocio, para saber cuánto aporta cada una. | Must | 5 |
| HU-11 | E4 | Como dueño, quiero ver el resultado y el porcentaje de rentabilidad de cada unidad, para saber cuáles ganan y cuáles pierden plata. | Must | 5 |
| HU-12 | E4 | Como dueño, quiero conocer el punto de equilibrio de cada unidad, para saber cuánto tiene que vender como mínimo. | Must | 3 |
| HU-13 | E4 | Como dueño, quiero ver la rentabilidad de cada producto, para detectar los que dan pérdida y decidir si los sigo vendiendo. | Should | 8 |
| HU-14 | E5 | Como dueño, quiero un tablero que compare las 4 unidades (ventas, costos, resultado, rentabilidad), para tener la foto de la empresa de un vistazo. | Must | 8 |
| HU-15 | E5 | Como dueño, quiero ver la evolución mensual de cada unidad, para detectar tendencias. | Should | 5 |
| HU-16 | E5 | Como contador, quiero exportar los reportes a PDF o Excel, para compartirlos con los dueños. | Could | 5 |
| HU-17 | E6 | Como dueño, quiero calcular el costo de tener stock o capital inmovilizado durante un tiempo, para saber si una compra grande conviene. | Should | 8 |
| HU-18 | E6 | Como dueño, quiero simular escenarios (subir precios, bajar costos, cerrar un producto), para ver cómo cambiaría la rentabilidad antes de decidir. | Could | 5 |
| HU-19 | E7 | Como usuario, quiero iniciar sesión con usuario y contraseña, para que solo personas autorizadas vean los números de la empresa. | Must | 3 |
| HU-20 | E7 | Como administrador, quiero asignar roles (dueño, contador), para que cada uno vea y haga solo lo que le corresponde. | Should | 5 |

## Criterios de aceptación de las historias Must

**HU-01: Alta de unidades de negocio**
- Puedo crear, editar y desactivar una unidad con nombre y descripción.
- No se permiten dos unidades con el mismo nombre.

**HU-02: Productos por unidad**
- Cada producto pertenece a una sola unidad de negocio.
- Puedo registrar nombre, unidad y, opcionalmente, costo variable unitario.

**HU-03: Empleados por unidad**
- Cada empleado se asigna a una unidad o a "estructura central".
- Se puede repartir un empleado entre varias unidades por porcentaje (la suma tiene que dar 100%).

**HU-04: Carga de ventas**
- Registro período (mes/año), unidad, producto, cantidad e importe.
- El sistema rechaza importes negativos o períodos inválidos.

**HU-05: Carga de costos**
- Cada costo tiene período, importe, tipo (fijo/variable), y si es directo (con su unidad) o indirecto.
- Puedo ver el total de costos por tipo para el período.

**HU-07: Revisión de datos**
- Veo un listado filtrable por período y unidad, y puedo editar o borrar un registro.

**HU-09: Reparto de costos indirectos**
- Para cada costo indirecto elijo un criterio: ventas, cantidad de empleados, m² o porcentaje manual.
- La suma de lo asignado a las unidades es igual al total del costo.

**HU-10: Margen de contribución**
- Margen = ventas − costos variables, por unidad y período, en importe y en porcentaje.

**HU-11: Resultado y rentabilidad**
- Resultado = margen de contribución − costos fijos directos − costos indirectos asignados.
- Rentabilidad sobre ventas = resultado / ventas. Las unidades con resultado negativo se destacan.

**HU-12: Punto de equilibrio**
- Punto de equilibrio en ventas = costos fijos totales de la unidad / (margen de contribución / ventas).
- Muestra cuánto falta (o cuánto sobra) respecto de las ventas reales.

**HU-14: Tablero comparativo**
- Muestra las 4 unidades lado a lado para el período elegido, con ventas, costos, resultado y rentabilidad.

**HU-19: Inicio de sesión**
- Sin sesión iniciada no se puede ver ningún dato.
- Se bloquea el acceso tras varios intentos fallidos.

## Definition of Ready (DoR)

Una historia entra a un sprint cuando:
- Está escrita en formato de historia de usuario y el equipo la entiende.
- Tiene criterios de aceptación.
- Está estimada por el equipo.
- No depende de información que el cliente todavía no nos dio.

## Definition of Done (DoD)

Una historia está terminada cuando:
- Cumple todos sus criterios de aceptación.
- El código está en el repositorio y revisado por al menos otro integrante.
- Tiene pruebas de los cálculos (rentabilidad, punto de equilibrio, reparto).
- Fue mostrada al Product Owner y aceptada.

## Pendiente de validar con el cliente

- Cuáles son las 4 unidades de negocio y qué vende cada una.
- De dónde salen hoy los datos (sistema contable, Excel, facturación) y con qué frecuencia (mensual).
- Cómo se clasifican los costos y qué costos son compartidos entre unidades.
- Qué criterio de reparto les parece justo para los costos compartidos.
- Qué tasa usar para el costo de oportunidad del capital (HU-17).
