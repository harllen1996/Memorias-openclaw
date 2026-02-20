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
