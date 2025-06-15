# Git TLDR

## Comandos mais usados

```sh
# Inicializar repositório
git init

# Clonar repositório
git clone <url-do-repo>

# Verificar status
git status

# Adicionar arquivos para commit
git add <arquivo-ou-pasta>
# Adicionar tudo
git add .

# Fazer commit
git commit -m "mensagem do commit"

# Ver histórico de commits
git log --oneline

# Ver branches
git branch

# Criar nova branch
git checkout -b nome-da-branch

# Trocar de branch
git checkout nome-da-branch

# Deletar branch local
git branch -d nome-da-branch

# Verificar URL do repositório remoto
git remote -v

# Alterar URL do repositório remoto
# (exemplo: mudar para SSH)
git remote set-url origin git@github.com:usuario/repo.git

# Adicionar repositório remoto
# (caso não exista)
git remote add origin <url-do-repo>

# Enviar branch para o remoto
# (primeiro push de uma branch nova)
git push -u origin nome-da-branch
# Push normal
git push

# Buscar atualizações do remoto
# (não altera arquivos locais)
git fetch

# Atualizar branch local com remoto
git pull

# Mesclar branch (merge)
git merge nome-da-branch

# Resolver conflitos: edite os arquivos, depois
#
git add <arquivo-resolvido>
git commit
```

## Como adicionar pasta vazia ao Git
O Git não versiona pastas vazias. Solução:

```sh
mkdir minha-pasta-vazia
cd minha-pasta-vazia
touch .gitkeep
cd ..
git add minha-pasta-vazia/.gitkeep
git commit -m "adiciona pasta vazia com .gitkeep"
```

## Como deletar arquivos de um repositório

Se você já versionou arquivos indesejados (ex: `__pycache__`, `.DS_Store`), siga estes passos para removê-los do repositório e evitar que voltem:

### 1. Adicione os padrões ao `.gitignore`
Crie ou edite o arquivo `.gitignore` na raiz do projeto e adicione:

```
__pycache__/
.DS_Store
```

### 2. Remova os arquivos do repositório (mas mantenha localmente)

```sh
git rm --cached -r __pycache__ .DS_Store
```
- O parâmetro `--cached` remove do repositório, mas mantém os arquivos no seu computador.
- O `-r` é para remover recursivamente pastas.

### 3. Faça commit das remoções

```sh
git commit -m "remove arquivos indesejados (__pycache__, .DS_Store) do repo"
```

### 4. Envie para o remoto

```sh
git push
```

Depois disso, o `.gitignore` impedirá que esses arquivos sejam adicionados novamente.

---

## Como usar e aplicar o .gitignore

1. **Crie um arquivo `.gitignore` na raiz do projeto:**
   
   Exemplo de conteúdo:
   ```
   # Ignorar pastas e arquivos comuns
   node_modules/
   .env
   dist/
   __pycache__/
   .DS_Store
   *.log
   ```

2. **Adicione arquivos ao .gitignore antes de versionar:**
   - Tudo que estiver listado será ignorado pelo Git nos próximos `git add`.

3. **Se já versionou arquivos que deveriam estar no .gitignore:**
   - Siga o tutorial acima para removê-los do repositório.

4. **Verifique o que está sendo ignorado:**
   ```sh
   git status --ignored
   ```

5. **Dica:**
   - Use [gitignore.io](https://www.toptal.com/developers/gitignore) para gerar `.gitignore` para diferentes linguagens e frameworks.

---

## Cuidados importantes
- **Nunca** suba arquivos sensíveis (.env, senhas, etc)
- Use `.gitignore` para ignorar arquivos/pastas
- Commits pequenos e frequentes
- Sempre escreva mensagens de commit claras
- Antes de subir código, faça `git pull` para evitar conflitos
- Use branches para novas features ou correções

## Dicas rápidas
- Ver arquivos modificados: `git status`
- Desfazer alterações não commitadas: `git checkout -- <arquivo>`
- Remover arquivo do stage: `git reset <arquivo>`
- Desfazer último commit (mantendo alterações): `git reset --soft HEAD~1`
- Stash (guardar alterações temporárias):
  - `git stash`
  - `git stash pop`

---

Copie e cole os comandos conforme sua necessidade. Para mais detalhes, consulte a [documentação oficial do Git](https://git-scm.com/doc). 