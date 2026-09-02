# Marketing Skills (copia local)

Estas skills provienen del repositorio público
[coreyhaines31/marketingskills](https://github.com/coreyhaines31/marketingskills),
licenciado bajo MIT (ver `LICENSE-marketingskills`).

- **Origen:** https://github.com/coreyhaines31/marketingskills
- **Commit copiado:** `d4ff28a9c8d56c06809860bf2800d4f5224b52db`
- **Autor original:** Corey Haines

## Qué se copió

- `.claude/skills/` — las 50 skills (`skills/` del repositorio original).
- `.claude/tools/` — el directorio `tools/` del original, necesario porque
  varias skills lo referencian con rutas relativas `../../tools/...`.

## Cómo se actualiza

Al ser una copia y no un marketplace, no se actualiza sola. Para traer una
versión nueva:

```bash
git clone --depth 1 https://github.com/coreyhaines31/marketingskills /tmp/ms
rm -rf .claude/skills .claude/tools
cp -r /tmp/ms/skills .claude/skills
cp -r /tmp/ms/tools  .claude/tools
cp /tmp/ms/LICENSE   .claude/skills/LICENSE-marketingskills
```

(y volver a crear este README, actualizando el commit de referencia)

## Alternativa: instalarlo como plugin

Desde la CLI local de Claude Code:

```
/plugin marketplace add coreyhaines31/marketingskills
/plugin install marketing-skills@marketingskills
```

Ese comando no está disponible en Claude Code web ni en sesiones remotas, que
es la razón por la que aquí se optó por la copia directa.
