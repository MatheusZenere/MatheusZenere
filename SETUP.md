# Setup & Deploy

## Local Setup

1. **Clone o repositório:**
   ```bash
   git clone https://github.com/MatheusZenere/MatheusZenere.git
   cd MatheusZenere
   ```

2. **Crie um GitHub Personal Access Token:**
   - Vá em: https://github.com/settings/tokens
   - Clique em "Generate new token (classic)"
   - Selecione as permissões:
     - `read:user` (conta)
     - `repo` (repositórios)
   - Copie o token

3. **Configure o `.env`:**
   ```bash
   cp .env.example .env
   ```
   - Abra `.env` e preencha com seu token e username

4. **Instale as dependências:**
   ```bash
   pip install -r requirements.txt
   ```

5. **Rode o script localmente:**
   ```bash
   python today.py
   ```

## Deploy Automático (GitHub Actions)

1. **Vá em:**
   - Settings → Secrets and variables → Actions

2. **Crie dois secrets:**
   - `ACCESS_TOKEN`: seu GitHub token
   - `USER_NAME`: seu username do GitHub

3. **O workflow roda automaticamente:**
   - Diariamente às 00:00 UTC
   - Ou manualmente em: Actions → Update README → Run workflow

## Segurança

- ✅ `.env` está em `.gitignore`
- ✅ Segredos são guardados no GitHub Actions
- ✅ Token nunca fica visível no repositório
- ✅ Workflow faz commit com as mudanças dos SVGs
