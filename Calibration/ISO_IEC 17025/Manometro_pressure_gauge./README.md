Patrón: pressure controller/calibrator o deadweight tester trazable.

## Procedimiento:

* Revisar rango, unidad y tipo de presión: gauge, absolute, differential.

* Comprobar conexiones, roscas, fugas y limpieza.

* Aplicar presión ascendente por puntos: 0 %, 25 %, 50 %, 75 %, 100 %.

* Repetir descendente para ver histéresis.

* Esperar estabilización en cada punto.

* Registrar lectura del instrumento y valor patrón.

* Calcular error, histéresis y repetibilidad.

* Ajustar cero/span si aplica.

* Certificar.

En aviación esto es especialmente relevante para pitot-static testers y air data testers, que SR Technics menciona explícitamente dentro de su acreditación para presión.


## Ejemplo
Supón que calibras un manómetro a:

10.00 bar

Lecturas del manómetro:

* 10.04 bar
* 10.05 bar
* 10.03 bar
* 10.05 bar
* 10.04 bar

Media:

10.042 bar

Patrón:

10.000 bar

Error:

10.042 - 10.000 = +0.042 bar

Ahora incertidumbre.

| Fuente               |            Dato |                       u |
| -------------------- | --------------: | ----------------------: |
| Pressure calibrator  | ±0.010 bar, k=2 |               0.005 bar |
| Resolución manómetro |        0.01 bar | 0.01 / √12 = 0.0029 bar |
| Repetibilidad        |            s/√n |       0.0037 bar aprox. |
| Estabilidad presión  |      ±0.005 bar | 0.005 / √3 = 0.0029 bar |
| Temperatura/fugas    |      ±0.006 bar | 0.006 / √3 = 0.0035 bar |

Combinación:

uc = √(0.005² + 0.0029² + 0.0037² + 0.0029² + 0.0035²)
uc ≈ 0.0082 bar

Expandida:

U = 2 · 0.0082 = 0.0164 bar

Resultado:

Error a 10 bar: +0.042 bar
Incertidumbre expandida: ±0.017 bar, k=2

Certificado expresado como:

Valor patrón: 10.000 bar
Lectura instrumento: 10.042 bar
Error: +0.042 bar
U = ±0.017 bar, k=2
