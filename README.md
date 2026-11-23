# Agendador — GEX Cloud Bot (Runner Público Ilimitado)

Repositório público dedicado exclusivamente à execução em nuvem do coletor `gex_profile_v7_cloud.py` (minutos ilimitados no GitHub Actions), mantendo o repositório principal (`gex_profile_v7`) privado com suas estratégias e indicadores do NinjaTrader.

## Configuração Obrigatória (1x apenas)

1. **Dropbox Secrets** neste repositório (`Settings → Secrets and variables → Actions → New repository secret`):
   - `DBX_SECRET`
   - `DBX_REFRESH`
2. **Disparador Externo Gratuito (`cron-job.org`)** apontando para:
   - **Method:** `POST`
   - **URL:** `https://api.github.com/repos/alanbezerrasilva70-ux/Agendador/actions/workflows/main.yml/dispatches`
   - **Body:** `{"ref":"main"}`
   - **Headers:** `Authorization: Bearer <FINE_GRAINED_PAT>`, `Accept: application/vnd.github+json`, `X-GitHub-Api-Version: 2022-11-28`, `Content-Type: application/json`
