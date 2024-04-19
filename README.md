[![N|Solid](https://universidadedevassouras.edu.br/wp-content/uploads/2022/03/campus_marica.png)](https://universidadedevassouras.edu.br/campus-marica/)

# Engenharia de Software
### Leandro Loffeu Pereira Costa - mat. 202212089
## Banco de dados não relacionais - 4º Período
### Professor: Fabicio

P1 - Enunciado
1. Criar um projeto utilizando mongodb, express e o padrão de projeto repository pattern, para o login de usuarios(usuarios podem ser cadastrados via requisição post, utilizado um postman ou insomnia). Deverá manter ainda o padrão MVC, utilizado em sala de aula e no trabalho anterior, só deverá dicionar o repository pattern.

2. Criar uma aplicação flask, que realize um CRUD dentro da aplicação(pode utilizar qualquer banco de dados relacional neste ponto).

3. Unir as duas camadas da aplicação, o login + o crud, nodejs + python.

4. Documentar em forma de resumo o processo ao qual vocês utilizaram para chegar no final da aplicação.

5. Colocar no GITHUB.

6. Enviar um vídeo com o projeto funcionando.(Somente a tela). Pode hospedar no youtube.

====== DETALHES =====

Código não deverá de forma alguma ser igual ao do colega de classe.(SUJEITO A ZERAR A AVALIAÇÃO).

Todas as avaliações serão sujeitas a análise do professor em sala de aula, para a devida nota, com perguntas pertinentes sobre o código criado pelo aluno, para que de fato, o aluno tenha pleno entendimento do que ele realizou.

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


# Criando um projeto com MongoDB, Express e Repository Pattern:

## Foi criado uma nova pasta para esta atividade, inciando um novo projeto Node.js
  
  mkdir node-mongo-repository
  cd node-mongo-repository
  npm init -y

## Instalando as dependências necessárias:

npm install express mongoose body-parser cors

## Criado uma pasta chamada "models" e dentro desta pasta, foi criado um arquivo "User.js":

![image](https://github.com/leandroloffeu/provap1node/assets/112645165/4e5040d7-6ff9-4843-9d79-058647d60b8e)



## Criando uma pasta "repositories" e dentro dela, foi criado um arquivo chamado "UserRepository.js":

![image](https://github.com/leandroloffeu/provap1node/assets/112645165/4ed15b85-4bee-48ed-aa51-54c6d2cca802)


## feito uma pasta chamada "controllers" e dentro dela, foi criado um arquivo chamado "UserController.js":

![image](https://github.com/leandroloffeu/provap1node/assets/112645165/d89b84d6-c039-4fb7-8e69-a0b1293346d7)



## feito um arquivo chamado "server.js" na raiz do projeto:

![image](https://github.com/leandroloffeu/provap1node/assets/112645165/b8d86cbe-2667-4800-bb2e-00be7617484d)


# Criando uma aplicação Flask com CRUD:

## Instalando o Flask e o SQLAlchemy:

pip install flask flask-sqlalchemy

## Foi criado um arquivo chamado "app.py":

![image](https://github.com/leandroloffeu/provap1node/assets/112645165/007c0502-6237-4fe1-9a8b-af3ad36134b6)
![image](https://github.com/leandroloffeu/provap1node/assets/112645165/a4f4fbe7-2def-465a-a63d-58b230f1edc9)



## Unindo as duas camadas da aplicação:

Para unir as duas camadas da aplicação, foi criado uma API RESTful para se comunicar com o servidor Node.js para o login e com o servidor Flask para o CRUD.
Foi feito um arquivo chamado "main.py" para esta aplicação:

![image](https://github.com/leandroloffeu/provap1node/assets/112645165/6e9cd38a-647a-4f6b-a43d-b8bbab1783d9)
![image](https://github.com/leandroloffeu/provap1node/assets/112645165/e60751b7-5c78-42a8-ad4a-c536e9dbe97d)


# Estrutura do projeto no Visual Studio Code:

![image](https://github.com/leandroloffeu/provap1node/assets/112645165/fa93a287-7c3f-4106-b7e2-17c29339c6d7)



## Rodando as aplicações:

  ## Inciniando o servidor Node.js:
    node server.js

  ## Inciando o servidor Flask:
    python app.py

  ## Inciando a aplicação principal com o seguinte comando:
    python main.py


  ## Executano a aplicação:

![image](https://github.com/leandroloffeu/provap1node/assets/112645165/aa5a5fe3-be48-4373-bf93-183f02ecea04)


## Erro encontrador:

Quando executa o aplicativo o mesmo não funciona e retorna a segunte mensagem de erro:

![image](https://github.com/leandroloffeu/provap1node/assets/112645165/8c22bc7f-b26d-402a-82bf-5da58e588756)

## Vídeo do erro quando executa:

https://youtu.be/KOZnwureieI?si=apOpJEB8UFkWucsj

#  Ao tentar executar todo enunciado da prova, não consegui atender o 3º enunciado, sendo assim abaixo refiz um novo projeto apenas com as informações do primeiro enunciado.

"Criar um projeto utilizando mongodb, express e o padrão de projeto repository pattern, para o login de usuarios(usuarios podem ser cadastrados via requisição post, utilizado um postman ou insomnia). Deverá manter ainda o padrão MVC, utilizado em sala de aula e no trabalho anterior, só deverá dicionar o repository pattern."






 # Ao tentar executar todo enunciado da prova, não consegui atender o 3º enunciado, sendo assim abaixo refiz um novo projeto apenas com as informações do segundo enunciado.
  "Criar uma aplicação flask, que realize um CRUD dentro da aplicação(pode utilizar qualquer banco de dados relacional neste ponto)."
  
  ## No semestre anterior, realizamos um exercício em Flask e aproveitei o código para estabelecer uma conexão com o banco de dados MySQL. 

  ![image](https://github.com/leandroloffeu/P1--Banco-de-Dados-Nao-Relacionais/assets/112645165/f0edf14c-4c36-467f-90e0-fc8540f114a7)

  1. Criando o Banco de Dados (CREATE DATABASE):
  Nesta linha estabelece um novo banco de dados denominado "empresa". Onde armazenará todas as tabelas relacionadas às informações da empresa.


  ![image](https://github.com/leandroloffeu/P1--Banco-de-Dados-Nao-Relacionais/assets/112645165/1f9ea35e-4e69-441a-b90a-f1a8431a60df)
  2. Selecionando o Banco de Dados (USE empresa):
  Este Comando [e para usar o database empresa banco de dados para operações subsequentes.Todas as CREATE TABLE instruções a seguir criarão tabelas neste banco de dados.

  ![image](https://github.com/leandroloffeu/P1--Banco-de-Dados-Nao-Relacionais/assets/112645165/231f9d35-8da6-4a98-ae09-17d62b9dbe6f)
  3. Criando tabela setor:
  Este comando cria uma tabela “setor” com as seguintes colunas:
  id: Um inteiro (int) que incrementa automaticamente (auto_increment) a cada novo registro, como chave primária (chave primária) da tabela. que garante que cada setor tenha um identificador exclusivo.
  nome: Uma string (varchar) com comprimento máximo de 50 caracteres para armazenar o nome do setor com not null onde indica que esta coluna não pode conter valores vazios.

  ![image](https://github.com/leandroloffeu/P1--Banco-de-Dados-Nao-Relacionais/assets/112645165/3b52f07b-cae9-4be3-99fb-664417806755)
  
  4. Criando tabela funcionario:
  Este comando define uma tabela chamada funcionario para armazenar informações dos funcionários com seguintes colunas:
  id: Um inteiro (int) que esta é uma chave primária inteira com incremento automático.
  primeiro_nome: Uma string (varchar) com comprimento máximo de 50 caracteres para armazenar o nome do funcionário.
  sobrenome: Outra string (varchar) para armazenar o sobrenome do funcionário.
  data_admissao: Um tipo de dados de data para armazenar a data de admissão do funcionário.
  status_funcionario: Um valor booleano para representar a situação profissional do funcionário.
  id_setor: uma chave estrangeira inteira (int) que faz referência à idcoluna da tabla setor. Isso cria um relacionamento entre os funcionários e seus setores atribuídos.

  ![image](https://github.com/leandroloffeu/P1--Banco-de-Dados-Nao-Relacionais/assets/112645165/851864c3-657a-4763-aaeb-e1997acc87cf)
  
  5. Criando a tabela cargo:
  Este comando define uma tabela chamada cargo para armazenar informações sobre os cargos dos funcionários.
  id: Um inteiro (int) que é uma chave primária com incremento automático.
  id_setor: Uma inteira (int), que se trata-se de uma chave estrangeira que faz referência à idcoluna da tabela setor, estabelecendo uma conexão entre as posições e seus setores.
  nome: Uma string (varchar(50)) para armazenar o nome do cargo.

  ![image](https://github.com/leandroloffeu/P1--Banco-de-Dados-Nao-Relacionais/assets/112645165/c73bb879-486d-4e82-a214-4dd75627bc84)  
  
  ## Este código cria um esquema de banco de dados relacional para gerenciar os dados da empresa:
  A tabela setor armazena departamentos ou setores dentro da empresa.
  A tabela funcionario contém detalhes dos funcionários, incluindo o setor atribuído.
  A tabela cargo define os cargos dos funcionários, também vinculados aos seus setores correspondentes.
  
  # Criando um arquivo app.py onde iremos criar as importaçãoes, aplicativo Flask, configuração do banco de dados, definições de modelo, 

  Fazendo as Importações:
  
  ![image](https://github.com/leandroloffeu/P1--Banco-de-Dados-Nao-Relacionais/assets/112645165/b86d769a-a643-4b22-8061-9d6af4bfabab)
  
  flask: esta é a estrutura principal usada para construir aplicativos da web em Python.
  render_template: esta função é usada para renderizar modelos HTML com conteúdo dinâmico.
  request: este objeto fornece acesso a solicitações HTTP recebidas do cliente onde são acessadas no navegador.
  redirect: esta função é usada para redirecionar um usuário para uma URL diferente.
  url_for: Esta função é usada para gerar URLs para rotas Flask.
  flask_sqlalchemy: Esta é uma extensão que integra SQLAlchemy, um popular mapeador objeto-relacional (ORM), com Flask.
  
  Criação de aplicativo Flask:
  
  ![image](https://github.com/leandroloffeu/P1--Banco-de-Dados-Nao-Relacionais/assets/112645165/3fab5eba-2787-4b87-87d1-07bf9746ed9a)
  
  Esparte do código se cria uma instância de aplicativo Flask chamada app. O __name__argumento garante que o aplicativo esteja configurado de manrora certa.

  Configuração do banco de dados:
  
  ![image](https://github.com/leandroloffeu/P1--Banco-de-Dados-Nao-Relacionais/assets/112645165/d12e11f1-868e-4c9d-b991-accc0e11d225)
  
  Esta parte configura a conexão com um banco de dados MySQL chamado empresa. onde precisará substituir roote 12345678pelas credenciais reais do banco de dados, se elas forem diferentes. A string de conexão especifica o    tipo de banco de dados, nome de usuário, senha, host e nome do banco de dados.
  SQLAlchemyé inicializado com a app instância, criando um objeto de conexão com o banco de dados denominado db.

  Definições de modelo - Setor (Departamento):
  
  ![image](https://github.com/leandroloffeu/P1--Banco-de-Dados-Nao-Relacionais/assets/112645165/cf12e011-7311-4184-a4d4-0546bb9089fd)
  


  


    


  

  


  
  

  


  

  







    
        
      



    












