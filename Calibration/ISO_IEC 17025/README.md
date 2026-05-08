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

