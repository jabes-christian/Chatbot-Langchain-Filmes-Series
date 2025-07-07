# 🎬 Chatbot de Filmes e Séries: Seu Guia de Entretenimento RAG

Explore o mundo do cinema e das séries com este chatbot inteligente, construído sobre uma poderosa arquitetura de **Retrieval Augmented Generation (RAG)**. Ele combina a inteligência de Modelos de Linguagem Grandes (LLMs) com uma rica base de dados externa, garantindo que suas perguntas sobre filmes e séries sejam respondidas com precisão e detalhe.

## ✨ Recursos Principais

* **Respostas Precisas com RAG:** Não apenas gera respostas, mas as fundamenta em informações reais, buscando dados relevantes antes de formular a resposta.
* **Base de Dados Abrangente:** Conecta-se diretamente à **API do The Movie Database (TMDB)** para obter informações atualizadas e detalhadas sobre uma vasta gama de filmes e séries.
* **Embeddings de Alta Performance:** Utiliza o modelo **BAAI/bge-m3** do Hugging Face, conhecido por sua capacidade de gerar representações vetoriais de texto que capturam nuances semânticas complexas, otimizando a busca por similaridade.
* **Busca Vetorial Ultrarrápida:** Emprega **FAISS (Facebook AI Similarity Search)** para armazenar e consultar os embeddings de forma incrivelmente eficiente, permitindo recuperar informações relevantes em milissegundos.
* **LLM Integrado:** Funciona com LLMs via **OpenRouter**, oferecendo flexibilidade para experimentar diferentes modelos de linguagem de última geração (atualmente configurado com DeepSeek Chat).
* **Interface Intuitiva:** Desenvolvido com **Gradio**, proporciona uma experiência de chat amigável e fácil de usar, ideal para prototipagem e demonstrações no Google Colab.

## 🚀 Começando

Siga estes passos simples para ter o chatbot rodando no seu ambiente Google Colab:

### 1. Obtenha suas Chaves de API

Para que o chatbot funcione, você precisará de chaves de API para acessar os serviços externos:

* **OpenRouter API Key:** Crie sua conta e obtenha a chave em [OpenRouter.ai](https://openrouter.ai/).
* **TMDB API Key:** Registre-se e gere sua chave em [The Movie Database (TMDB) API](https://www.themoviedb.org/documentation/api/getting-started).

### 2. Configure os Segredos no Google Colab

1.  Abra seu notebook Colab.
2.  No painel esquerdo, clique no ícone **"🔑 Secrets"**.
3.  Adicione duas novas variáveis de ambiente, garantindo que "Notebook access" esteja marcado para ambas:
    * `OPENROUTER_API_KEY`: Cole sua chave da OpenRouter aqui.
    * `TMDB_API_KEY`: Cole sua chave da TMDB aqui.

### 3. Execute o Notebook

1.  Cole o código do seu chatbot nas células do seu notebook Colab.
2.  Comece executando a célula de instalação de bibliotecas:
    ```bash
    !pip install -q langchain openai langchain-community sentence-transformers gradio requests faiss-cpu
    ```
3.  Execute as demais células em ordem.
4.  Após a conclusão da execução, o Gradio irá gerar um link público. Clique nele para interagir com o chatbot.

## 💻 Tecnologias

Este projeto é um exemplo prático de como integrar várias tecnologias de IA e desenvolvimento web:

* **Python:** A base de todo o projeto.
* **LangChain:** Framework que orquestra a comunicação entre o LLM, o banco de dados vetorial e as fontes de dados. Ele gerencia o fluxo RAG e a estruturação dos prompts.
* **Hugging Face Embeddings (BAAI/bge-m3):** Provê o modelo de embeddings que transforma texto em vetores numéricos de alta dimensão, essenciais para a busca semântica.
* **FAISS:** Biblioteca otimizada para busca de vizinhos mais próximos em espaços vetoriais, crucial para a recuperação eficiente de documentos relevantes.
* **TMDB API:** A fonte de informações sobre filmes e séries. O chatbot consulta esta API para construir sua base de conhecimento.
* **OpenRouter:** Uma camada de abstração para acessar diversos LLMs de forma unificada.
* **Gradio:** Usado para construir a interface de usuário web do chatbot, tornando-o acessível e interativo.

## 👨‍💻 Autor

* **Jabes Christian**

## 🌟 Contribua

Este projeto está em constante evolução. Sinta-se à vontade para abrir issues, enviar pull requests ou sugerir novas funcionalidades!
