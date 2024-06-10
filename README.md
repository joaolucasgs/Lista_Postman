# Teste de API com PostMan

## Descrição

Este repositório contém cenários de teste desenvolvidos para a API pública de usuários do ReqRes (https://reqres.in/).

## Cenários de Teste

1. **Listar Usuários**
   - Método: GET
   - Endpoint: `/api/users?page=2`
 

2. **Obter Detalhes de um Usuário**
   - Método: GET
   - Endpoint: `/api/users/2`
  

3. **Criar um Novo Usuário**
   - Método: POST
   - Endpoint: `/api/users`
   - Body:
     ```json
     {
       "name": "John",
       "job": "developer"
     }
     ```


4. **Atualizar um Usuário**
   - Método: PUT
   - Endpoint: `/api/users/2`
   - Body:
     ```json
     {
       "name": "Jane",
       "job": "manager"
     }
     ```

5. **Obter Detalhes de um Usuário com ID Inválido (Negativo)**
   - Método: GET
   - Endpoint: `/api/users/abc`
  
6. **Deletar um Usuário com ID Inválido (Negativo)**
   - Método: DELETE
   - Endpoint: `/api/users/abc`
 

## Como Executar os Testes

1. Importe a coleção de testes no PostMan.
2. Execute os testes individualmente ou em conjunto.
3. Verifique os resultados e as validações conforme descrito em cada cenário.

### Pré-requisitos

Certifique-se de ter o Node.js instalado na sua máquina. Você pode baixá-lo [aqui](https://nodejs.org/).

### Passos para o relatório

1. **Instalar o Newman e newman reporter htmlextra**
   Execute o seguinte comando no terminal para instalar o Newman globalmente:
   ```sh
   npm install -g newman
   npm i -g newman-reporter-htmlextra

2. **Gerar e vizualizar relatorio**
   Execute o seguinte comando no terminal para gerar o relatório:
   ```sh
  newman run 'Lista Postman.postman_collection.json' -r htmlextra
  Após gerar, vizualizar relatório na pasta criada com o nome de 'newman'    
