# README – Chat with Database (LangChain + MS SQL Server)

## 1. Introdução
Este projeto demonstra a implementação de um sistema de interação em linguagem natural com uma base de dados Microsoft SQL Server, utilizando LangChain e um modelo de linguagem de grande escala (LLM). O sistema converte perguntas formuladas em linguagem natural em queries SQL, executa-as na base de dados e devolve uma resposta estruturada.

A chave de API foi propositadamente removida para garantir boas práticas de segurança.

## 2. Objetivo
O objetivo central é apresentar uma abordagem programática para:
- Interpretar perguntas de utilizadores,
- Gerar automaticamente queries SQL válidas,
- Interagir com um SGBD real (MS SQL Server),
- Consolidar o resultado numa resposta inteligível.

Este projeto pretende demonstrar os fundamentos da integração entre LLMs e bases de dados relacionais.

## 3. Funcionalidades
- Conversão de linguagem natural em SQL.
- Execução automática da query no MS SQL Server.
- Utilização de ChatPromptTemplate para estruturar a comunicação com o modelo.
- Obtenção do esquema da base de dados como contexto para a geração das queries.
- Pipeline completo para responder a perguntas sobre dados.

## 4. Tecnologias e Bibliotecas Utilizadas
- Python 3.x  
- LangChain  
- Biblioteca do fornecedor do LLM (OpenAI ou compatível)  
- pyodbc ou SQLAlchemy para ligação ao MS SQL Server  
- Jupyter Notebook

## 5. Estrutura do Notebook
O notebook inclui os seguintes componentes principais:

1. Importação das dependências necessárias.  
2. Definição da chave de API como variável de ambiente.  
3. Configuração da ligação ao MS SQL Server.  
4. Construção do prompt utilizado para gerar SQL.  
5. Implementação da cadeia de geração de queries com LangChain.  
6. Função de execução de SQL via pyodbc/SQLAlchemy.  
7. Construção da cadeia completa que:
   - recebe a pergunta,
   - gera SQL,
   - executa a query,
   - sintetiza a resposta final.  
8. Demonstração prática com exemplo de consulta.

## 6. Execução do Projeto

### 6.1 Instalação das dependências
```bash
pip install langchain openai pyodbc
