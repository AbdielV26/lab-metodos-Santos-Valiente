# Reflexión del equipo

**Instrucciones:** respondan **solo las 4 preguntas de su versión** (A o B), con **sus propias palabras** (3–5 líneas cada una)
y **citando nombres de métodos o líneas de SU código**. Las respuestas genéricas o iguales a las de otro grupo se califican en 0.
Escriban debajo de cada pregunta. (Se evalúa después; el autograde no califica este archivo.)

---

## VERSIÓN A

**A1.** `aplicarFactor` modifica el arreglo original, pero `copiaEscalada` no. Expliquen por qué, y qué es lo que
realmente se copia cuando le pasan un arreglo a un método.

> aplicarFactor modifica el arreglo original porque recibe nuevos valores al momento de multiplicar cada lectura por factor. Ejemplo linea 83-84.
>copiaEscalada no modifica el arreglo ya que al usar la palabra reservada new devuelve un arreglo NUEVO con cada lectura * factor. Ejemplo linea 94-96. 
> Lo que realmemnte se copia es el valor de referencia. 

**A2.** ¿Por qué Java no permite tener `double calcularCosto(double kwh)` y `int calcularCosto(double kwh)` en la misma clase?
¿Qué versión de `calcularCosto` elige Java para la llamada `calcularCosto(5, 2.5, 0.1)` y por qué?

> Porque eso genera un conflicto al momento de decidir cual de los 2 métodos usar ya que ambos tienen la misma firma que sería calcularCosto (double kwh). 
> Usa la versión 3 que va de la linea 132 a la 133. Porque calcularCosto(5, 2.5, 0.1) complementa perfectamente con calcularCosto(int dias, double kwhPorDia, double tarifa) si hablamos de los tipos de datos y su posición. 

**A3.** En `Medidor`, ¿para qué sirve `this(id, 0)` en el constructor de un solo parámetro? ¿Qué ventaja tiene frente a copiar y pegar el código del otro constructor?

> this(id, 0) sirve para llamar a otro constructor de la msima clase que acepta números enteros como parametro. 
> La ventaja es que facilita hacer cambios a futuro sin ningún problema. 

**A4.** ¿Por qué los atributos de `Medidor` son `private`? ¿Qué protege `registrarLectura` y qué podría pasar si `lecturaActual` fuera público?

> Es private para salvaguardar que nadie fuera de la clase pueda tocar los atributos de Medidor. 
>Protege que la lectura no pueda retroceder. NO cambia nada y devuelve false. Si es valida: lecturaAnterior toma el valor de lecturaActual, lecturaActual toma nuevaLectura, y devuelve true. Linea 51 a la 57.
>Lo principal es que cualquiera puede modificar los atributos de lecturaActual y poner datos a su antojo en lecturaActual. 

---

## VERSIÓN B

**B1.** Dibujen con texto (cajas y flechas) qué pasa en la memoria —variable `datos`, el arreglo y el parámetro del método—
cuando se ejecuta `aplicarFactor(datos, 2)`. ¿Por qué el arreglo original queda modificado?

> _Respuesta:_

**B2.** `imprimirEncabezado` es `void` y `clasificarConsumo` devuelve `String`. ¿Qué error da el compilador si olvidan un `return`
en alguna rama de `clasificarConsumo`? Expliquen con un caso de su código.

> _Respuesta:_

**B3.** ¿Por qué `sumaRecursiva` necesita un caso base? ¿Qué error aparece en Java si se omite y por qué ocurre?

> _Respuesta:_

**B4.** Si `Medidor` tuviera un atributo `double[] historial` y un getter que lo devolviera directamente, ¿qué riesgo hay para el
encapsulamiento? ¿Cómo se soluciona (idea de *copia defensiva*)?

> _Respuesta:_
