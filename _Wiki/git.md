# Git — Comandos e fluxo básico

Esse documento reúne comandos essenciais e um fluxo prático (terminal + VS Code) do ciclo: criar branch → desenvolver → enviar → pull request → atualizar e continuar.

## Comandos principais (resumo)
- `git clone <url>` — copia o repositório remoto para sua máquina.
- `git status` — mostra estado dos arquivos e branch atual.
- `git branch` / `git branch -a` — lista branches locais (e remotas com `-a`).
- `git switch <branch>` — muda para outra branch (`git checkout <branch>` alternativa).
- `git fetch origin` — baixa referências/remotas sem alterar sua branch local.
- `git pull origin <branch>` — busca e faz merge automático (equivale a `fetch` + `merge`).
- `git push origin <branch>` — envia commits locais para o remoto.
- `git push origin --delete <nome-da-branch>` — remove branch no repositório remoto.
- `git branch -d <branch>` / `git branch -D <branch>` — apaga branch local (`-D` força).

## Fluxo básico de trabalho (objetivo)
1. Criar branch: `git switch -c feature/minha-tarefa` — isola o trabalho.
2. Desenvolver: adicionar/alterar arquivos localmente.
3. Commit: `git add .` e `git commit -m "mensagem"` — registra alterações localmente.
4. Push: `git push origin feature/minha-tarefa` — publica sua branch e commits no remoto.
5. Abrir Pull Request (no GitHub/GitLab/etc): revisar, testar e aprovar.
6. Merge: após aprovação, a branch é mesclada na `main` (ou outra branch de destino).
7. Atualizar seu repositório local e sua branch:
	- Trazer mudanças da `main` remota: `git fetch origin` e `git switch main` → `git pull origin main`.
	- Voltar para sua branch: `git switch feature/minha-tarefa` e integrar `main` nela: `git merge main` (ou `git rebase main` se preferir).
	- Resolver conflitos, commitar e `git push origin feature/minha-tarefa`.
8. Continuar o desenvolvimento repetindo o ciclo.

## Fluxo resumido no VS Code (passos práticos)
- Commit: abra Source Control (Ctrl+Shift+G), escreva a mensagem e clique em Commit (✔️).
- Push: Use o menu de três pontos no painel Source Control → `Push` (ou `Push to...` para escolher remoto/branch).
- Criar/Trocar branch: clique no nome da branch no canto inferior esquerdo → `Create Branch` ou `Checkout` para trocar.
- Publicar branch: após criar localmente, clique em `Publish Branch` para enviar ao remoto.
- Criar Pull Request: abra o repositório no GitHub (ou use a extensão GitHub PR) e crie o PR com a branch publicada.
- Após merge no remoto: no VS Code, `Pull` na `main` (ou `Pull From...` → `origin/main`) para atualizar o `main` local.
- Trazer `main` para sua branch: mude para sua branch local e escolha `Merge` → selecione `main` (ou faça `git merge main` no terminal integrado). Resolva conflitos e faça push.

## Observações importantes e boas práticas
- Sempre troque para outra branch antes de apagar uma branch local (`git switch main`).
- Use `git fetch --prune` para remover refs remotas obsoletas localmente.
- Prefira `merge` quando quiser preservar histórico explícito; `rebase` deixa um histórico linear (use com cuidado).
- Escreva mensagens de commit claras; PRs com descrição objetiva facilitam a revisão.

## Exemplo prático (fluxo completo curto)
1. `git switch -c feature/x`
2. editar código → `git add .` → `git commit -m "feat: implementar X"`
3. `git push origin feature/x` → abrir PR no GitHub → revisão → merge
4. `git switch main` → `git pull origin main`
5. `git switch feature/x` → `git merge main` → resolver conflitos → `git push origin feature/x`

---