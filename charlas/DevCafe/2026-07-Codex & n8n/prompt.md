Usa obligatoriamente las skills instaladas para desarrollar, validar y debuguear workflows de n8n. Trabaja únicamente mediante el MCP de n8n conectado a **DEV**. Nunca accedas, modifiques ni ejecutes nada en PROD.

Crea en DEV un workflow nuevo, inicialmente desactivado, con este comportamiento:

1. Comenzar con `Manual Trigger`.
2. Leer el Google Sheet con ID:

`_INSERTE_SU_GOOGLE_SHEETS_ID_ACA_`

3. Antes de construir el flujo, inspeccionar el Sheet mediante el MCP para:

   * detectar la pestaña correcta;
   * reconocer los nombres reales de las columnas;
   * identificar las columnas equivalentes a estado, teléfono y temática;
   * conservar el identificador o número de cada fila para poder actualizarla.

4. Procesar únicamente las filas cuyo estado sea equivalente a `pendiente`.

5. Procesar cada fila individualmente.

6. Usar OpenAI para generar una salida estructurada con:

   * `titulo`: máximo 4 palabras;
   * `cuento`: cuento original en español basado en la temática de la fila.

Usar la credencial:

`_NOMBRE_DE_LA_CREDENCIAL_DE_OPENAI_EN_N8N_`

7. Crear un Google Doc:

   * título del documento: el `titulo` generado por el LLM;
   * contenido: solamente el cuento;
   * carpeta de destino de Google Drive:

`_ID_GOOGLE_DRIVE_FOLDER_`

Credenciales:

* `_NOMBRE_DE_LA_CREDENCIAL_DE_SHEETS_EN_N8N_`
* `_NOMBRE_DE_LA_CREDENCIAL_DE_DRIVE_EN_N8N_`
* `_NOMBRE_DE_LA_CREDENCIAL_DE_DOCS_EN_N8N_`

8. Una vez creado correctamente el documento, enviar un WhatsApp al teléfono de la fila indicando que el cuento fue creado. No enviar el cuento completo, salvo que el workflow existente lo requiera.

Usar como subworkflow el workflow existente:

`_FLUJO_PRE-EXISTENTE_EN_n8n_que_envia_whatsapp_`

Inspeccionarlo primero para conocer exactamente sus inputs, formato de teléfono y contrato de ejecución. No modificarlo.

Mensaje sugerido:

`¡Tu cuento "{{ $json.titulo }}" ya fue creado correctamente!`

9. Solo después de crear el Google Doc y enviar correctamente el WhatsApp, actualizar esa misma fila del Sheet como `terminado`, respetando el nombre y formato real de la columna detectada.
10. Si ocurre cualquier error, no marcar la fila como terminada.
11. Evitar duplicados y no volver a procesar filas ya terminadas.
12. Para la primera prueba, limitar la ejecución a una sola fila pendiente.

Requisitos:

* Usar nodos nativos de n8n siempre que sea posible.
* No hardcodear credenciales ni secretos.
* Usar nombres claros para los nodos.
* Validar expresiones, conexiones y tipos de datos.
* Ejecutar las herramientas de validación y debugging provistas por las skills de n8n.
* No activar el workflow automáticamente.
* No ejecutar pruebas que envíen WhatsApp sin confirmar antes que se está trabajando en DEV y que solo se procesará una fila.

Al terminar, informar:

* nombre e ID del workflow creado;
* pestaña y columnas detectadas en el Sheet;
* nodos utilizados;
* contrato detectado del subworkflow de WhatsApp;
* resultado de las validaciones;
* resultado de la prueba controlada, si pudo realizarse;
* cualquier dato que haya quedado pendiente.

