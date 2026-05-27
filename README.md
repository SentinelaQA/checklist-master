# 📋 Checklist de Qualidade — SentinelaQA

Sistema web de monitorias de qualidade desenvolvido para controle e acompanhamento de avaliações de analistas de atendimento.

---

## 🧭 Sobre o sistema

O **Checklist de Qualidade** é uma plataforma interna utilizada pela equipe de Qualidade para realizar, registrar e acompanhar monitorias de atendimento. O sistema permite avaliar analistas com base em formulários específicos por caixa de atuação, registrar desvios, acompanhar métricas e gerar relatórios.

---

## ✨ Funcionalidades

### 📋 Formulários de Avaliação
- Formulários segmentados por área: **Agenda Financeira**, **Cancelamento**, **Suporte Conciliação** e **Eventos**
- Checklist com itens de **NC (Não Conformidade)** e **NCG (Não Conformidade Grave)**
- Cálculo automático de pontuação com desconto por item marcado
- Campo de observação por item descontado
- Exportação do formulário preenchido em **XLSX**

### 📊 Controle de Avaliações
- Tabela completa de todas as monitorias lançadas por categoria
- Filtros por analista, caixa e ciclo/mês
- Visualização de detalhes completos de cada monitoria (itens descontados, observações, data/hora da interação)
- Registro e acompanhamento de **contestações** (Procedente / Improcedente)
- Remarcação de ciclo retroativo para lançamentos atrasados
- Exportação dos registros filtrados em **XLSX**
- Notificação de novas monitorias lançadas

### 📈 Análise e Relatórios
- Overview com totais de monitorias, NC's, NCG's, média geral e contestações
- Gráficos por ciclo, caixa e analista
- Histórico completo de contestações com resultado e justificativa
- Filtro por mês

### 👤 Gestão de Analistas
- Cadastro de analistas com status: **Ativo, Férias, Afastado, Licença, Desligado, Outro**
- Registro de ausências com período, motivo e ciclos ausentes
- Retorno automático ao status **Ativo** quando a data de fim da ausência é atingida
- Edição das caixas de atuação de cada analista
- Controle de monitorias faltantes por ciclo atual com justificativa

### 👥 Gerenciar Usuários *(admin)*
- Cadastro de novos usuários com perfil (admin / analista)
- Log de acessos

---

## 🔐 Perfis de acesso

| Perfil | Permissões |
|--------|-----------|
| **Admin** | Acesso total: lançar, editar, excluir, contestar, remarcar ciclo, gerenciar analistas e usuários |
| **Usuário/Analista** | Visualização das monitorias, detalhes e contestações registradas (somente leitura) |

---

## 🛠️ Tecnologias utilizadas

- **HTML / CSS / JavaScript** — interface web single-page
- **Firebase Authentication** — autenticação de usuários
- **Cloud Firestore** — banco de dados em tempo real
- **SheetJS (XLSX)** — exportação de planilhas
- **Chart.js** — gráficos no dashboard

---

## 📁 Estrutura do repositório

```
checklist-master/
├── public/
│   ├── checklist.html   # Aplicação principal
│   └── login.html       # Tela de login
└── src/                 # Arquivos fonte (React/Vite)
```

---

## 👩‍💻 Desenvolvido por

**Yasmin de Melo Campos** — Analista de Qualidade Jr  
© 2025 SentinelaQA
