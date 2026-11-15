# Cómo contribuir a Mi Barrio Reporta

Estas reglas aplican a todo cambio del repositorio, sea código o documentación. El proceso completo (metodología, roles y artefactos) está en [docs/proceso/PROCESO.md](docs/proceso/PROCESO.md).

## 1. Flujo de trabajo (GitHub Flow)

1. Todo trabajo nace de un **issue** del tablero, con su etiqueta (`historia`, `tarea`, `documentación`, `defecto` o `cambio`).
2. Se crea una rama corta desde `main` para ese issue.
3. Se abre un **pull request** con la plantilla y `Closes #N`.
4. El **otro integrante** revisa, deja al menos un comentario y aprueba. El autor nunca aprueba su propio PR.
5. Se fusiona con **Squash and merge** y la rama se borra automáticamente.

`main` está protegida: no acepta push directo, exige 1 aprobación y que todas las conversaciones estén resueltas.

## 2. Ramas

Formato: `tipo/N-descripcion-corta`, en minúsculas, con guiones y sin tildes. `N` es el número del issue.

| Tipo | Uso | Ejemplo |
|---|---|---|
| `feature` | Funcionalidad nueva | `feature/20-reportar-sin-cuenta` |
| `fix` | Corrección de un defecto | `fix/35-validacion-foto` |
| `docs` | Documentación | `docs/3-proceso-del-equipo` |
| `test` | Solo pruebas | `test/40-transiciones-rn4` |
| `chore` / `ci` | Configuración, dependencias, pipeline | `ci/12-github-actions` |

## 3. Commits

Formato: Conventional Commits en español, con el verbo en infinitivo y el número de issue al final.

```
tipo(ámbito): descripción en infinitivo (#N)
```

- Tipos: `feat`, `fix`, `docs`, `test`, `refactor`, `chore`, `ci`.
- El ámbito es opcional: `reportes`, `catalogos`, `gestores`, `proceso`, `github`, etc.
- Ejemplos: `feat(reportes): generar código de seguimiento (#22)` · `docs(proceso): agregar matriz RACI (#3)` · `fix(reportes): validar tamaño de la foto (#31)`.

## 4. Pull requests

- **Título:** con el mismo formato que un commit, sin el número de issue. Por ejemplo, `docs(proceso): agregar PROCESO.md`.
- **Cuerpo:** la plantilla de `.github/pull_request_template.md`, con `Closes #N`.
- **Revisión:** comentarios concretos. Si algo falta, el revisor usa **Request changes** y el autor corrige con un nuevo commit en la misma rama.
- **Conflictos:** los resuelve el autor del PR que se fusiona después, en su rama, y lo explica en un comentario del PR.
- **Fusión:** solo *Squash and merge*.

## 5. Versiones

Etiquetas anotadas con versionado semántico sobre `main`: `v0.1.0` (semana 6), `v1.0.0` (semana 11) y `v1.1.0` (semana 16). Las crea el responsable de Calidad y DevOps del sprint.

## 6. Definición de terminado

Un issue está terminado solo cuando se cumplen todas estas condiciones:

1. Cumple todos sus criterios de aceptación (Dado/Cuando/Entonces) y se demostró en la revisión del sprint.
2. La rama y los commits siguen las convenciones de este documento.
3. El PR tiene `Closes #N`, al menos un comentario de revisión y la aprobación del otro integrante, y todas las conversaciones resueltas.
4. Si incluye código: tiene pruebas automatizadas de su lógica, la cobertura total se mantiene en al menos el 70 % y la integración continua está en verde.
5. La documentación afectada (README, `docs/`, manuales) está actualizada en el mismo PR.
6. Se fusionó con *Squash and merge*, el issue quedó en **Hecho** y, si incluye código, el cambio quedó desplegado en el entorno de pruebas.

## 7. Regla para los documentos

Los documentos de `docs/` solo se modifican mediante un PR revisado. Si el cambio afecta el alcance aprobado, primero se abre un issue con la etiqueta `cambio`, el Líder evalúa el impacto y la docente lo aprueba.
