- Iniciando Repositório
```bash
git init
```

- Adicionando ao stage
```bash
git add .
```

- Adicionando etiqueta ao stage
```bash
git commit -m "first commit"
```
> [!IMPORTANTE]
> Utilizar mensagens objetivas e curtas

- Informações de commits
```bash
git log
git log --oneline
git log -n 3
```

- Visualizar os estágios dos arquivos
```bash
git status
```

- Comparar modificações
```bash
git diff
```

- Desfazendo alteração
```bash
git restore nomedoarquivo.html
```

- Restaurando da Staged
```bash
git restore --staged nomedoarquivo.html
gist restore --staged .
```

- Corrigindo ultimo commit
```bash
git commit --amend -m "mudança de etiqueta do ultimo commit"
```

- Desfazendo ultimo commit
```bash
git reset --soft HEAD-1
```