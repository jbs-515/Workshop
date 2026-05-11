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

Por ejemplo cuando mides una llave dinamometrica a 100 Nm y obtienes 100.4 Nm. Con esto establecemos una incertidumbre expandida de +-0.3Nm, k=2. 
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
u = incertidumbre base
U = incertidumbre expandida

U = k * u

$$

>[!NOTE]
>k=2 suele darse para dar una cobertura aproximada del 95%, siempre que las condiciones estadisticas sean razonables (la cobertura si que se elige a dedo)
>
>



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

