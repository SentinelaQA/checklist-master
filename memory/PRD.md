# PRD — Checklist de Qualidade

## Problema Original
Projeto clonado de https://github.com/SentinelaQA/checklist-master com erro de conexão Firebase.

## Stack
- HTML/CSS/JS puro (sem framework)
- Firebase Authentication + Cloud Firestore
- Vite (build tool)
- Firebase Hosting (deploy)

## Arquivos Principais
- `public/login.html` — tela de login
- `public/checklist.html` — sistema principal

## O que foi implementado

### 2025-02 — Correção de Erros Firebase
1. **Bug Corrigido: Regras Firestore ausentes**
   - Criado `firestore.rules` com regras de acesso por usuário autenticado
   - Criado `firestore.indexes.json`

2. **Bug Corrigido: Admin deslogado ao criar usuário**
   - `createUserWithEmailAndPassword` usava a auth principal, deslogando o admin
   - Solução: app Firebase secundário (`initializeApp(firebaseConfig, 'Secondary')`)
   - `signOut(secondaryAuth)` após criação para limpar sessão secundária

3. **Configuração Firebase completa**
   - `firebase.json` com hosting + regras
   - `.firebaserc` com projeto vinculado
   - `DEPLOY.md` com guia passo a passo

## Próximos Passos
- [ ] Usuário deve publicar regras Firestore no console Firebase
- [ ] Usuário deve usar "Save to Github" para enviar ao GitHub
- [ ] Deploy via `firebase deploy` ou GitHub Actions

## Backlog
- P1: Configurar domínio personalizado no Firebase Hosting
- P2: Notificações por e-mail para avaliações
- P3: Relatórios automáticos mensais
