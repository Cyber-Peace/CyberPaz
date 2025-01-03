# Introdução
Este é um guia para  projeto BookGuardian. Ele inclui instruções sobre como configurar um ambiente virtual, instalar pacotes necessários e executar o projeto.


## Recomendado:
`PYTHON >= 3.10`
`Django == 5`

## Como Executar
Para executar o projeto, siga as etapas abaixo:

### 1. Criação de Ambiente Virtual
Para isolar as dependências do projeto, é recomendável criar um ambiente virtual. Utilize o seguinte comando:

```bash
# No diretório do seu projeto
python -m venv venv
```

### 2. Ativação do Ambiente Virtual
#### Windows
```bash
venv\Scripts\activate
```

#### Linux
```bash
source venv/bin/activate
```

### 3. Instalação de Pacotes
Com o ambiente virtual ativado, instale os pacotes necessários usando o `pip`:

```bash
pip install -r requirements.txt
```

Certifique-se de ter um arquivo `requirements.txt` com as dependências do seu projeto.



### 4. Remova o "-example do arquivo .env"

Para configurar corretamente o arquivo `.env`, remova o sufixo `-example` do nome do arquivo.

Exemplo:

![Remova o "-example do arquivo .env"](utils/img/env-example.png)

Deixa assim:

![.env](utils/img/env.png)


### 5.  Configuração do Banco de Dados

Este projeto carrega dados do banco de dados utilizando o gerenciador Python `makemigrations` e `migrate`.

Antes de começar, certifique-se de ter configurado corretamente o banco de dados. Para isso, execute os seguintes comandos:

```bash
python manage.py makemigrations
python manage.py migrate
```

### 6. Cria User Admin

Rode esse comando pra cria um usuario admin e poder acessar a zona admistrativa para gerenciamento de dados.

```bash
python manage.py createsuperuser
```

Depois acesse a rota do admin e faça o login com email e senha que você cadastrou

### 7. Execução do Projeto

Após instalar as dependências, você pode rodar o projeto:


```bash
python manage.py runserver
```


O servidor de desenvolvimento será iniciado e você poderá acessar o projeto em `http://localhost:8000/`.
