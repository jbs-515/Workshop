# ISO_IEC 17025

Es la norma internacional usada para demostrar que un laboratorio opera de forma competente y puede generar resultados válidos.
Exige, no solo conocer el procedimiento de calibración para una herramienta/máquina, si no tambien poder demostrar y corroborar que los resultados son tecnicamente válidos.

## Calibración, Verificaciñon y Ajuste.
Existe una diferencia fundamental entre estos tres conceptos que es necesario aplicar.

### CALIBRACIÓN

Es comparar un instrumento con un patrón ya conocido y trazable. Como tener una dinamometrica que indica estar ajustada a 100 Nm; la colocas en un banco patrón y en la prueba se dispara a 101.2 Nm

* Valor nominal: 100 Nm

* Valor medido: 101.2 Nm

* Error: +1.2 Nm

La calibración no tiene por que implicar tocar o corregir la herramienta. Pero si que requiere obligatoriamente medirla y documentarla.

### VERIFICACIÓN

Es decidir si el instrumento cumple o no una especificación atribuida al mismo.

* Tolerancia permitida: +-4%

* A 100 Nm, el limite sería 96-104 Nm

* Si mide en la prueba 101.2 Nm, está dentro de lo permitido.

### AJUSTE

Comprende el corregir o modificar la erramienta para reduciar el error.

* La llave dispara a 106 Nm, que se sale de la desviación permitida acorde a la tolerancia para este elemento. En este caso, si dentro de las tareas se encuentra corregirla, se ajustaría el mecanismo y se volvería a medir.

>[!WARNING]
>El ajuste no sustituye a la calibración. Primero de registra el estado inicial, luego se ajusta si procede, y después se vuelve a calibrar.


## As found, As left

Estos son conceptos fundamentales en la calibración para aviación.

### As found
Se refiere al estado en el que llega la herramienta al laboratorio antes de ajustarla o repararla.

Esto es importante porque la herramienta pudo haberse usado en mantenimiento real antes de llegar al laboratorio, y esto podría desarrollarse en una investigación; en que trabajos se usaron, que aeronave, que fecha,...

### As left
Se refiere del estado final en el que se devuelve la herramienta, por lo general despues de un ajuste.

>[!WARNING]
>Nunca se debería de ajustar una herramienta sin registrar primero el as found, porque se perdería la evidencia del estado real en la que estuvo trabajando.


## Trazabilidad Metrológica
La trazabilidad se refiere a que las mediciones pueden relacionarse con una referencia superior mediante una cadena documentada ininterrumpida.

Llave del taller
↓
Banco de torque del laboratorio
↓
Transductor de torque calibrado
↓
Laboratorio acreditado ISO/IEC 17025
↓
Instituto nacional de metrología
↓
Unidades SI

ILAC P10 trata precisamente la política de trazabilidad metrológica para resultados de medición en ensayos y calibraciones.

En Suiza, el Swiss Accreditation Service también explica que la trazabilidad de equipos y patrones debe asegurarse mediante calibraciones adecuadas y certificados que incluyan resultados e incertidumbre o declaración de conformidad.

Un patrón (elemento para la calibración) no es vaido solo porque sea caro y preciso. Es valido si se encuentra identificado, dentro de fecha, dentro de rango, con una incertidumbre adecuada y una trazabilidad documentada.

## Incertidumbre de medida
Esta caracteristica refiere a la estimación de la duda asociada al resultado.

Por ejemplo cuando mides una llave dinamometrica a 100 Nm y obtienes 100.4 Nm. Con esto establecemos una incertidumbre expandida de ±0.3Nm, k=2. 
Esto quiere decir que el resultado no debemos de interpretarlo como un punto perfecto, si no que en si mismo la medida presenta un intervalo razonable.

Fuentes típicas de incertidumbre:
* Incertidumbre en el patrón
* Resolución del instrumento
* Repetibilidad
* Histeresis
* Deriva del patrón desde su ultima calibración
* Temperatura
* Humedad
* Técnica del operador
* Montaje mecánico
* Estabilidad electrica
* Lectura analógica/paralaje

Esta clase de incertidumbre no se estima, se calcula a partir de todas las fuentes que puedan hacer que la medición varíe. Y k es el "factor de cobertura" que se usa para pasar de una incertidumbre base a una expandida.

$$
u = incertidumbre_base
$$

$$
U = incertidumbre_expandida
$$

$$
U = k * u
$$

>[!NOTE]
>k=2 suele darse para dar una cobertura aproximada del 95%, siempre que las condiciones estadisticas sean razonables (la cobertura si que se elige a dedo)

### ¿Como convertir cada fuente en incertidumbre estandar?

Hay que identificar las fuentes de incertidumbre que se aplican a nuestra calibración, y no tenemos por que usar todas, solo las relevantes y justificadas.

Aquí viene lo importante: todas las fuentes deben convertirse a la misma forma, llamada incertidumbre estándar, normalmente equivalente a una desviación típica.

| Fuente              |                  Valor estimado | Cómo se convierte |        u |
| ------------------- | ------------------------------: | ----------------: | -------: |
| Patrón de torque    |                   ±0.10 Nm, k=2 |          0.10 / 2 | 0.050 Nm |
| Resolución          |                          0.1 Nm |         0.1 / √12 | 0.029 Nm |
| Repetibilidad       | desviación típica de mediciones |    ya es estándar | 0.120 Nm |
| Temperatura/montaje |   ±0.10 Nm estimado rectangular |         0.10 / √3 | 0.058 Nm |

Si las analizamos una por una obtenemos:

Incertidumbre del patrón -> segun el certificado del patron nos indica Uncertainty=+-0.10Nm, k=2. Lo cual ya suele incluir la incertidumbre espandida, pero la pasamos a la incertidumbre base dividiendolo entre el k empleado.

Incertidumbre del instrumento -> directamente relacionado con su resolución. Supongamos que el banco de torque muestra 100.0 ; 100.1 ; 100.2 ; ...; con esto sabemos que su resolución es de 0.1 Nm. Como no sabes donde está el valor dentro del ultimo dígito, se suele tratar como distribución rectangular

$$
u_resolución = resolución/√12
$$

en este caso

$$
u_resolución = 0.1 / √12 = 0.029 Nm
$$

Otra forma equivalente es con el semiancho

$$
semiancho = resolución / 2 = 0.05 Nm
$$

$$
u = semiancho/ √3 = 0.029 Nm
$$

Incertidumbre de repetibilidad -> en este caso se hacen varias mediciones en las mismas condiciones. Por ejemplo con la misma llave heciendo pruebas a 100 Nm obtenemos 100.3Nm ; 100.5Nm ; 100.4Nm ; 100.6Nm ; 100.2Nm. 
A partir de estos valores se calcula la desviación típica (la media de la diferencia de los resultados hasta el valor objetivo) 

$$
s = 0.16 Nm
$$

$$
u_repeat = s/√n = 0.16 / √5 = 0.072 Nm
$$

>[!WARNING]
>Algunos procedimientos usan directamente la repetibilidad observada o el maximo rango, dependiendo de la guia tecnica

Incertidumbre por temperatura, montaje, operador, histeresis -> estos valores de incertidumbre son estimados por el propio laboratorio. Por ejemplo, a causa de montaje y alineación puede haber un máximo de ±0.10 Nm
Y si se asume que cualquier valor dentro de ese intervalo es igualmente probable se usa la distribución rectangular.

$$
u_montaje=0.10/√3 = 0.058 Nm
$$

COMBINAR INCERTIDUMBRES -> cuando ya hemos obtenido todas las incertidumbres en forma estandar, se combina por raiz de suma de cuadrados:

$$
uc = √(u1² + u2² + u3² + u4²...)
$$

Notar que esto nos da la "incertidumbre estandar combinada", para obtener la incertidumbre expandida aun tenemos que multiplicar por k. Se recomienda redondear, o incluso truncar, a la alta hasta una magnitud de decimal: 0.x


### Flujo correctod e una calibración
1. Recepción de la herramienta
2. Identificación
3. Revisión visual y funcional
4. Confirmar procedimiento aplicable
5. Confirmar tolerancias
6. Seleccionar patrón trazable
7. Controlar condiciones ambientales
8. Medir as found
9. Calcular error
10. Estimar incertidumbre
11. Evaluar conformidad
12. Ajustar/reparar si procede
13. Medir as left
14. Emitir certificado
15. Etiquetar y liberar / bloquear


## Documentación que debería contener un certificado de calibración

Un certificado serio debería incluir:

* Laboratorio emisor.
* Identificación del cliente.
* Identificación del instrumento.
* Marca, modelo, número de serie.
* Fecha de calibración.
* Procedimiento usado.
* Condiciones ambientales relevantes.
* Patrones utilizados o trazabilidad.
* Resultados de medición.
* Incertidumbre de medición.
* Criterio de aceptación.
* Regla de decisión si hay declaración de conformidad.
* Resultado: conforme/no conforme.
* Firma o autorización.
* Limitaciones, si existen.

En SR Technics, por ejemplo, su servicio habla de certificate, findings report y calibration protocol como documentación de salida




---
---

Método documentado

Para cada herramienta necesitas un procedimiento aprobado:

Identificación del equipo.
Rango de medida.
Puntos de calibración.
Patrón usado.
Condiciones ambientales.
Secuencia de medición.
Cálculo de error.
Incertidumbre.
Criterio de aceptación.
Resultado: conforme/no conforme.
Certificado y registros.
C. Condiciones ambientales

Temperatura, humedad, vibraciones, limpieza, estabilidad eléctrica y tiempo de aclimatación importan. ISO/IEC 17025 exige controlar equipos e instalaciones que puedan afectar la validez de los resultados; SAS resume que deben existir procesos para seleccionar, aplicar, calibrar, verificar, monitorizar y mantener estándares/equipos.

Para dimensional, por ejemplo, una pieza fría o caliente puede cambiar micras. Para presión, una fuga o temperatura inestable puede alterar la lectura. Para electrónica, ruido eléctrico o calentamiento interno afectan la medición.

D. Incertidumbre de medición

No basta con medir el error. Debes expresar algo como:

Valor medido = 100.02 Nm
Incertidumbre expandida = ±0.15 Nm, k=2

La incertidumbre incluye patrón, resolución, repetibilidad, histéresis, ambiente, operador, método, deriva, etc.

E. Regla de decisión

Cuando emites “pass/fail” o “conforme/no conforme”, debes aplicar una decision rule. ISO/IEC 17025:2017 exige definir cómo se considera la incertidumbre cuando se declara conformidad; en certificados debe quedar claro el criterio usado.

Ejemplo simple:

Tolerancia del fabricante: ±1.0 Nm.
Resultado: error +0.8 Nm.
Incertidumbre: ±0.3 Nm.

Sin considerar incertidumbre, parece conforme. Pero si aplicas una regla conservadora, +0.8 + 0.3 = +1.1 Nm, podría no ser aceptable.

Esto es muy importante en aviación porque una decisión incorrecta puede liberar una herramienta que luego afecte mantenimiento crítico.

---
---

Procedimiento general correcto de calibración

Este esquema te sirve para casi cualquier herramienta:

1. Recepción e identificación

Comprueba:

Número de serie.
ID interno.
Cliente/departamento.
Estado físico.
Rango.
Accesorios.
Manual aplicable.
Última calibración.
Daños, golpes, contaminación, batería baja, conectores dañados.

Registra el estado as found, es decir, cómo llega la herramienta antes de tocarla.

2. Revisión documental

Verifica:

Procedimiento vigente.
Especificación del fabricante.
Tolerancias requeridas por cliente o normativa interna.
Patrones necesarios.
Certificados de patrones vigentes.
Capacidad de medición suficiente.

Aquí es donde demuestras mentalidad ISO 17025: no improvisar.

3. Acondicionamiento

Antes de medir:

Limpia si procede.
Deja estabilizar a temperatura de laboratorio.
Enciende equipos electrónicos y respeta warm-up.
Comprueba cero.
Comprueba batería/alimentación.
Monta fixtures correctamente.
Evita cargas laterales, vibraciones, fugas o mala conexión.
4. Medición “as found”

Mides antes de ajustar. Esto es crítico porque indica si la herramienta estuvo trabajando fuera de tolerancia.

Si falla en as found, se debe informar porque puede requerir análisis de impacto: qué trabajos se hicieron con esa herramienta desde la última calibración.

5. Ajuste o reparación, si aplica

Solo ajustas si:

El procedimiento lo permite.
Tienes autorización.
Está documentado.
Puedes repetir la calibración después.

Después del ajuste se registra as left, es decir, el estado final.

6. Cálculo de error e incertidumbre

Fórmula básica:

Error = lectura del instrumento − valor del patrón

Ejemplo:

Patrón: 100.00 Nm.
Llave indica/dispara a: 100.7 Nm.
Error: +0.7 Nm.

Luego añades incertidumbre, normalmente expandida con factor k≈2 para aproximadamente 95 % de cobertura, si así lo define el laboratorio.

7. Evaluación de conformidad

Comparas error + incertidumbre según la regla de decisión aplicable.

Resultado:

Conforme.
No conforme.
Conforme limitado.
Ajustado y conforme.
Fuera de tolerancia as found, conforme as left.
No calibrable / dañado / requiere reparación.
8. Certificado

Un certificado correcto debe incluir, como mínimo:

Identificación del instrumento.
Fecha de calibración.
Condiciones ambientales relevantes.
Método/procedimiento.
Patrones utilizados o trazabilidad.
Resultados medidos.
Incertidumbre.
Declaración de conformidad, si aplica.
Regla de decisión.
Firma/autorización.
Fecha recomendada de próxima calibración, si el laboratorio/cliente lo establece.

SAS indica que los certificados de calibración deben declarar resultados con incertidumbre o una declaración de conformidad con una especificación metrológica.

---
---

