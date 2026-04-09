# Xbit — Inteligência em Criptomoedas

Plataforma de educação financeira e análise de criptomoedas.

---

## 🚀 Como rodar o projeto

### 1. Instale o Node.js
Baixe em: https://nodejs.org (versão LTS)

### 2. Abra o terminal na pasta do projeto
```
cd xbit
```

### 3. Instale as dependências
```
npm install
```

### 4. Configure o Firebase (veja abaixo)

### 5. Rode o projeto
```
npm start
```
O site abre automaticamente em http://localhost:3000

---

## 🔥 Configurando o Firebase

### Passo a passo:

1. Acesse https://console.firebase.google.com
2. Clique em "Criar projeto" → dê um nome (ex: xbit-app)
3. No menu lateral, clique em "Authentication" → "Começar"
   - Ative o provedor: **E-mail/senha**
4. No menu lateral, clique em "Firestore Database" → "Criar banco de dados"
   - Escolha "Iniciar no modo de teste"
5. No menu lateral, clique na engrenagem ⚙️ → "Configurações do projeto"
6. Role até "Seus aplicativos" → clique em `</>` (Web)
7. Registre o app → copie as credenciais

### Cole as credenciais em `src/services/firebase.js`:
```js
const firebaseConfig = {
  apiKey: "SUA_API_KEY",
  authDomain: "SEU_PROJECT.firebaseapp.com",
  projectId: "SEU_PROJECT_ID",
  storageBucket: "SEU_PROJECT.appspot.com",
  messagingSenderId: "SEU_SENDER_ID",
  appId: "SEU_APP_ID",
};
```

---

## 📁 Estrutura do projeto

```
xbit/
├── public/
│   └── index.html
├── src/
│   ├── components/
│   │   ├── UI.js          # Componentes reutilizáveis
│   │   └── Navbar.js      # Barra de navegação
│   ├── contexts/
│   │   └── AuthContext.js # Contexto de autenticação
│   ├── pages/
│   │   ├── Login.js       # Login, cadastro, recuperação
│   │   ├── Onboarding.js  # Configuração inicial do perfil
│   │   ├── Dashboard.js   # Painel principal
│   │   ├── Carteira.js    # Carteira sugerida
│   │   ├── Educacao.js    # Módulos de ensino
│   │   ├── Relatorios.js  # Relatórios de mercado
│   │   ├── Alertas.js     # Alertas e notificações
│   │   ├── Comunidade.js  # Grupos por nível
│   │   ├── Planos.js      # Planos e assinaturas
│   │   └── Perfil.js      # Perfil do usuário
│   ├── services/
│   │   └── firebase.js    # Firebase + lógica de negócio
│   ├── App.js             # Roteamento principal
│   ├── index.js           # Entrada da aplicação
│   └── index.css          # Estilos globais
└── package.json
```

---

## 🏷️ Sistema de níveis

| Nível | Capital mínimo |
|-------|---------------|
| 1     | R$ 5.000      |
| 2     | R$ 10.000     |
| 3     | R$ 20.000     |
| 4     | R$ 30.000     |
| 5     | R$ 50.000     |
| 6     | R$ 100.000    |
| 7     | R$ 1.000.000  |

---

## ⚠️ Aviso legal

Este conteúdo tem caráter educativo e não constitui recomendação de investimento.
