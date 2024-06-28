### Pipeline de ETL: Extração, Transformação e Carregamento

#### Objetivo:
Criar uma pipeline de ETL eficiente para extrair dados de um banco de dados inicial, transformá-los conforme necessário e carregá-los em um banco de dados final, resultando em um arquivo consolidado com os dados.

### Passos para Implementação

#### Configuração Inicial:

1. **Instalação do Docker:**
   Certifique-se de que o Docker está instalado em sua máquina.

2. **Navegação para a Pasta do Projeto:**
   Abra o terminal e navegue até o diretório do projeto.

3. **Construção das Imagens Docker:**
   Execute o comando:
   ```bash
   docker-compose build
   ```
   para construir as imagens necessárias.

4. **Inicialização dos Serviços:**
   Execute o comando:
   ```bash
   docker-compose up
   ```
   para iniciar os serviços definidos no arquivo `docker-compose.yml`.

#### Execução dos Scripts:

Os scripts Python foram desenvolvidos para serem executados manualmente.

1. **Instalação de Bibliotecas Python:**
   Certifique-se de instalar as bibliotecas necessárias:
   ```bash
   pip install psycopg2 pandas
   ```

2. **Execução do Script de Exportação:**
   Utilize o terminal ou uma IDE de sua preferência para executar o script `export.py`, que extrairá os dados das tabelas do banco de dados inicial e os salvará em arquivos CSV no diretório:
   ```plaintext
   /data/postgres/nome_da_tabela/data_atual/nome_da_tabela.csv
   ```

3. **Execução do Script de Importação:**
   Execute o script `import.py` para importar os dados dos arquivos CSV para o banco de dados final. Este processo resultará na criação de um arquivo CSV consolidado contendo todas as tabelas e linhas importadas, localizado em:
   ```plaintext
   /result_csv/result.csv
   ```

### Resultado Final:

Após a execução bem-sucedida dos scripts, você terá um arquivo CSV final que consolida todos os dados das tabelas, disponível para análise. Este projeto demonstra a capacidade de transferir dados entre bancos de dados, mantendo a organização e a integridade dos dados.

