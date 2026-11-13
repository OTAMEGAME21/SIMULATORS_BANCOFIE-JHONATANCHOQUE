# Pruebas manuales recomendadas

1. En Inicio, comprobar que el carrusel de monedas avanza con las flechas y desplazamiento horizontal, y que las tarjetas no seleccionan ni modifican la moneda.
2. En Plan de Pagos y Capacidad de Pagos, cambiar la moneda dentro de cada formulario y verificar que la unidad de los importes se actualice.
3. En Parámetros, modificar desgravamen, cesantía y otros seguros, guardar, recargar la página y verificar que los valores persistan y se apliquen al Plan de Pagos.
4. En Plan de Pagos, seleccionar “Crédito de consumo” y “Compra de vivienda o departamento”; comprobar que se abra la ventana de validación y que indique que el motivo corresponde orientativamente a crédito de vivienda.
5. Cambiar el tipo a vivienda y verificar que el formulario permita calcular el cronograma.
6. Elegir “Otro motivo”; comprobar que aparezca el campo de texto y que sea obligatorio.
7. En Capacidad de Pagos, seleccionar modalidad de gastos por porcentaje y luego por detalle; comprobar que se muestren solamente los campos correspondientes.
8. Ejecutar una evaluación personal y comprobar que el dictamen incluya los escenarios favorable, base y adverso, con margen, DTI, DSCR y explicación.
9. Ejecutar una evaluación de negocio y comprobar que cada escenario refleje ventas, egresos y flujo neto.
10. Descargar el Excel y revisar las hojas Resumen, Detalle y Dictamen, incluidos los tres escenarios y el gráfico.
11. Generar el PDF y revisar que el encabezado, los datos académicos, el dictamen y el gráfico se impriman correctamente.
12. Guardar una operación, abrir Historial y eliminarla.

**Nota de validación:** la sintaxis JavaScript se comprueba con `node --check`. Las pruebas interactivas deben realizarse en el navegador local del usuario, con conexión a internet para cargar las bibliotecas externas.

## Pruebas correctivas (noviembre 2026)
1. Abrir Capacidad de pago, elegir perfil «Comerciante o empresa» y evaluar: el formulario debe ejecutar el cálculo sin que la modalidad de gastos personales oculta bloquee el envío.
2. Elegir perfil «Persona o familia» y no seleccionar modalidad de gastos: debe aparecer un mensaje claro solicitando modalidad, sin quedarse sin respuesta.
3. Completar antecedentes 5 C y evaluar: el dictamen debe mostrar C1 carácter, C2 capacidad, C3 capital, C4 colateral, C5 condiciones y resultado conjunto.
4. Descargar Excel: verificar que la hoja «Dictamen» contenga las 5 C, escenarios, recomendaciones y cifras.
5. Generar PDF: en la ventana de impresión elegir «Guardar como PDF» y comprobar que el informe incluya dictamen, 5 C y escenarios.
6. En Plan de pagos, elegir modalidad fija: TRe debe quedar en cero. Elegir variable/mixta: debe cargar MN 3,78% o ME 0,50% según moneda para noviembre de 2026.
7. Seleccionar una referencia del tarifario 2026 y comprobar que se traslade a la tasa nominal anual; revisar que se ajuste al rango contractual antes de usar.


## Prueba adicional: dictamen integral y exportaciones 5 C
1. Completar todos los campos requeridos de capacidad de pago y ejecutar la evaluación.
2. Confirmar que aparece la sección visual "Evaluación integral de las 5 C del crédito".
3. Verificar que cada C muestra puntaje, nivel, hallazgo, riesgo, documentos a verificar y acción recomendada.
4. Confirmar que el fundamento técnico distingue entre resultado favorable condicionado, observado o desfavorable.
5. Descargar Excel y revisar la hoja "Dictamen", sección "EVALUACIÓN DETALLADA DE LAS 5 C".
6. Usar "Imprimir / Guardar PDF" y verificar que el PDF incluya 5 C, escenarios y recomendaciones.
7. Probar un perfil con historial desconocido, sin garantía y margen negativo para verificar que las recomendaciones cambien con los datos.
