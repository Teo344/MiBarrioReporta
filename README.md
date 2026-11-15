# Mi Barrio Reporta

Aplicación web para que los vecinos del **Barrio Cuendina (Amaguaña)** reporten problemas urbanos (baches, luminarias, basura, fugas) **sin crear una cuenta**, y para que la directiva del barrio los revise, priorice y gestione hasta su solución.

- **Asignatura:** Construcción y Evolución de Software · NRC 36848 · Grupo 6 · ESPE
- **Docente (product owner y cliente):** Ing. Nancy Betancourt
- **Cliente piloto:** directiva del Barrio Cuendina
- **Tablero:** GitHub Projects del repositorio

## Estado

| Hito | Semana | Estado |
|---|---|---|
| v0.1.0: requisitos, casos de uso, arquitectura y prototipo | 6 | En curso |
| v1.0: reporte, consulta, moderación y listado público | 11 | Pendiente |
| v1.1: versión validada en el piloto | 16 | Pendiente |

## Tecnología

Python 3.13 · Django 5.2 LTS · PostgreSQL 17 · Bootstrap · Docker Compose v2 · GitHub Actions. Las razones de la arquitectura y de la tecnología están en el [borrador de arquitectura](docs/04-arquitectura/Borrador_Arquitectura_Criollo_Cepeda.pdf).

## Estructura del repositorio

```
.
├── README.md            qué es el proyecto, equipo y cómo trabajar
├── CONTRIBUTING.md      ramas, commits, pull requests y definición de terminado
├── .gitignore
├── .github/             plantillas de pull request e issues
└── docs/
    ├── 01-inicio/       concepto, acta, matriz de decisión, riesgos y plan de construcción (Taller 1 y 2)
    ├── 02-requisitos/   requisitos, historias, backlog y plan de sprints (Tarea 2)
    ├── 03-modelado/     casos de uso y diagrama editable (Tarea 3)
    ├── 04-arquitectura/ decisión de arquitectura
    └── proceso/         PROCESO.md y actas de retrospectiva
```

## Cómo trabajar

1. Toma un issue de la columna **Por hacer** del tablero y asígnatelo.
2. Crea una rama desde `main` con el formato `tipo/N-descripcion` (por ejemplo, `feature/20-reportar-sin-cuenta`).
3. Haz commits con el formato `tipo(ámbito): descripción (#N)`.
4. Abre un pull request con la plantilla, incluye `Closes #N` y pide revisión al otro integrante.
5. Cuando esté aprobado, fusiona con **Squash and merge**.

El detalle está en [CONTRIBUTING.md](CONTRIBUTING.md).

## Equipo

| Integrante | Usuario de GitHub | Aportes en el laboratorio |
|---|---|---|
| Mateo Criollo | Teo344 | Estructura, CONTRIBUTING, PROCESO.md y retrospectiva |
| David Cepeda | davidcepeda1 | Plantillas, diagrama editable y revisión de PR |

Tablero del proyecto: https://github.com/users/Teo344/projects/2
