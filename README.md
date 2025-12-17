# LLM App com Pinecone e LangChain

Este projeto implementa um sistema de **Retrieval-Augmented Generation (RAG)** capaz de responder perguntas baseadas em documentos PDF. A aplicação utiliza a **OpenAI** para geração de embeddings e respostas, e o **Pinecone** como banco de dados vetorial para armazenamento e busca semântica.

## 📋 Funcionalidades

- **Carregamento de Documentos**: Leitura automática de arquivos PDF de um diretório.
- **Processamento de Texto**: Divisão do texto em chunks para otimizar a vetorização.
- **Embeddings**: Conversão de texto em vetores utilizando modelos da OpenAI.
- **Banco de Dados Vetorial**: Indexação e busca de similaridade utilizando Pinecone.
- **Question Answering (QA)**: Geração de respostas contextualizadas utilizando LangChain e GPT.

## 🛠️ Tecnologias Utilizadas

- [Python](https://www.python.org/)
- [LangChain](https://www.langchain.com/)
- [Pinecone](https://www.pinecone.io/)
- [OpenAI API](https://openai.com/)
- [Jupyter Notebook](https://jupyter.org/)

## 🚀 Como Executar

### 1. Pré-requisitos

Certifique-se de ter o Python instalado (versão 3.10 ou superior recomendada).

### 2. Instalação das Dependências

Instale as bibliotecas listadas no arquivo [`requirements.txt`](requirements.txt):

```bash
pip install -r requirements.txt
```

### 3. Configuração das Variáveis de Ambiente

Renomeie o arquivo [`.env.example`](.env.example) para `.env` e preencha com suas chaves de API:

```ini
OPENAI_API_KEY="sua-chave-openai"
PINECONE_API_KEY="sua-chave-pinecone"
PINECONE_ENVIRONMENT="seu-ambiente-pinecone" (ex: gcp-starter)
PINECONE_INDEX_NAME="nome-do-seu-indice"
```

> **Nota:** Você precisará criar um índice no Pinecone com a dimensão **1536** (padrão para `text-embedding-ada-002`).

### 4. Adicionando Documentos

Coloque os arquivos PDF que deseja analisar dentro da pasta `documents/`. O script irá ler todos os PDFs contidos nela.

### 5. Executando o Projeto

Abra e execute as células do notebook [`test.ipynb`](test.ipynb). O fluxo de execução é:

1.  Carrega as variáveis de ambiente.
2.  Lê e processa os PDFs.
3.  Gera embeddings e envia para o Pinecone.
4.  Realiza perguntas ao modelo (ex: "How is the agriculture doing?").

## 📂 Estrutura do Projeto

- [`test.ipynb`](test.ipynb): Notebook principal com a lógica da// filepath: c:\Users\OlavoDefendiDalberto\Projetos\LLM-App-PineconeDB\README.md
# LLM App com Pinecone e LangChain

Este projeto implementa um sistema de **Retrieval-Augmented Generation (RAG)** capaz de responder perguntas baseadas em documentos PDF. A aplicação utiliza a **OpenAI** para geração de embeddings e respostas, e o **Pinecone** como banco de dados vetorial para armazenamento e busca semântica.

## 📋 Funcionalidades

- **Carregamento de Documentos**: Leitura automática de arquivos PDF de um diretório.
- **Processamento de Texto**: Divisão do texto em chunks para otimizar a vetorização.
- **Embeddings**: Conversão de texto em vetores utilizando modelos da OpenAI.
- **Banco de Dados Vetorial**: Indexação e busca de similaridade utilizando Pinecone.
- **Question Answering (QA)**: Geração de respostas contextualizadas utilizando LangChain e GPT.

## 🛠️ Tecnologias Utilizadas

- [Python](https://www.python.org/)
- [LangChain](https://www.langchain.com/)
- [Pinecone](https://www.pinecone.io/)
- [OpenAI API](https://openai.com/)
- [Jupyter Notebook](https://jupyter.org/)

## 🚀 Como Executar

### 1. Pré-requisitos

Certifique-se de ter o Python instalado (versão 3.10 ou superior recomendada).

### 2. Instalação das Dependências

Instale as bibliotecas listadas no arquivo [`requirements.txt`](requirements.txt):

```bash
pip install -r requirements.txt
```

### 3. Configuração das Variáveis de Ambiente

Renomeie o arquivo [`.env.example`](.env.example) para `.env` e preencha com suas chaves de API:

```ini
OPENAI_API_KEY="sua-chave-openai"
PINECONE_API_KEY="sua-chave-pinecone"
PINECONE_ENVIRONMENT="seu-ambiente-pinecone" (ex: gcp-starter)
PINECONE_INDEX_NAME="nome-do-seu-indice"
```

> **Nota:** Você precisará criar um índice no Pinecone com a dimensão **1536** (padrão para `text-embedding-ada-002`).

### 4. Adicionando Documentos

Coloque os arquivos PDF que deseja analisar dentro da pasta `documents/`. O script irá ler todos os PDFs contidos nela.

### 5. Executando o Projeto

Abra e execute as células do notebook [`test.ipynb`](test.ipynb). O fluxo de execução é:

1.  Carrega as variáveis de ambiente.
2.  Lê e processa os PDFs.
3.  Gera embeddings e envia para o Pinecone.
4.  Realiza perguntas ao modelo (ex: "How is the agriculture doing?").

## 📂 Estrutura do Projeto

- [`test.ipynb`](test.ipynb): Notebook principal com a lógica da aplicação.
- [`documents`](documents/): Diretório para armazenar os arquivos PDF de entrada.
- [`requirements.txt`](requirements.txt): Lista de dependências do Python.
- [`.env.example`](.env.example): Modelo para configuração de variáveis de ambiente.