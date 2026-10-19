# Onoxia AI — Frontend Institucional & ChatBot

Plataforma institucional de inteligência artificial cujo produto principal é um **ChatBot moderno, intuitivo, elegante e responsivo**, desenhado em tema escuro premium com destaques seletivos em vermelho rubro, de acordo com o design system da Onoxia.

---

## 📁 Estrutura de Pastas do Projeto

```text
onoxia/
│
├── index.html              # Página Principal / Landing Page & Acesso
│
├── pages/                  # Todas as páginas internas da aplicação
│   ├── login.html          # Autenticação de utilizadores
│   ├── cadastro.html       # Registo de novas contas e escolha de Persona
│   ├── recuperar-senha.html# Recuperação de palavra-passe
│   ├── chat.html           # ChatBot Principal com Modo de Voz
│   ├── historico.html      # Gestão e pesquisa de histórico de conversas
│   ├── projetos.html       # Gestão estratégica de projetos e metas
│   ├── perfil.html         # Perfil de utilizador e estatísticas
│   └── configuracoes.html  # Preferências, acessibilidade e armazenamento
│
├── assets/
│   ├── images/             # Imagens e marcas oficiais
│   │   ├── logo-onoxia.png         # [Reservado] Logótipo completo
│   │   ├── logo-onoxia-symbol.png  # [Reservado] Símbolo rubro em espiral
│   │   ├── blood-cells-hero.png    # [Reservado] Células sanguíneas em 3D
│   │   └── onoxia-avatar.png       # [Reservado] Avatar do assistente
│   └── icons/
│
├── css/
│   ├── styles.css          # Tipografia, variáveis de cor, animações
│   └── components.css      # Botões, inputs, cartões, toasts e modais
│
├── js/
│   ├── app.js              # Toasts, modais, menu mobile, navegação
│   ├── auth.js             # Validação e simulação de autenticação
│   ├── chat.js             # Lógica do ChatBot, modo de voz e exportação
│   ├── history.js          # Pesquisa, filtragem e remoção de conversas
│   ├── profile.js          # Visualização e edição do perfil local
│   ├── settings.js         # Gestão de temas, idioma e preferências
│   └── storage.js          # Gestor de LocalStorage e dados padrão
│
└── README.md               # Documentação técnica e guia de execução
```

---

## 🎨 Paleta de Cores e Design System

- **Preto principal**: `#030405`
- **Preto secundário**: `#080C12`
- **Azul-preto dos painéis**: `#0A111B`
- **Superfície elevada**: `#101925`
- **Vermelho principal**: `#F20D2F`
- **Vermelho escuro**: `#A80720`
- **Vermelho luminoso**: `#FF2947`
- **Texto principal**: `#F8FAFC`
- **Texto secundário**: `#A8B2C2`
- **Bordas discretas**: `#243143`
- **Estado online**: `#22C55E`

---

## 🚀 Como Executar o Projeto

Este projeto foi construído em **HTML5 semântico**, **CSS3 puro**, **Tailwind CSS via CDN** e **JavaScript ES6+**. Não requer compiladores nem dependências de Node.js no cliente.

### Opção 1: VS Code (Live Server) — Recomendado
1. Abra a pasta do projeto no **Visual Studio Code**.
2. Clique com o botão direito sobre `index.html` (ou `chat.html`).
3. Selecione **"Open with Live Server"**.
4. O navegador abrirá automaticamente em `http://127.0.0.1:5500/index.html`.

### Opção 2: Servidor Local Simples (Python / Navegador)
```bash
# Com Python 3:
python -m http.server 3000

# Ou simplesmente abra qualquer arquivo .html diretamente no seu navegador.
```

---

## 🖼️ Personalização de Imagens (Assets)

Os nomes abaixo são caminhos reservados no HTML/CSS:

1. `assets/images/logo-onoxia.png` — Logótipo oficial com fundo transparente.
2. `assets/images/logo-onoxia-symbol.png` — Símbolo em espiral com gota rubra.
3. `assets/images/blood-cells-hero.png` — Imagem com células sanguíneas e profundidade 3D.
4. `assets/images/onoxia-avatar.png` — Avatar do assistente ou perfil.

> **Fallback Automático**: Se os ficheiros PNG ainda não tiverem sido adicionados, o sistema utiliza automaticamente vetores SVG e composições de iluminação, garantindo que nunca surjam ícones de imagem quebrada.

---

## 💡 Modo de Demonstração e Preparação para Backend

- **Armazenamento**: O histórico de conversas, o perfil de utilizador e as preferências são salvos de forma privada no `LocalStorage` do navegador.
- **Respostas de Demonstração**: O módulo `js/chat.js` inclui um gerador contextual de respostas em português (Angola / Lusófono) para testes de interface.
- **Integração Futura com IA**: A função `triggerBotResponse(prompt)` em `js/chat.js` está desacoplada e preparada para substituir a resposta simulada por uma chamada `fetch('/api/chat', ...)` a um backend seguro com chaves de API protegidas.
