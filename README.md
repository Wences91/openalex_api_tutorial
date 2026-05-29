# OpenAlex API con R

Material del curso **[OpenAlex Database: todo lo que necesitas saber](https://yosigo.ugr.es/courses/openalex-database-todo-lo-que-necesitas-saber/)** 

## Autoría
[Wenceslao Arroyo-Machado](https://orcid.org/0000-0001-9437-8757) - INGENIO (CSIC-Universitat Politècnica de València)

---

## Descripción

Notebook en R Markdown que muestra cómo consultar la API de OpenAlex de forma eficiente, controlando costes y eligiendo el endpoint adecuado según el caso de uso. Se cubren dos aproximaciones: peticiones directas con `httr2` + `jsonlite` y el paquete `openalexR`.

## Contenidos

- **Consulta manual del rate limit** — cómo revisar el presupuesto diario disponible antes de lanzar consultas pesadas
- **Endpoint 1 – Singleton** (gratis) — recuperar un trabajo concreto por DOI o en batch hasta 100 DOIs
- **Endpoint 2 – List + Filter** ($0.10/1K) — filtrar por institución, año, tipo de documento... con paginación por cursor
- **Endpoint 3 – Search** ($1/1K) — búsqueda por palabras clave en títulos y abstracts
- **Endpoint 4 – Semantic Search** ($1/1K) — búsqueda por significado con IA
- **openalexR** — los mismos casos de uso con `oa_fetch()` y cuándo conviene cada enfoque

## Requisitos

```r
install.packages(c("httr2", "jsonlite", "openalexR"))
```

Es necesaria una API key de OpenAlex ([obtenerla aquí](https://openalex.org/settings)). Debe guardarse en `.Renviron` para que no aparezca en el código:

```
OPENALEX_API_KEY=tu_clave
```

## Uso

Abre `openalex_api.Rmd` en RStudio y ejecuta los chunks en orden. El notebook está pensado para seguirse de principio a fin, aunque cada sección es independiente.

## Recursos

- [Documentación oficial de la API](https://developers.openalex.org/api-reference/introduction)
- [Panel de uso y costes](https://openalex.org/settings/usage)
- [Paquete openalexR (rOpenSci)](https://docs.ropensci.org/openalexR/)
