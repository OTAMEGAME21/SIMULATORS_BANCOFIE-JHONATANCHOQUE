# Sistema de Simulación y Evaluación Crediticia · Banco FIE Tarija

## Contenido
- `index.html`: página de inicio, área privada y dos simuladores independientes.
- `css/styles.css`: diseño adaptable a computadora y celular.
- `js/app.js`: validaciones, cálculos, escenarios, moneda, historial y exportaciones.
- `assets/`: recursos gráficos de la interfaz.

## Inicio
1. Descomprime el ZIP.
2. Abre `index.html` en Chrome o Edge.
3. Inicia sesión para acceder a los simuladores.

## Funciones de esta versión
- Carrusel informativo de monedas en Inicio (sin selección ni cambio de moneda desde esa pantalla).
- Cada simulador permite elegir su moneda; la moneda inicial predeterminada es BOB.
- La selección de moneda cambia la unidad de los importes; no realiza conversión de divisas.
- Las referencias de tasas productivas/comerciales cargadas para Banco FIE están expresadas en bolivianos. Para moneda extranjera, el sistema solicita utilizar el tarifario específico y no reutiliza automáticamente tasas en Bs.
- Catálogo de motivos de préstamo, opción “Otro motivo” y validación de coherencia con el tipo de crédito.
- Ventana emergente que explica el tipo seleccionado, la finalidad ingresada y la clasificación orientativa a la que corresponde el motivo.
- Capacidad de pagos con gastos por porcentaje o por detalle, clasificación empresarial, indicadores y tres escenarios (favorable, base y adverso).
- Dictamen detallado y gráfico de escenarios; el gráfico se incorpora al Excel cuando el navegador permite exportarlo.
- Exportación `.xlsx` y generación de PDF mediante impresión del navegador.
- Historial local con guardado voluntario y eliminación de operaciones.
- Parámetros editables y persistentes para tasa, límite DTI, desgravamen, cesantía y otros seguros; conjunto inicial identificado para la gestión 2026.

## Acceso de demostración
- Usuario: `JhonatanChoqueFie1`
- Contraseña: `JACRFIE1`

## Requisitos y limitaciones
- Para los gráficos y archivos `.xlsx`, el navegador debe poder cargar Chart.js y ExcelJS desde sus CDN, por lo que se requiere conexión a internet.
- El PDF se genera con la función de impresión del navegador: seleccionar “Guardar como PDF”.
- Los datos del historial se guardan en el almacenamiento local del navegador y no se sincronizan entre dispositivos.
- Las tasas de referencia en moneda extranjera no se convierten desde Bs. Deben introducirse o verificarse con la tabla específica correspondiente.
- Los montos ingresados se interpretan en la moneda seleccionada. Cambiar de moneda no convierte automáticamente los valores existentes.
- El inicio de sesión de esta versión es una demostración de interfaz y no debe utilizarse para proteger información real.


## Actualización correctiva – noviembre de 2026

- Se corrigió el bloqueo del formulario de capacidad de pago causado por el selector obligatorio de modalidad de gastos, que podía impedir que el evento de evaluación se ejecutara cuando el perfil comercial estaba activo.
- El dictamen ahora incorpora un análisis explícito de las 5 C del crédito: carácter, capacidad, capital, colateral y condiciones. Incluye criterios, indicadores, observaciones y limitaciones; la puntuación es orientativa y no sustituye la evaluación oficial.
- El Excel de capacidad exporta las 5 C dentro de la hoja «Dictamen», además de escenarios, indicadores y recomendaciones.
- El botón «Generar PDF / Guardar como PDF» abre la vista de impresión del navegador; seleccionar «Guardar como PDF» para obtener el archivo. La vista incluye el dictamen y los escenarios generados.
- Se añadieron referencias del tarifario activo de Banco FIE vigente desde el 01/11/2026 y un selector para cargar tasas de referencia al plan. Los valores deben ajustarse al rango y condiciones de la operación real.
- La TRe de noviembre de 2026 se identifica por moneda: MN 3,78%; ME 0,50%; MVDOL 1,56%; MN-UFV 0,01%. Por defecto, la modalidad es tasa fija y no se suma TRe. Solo se incorpora cuando se selecciona tasa variable o mixta y corresponde contractualmente.
- Fuentes de referencia: Banco FIE, Tarifario de Tasas Activas y Comisiones vigente desde 01/11/2026; Banco Central de Bolivia, TRe Gestión 2026 (vigencia noviembre de 2026).

**Importante:** simulador académico. Los resultados dependen de la calidad de los datos declarados y no representan una aprobación crediticia de Banco FIE.


## Actualización del dictamen integral 2026
- La evaluación de las 5 C se presenta en una matriz visual independiente del diseño de escenarios.
- Cada C contiene puntaje, nivel, hallazgo, riesgo e implicación, evidencia documental requerida y acción recomendada.
- El dictamen incorpora fundamento técnico, alcance de la decisión y plan de recomendaciones priorizadas.
- La exportación Excel agrega una sección específica para las 5 C con sus hallazgos y acciones.
- La impresión/guardado en PDF incluye la matriz visual, el fundamento y las recomendaciones, junto con el análisis de escenarios.
- Los puntajes de las 5 C son orientativos y no representan la metodología oficial ni una aprobación de Banco FIE.
