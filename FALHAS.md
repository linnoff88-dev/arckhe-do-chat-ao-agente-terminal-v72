# FALHAS — do-chat-ao-agente-terminal-v72

| data | o que quebrou | menor correçêo | prompt \| infra |
|---|---|---|---|
| 2026-10-19 | Capa EN/ES pelo Codex image_gen saiu com a capa de OUTRO curso: com 4 agentes gerando ao mesmo tempo, o Codex copiou o PNG mais recente de `~/.codex/generated_images/` (de outra sessêo) | pedir ao Codex só para gerar (sem copiar arquivo) e pegar a imagem na pasta da PRÓPRIA sessêo (`session id` do log) | infra + prompt |
| 2026-10-19 | Traduçêo manteve regra "Write in Portuguese" no modelo de AGENTS.md e "êxito"/"Saídas" com grafia PT | corrigir as entradas em `i18n/<lang>.json` e rodar `traduzir.py` de novo (só cache) | prompt |
