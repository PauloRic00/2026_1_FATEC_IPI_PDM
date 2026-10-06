# Repositório — Programação para Dispositivos Móveis (Fatec Ipiranga)

Este repositório contém os códigos e projetos desenvolvidos durante as aulas da disciplina de **PDM** (Programação para Dispositivos Móveis) na **Fatec Ipiranga** (Semestre 2026/1).  
O foco principal deste projeto é o estudo prático e o desenvolvimento de aplicações móveis modernas, abordando desde a criação de interfaces reativas e navegação entre telas até o gerenciamento de estado, consumo de APIs e integração com recursos do dispositivo.

---

## Funcionalidades e Tópicos Abordados

* **Componentes e UI Móvel:** Construção de interfaces de usuário dinâmicas, adaptáveis e amigáveis utilizando componentes nativos e estilização flexível (Flexbox).
* **Navegação e Fluxo de Telas:** Implementação de pilhas de navegação (Stack), abas (Tabs) e menus para uma experiência fluida de transição entre telas.
* **Gerenciamento de Estado:** Manipulação de estados locais e globais (`useState`, `useContext` ou gerenciadores dedicados) para atualização reativa da interface.
* **Consumo de APIs REST:** Integração assíncrona com serviços web externos para busca, envio e sincronização de dados em tempo real no aplicativo.
* **Persistência Local e Recursos Nativos:** Armazenamento de dados no dispositivo (ex: AsyncStorage/SQLite) e acesso a funcionalidades do dispositivo (Câmera, GPS/Localização).

---

## Arquitetura e Estrutura dos Arquivos

O repositório está dividido conceitualmente entre as camadas de interface, roteamento e serviços do aplicativo:

| Arquivo / Diretório | Descrição |
| :--- | :--- |
| `src/components/` | Componentes reutilizáveis de interface (botões estilizados, cards, campos de entrada, modais). |
| `src/screens/` | Telas e páginas principais do aplicativo móvel (Home, Detalhes, Perfil, Configurações). |
| `src/navigation/` | Configuração das rotas e controle do fluxo de navegadores (Stack, Tab Navigator). |
| `package.json` | Arquivo de manifesto do Node.js contendo as dependências mobile e scripts de inicialização. |
| `.env` | (Omitido do controle de versão) Arquivo de parametrização para URLs de API e chaves privadas do aplicativo. |

---

## Aprendizado Progressivo de Conceitos

Através do desenvolvimento dos módulos e aplicativos móveis, foi possível consolidar uma evolução clara de conceitos essenciais para o ecossistema de desenvolvimento mobile:

### 1. Layouts Reativos e Componentização
* **Design System e Flexbox:** Compreensão da anatomia dos componentes visuais e alinhamento responsivo para diferentes tamanhos de tela e orientações (Portrait/Landscape).
* **Reutilização de Código:** Criação de componentes genéricos e modulares, otimizando o tempo de renderização e manutenção do app.

### 2. Controle de Fluxo e Estado
* **O Problema (Telas Isoladas):** A dificuldade em compartilhar dados de usuário e manter a consistência do estado ao navegar por múltiplos fluxos.
* **A Solução (Roteadores e Contextos):** Utilização de navegadores estruturados e passagem de propriedades (*props*) ou contextos globais para manter as informações sincronizadas.

### 3. Integração Assíncrona e Segurança
* **Requisições HTTP Móveis:** Comunicação eficiente com APIs externas utilizando `fetch`/`axios`, tratando estados de carregamento (*loading*) e cenários de erro ou ausência de conexão.
* **Variáveis de Ambiente (`dotenv`):** Proteção de endpoints e chaves de serviços de terceiros através de variáveis carregadas no `process.env`, evitando o versionamento de dados sensíveis no Git via `.gitignore`.

---

## Como Executar o Projeto de PDM

### Pré-requisitos
* **Node.js** instalado na máquina.
* Aplicativo **Expo Go** instalado no smartphone ou um **Emulador Android/iOS** configurado no computador.

### Passos para configuração e execução:

1. **Acesse o diretório do projeto:**
   ```bash
   cd 20261_fatec_ipi_pdm

2. **Instale as dependências do pacote:**
   ```bash
   npm install

3. **Configure as Variáveis de Ambiente:**
  
   Crie um arquivo chamado .env na raiz do projeto e preencha com as suas configurações:
   ```bash
   API_BASE_URL=[https://api.exemplo.com/v1](https://api.exemplo.com/v1)
   APP_ENV=development

4. **Inicie o servidor de desenvolvimento:**
   ```bash
   npm start

5. **Abra a aplicação no dispositivo:**
   
   Escaneie o código QR gerado no terminal utilizando a câmera do dispositivo (iOS) ou o aplicativo Expo Go (Android).
