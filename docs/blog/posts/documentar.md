--- 
draft: true
date: 2024-04-03
authors:
  - fab
categories:
  - Programación
---

# Documentar, documentar, documentar (software)

Con la novedad de que he estado participando en el desarrollo de varios proyectos de software, me he enfrentado con la necesidad de leer mucha documentación y, ahora también, de crearla. He encontrado herramientas muy valiosas que estoy usando que quiero comentar por aquí.

Actualmente, mi combinación preferida para proyectos en Python es: [NumPy docstrings](https://numpydoc.readthedocs.io/en/latest/format.html) + [Markdown](https://www.markdownguide.org/) + [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/) + [GitHub Pages](https://squidfunk.github.io/mkdocs-material/publishing-your-site/). Quiero dar más detalles de estas opciones y hablar de otras también.

<!-- more -->

## ¿Qué escribir? 

Documentar puede ser abrumador. Punto. Pero es necesario. Punto.

> "El código es más a menudo leído que escrito",
> Guido van Rossum (Python [BDFL](https://es.wikipedia.org/wiki/Benevolent_Dictator_for_Life))

Quizá una forma de aliviar la carga es tener esta necesidad en mente desde el principio del desarrollo, y comenzar con lo más básico.

¿Quién agradecerá esto en un mundo ingrato? Nosotros mismos en el futuro, y cualquier persona que utilice lo que desarrollamos.

### No hay una documentación, hay cuatro

En un excelente [artículo de Divio](https://documentation.divio.com/), hay una explicación bien amplia sobre las distintas formas (cuatro) que puede asumir una documentación, según consideraciones de **teoría/práctica** y **estudio/trabajo**.

En síntesis, hay cuatro tipos de documentación:

- **Tutoriales**: orientado al *aprendizaje*
- **Guías paso a paso** (*how-to guides*): orientado a *problemas*
- **Explicaciones**: orientado a la *comprensión*
- **Referencia**: orientado a la *información*

En forma de tabla:

|                           | **Útil al estudiar** | **Útil al trabajar** |
|---------------------------|----------------------|----------------------|
| **Pasos prácticos**       | Tutoriales           | Guías                |
| **Conocimiento práctico** | Explicaciones        | Referencia           |


En síntesis, según Divio, cómo escribir buenos tutoriales: 

- Permita al usuario aprender haciendo 
- Haga que el usuario comience 
- Asegúrese de que el tutorial funcione 
- Asegúrese de que el usuario vea resultados inmediatamente 
- Haga que el tutorial sea repetible 
- Enfóquese en pasos concretos, no en conceptos abstractos 
- Proporcione la explicación mínima necesaria 
- Enfóquese solo en los pasos que el usuario necesita tomar

Hay mucha más información en el artículo citado.

## ¿Cómo escribir?

Quiero enfatizar en tres aspectos:

- Cómo escribir en el código
- Cómo escribir texto
- Cuál plataforma utilizar para organizar la documentación

### Comentarios en el código

El primer lugar para una buena documentación es en el código mismo. 

Los comentarios son la forma obvia, sin embargo, a veces la documentación no nace necesariamente de *hacer comentarios*:

```python
# Índice temporal
it = np.linspace(0, 100, 1000)
```

sino de **elegir buenos nombres de variables**:

```python
time_index = np.linspace(0, 100, 1000)
```

Quiero enfatizar esto, aunque parezca una broma: elegir buenos nombres de las variables puede tomarnos mucho tiempo, y estaría bien justificado. Esto porque hacerlo no es fácil, ya que requiere **conocimiento del dominio** en el que estamos trabajando. Me refiero a que si, por cosas de la vida, el proyecto está relacionado con la biología, entonces hay que conocer bien los conceptos y relaciones **de la biología** (no de la programación) para utilizar nombres apropiados.

Ahora bien: no seamos mezquinos con los comentarios en el texto. Aun con buenos nombres de variables y la sintaxis amistosa de Python, es una cortesía con los demás explicar qué está pasando en una línea de código como:

```python
# Lista de números primos del 0 al 100
primes = [i for i in range(2, 101) if all(i%j != 0 for j in range(2, int(i**0.5) + 1))]
```

Nadie perderá la dignidad por escribir ese comentario (aunque desarrolladores avanzados entiendan esa línea en un vistazo; yo no).

#### Docstrings

En Python, los `docstrings`

### Markdown, RST, ¿LaTeX?

Partamos del hecho de que la gran mayoría de la documentación de software será desplegada en un sitio web. Ya no son necesariamente unas "hojas del fabricante" (como la del buen [LM741 *datasheet*](https://www.ti.com/product/LM741)) que serían típicamente impresas o distribuidas como PDF.

Esto condiciona la forma en la que vamos a escribir.

Veamos algunas diferencias de sintaxis:

```markdown title="hola.md"
# Hola

Sí.
```

```rst title="hola.rst"
Hola
----

Sí.

```

```latex title="hola.tex"
\section{Hola}

Sí
```

### Material for MkDocs

### Sphinx

La primera documentación que intenté fue con Sphinx, que es un "clásico"

## ¿Cómo publicar?

### GitHub

### ReadTheDocs

## Anexos

```yaml title="ci.yml"
name: ci 
on:
  push:
    branches:
      - master 
      - main
permissions:
  contents: write
jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - name: Configure Git Credentials
        run: |
          git config user.name github-actions[bot]
          git config user.email 41898282+github-actions[bot]@users.noreply.github.com
      - uses: actions/setup-python@v5
        with:
          python-version: 3.x
      - run: echo "cache_id=$(date --utc '+%V')" >> $GITHUB_ENV 
      - uses: actions/cache@v4
        with:
          key: mkdocs-material-${{ env.cache_id }}
          path: .cache
          restore-keys: |
            mkdocs-material-
      - run: pip install mkdocs-material 
      - run: mkdocs gh-deploy --force
```
