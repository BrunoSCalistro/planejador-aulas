# 📚 Planejador de Aulas

Aplicativo web para planejamento pedagógico, desenvolvido para professores que precisam organizar aulas, registrar conteúdos, acompanhar habilidades da BNCC e manter um banco de aulas reutilizáveis.

Funciona como um **PWA (Progressive Web App)** — pode ser instalado no celular como um app nativo, diretamente pelo navegador, sem precisar de loja de aplicativos.

🔗 **Acesse:** [brunoscalistro.github.io/planejador-aulas/planejador-aulas.html](https://brunoscalistro.github.io/planejador-aulas/planejador-aulas.html)

---

## ✨ Funcionalidades

### 🗓 Planejamento
- **Visualização por mês (Calendário)** — visão geral do mês com indicadores de aulas planejadas, rascunhos e sem plano
- **Visualização por semana** — grade detalhada por período e turno, com arrastar e soltar para reagendar aulas
- **Status de aulas** — rascunho (📝) ou publicada (✅), com indicadores visuais no calendário
- **Aula Avaliativa** — marcação especial (★) para aulas com instrumento formal de avaliação com nota
- **Exceções e aulas extras** — possibilidade de reagendar ou adicionar aulas fora da grade padrão

### 📋 Plano de Aula
Cada aula suporta os seguintes campos:
- Habilidades BNCC (com tags e descrição)
- Objetivo da Aula
- Conteúdo
- Dinâmica / Metodologia
- Material Utilizado
- Avaliação / Instrumentos
- Observações

### 📖 Banco de Aulas
- Criação de **aulas avulsas**, independente do planejamento
- Busca por texto, ano escolar, habilidade BNCC e objetivo
- **Aplicar ao planejamento** — use uma aula do banco diretamente em uma turma e data
- Exportação individual de cada aula

### 📋 Registro Pedagógico
- Gera automaticamente um registro em tópicos a partir dos dados do plano
- Estrutura: BNCC → Objetivo → Conteúdo → Metodologia → Material → Avaliação → Observações
- Copiar para área de transferência ou baixar como `.txt`

### ⬇ Exportação de Aulas
- **PDF** — abre janela de impressão formatada, basta salvar como PDF
- **DOCX** — compatível com Word, Google Docs e LibreOffice
- **Google Drive** — salva diretamente em uma pasta de sua escolha no Drive

### 📊 Relatório e Trimestres
- Relatório de aulas por turma e trimestre, com filtro de rascunhos
- Cadastro de trimestres com datas de início e término
- Indicador visual de progresso do planejamento por trimestre

### ☁ Integração com Google Drive
- Backup automático dos dados de planejamento na nuvem
- Sincronização ao salvar qualquer alteração
- Importação de dados existentes ao reconectar

---

## 📱 Instalação como App (PWA)

### Android (Chrome)
1. Acesse o link do app no Chrome
2. Toque nos **três pontinhos** (menu) no canto superior direito
3. Toque em **"Adicionar à tela inicial"** ou **"Instalar app"**
4. Confirme — o ícone aparece na tela inicial

### iPhone / iPad (Safari)
1. Acesse o link no **Safari** (obrigatório — o Chrome no iOS não suporta instalação de PWA)
2. Toque no botão de **compartilhar** (quadrado com seta para cima)
3. Role a lista e toque em **"Adicionar à Tela de Início"**
4. Confirme

> O app funciona **offline** após a instalação. Os dados ficam salvos localmente e sincronizam com o Google Drive quando houver conexão.

---

## 🖥 Interface

### Desktop
- Sidebar lateral com turmas, trimestres e legenda
- Abas de navegação no topo: Calendário, Semana, Busca, Banco, Trimestres, Relatório

### Mobile
- **Header compacto** com menu (☰), título da tela atual e botão de nova turma
- **Menu lateral deslizante** (drawer) com turmas, ações e configurações
- **Barra de navegação inferior** com as principais seções
- Modais em **bottom sheet** (deslizam de baixo para cima)

---

## 🔧 Configuração do Google Drive (opcional)

Para ativar o backup automático:

1. Acesse [console.cloud.google.com](https://console.cloud.google.com/)
2. Crie um projeto e ative a **Google Drive API**
3. Vá em **Credenciais → Criar → ID do cliente OAuth → Aplicativo da Web**
4. Adicione a URL do app como origem autorizada
5. Copie o **Client ID** gerado
6. No app, clique no botão **Drive** no topo e cole o Client ID

---

## 💾 Dados e Privacidade

- Todos os dados são salvos **localmente no navegador** (`localStorage`)
- O backup no Google Drive é opcional e usa apenas a permissão `drive.file` — o app só acessa arquivos que ele mesmo criou
- Nenhum dado é enviado para servidores externos além do Google Drive (quando configurado)

---

## 🛠 Tecnologias

- HTML5 + CSS3 + JavaScript puro (sem frameworks)
- PWA com Service Worker para funcionamento offline
- Google Identity Services (OAuth2) para integração com Drive
- Hospedado via GitHub Pages

---

## 📁 Estrutura do Repositório

```
planejador-aulas/
├── planejador-aulas.html   # App completo (arquivo único)
└── manifest.json           # Configuração PWA (nome, ícone, cores)
```

---

## 📄 Licença

Uso pessoal. Projeto desenvolvido para fins educacionais.
