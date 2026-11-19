# 📘 Guia Rápido de Git e GitHub

Resumo prático dos principais comandos usados para versionar projetos e enviá-los ao GitHub.

---

## 1. Configuração Inicial (apenas uma vez no computador)

Define quem é o autor dos commits e o nome padrão da branch principal:

```bash
git config --global user.name "Seu Nome"
git config --global user.email "seu-email@exemplo.com"
git config --global init.defaultBranch main
```

---

## 2. Iniciar um Novo Repositório e Enviar ao GitHub

Use esta sequência na primeira vez que for conectar uma pasta local a um repositório vazio criado no GitHub:

```bash
git init
git add .
git commit -m "Primeiro commit"
git branch -M main
git remote add origin https://github.com
git push -u origin main
```

---

## 3. Rotina do Dia a Dia (Enviar Atualizações)

Sempre que criar ou editar arquivos no projeto, siga estes 3 passos:

1. **Verificar o que foi alterado:**
   ```bash
   git status
   ```
2. **Preparar todos os arquivos modificados:**
   ```bash
   git add .
   ```
3. **Salvar a versão (commit) com uma mensagem clara:**
   ```bash
   git commit -m "Descrição do que foi feito"
   ```
4. **Enviar para o GitHub:**
   ```bash
   git push
   ```

---

## 4. Baixar Atualizações do GitHub

Se você alterou algum arquivo direto no site do GitHub ou em outro computador:

```bash
git pull
```

---

## 5. Erros Comuns e Soluções Rápidas

| Erro | O que significa | Como resolver |
| :--- | :--- | :--- |
| `fatal: not a git repository` | Você não está na pasta do projeto ou ainda não rodou `git init`. | Entre na pasta certa (`cd caminho/da/pasta`) ou rode `git init`. |
| `fatal: repository '...' not found` | O link do repositório remoto está errado ou incompleto. | Atualize o link com `git remote set-url origin <URL-CORRETA>`. |
| `remote origin already exists` | Já existe um endereço remoto configurado. | Substitua usando `git remote set-url origin <URL-CORRETA>`. |
| `rejected (fetch first)` | O GitHub tem arquivos que ainda não estão no seu computador. | Rode `git pull origin main --allow-unrelated-histories` e depois `git push`. |

---
*Material de apoio criado durante o **Curso Python — Conectadas**.*
