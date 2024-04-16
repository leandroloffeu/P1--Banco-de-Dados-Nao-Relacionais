[![N|Solid](https://universidadedevassouras.edu.br/wp-content/uploads/2022/03/campus_marica.png)](https://universidadedevassouras.edu.br/campus-marica/)

# Engenharia de Software
### Leandro Loffeu Pereira Costa - mat. 202212089
## Estrutura de Dados - 4º Período
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

## Víde do erro quando executa:

https://youtu.be/KOZnwureieI?si=apOpJEB8UFkWucsj


 





    
        
      



    












