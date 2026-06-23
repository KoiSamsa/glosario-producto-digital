# Cómo contribuir

Gracias por querer mejorar el glosario. Toda aportación con criterio es bienvenida.

## Qué puedes aportar

- **Corregir** una definición imprecisa o desactualizada.
- **Sugerir** un término que falte.
- **Mejorar** un ejemplo o un matiz.
- **Reportar** un error de la app (algo que no funciona, un enlace roto).

## Cómo hacerlo

### Opción sencilla — abrir un *issue*

Si no te manejas con código, solo abre un **issue** (pestaña _Issues_ del repositorio) describiendo el cambio. Ejemplos:

- _"Falta el término **Service Blueprint**"_
- _"La definición de **MVP** debería mencionar que 'viable' es la palabra clave"_
- _"El buscador no encuentra X"_

### Opción con código — *pull request*

Si te manejas con git:

1. Haz un *fork* del repositorio.
2. Los términos viven en un bloque JSON dentro de `index.html` (busca `id="glo-data"`). Cada término tiene esta forma:

   ```json
   {
     "id": "identificador-unico",
     "t": "Nombre del término",
     "cat": "Categoría",
     "def": "Definición breve.",
     "como": "Cómo se hace o se calcula.",
     "ej": "Un ejemplo concreto.",
     "mat": "Matices y trampas.",
     "rel": [{ "t": "Término relacionado", "id": "su-id" }]
   }
   ```

3. Mantén el tono: **definición → cómo → ejemplo → matices**. Concreto, con criterio, sin relleno.
4. Las categorías válidas son: `UX Research`, `UI & Visual`, `Design Systems`, `Accesibilidad`, `Métricas`, `Product & Delivery`, `Métodos & Procesos`, `Técnico & IA`.
5. Abre un *pull request* describiendo el cambio.

## Estilo de las definiciones

- Una idea por término.
- El ejemplo debe ser real y reconocible, no abstracto.
- El campo "matices" es donde va lo que distingue a alguien que sabe: la trampa, el error común, el matiz que cambia la decisión.
- Sin jerga innecesaria. Si un término técnico aparece en la definición, enlázalo en `rel`.

Toda contribución se revisa antes de incorporarse. Gracias por cuidar el detalle.
