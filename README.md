### Contexto
Este é um projeto de pipeline de dados construído com Apache Airflow para processar dados de entrada e gerar insights úteis. O pipeline foi desenvolvido para rodar em um ambiente Python 3.x.

### Pré-requisitos
Certifique-se de ter o Python 3.x instalado em seu sistema. Você pode baixar e instalar Python no site oficial.

### Tecnologias Utilizadas
- Python (Versão: 3.9.9)
- Apache Airflow (Versão: 2.7.2)
- Embulk (Versão: 0.10.27)
- Docker (Versão: 20.10.11)
- Docker Compose (Versão: 1.29.2)

### ⚙️ Executando o Pipeline Localmente
Para executar o pipeline de dados localmente usando Docker e Apache Airflow, siga estes passos:

1. **Clone o repositório:**
   ```bash
   git clone https://github.com/vlruiz108/LH_ED_VANESSA_RUIZ
   ```

2. **Navegue até o diretório do projeto:**
   ```bash
   cd data-pipeline
   python data_pipeline.py
   ```

3. **Crie e ative um ambiente virtual (opcional, mas recomendado):**
   ```bash
   python -m venv venv
   source venv/bin/activate  # no Windows use venv\Scripts\activate.bat
   ```

4. **Instale as dependências do projeto:**
   ```bash
   pip install -r requirements.txt
   ```

5. **Configure as credenciais e parâmetros necessários no arquivo `config.py`. Você pode criar uma cópia do arquivo de exemplo `config_example.py` e renomeá-la para `config.py`.**

6. **Certifique-se de que o Apache Airflow está configurado corretamente. Consulte a documentação oficial do Apache Airflow para instruções detalhadas sobre a configuração.**

7. **Construa e inicie os contêineres Docker:**
   ```bash
   docker-compose up --build
   ```

8. **Para levantar os contêineres:**
   ```bash
   docker-compose up -d
   ```

9. **Verifique os contêineres:**
   ```bash
   docker-compose ps
   ```

10. **Inicie o Apache Airflow:**
    ```bash
    airflow webserver --port 8080
    ```
    Em outro terminal:
    ```bash
    airflow scheduler
    ```

11. **Acesse o painel do Airflow em `http://localhost:8080` no seu navegador.**

12. **Ative o DAG (Directed Acyclic Graph) `data_pipeline` no painel do Airflow.**

O pipeline está agora configurado para rodar conforme o agendamento definido no DAG.
