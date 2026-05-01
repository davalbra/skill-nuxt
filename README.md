# Skills Project

Repositorio central para skills reutilizables de Codex.

## Estructura

```text
skills-project/
  skills/
    lavepresto-nuxt-standards/
      SKILL.md
      agents/openai.yaml
      references/project-architecture.md
```

Cada carpeta dentro de `skills/` es una skill independiente. La skill debe mantener su propio `SKILL.md` con frontmatter `name` y `description`.

## Instalacion local

Para probar una skill sin GitHub:

```bash
mkdir -p "${CODEX_HOME:-$HOME/.codex}/skills"
cp -R skills/lavepresto-nuxt-standards "${CODEX_HOME:-$HOME/.codex}/skills/"
```

Luego puedes invocarla por nombre:

```text
Usa $lavepresto-nuxt-standards para implementar este cambio.
```

## Uso desde GitHub

Cuando este proyecto este subido a GitHub, puedes pedirle a Codex que instale una skill desde la ruta del repo, por ejemplo:

```text
Instala la skill lavepresto-nuxt-standards desde tu-usuario/skills-project/skills/lavepresto-nuxt-standards
```

## Reglas del repo

- No agregues documentacion auxiliar dentro de cada skill salvo que sea una referencia que Codex deba cargar bajo demanda.
- Manten `SKILL.md` corto y mueve detalles largos a `references/`.
- Usa `scripts/` solo para automatizaciones repetibles o fragiles.
- Usa `assets/` solo para plantillas o archivos que Codex deba copiar/modificar como parte de un resultado.
# skill-nuxt
