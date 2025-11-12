# 🎧 Alive - Music Player Web 🎶

## ✨ Descrição
O **Alive** é uma aplicação web de reprodutor de música moderna e responsiva, desenvolvida com Node.js e Express. Sua principal característica é a experiência de áudio imersiva e altamente visual, com recursos que dão "vida" à música através de efeitos dinâmicos e sincronizados.

## 💡 Funções em Destaque

* **🌈 Tema Dinâmico:** O player adapta-se visualmente, alterando suas cores de fundo e gradientes com base na paleta de cores da capa do álbum da música atual.
* **❤️‍🔥 Efeito Pulse (BPM):** Um efeito de "pulsação" no fundo da tela que se sincroniza com os *Beats Per Minute* (BPM) da faixa em reprodução, se a informação estiver disponível, aumentando a imersão.
* **🤖 Curiosidades da IA:** Um botão dedicado que utiliza um serviço de Inteligência Artificial para gerar e exibir fatos interessantes sobre a canção que está tocando.
* **📊 Visualizador de Áudio:** Exibe uma visualização gráfica simples e em tempo real das frequências sonoras.
* **📱 Responsividade Total:** Interface otimizada para computadores e dispositivos móveis, com layouts compactos e menus estilo *drawer* para a fila de reprodução e playlists.
* **▶️ Controles Completos:** Inclui funções essenciais como Play/Pause, Shuffle, Repetição (faixa única/playlist) e atalhos de teclado.
* **⚙️ Backend Estruturado:** Utiliza Node.js, Express e SQLite para gerenciar e servir as músicas e listas de reprodução.



# 🎧 Alive - Music Player Web 🎶

## ✨ Descrição

O **Alive** é uma aplicação web de reprodutor de música moderna e responsiva, desenvolvida com **Node.js** e **Express**. Sua principal característica é a experiência de áudio imersiva e altamente visual, com recursos que dão "vida" à música através de efeitos dinâmicos e sincronizados.

-----

## 💡 Funções em Destaque

  * **🌈 Tema Dinâmico:** O *player* adapta-se visualmente, alterando suas cores de fundo e gradientes com base na paleta de cores da capa do álbum da música atual.
  * **❤️‍🔥 Efeito Pulse (BPM):** Um efeito de "pulsação" no fundo da tela que se sincroniza com os *Beats Per Minute* (BPM) da faixa em reprodução, se a informação estiver disponível, aumentando a imersão.
  * **🤖 Curiosidades da IA:** Um botão dedicado que utiliza um **Serviço de IA Generativa** para gerar e exibir fatos interessantes sobre a canção que está tocando.
  * **📊 Visualizador de Áudio:** Exibe uma visualização gráfica simples e em tempo real das frequências sonoras.
  * **📱 Responsividade Total:** Interface otimizada para computadores e dispositivos móveis, com layouts compactos e menus estilo *drawer* para a fila de reprodução e *playlists*.
  * **▶️ Controles Completos:** Inclui funções essenciais como Play/Pause, Shuffle, Repetição (faixa única/playlist) e **atalhos de teclado**.
  * **⚙️ Backend Estruturado:** Utiliza Node.js, Express e SQLite para gerenciar e servir as músicas e listas de reprodução.

-----

## 🛠️ Tecnologias Utilizadas

| Componente | Tecnologia | Uso Principal |
| :--- | :--- | :--- |
| **⚙️ Backend** | `Node.js` + `Express` | Servidor web e rotas de API. |
| **🗃️ Banco de Dados** | `SQLite3` | Armazenamento de dados de músicas e playlists. |
| **☁️ API Externa** | Serviço de IA Generativa | Geração de curiosidades sobre as músicas. |
| **💻 Frontend** | `HTML5`, `CSS3`, `JavaScript` | Interface do usuário, lógica de interatividade e animações. |
| **🎨 Utilitário JS**| `Color Thief` | Extração de cores das capas para o tema dinâmico. |
| **🔑 Config.** | `dotenv` | Gerenciamento de chaves de API e variáveis de ambiente. |

-----

## 📁 Estrutura do Projeto

```
/
├── public/                     # Arquivos estáticos do Frontend
│   ├── index.html              # Layout principal
│   ├── style.css               # Estilização
│   ├── projetoclp.js           # Lógica do Player (Visualizer, BPM Pulse, API calls)
│   ├── musicas/                # Arquivos de música (.mp3)
│   └── imgs/                   # Capas de álbum e outras imagens
├── server.js                   # Backend (Express, SQLite, AI API)
├── music.db                    # Banco de dados SQLite com dados de músicas
├── package.json                # Dependências e scripts
└── .env (NECESSÁRIO CRIAR)     # Variáveis de ambiente
```

-----

## 🚀 Instalação e Uso

### 1\. Pré-requisitos

  * **Node.js** (LTS recomendado)
  * **Chave de API** para o serviço de Inteligência Artificial

### 2\. Configuração do Projeto

1.  **⬇️ Instale as dependências** do Node.js listadas no `package.json`:
    ```bash
    npm install
    ```
2.  **🤖 Configure a API de IA:**
      * Crie um arquivo chamado **`.env`** na raiz do projeto.
      * Adicione sua chave de API, que deve ser definida como `OPENAI_API_KEY` (conforme o arquivo `server.js`) para a rota `/api/curiosities`:
        ```
        OPENAI_API_KEY="SUA_CHAVE_DE_API_AQUI"
        ```

### 3\. Execução

Inicie o servidor Node.js com o seguinte comando:

```bash
node server.js
```

O servidor será executado na porta **`3000`**.

Abra seu navegador e acesse: [http://localhost:3000](https://www.google.com/search?q=http://localhost:3000).

-----

## ➕ Como Adicionar Músicas

Para incluir novas faixas, insira registros nas tabelas `playlists` e `songs` no `music.db`.

1.  Coloque o arquivo **`.mp3`** 🎵 na pasta `public/musicas/`.
2.  Coloque a imagem de capa 🖼️ na pasta `public/imgs/`.
3.  No banco de dados, insira o novo registro, usando caminhos **relativos** à pasta `public/` para os campos `song_path` e `cover` (Ex: `./musicas/nome.mp3`). Preencher o campo **`bpm`** é opcional, mas ativa o efeito Pulse ❤️‍🔥.


# 🎧 Alive - Music Player Web 🎶

## ✨ Descrição
O **Alive** é uma aplicação web de reprodutor de música moderna e responsiva, desenvolvida com Node.js e Express. Sua principal característica é a experiência de áudio imersiva e altamente visual, com recursos que dão "vida" à música através de efeitos dinâmicos e sincronizados.

## 💡 Funções em Destaque

* **🌈 Tema Dinâmico:** O player adapta-se visualmente, alterando suas cores de fundo e gradientes com base na paleta de cores da capa do álbum da música atual.
* **❤️‍🔥 Efeito Pulse (BPM):** Um efeito de "pulsação" no fundo da tela que se sincroniza com os *Beats Per Minute* (BPM) da faixa em reprodução, se a informação estiver disponível, aumentando a imersão.
* **🤖 Curiosidades da IA:** Um botão dedicado que utiliza um serviço de Inteligência Artificial para gerar e exibir fatos interessantes sobre a canção que está tocando.
* **📊 Visualizador de Áudio:** Exibe uma visualização gráfica simples e em tempo real das frequências sonoras.
* **📱 Responsividade Total:** Interface otimizada para computadores e dispositivos móveis, com layouts compactos e menus estilo *drawer* para a fila de reprodução e playlists.
* **▶️ Controles Completos:** Inclui funções essenciais como Play/Pause, Shuffle, Repetição (faixa única/playlist) e atalhos de teclado.
* **⚙️ Backend Estruturado:** Utiliza Node.js, Express e SQLite para gerenciar e servir as músicas e listas de reprodução.



# 🎧 Alive - Music Player Web 🎶

## ✨ Descrição

O **Alive** é uma aplicação web de reprodutor de música moderna e responsiva, desenvolvida com **Node.js** e **Express**. Sua principal característica é a experiência de áudio imersiva e altamente visual, com recursos que dão "vida" à música através de efeitos dinâmicos e sincronizados.

-----

## 💡 Funções em Destaque

  * **🌈 Tema Dinâmico:** O *player* adapta-se visualmente, alterando suas cores de fundo e gradientes com base na paleta de cores da capa do álbum da música atual.
  * **❤️‍🔥 Efeito Pulse (BPM):** Um efeito de "pulsação" no fundo da tela que se sincroniza com os *Beats Per Minute* (BPM) da faixa em reprodução, se a informação estiver disponível, aumentando a imersão.
  * **🤖 Curiosidades da IA:** Um botão dedicado que utiliza um **Serviço de IA Generativa** para gerar e exibir fatos interessantes sobre a canção que está tocando.
  * **📊 Visualizador de Áudio:** Exibe uma visualização gráfica simples e em tempo real das frequências sonoras.
  * **📱 Responsividade Total:** Interface otimizada para computadores e dispositivos móveis, com layouts compactos e menus estilo *drawer* para a fila de reprodução e *playlists*.
  * **▶️ Controles Completos:** Inclui funções essenciais como Play/Pause, Shuffle, Repetição (faixa única/playlist) e **atalhos de teclado**.
  * **⚙️ Backend Estruturado:** Utiliza Node.js, Express e SQLite para gerenciar e servir as músicas e listas de reprodução.

-----

## 🛠️ Tecnologias Utilizadas

| Componente | Tecnologia | Uso Principal |
| :--- | :--- | :--- |
| **⚙️ Backend** | `Node.js` + `Express` | Servidor web e rotas de API. |
| **🗃️ Banco de Dados** | `SQLite3` | Armazenamento de dados de músicas e playlists. |
| **☁️ API Externa** | Serviço de IA Generativa | Geração de curiosidades sobre as músicas. |
| **💻 Frontend** | `HTML5`, `CSS3`, `JavaScript` | Interface do usuário, lógica de interatividade e animações. |
| **🎨 Utilitário JS**| `Color Thief` | Extração de cores das capas para o tema dinâmico. |
| **🔑 Config.** | `dotenv` | Gerenciamento de chaves de API e variáveis de ambiente. |

-----

## 📁 Estrutura do Projeto

```
/
├── public/                     # Arquivos estáticos do Frontend
│   ├── index.html              # Layout principal
│   ├── style.css               # Estilização
│   ├── projetoclp.js           # Lógica do Player (Visualizer, BPM Pulse, API calls)
│   ├── musicas/                # Arquivos de música (.mp3)
│   └── imgs/                   # Capas de álbum e outras imagens
├── server.js                   # Backend (Express, SQLite, AI API)
├── music.db                    # Banco de dados SQLite com dados de músicas
├── package.json                # Dependências e scripts
└── .env (NECESSÁRIO CRIAR)     # Variáveis de ambiente
```

-----

## 🚀 Instalação e Uso

### 1\. Pré-requisitos

  * **Node.js** (LTS recomendado)
  * **Chave de API** para o serviço de Inteligência Artificial

### 2\. Configuração do Projeto

1.  **⬇️ Instale as dependências** do Node.js listadas no `package.json`:
    ```bash
    npm install
    ```
2.  **🤖 Configure a API de IA:**
      * Crie um arquivo chamado **`.env`** na raiz do projeto.
      * Adicione sua chave de API, que deve ser definida como `OPENAI_API_KEY` (conforme o arquivo `server.js`) para a rota `/api/curiosities`:
        ```
        OPENAI_API_KEY="SUA_CHAVE_DE_API_AQUI"
        ```

### 3\. Execução

Inicie o servidor Node.js com o seguinte comando:

```bash
node server.js
```

O servidor será executado na porta **`3000`**.

Abra seu navegador e acesse: [http://localhost:3000](https://www.google.com/search?q=http://localhost:3000).

-----

## ➕ Como Adicionar Músicas

Para incluir novas faixas, insira registros nas tabelas `playlists` e `songs` no `music.db`.

1.  Coloque o arquivo **`.mp3`** 🎵 na pasta `public/musicas/`.
2.  Coloque a imagem de capa 🖼️ na pasta `public/imgs/`.
3.  No banco de dados, insira o novo registro, usando caminhos **relativos** à pasta `public/` para os campos `song_path` e `cover` (Ex: `./musicas/nome.mp3`). Preencher o campo **`bpm`** é opcional, mas ativa o efeito Pulse ❤️‍🔥.
