# Chat with Database (LangChain + MS SQL Server)

## 1. Introdução
Este repositório apresenta um sistema de interação em linguagem natural com uma base de dados Microsoft SQL Server, utilizando LangChain e modelos da OpenAI. O sistema converte perguntas formuladas em linguagem natural em instruções SQL válidas, executa essas instruções na base de dados e devolve uma resposta sintetizada.

A chave de API foi propositadamente removida por motivos de segurança.

## 2. Objetivo
O objetivo deste projeto é demonstrar a integração entre modelos de linguagem e sistemas de gestão de bases de dados relacionais. O sistema permite:
- Interpretar perguntas em linguagem natural,
- Gerar automaticamente queries SQL,
- Executar as queries numa instância real de MS SQL Server,
- Produzir uma resposta compreensível para o utilizador.

## 3. Ambiente e Tecnologias
O ambiente foi configurado utilizando o gestor de ambientes Conda.  
As principais tecnologias utilizadas são:
- Python 3.11  
- LangChain  
- OpenAI Python Client  
- pyodbc (ligação ao MS SQL Server)  
- Jupyter Notebook 

## 4. Estrutura do Notebook
O notebook incluído neste repositório contém:
1. Importação das bibliotecas necessárias.  
2. Definição da chave de API da OpenAI via variável de ambiente:
   ```python
   import os
   os.environ['OPENAI_API_KEY'] = ""
   Configuração da ligação ao MS SQL Server via pyodbc.
3.Construção do template utilizado para gerar instruções SQL.

4.Implementação da cadeia de geração de SQL através de LangChain.

5.Função de execução de SQL.

6.Composição do pipeline completo (pergunta → SQL → execução → resposta).

7.Exemplo de utilização.
