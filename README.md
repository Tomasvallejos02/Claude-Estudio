# Claude-Estudio

## Integración MCP: Conciliabot

Este proyecto declara el servidor MCP de [Conciliabot](https://mcp.conciliabot.ar/mcp) en `.mcp.json` para que Claude Code lo cargue automáticamente al abrir el repo.

### Configuración

El token de autenticación **no** se guarda en el repositorio. Antes de usar Claude Code en este proyecto, configurá la variable de entorno `CONCILIABOT_MCP_TOKEN` con tu token de Conciliabot:

```bash
export CONCILIABOT_MCP_TOKEN="cbp_..."
```

`.mcp.json` referencia esta variable (`${CONCILIABOT_MCP_TOKEN}`) para armar el header `Authorization: Bearer ...` sin exponer el valor real. Nunca commitees el token directamente en `.mcp.json` ni en ningún otro archivo del repo.
