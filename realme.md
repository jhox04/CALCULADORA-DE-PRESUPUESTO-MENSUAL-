 # Calculadora de Presupuesto Mensual

## Descripción del Caso
La Calculadora de Presupuesto Mensual es un sistema que permite a un usuario registrar sus ingresos y gastos para obtener automáticamente el balance del mes. El sistema facilita la organización financiera mediante operaciones simples de entrada de datos, procesamiento interno y salida de información clara y útil.

## Objetivos
- Registrar ingresos y gastos de forma ordenada.
- Calcular automáticamente el total de ingresos, total de gastos y el balance mensual.
- Permitir la modificación y eliminación de registros.
- Presentar un resumen mensual de fácil lectura.

---

## Requerimientos del Sistema

### Requerimientos Funcionales (RF)

| Código | Tipo | Descripción |
|--------|------|-------------|
| RF1 | Entrada de datos | El sistema debe permitir registrar un nuevo ingreso con monto, fecha y descripción. |
| RF2 | Entrada de datos | El sistema debe permitir registrar un nuevo gasto con monto, fecha y descripción. |
| RF3 | Procesamiento | El sistema debe calcular automáticamente los totales de ingresos, gastos y el balance mensual. |
| RF4 | Procesamiento / Edición | El sistema debe permitir modificar o eliminar ingresos o gastos registrados. |
| RF5 | Salida de información | El sistema debe generar un resumen mensual con totales y balance final. |

---

### Requerimientos No Funcionales (RNF)

| Código | Tipo | Descripción |
|--------|------|-------------|
| RNF1 | Rendimiento | El sistema debe responder a las operaciones en menos de 2 segundos. |
| RNF2 | Usabilidad | La interfaz debe ser intuitiva y fácil de navegar. |
| RNF3 | Almacenamiento | Los datos deben guardarse de forma persistente en archivo o base de datos ligera. |

---

## Criterios de Aceptación

| Código | Criterio |
|--------|----------|
| RF1 | No se permite guardar un ingreso si faltan datos obligatorios. |
| RF2 | Solo se aceptan valores numéricos mayores a cero para gastos. |
| RF3 | El balance debe actualizarse automáticamente con cada cambio. |
| RF4 | Cualquier modificación debe reflejarse inmediatamente en la lista y el balance. |
| RF5 | El resumen mensual debe mostrar totales correctos según los datos ingresados. |

---

## Tabla de Pruebas

### Pruebas Unitarias

| ID | Requerimiento | Descripción de Prueba | Datos de Entrada | Resultado Esperado |
|----|----------------|------------------------|-------------------|--------------------|
| CU-01 | RF1 | Verificar que el sistema registre correctamente un ingreso. | Monto: 1000, Fecha: 01/10/2025, Desc: “Sueldo” | El ingreso se guarda y el total de ingresos aumenta. |
| CU-02 | RF2 | Verificar que el sistema registre correctamente un gasto. | Monto: 400, Fecha: 02/10/2025, Desc: “Alquiler” | El gasto se guarda y el total de gastos aumenta. |
| CU-03 | RF3 | Validar el cálculo del balance. | Ingresos 1000, Gastos 400 | Balance calculado: 600. |

---

### Pruebas de Validación

| ID | Requerimiento | Descripción | Datos de Entrada | Resultado Esperado |
|----|--------------|-------------|------------------|--------------------|
| CV-01 | RF1, RF2, RF3 | Validar funcionamiento general del registro y cálculo. | Varios ingresos y gastos del mes | Totales correctos y balance coherente. |
| CV-02 | RF4, RF5 | Validar edición y generación de reporte mensual. | Modificación de gasto + solicitud de reporte | El balance y el resumen reflejan los cambios. |

---

### Tipo de Mantenimiento Propuesto
**Mantenimiento perfectivo:**  
Se propone añadir gráficos visuales de barras o pastel para mejorar la comprensión del presupuesto mensual, aumentando la usabilidad general del sistema.

---

## Reflexión sobre el Control de Versiones
El control de versiones permitió gestionar los cambios del proyecto de forma ordenada, facilitando la actualización del DRS, pruebas y archivos del sistema sin perder información previa. GitHub resultó esencial para mantener versiones limpias, registrar mejoras y asegurar un seguimiento claro de la evolución del software.

