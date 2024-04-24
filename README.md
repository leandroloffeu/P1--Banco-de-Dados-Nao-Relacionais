[![N|Solid](https://universidadedevassouras.edu.br/wp-content/uploads/2022/03/campus_marica.png)](https://universidadedevassouras.edu.br/campus-marica/)

# Engenharia de Software
### Leandro Loffeu Pereira Costa - mat. 202212089
## Banco de dados não relacionais - 5º Período
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

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## "Criar um projeto utilizando mongodb, express e o padrão de projeto repository pattern, para o login de usuarios(usuarios podem ser cadastrados via requisição post, utilizado um postman ou insomnia). Deverá manter ainda o padrão MVC, utilizado em sala de aula e no trabalho anterior, só deverá dicionar o repository pattern."

 ## Estrutura do projeto no Visual Studio Code:

![image](https://github.com/leandroloffeu/P1--Banco-de-Dados-Nao-Relacionais/assets/112645165/aa1d1423-f407-41a8-b176-d78e353dbb30)



Em: 

![image](https://github.com/leandroloffeu/P1--Banco-de-Dados-Nao-Relacionais/assets/112645165/785eaee5-763c-4cb9-a633-ee3e031d4d54)

Nessa parte do código estabelecem a base básica para um servidor web usando Express.js em Node.js. 
Eles fornecem as ferramentas necessárias para desenvolver e criar um aplicativo Web funcional que possa lidar com solicitações HTTP e entregar respostas.

![image](https://github.com/leandroloffeu/P1--Banco-de-Dados-Nao-Relacionais/assets/112645165/e94f4a1a-a849-43e7-b56b-1f9f660d7e8d)

Essa parte do código implementa um login simples usando o Express e EJS. 
Ele permite que os usuários se autentiquem com um nome de usuário e senha específicos. 
Se as credenciais forem válidas, o usuário é redirecionado para a página inicial; caso contrário, uma mensagem de erro é exibida na página de login.

![image](https://github.com/leandroloffeu/P1--Banco-de-Dados-Nao-Relacionais/assets/112645165/d29c3b5a-d1e6-4408-8820-545ef05600a4)

Em:

![image](https://github.com/leandroloffeu/P1--Banco-de-Dados-Nao-Relacionais/assets/112645165/23c44107-55e7-4871-8b61-6d3168b35ce7)

O Código abaixo HTML/EJS define a página de login com um formulário para inserir nome de usuário e senha. 
Ele usa estilos CSS para formatar a aparência da página e usa EJS para exibir a mensagem de erro, se houver, recebida do servidor Express.

![image](https://github.com/leandroloffeu/P1--Banco-de-Dados-Nao-Relacionais/assets/112645165/b8c89062-1a28-43a1-939e-913f570452eb)
![image](https://github.com/leandroloffeu/P1--Banco-de-Dados-Nao-Relacionais/assets/112645165/fe9c9d4d-5768-4bf5-8537-f8e448f54847)

EM:

![image](https://github.com/leandroloffeu/P1--Banco-de-Dados-Nao-Relacionais/assets/112645165/d8f67f8e-fdde-48ef-b93e-78f17a6d35cd)

A parte do código abaixo do javascript força a página a ser recarregada em um novo endereço URL: http://127.0.0.1:5000. Referente a aplicação Flask.

![image](https://github.com/leandroloffeu/P1--Banco-de-Dados-Nao-Relacionais/assets/112645165/1a5a51e4-2357-489c-9570-a1546bb2c0c2)




## "Criar uma aplicação flask, que realize um CRUD dentro da aplicação(pode utilizar qualquer banco de dados relacional neste ponto)."

  ## Estrutura do projeto no Visual Studio Code:
  
  ![image](https://github.com/leandroloffeu/P1--Banco-de-Dados-Nao-Relacionais/assets/112645165/ab5b2b3b-6f35-43a3-b1d5-8df79c63e88b)

  
 
Criando o Banco de Dados (CREATE DATABASE):
Nesta linha estabelece um novo banco de dados denominado "empresa". Onde armazenará todas as tabelas relacionadas às informações da empresa.
  
![image](https://github.com/leandroloffeu/P1--Banco-de-Dados-Nao-Relacionais/assets/112645165/f0edf14c-4c36-467f-90e0-fc8540f114a7)

  

Selecionando o Banco de Dados (USE empresa):
Este Comando [e para usar o database empresa banco de dados para operações subsequentes.Todas as CREATE TABLE instruções a seguir criarão tabelas neste banco de dados.
  
![image](https://github.com/leandroloffeu/P1--Banco-de-Dados-Nao-Relacionais/assets/112645165/1f9ea35e-4e69-441a-b90a-f1a8431a60df)
  
 

Criando tabela setor:
Este comando cria uma tabela “setor” com as seguintes colunas:
id: Um inteiro (int) que incrementa automaticamente (auto_increment) a cada novo registro, como chave primária (chave primária) da tabela. que garante que cada setor tenha um identificador exclusivo.
nome: Uma string (varchar) com comprimento máximo de 50 caracteres para armazenar o nome do setor com not null onde indica que esta coluna não pode conter valores vazios.
  
![image](https://github.com/leandroloffeu/P1--Banco-de-Dados-Nao-Relacionais/assets/112645165/faf66a23-1654-442c-89ab-3d6a7c5b4cad)

  
  
  
Criando tabela funcionario:
Este comando define uma tabela chamada funcionario para armazenar informações dos funcionários com seguintes colunas:
id: Um inteiro (int) que esta é uma chave primária inteira com incremento automático.
primeiro_nome: Uma string (varchar) com comprimento máximo de 50 caracteres para armazenar o nome do funcionário.
sobrenome: Outra string (varchar) para armazenar o sobrenome do funcionário.
data_admissao: Um tipo de dados de data para armazenar a data de admissão do funcionário.
status_funcionario: Um valor booleano para representar a situação profissional do funcionário.
id_setor: uma chave estrangeira inteira (int) que faz referência à idcoluna da tabla setor. Isso cria um relacionamento entre os funcionários e seus setores atribuídos.
  
![image](https://github.com/leandroloffeu/P1--Banco-de-Dados-Nao-Relacionais/assets/112645165/3b45508e-d447-4609-86e3-a6dedce1ebd4)

 
  
Criando a tabela cargo:
Este comando define uma tabela chamada cargo para armazenar informações sobre os cargos dos funcionários.
id: Um inteiro (int) que é uma chave primária com incremento automático.
id_setor: Uma inteira (int), que se trata de uma chave estrangeira que faz referência à idcoluna da tabela setor, estabelecendo uma conexão entre as posições e seus setores.
nome: Uma string (varchar(50)) para armazenar o nome do cargo.
  
![image](https://github.com/leandroloffeu/P1--Banco-de-Dados-Nao-Relacionais/assets/112645165/50109966-6529-4b63-870a-fbd863f39671)

  
 

  
## Este código cria um esquema de banco de dados relacional para gerenciar os dados da empresa:
  
A tabela setor armazena departamentos ou setores dentro da empresa.
A tabela funcionario contém detalhes dos funcionários, incluindo o setor atribuído.
A tabela cargo define os cargos dos funcionários, também vinculados aos seus setores correspondentes.  

## Criando um arquivo app.py onde iremos criar as importaçãoes, aplicativo Flask, configuração do banco de dados, definições de modelo, rotas para aplicativo Flask. 
  
![image](https://github.com/leandroloffeu/P1--Banco-de-Dados-Nao-Relacionais/assets/112645165/27d0716b-16b9-446e-8807-4450ce02b4ba)

 
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
  
Essa parte do código se cria uma instância de aplicativo Flask chamada app. O __name__argumento garante que o aplicativo esteja configurado de manrora certa.

Configuração do banco de dados:
  
![image](https://github.com/leandroloffeu/P1--Banco-de-Dados-Nao-Relacionais/assets/112645165/d12e11f1-868e-4c9d-b991-accc0e11d225)
  
Esta parte configura a conexão com um banco de dados MySQL chamado empresa. onde precisará substituir roote pelas credenciais reais do banco de dados, se elas forem diferentes. A string de conexão especifica o tipo 
de banco de dados, nome de usuário, senha, host e nome do banco de dados.
SQLAlchemyé inicializado com a app instância, criando um objeto de conexão com o banco de dados denominado db.

Definições de modelo - Setor:
  
![image](https://github.com/leandroloffeu/P1--Banco-de-Dados-Nao-Relacionais/assets/112645165/a849f843-181d-4e62-90ea-4a9d9114d02d)

Esta classe representa um departamento dentro da empresa.
id_setor: esta é a chave primária da tabela.
nome: esta coluna armazena o nome do departamento.
__str__(): Este método define como um Setor objeto é representado como uma string, retornando "Setor {nome do departamento}".


Definições de modelo - Cargo:
   
!![image](https://github.com/leandroloffeu/P1--Banco-de-Dados-Nao-Relacionais/assets/112645165/56d539dd-099d-4ace-ac27-865f2b7783c0)

Esta classe representa um cargo dentro da empresa.
id_cargo: chave primária da tabela.
nome: esta coluna armazena o nome da posição.
__str__(): Este método define como um Cargo objeto é representado como uma string, retornando "Carga {nome da posição}".
  
Definições de modelo - Funcionario:
  
![image](https://github.com/leandroloffeu/P1--Banco-de-Dados-Nao-Relacionais/assets/112645165/887e6dfc-1611-4424-8df4-29b19cb1af3f)

Esta classe representa um funcionario dentro da empresa.
id_funcionario: Identificador único do funcionário.
primeiro_nome: Nome próprio do funcionário.
sobrenome: Sobrenome do funcionário.
data_admissao: Data de admissão do funcionário.
status_funcionario: Status do funcionário.
id_setor: Chave estrangeira para o departamento do funcionário.
id_cargo: Chave estrangeira para o cargo do funcionário.
setor: Objeto Setor associado ao funcionário.
cargo: Objeto Cargo associado ao funcionário.

Relações:
Um funcionário pertence a um único departamento e um único cargo.
Um departamento pode ter vários funcionários.
Um cargo pode ter vários funcionários.
  
  
Este bloco de código é responsável por criar as tabelas do banco de dados com base nos modelos definidos ( Setor, Cargo, e Funcionario).
   
![image](https://github.com/leandroloffeu/P1--Banco-de-Dados-Nao-Relacionais/assets/112645165/97a11f14-fc21-4792-9919-eaa0ebcf2bc9)
  
 
## "Importante o codigo"
O código abaixo, demonstra a criação de modelos de dados e uma rota básica para um aplicativo Web Flask usando Flask- SQLAlchemy para gerenciar dados e interagir com um banco de dados MySQL.
  
![image](https://github.com/leandroloffeu/P1--Banco-de-Dados-Nao-Relacionais/assets/112645165/922b771f-ebf6-42af-8bb1-8819184e9b24)



Esta Rota renderiza o template HTML chamado index.html. Onde define a página inicial da aplicação.
  
![image](https://github.com/leandroloffeu/P1--Banco-de-Dados-Nao-Relacionais/assets/112645165/81651dbf-8bb5-4930-b373-0e4776cda4f1)

 
É a rota aceita requisições GET e POST
Permite que os usuários criem novos setores.
  
![image](https://github.com/leandroloffeu/P1--Banco-de-Dados-Nao-Relacionais/assets/112645165/1c80ea98-5cf2-4d5b-b71c-2c10b58987dc)
  
 
Esta rota permite que os usuários cadastrem novos funcionários.
  
![image](https://github.com/leandroloffeu/P1--Banco-de-Dados-Nao-Relacionais/assets/112645165/e241aa7e-6886-490e-bff5-fad098e5acb3)

 
Essa rota de cadastro_cargo abre o formulário para cadastrar cargos.
Preenchendo o nome do cargo e envia o formulário. O sistema salva o cargo no banco de dados e retorna para a página de cadastro.
  
![image](https://github.com/leandroloffeu/P1--Banco-de-Dados-Nao-Relacionais/assets/112645165/60053149-dcca-4543-b54a-64eff055e909)

  
 Essa rota de visualizar_funcionarios para ver uma lista de todos os funcionários cadastrados.
  
![image](https://github.com/leandroloffeu/P1--Banco-de-Dados-Nao-Relacionais/assets/112645165/df2c01af-6dd9-4d1b-8ffc-174f66800bca)
  
  
  Esssa rota permite excluir_funcionario/<ID do funcionário> para excluir um funcionário específico.
  
  ![image](https://github.com/leandroloffeu/P1--Banco-de-Dados-Nao-Relacionais/assets/112645165/f0e6d392-9b6f-4579-bdf3-05fd9d40c932)

 
  Essa rota permite voltar para retornar à página inicial da aplicação.
  
  ![image](https://github.com/leandroloffeu/P1--Banco-de-Dados-Nao-Relacionais/assets/112645165/9a624bb7-534c-448e-b600-1171ba919804)

 
  Este código serve para executar a aplicação web.
  Verifica se o código está sendo executado como script principal.
  Cria um contexto de aplicativo para a variável app.
  Inicia o servidor de desenvolvimento do Flask
  
  ![image](https://github.com/leandroloffeu/P1--Banco-de-Dados-Nao-Relacionais/assets/112645165/9d4ac576-ae73-40fc-b5be-754f27a385a3)

  
  Templates em HTML para navegação.
  
  ![image](https://github.com/leandroloffeu/P1--Banco-de-Dados-Nao-Relacionais/assets/112645165/ed97c622-39cf-4d09-944b-142eb5b4a9d6)

   Arquivos CSS onde se faz o controle dos elementos em HTML
   
  ![image](https://github.com/leandroloffeu/P1--Banco-de-Dados-Nao-Relacionais/assets/112645165/d5018be1-76a2-4393-b982-b164ca5e5e25)
  

## "Unir as duas camadas da aplicação, o login + o crud, nodejs + python."

Vídeo da aplicação em funcionamento:






   




 



  
  




  




  


  





  



  


    


  

  


  
  

  


  

  







    
        
      



    












