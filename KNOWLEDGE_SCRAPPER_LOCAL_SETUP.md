# Knowledge Scrapper Local Setup

**Project Name:** Knowledge Scrapper
**Date:** June 8, 2026
**Origin Repo:** https://github.com/Harshaldorlikar/firecrawl-ks
**Upstream Repo:** https://github.com/firecrawl/firecrawl

## Purpose of the Workspace
This local workspace sets up a fork of Firecrawl to serve as the foundation for the Knowledge Vault ingestion pipeline. 

This repository will later be customized for:
- Knowledge Vault source crawling
- Normalization
- Chunking
- Embedding
- Content-hash deduplication
- Supabase upsert to `docs_vault_chunks`

**Note:** None of the above ingestion customization features have been implemented yet. This is purely a baseline setup for the upstream codebase.

## Local Setup Findings
- **Important Files Discovered:** `docker-compose.yaml`, `package.json`, `apps/api/.env.example`
- **Startup Docs Discovered:** `SELF_HOST.md`, `README.md`
- **Expected Env Files:** The setup expects an `.env` file in the root directory. This has been created from the `SELF_HOST.md` template with placeholders.
- **Likely Local Boot Command(s):** 
  - `docker compose build`
  - `docker compose up`

## Do Not Change Yet
- Upstream crawl engine internals
- Firecrawl service wiring
- Docker setup (`docker-compose.yaml`)
- App code unrelated to future ingestion customization

## Likely Future Customization Areas
- `apps/api/src/` (Main logic for handling crawls and routing data)
- Database schema / configurations to adapt to Supabase upsert paths
- Potential new folders or services to handle Knowledge Vault specific chunking and embedding pipelines
