# CLAUDE.md — do-chat-ao-agente-terminal-v72

Curso completo do degrau 1 (Do chat para o terminal / OSWork) da formaçêo Do chat ao agente, no formato ARCKHÉ Learning v7.2 (skill `formato-curso-v72`). Visêo geral da formaçêo: https://linnoff88-dev.github.io/ (nêo editar daqui).

- Conteúdo em `conteudo/pt/`; nunca editar o HTML gerado à mêo: editar o JSON e rodar o portêo.
- Portêo: `python3 gerar.py && python3 validar.py --links` + `node ~/.claude/skills/formato-curso-v72/scripts/conferir-tela.cjs .` (HTTP local, 1366/390).
- Tipo de seçêo próprio deste curso: `simterm` (terminal de ensaio com missões) — `sec_simterm` em `gerar.py`, `assets/terminal.js` e `assets/terminal.css`. Campos: `janela`, `sistema` (windows|linux), `inicio` (caminho/prompt inicial), `sufixo` (">" padrêo; "" quando `inicio`/`vai` já trazem o fim do prompt), `missoes [{pede, aceita[], saida (aceita {cwd}), vai?, explica, mostra?}]`, `fim`, `legenda`.
- EN/ES (7.3): `conteudo/en|es/` vêm de `python3 ~/.claude/skills/formato-curso-v72/scripts/traduzir.py . en es` (Codex da assinatura, cache em `i18n/`, glossário em `i18n/glossario.json`); saem em `en/` e `es/`. Capa por idioma: `assets/img/capa-en.jpg`, `capa-es.jpg`.
- simterm em EN/ES: caminhos de `terminal.js`/`terminal.css` usam `ativo(prefixo)` (raiz do repo), nunca `prefixo`. Todo texto visível vem do JSON (`pede`, `explica`, `saida`, `fim`, `janela`, `legenda`) ou do `ui` (`st_*`: botões, "Missêo {n} de {t}", erros) — nada fixo em `terminal.js`. Comandos e caminhos (`aceita`, `mostra`, `vai`, `inicio`, `sufixo`, `sistema`) o `gerar.py` pega SEMPRE do PT: o aluno digita o mesmo comando em qualquer idioma.
- Fonte do conteúdo: `~/projetos/oswork-v62`, `~/projetos/oswork-quick`, `~/projetos/jornada-agentes/exercicios/01-oswork.md`. Nêo inventar comando nem número.
- Imagens: Codex image_gen na assinatura (luz neutra, sem texto; capa com texto). Fontes em `img-src/` (fora do Git).
- Autor dos commits: `linnoff88-dev <linnoff88-dev@gmail.com>`. Publicaçêo = commit + push (GitHub Pages, raiz da main).

## Self-learning

When I correct you, or you catch yourself making a mistake: before continuing, add the lesson as a one-line rule at the TOP of the Lessons section below.

## Lessons

- Marca-texto (anotaçêo) dentro de elemento flex/grid vira item solto e abre espaço no meio da palavra: o texto anotável tem que estar num `span`/`p` próprio (ex.: `.nesta2 li > span`). Bloco anotável novo → conferir o `display` dele (18/10/2026).
- Rolagem guiada no desktop: o texto da etapa fica DENTRO do painel fixo (legenda que troca); cartões rolando por baixo do diagrama aparecem cortados e espiando no topo — o Nei viu na aula 1 (18/10/2026).
- Rolagem guiada: posiçêo de destino calculada com o diagrama JÁ grudado no topo (top do sticky + altura), nunca pela posiçêo atual; e a etapa só vira ativa quando o cartêo está visível abaixo do diagrama (18/10/2026).
- Menu do topo de curso segue o padrêo v2 (curso | ARCKHÉ AI - PRO à esquerda; seções e Aa à direita); nêo inventar outro topo (18/10/2026).
- Simulaçêo com falha proposital: amarrar a falha à primeira execuçêo da tarefa, nêo à primeira rodada — senêo interromper e retomar esconde a falha (18/10/2026).
- Validar por HTTP local, nunca `file://` (o progresso e os caminhos relativos se comportam diferente) (18/10/2026).
