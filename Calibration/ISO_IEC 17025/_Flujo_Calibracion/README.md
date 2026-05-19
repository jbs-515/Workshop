# Flujo real de una calibración
1. Recepción de la herramienta
2. Identificación
3. Inspección visual y funcional
4. Revisión de solicitud del cliente/taller
5. Confirmación del procedimiento aplicable
6. Confirmación de tolerancias
7. Selección de patrón trazable
8. Verificación de condiciones ambientales
9. Medición as found
10. Cálculo de error
11. Estimación/aplicación de incertidumbre
12. Evaluación de conformidad
13. Ajuste/reparación si procede
14. Medición as left
15. Certificado/informe/protocolo
16. Etiquetado
17. Liberación o bloqueo
18. Archivo de registros

## Punto por punto
### Recepción de herramienta
Cuando entra una herramienta al laboratorio, lo primero no es calibrarla. Lo primero es identificarla y saber qué se espera de ti.

Debes comprobar:

* Qué herramienta es.
* Quién la envía.
* Para qué departamento/taller es.
* Si tiene orden de trabajo.
* Si requiere calibración completa, verificación, ajuste o reparación.
* Si hay urgencia.
* Si hay tolerancias específicas del cliente.
* Si la herramienta viene con accesorios necesarios.

>Ejemplo:
>Herramienta: Torque wrench
>
>Marca: Stahlwille
>
>Modelo: 730N/20
>
>Número de serie: 123456
>
>Rango: 40–200 Nm
>
>Cliente/departamento: Engine shop
>
>Solicitud: Calibration according to internal procedure

### Identificación
Cada instrumento debe estar inequívocamente identificado.

Normalmente se registra:
* ID interno
* Marca
* Modelo
* Número de serie
* Rango
* Resolución
* Unidad
* Ubicación/departamento
* Fecha de recepción
* Estado de calibración anterior

>Ejemplo
>
>Equipment ID: TW-04581
>
>Description: Torque wrench
>
>Range: 40–200 Nm
>
>Resolution: 1 Nm
>
>Serial number: 123456
>
>Previous calibration due date: 2026-04-30
>
>Received: 2026-05-11

### Inspección visual y funcional
En una llave dinamométrica

| LLave                                   | Multimetro                      | Manómetro             |
| --------------------------------------- | ------------------------------: | --------------------: |
| Golpes                                  | Pantalla                        |                 Rosca |
| Deformaciones                           | Batería                         |       Cristal/display |
| Carraca dañada.                         | Fusibles                        |                 Aguja |
| Escala legible.                         | Bornes                          |                  Cero |
| Mecanismo de bloqueo                    | Carcasa                         |        Fugas visibles |
| Unidad correcta.                        | Selector                        |                 Rango |
| Mango en buen estado                    | Puntas de prueba                |                Unidad |
| Si vuelve a cero o al mínimo de escala. | Etiqueta de calibración         | Sobrepresión aparente |
| Si hay adaptadores.                     | Seguridad CAT, si aplica        |                     - |

Si detectas daño grave, no sigues como si nada. Puedes emitir:

- Rejected before calibration
- Not calibratable
- Repair required
- Limited calibration

### Revisión de solicitud
En SR Technics, por ejemplo, su servicio habla de distintos entregables como certificate, findings report y calibration protocol, y cubre herramientas eléctricas, mecánicas, presión, longitud y aviónica.

En una empresa real puede haber varios niveles:

| Solicitud                   | Qué significa                                        |
| --------------------------- | ---------------------------------------------------- |
| Calibration only            | Mides y documentas, sin ajustar                      |
| Calibration with adjustment | Mides as found, ajustas si hace falta, mides as left |
| Repair + calibration        | Reparas y luego calibras                             |
| Verification                | Solo pass/fail contra tolerancia                     |
| Accredited calibration      | Dentro del alcance acreditado ISO/IEC 17025          |
| Internal check              | Control interno, quizá no acreditado                 |

>[!CAUTION]
>Pregunta siempre si tienes autoridad para ajustar o solo para medir

### Confirmación del Procedimiento aplicable
Debes tener un procedimiento, por ejemplo:

>Internal procedure CAL-TOR-001 for torque wrenches
>
>Manufacturer manual
>
>EURAMET guide
>
>Customer-specific procedure
>
>Aircraft maintenance organization requirement

El procedimiento debe definir:

* Rango aplicable.
* Equipos necesarios.
* Condiciones ambientales.
* Puntos de medición.
* Número de repeticiones.
* Secuencia.
* Cálculo.
* Tolerancias.
* Criterio de aceptación.
* Formato de registro.

| Ejemplo llave torque                                       | Ejemplo manómetro                                    |
| :--------------------------------------------------------- | ---------------------------------------------------: |
| Puntos: 20 %, 60 %, 100 % del rango                        | Puntos: 0 %, 25 %, 50 %, 75 %, 100 %                 |
| Repeticiones: 5 por punto                                  | Secuencia: ascendente y descendente                  |
| Dirección: clockwise, counterclockwise if applicable       | Estabilización: esperar hasta lectura estable        |
| Preload: 3 activaciones antes de registrar                 | Leak check: obligatorio antes de medición            |

### Confirmación de tolerancia
Las tolerancias pueden venir de varias fuentes, como el fabricante, procedimientos internos, trabajar en caliente, la normativa tecnica, los requisitos, el historial, etc.

>Ejemplo:
>Torque wrench tolerance: ±4 % of indicated value
>
>Pressure gauge tolerance: ±0.25 % FS
>
>Digital multimeter: manufacturer specification ±(% reading + digits)
>
>Caliper: ±0.02 mm

>[!WARNING]
>Se debe de tener cuidado con las tolerancias FS (Full Scale) y las tolerancias de lectura.
>
>El porcentaje de tolerancia en FS es establecido respecto a un rango predefinido (se mantiene constante dentro de ese rango)
>
>Mientras que la tolerancia de lectura es el porcentaje incremental que se aplica a cada valor concreto (incrementando así junto a la magnitud que se mida)


### Selección del patron adecuado
El patrón debe ser adecuado en:
* Rango.
* Resolución.
* Incertidumbre.
* Estado de calibración.
* Trazabilidad.
* Compatibilidad física.
* Condiciones de uso.

No deberías calibrar una llave de 200 Nm con un patrón cuyo rango máximo fiable es 100 Nm.
Tampoco deberías usar un calibrador de presión con incertidumbre demasiado grande para evaluar un manómetro muy preciso.

Para estos casos existe la regla TUR (Test Uncertainity Ratio)

$$
TUR = tolerancia del instrumento / incertidumbre del sistema de calibración
$$

Es una regla antigua y no debería ser un pilar para la fiabilidad del proceso, pero puede ser util para una rapida estimación.

### Verificación del patrón

* ¿Está identificado?
* ¿Está dentro de fecha?
* ¿Tiene certificado válido?
* ¿Cubre el rango?
* ¿Su incertidumbre es adecuada?
* ¿Tiene restricciones?
* ¿Necesita warm-up?
* ¿Necesita cero?
* ¿Tiene daños?

### Condiciones ambientales
Tenemos claro que las condiciones ambientales pueden afectar a la medición. Como norma general se deben de controlar los soguientes parámetros:
* Temperatura.
* Humedad.
* Presión atmosférica, si aplica.
* Vibración.
* Limpieza.
* Estabilidad eléctrica.
* Tiempo de aclimatación.
* Corrientes de aire, si aplica.

| Torque                   | Dimensional                  | Presion                                   | Electronica          |
| ------------------------ | ---------------------------- | ----------------------------------------- | -------------------- | 
| Montaje                  | Temperatura                  | Temperatura                               | Warm-up              |
| Temperatura razonable    | Limpieza                     | Fugas                                     | Temperatura          |
| Estabilidad mecánica     | Dilatación termica           | Estabilidad                               | Humedad              |
| Alineación               | Manipulación con las manos   | Tipo de fluido                            | Ruido eléctrico      |
|                          |                              | Altura de columna, si aplica              | Cables y conexiones  |
|                          |                              | Presión atmosferica para presión absoluta |                      |
