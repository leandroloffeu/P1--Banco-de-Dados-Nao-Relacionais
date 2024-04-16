[![N|Solid](https://universidadedevassouras.edu.br/wp-content/uploads/2022/03/campus_marica.png)](https://universidadedevassouras.edu.br/campus-marica/)

# Engenharia de Software
### Leandro Loffeu Pereira Costa - mat. 202212089
## Estrutura de Dados - 4º Período
### Professor: Fabicio

P1 - Enunciado
1. Criar um projeto utilizando mongodb, express e o padrão de projeto repository pattern, para o login de usuarios(usuarios podem ser cadastrados via requisição post, utilizado um postman ou insomnia). Deverá manter ainda o padrão MVC, utilizado em sala de aula e no trabalho anterior, só deverá dicionar o repository pattern.

2. Criar uma aplicação flask, que realize um CRUD dentro da aplicação(pode utilizar qualquer banco de dados relacional neste ponto).

3. Unir as duas camadas da aplicação, o login + o crud, nodejs + python.

4 . Documentar em forma de resumo o processo ao qual vocês utilizaram para chegar no final da aplicação.

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


## Criando uma aplicação Flask com CRUD:

## Instalando o Flask e o SQLAlchemy:

pip install flask flask-sqlalchemy

## Foi criado um arquivo chamado "app.py":

from flask import Flask, request, jsonify
from flask_sqlalchemy import SQLAlchemy

app = Flask(__name__)
app.config['SQLALCHEMY_DATABASE_URI'] = 'sqlite:///crud.db'
db = SQLAlchemy(app)

class User(db.Model):
    id = db.Column(db.Integer, primary_key=True)
    name = db.Column(db.String(50), nullable=False)
    email = db.Column(db.String(50), unique=True, nullable=False)

    def __repr__(self):
        return f'<User {self.name}>'

db.create_all()

@app.route('/users', methods=['GET', 'POST'])
def users():
    if request.method == 'GET':
        users = User.query.all()
        return jsonify([user.__dict__ for user in users])

    data = request.get_json()
    new_user = User(name=data['name'], email=data['email'])
    db.session.add(new_user)
    db.session.commit()
    return jsonify(new_user.__dict__), 201

@app.route('/users/<int:user_id>', methods=['GET', 'PUT', 'DELETE'])
def user(user_id):
    user = User.query.get_or_404(user_id)

    if request.method == 'GET':
        return jsonify(user.__dict__)

    if request.method == 'PUT':
        data = request.get_json()
        user.name = data['name']
        user.email = data['email']
        db.session.commit()
        return jsonify(user.__dict__)

    if request.method == 'DELETE':
        db.session.delete(user)
        db.session.commit()
        return '', 204

if __name__ == '__main__':
    app.run(debug=True)

## Unindo as duas camadas da aplicação:

Para unir as duas camadas da aplicação, foi criado uma API RESTful para se comunicar com o servidor Node.js para o login e com o servidor Flask para o CRUD.
Foi feito um arquivo chamado "main.py" para esta aplicação:

import requests

class App:
    def __init__(self):
        self.node_url = 'http://localhost:3000'
        self.flask_url = 'http://localhost:5000'

    def login(self, username, password):
        url = f'{self.node_url}/users/login'
        data = {'username': username, 'password': password}
        response = requests.post(url, json=data)
        return response.json()

    def create_user(self, name, email, password):
        url = f'{self.node_url}/users'
        data = {'name': name, 'email': email, 'password': password}
        response = requests.post(url, json=data)
        return response.json()

    def get_users(self):
        url = f'{self.flask_url}/users'
        response = requests.get(url)
        return response.json()

    def get_user(self, user_id):
        url = f'{self.flask_url}/users/{user_id}'
        response = requests.get(url)
        return response.json()

    def create_user(self, name, email, password):
        url = f'{self.flask_url}/users'
        data = {'name': name, 'email': email, 'password': password}
        response = requests.post(url, json=data)
        return response.json()

    def update_user(self, user_id, name, email, password):
        url = f'{self.flask_url}/users/{user_id}'
        data = {'name': name, 'email': email, 'password': password}
        response = requests.put(url, json=data)
        return response.json()

    def delete_user(self, user_id):
        url = f'{self.flask_url}/users/{user_id}'
        response = requests.delete(url)
        return response.status_code
        
if __name__ == '__main__':
    app = App()
    user_id = app.create_user('John Doe', 'john.doe@example.com', 'secret')
    print(f'Created user with ID {user_id}')
    user = app.get_user(user_id)
    print(f'Retrieved user: {user}')
    updated_user = app.update_user(user_id, 'fabricio', 'fabricio@example.com', 'new_secret')
    print(f'Updated user: {updated_user}')
    response = app.delete_user(user_id)
    print(f'Deleted user with status code {response}')

## Rodando as aplicações:

  ## Inciniando o servidor Node.js:
    node server.js

  ## Inciando o servidor Flask:
    python app.py

  ## Inciando a aplicação principal com o seguinte comando:
    python main.py


    
        
      



    












