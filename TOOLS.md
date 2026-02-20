# TOOLS.md - Local Notes

## ClickUp

- **API Key:** Salva em `/root/.openclaw/credentials/clickup.json`
- **Workspace:** Shopee (ID: 90133006700)
- **Spaces:**
  - Espaço da equipe (901313069561)
  - Rafael (901313201192)
  - Trello Rafael (901313203043)

### Comandos úteis

```bash
# Listar tasks do space "Espaço da equipe"
curl -H "Authorization: $CLICKUP_TOKEN" "https://api.clickup.com/api/v2/team/90133006700/space/901313069561/list"

# Criar task
curl -X POST -H "Authorization: $CLICKUP_TOKEN" \
  -H "Content-Type: application/json" \
  "https://api.clickup.com/api/v2/list/{list_id}/task" \
  -d '{"name": "Nova task", "description": "Descrição"}'
```

## Telegram

- **Bot Token:** Configurado no OpenClaw
- **Chat ID:** 6463394115 (Harllen)

## Git Backup

- **Repo:** git@github.com:harllen1996/Memorias-openclaw.git
- **Schedule:** A cada 2 horas

## Veritas Kanban

- **URL:** http://localhost:3000 (web) | http://localhost:3001 (api)
- **Admin Key:** `atlas-admin-key-2026-harllen-shopee-secure`
- **Localização:** `/root/veritas-kanban`

### API Endpoints

```bash
# Listar tasks
curl -H "Authorization: Bearer atlas-admin-key-2026-harllen-shopee-secure" \
  http://localhost:3001/api/tasks

# Criar task
curl -X POST \
  -H "Authorization: Bearer atlas-admin-key-2026-harllen-shopee-secure" \
  -H "Content-Type: application/json" \
  http://localhost:3001/api/tasks \
  -d '{"title": "Nova task", "description": "Descrição", "type": "code"}'

# Atualizar status
curl -PATCH \
  -H "Authorization: Bearer atlas-admin-key-2026-harllen-shopee-secure" \
  -H "Content-Type: application/json" \
  http://localhost:3001/api/tasks/{id} \
  -d '{"status": "in-progress"}'
```

### Status possíveis
- `todo` — A fazer
- `in-progress` — Em progresso
- `done` — Concluído

### Tipos de task
- `code` — Código
- `research` — Pesquisa
- `automation` — Automação
