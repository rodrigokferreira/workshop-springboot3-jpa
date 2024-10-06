# SpringBot3

SpringBot3 é um projeto desenvolvido usando Spring Boot 3, JPA e Hibernate, com um banco de dados em memória H2. O objetivo é fornecer uma API RESTful para gerenciar entidades como categorias de produtos, pedidos, itens de pedidos, usuários, entre outros.

## Estrutura do Projeto

A organização das pastas e classes do projeto é a seguinte:

### 1. Config
- **Config.java**: Responsável por inicializar e inserir dados no banco de dados utilizando os repositórios.

### 2. Entities
#### Subpastas:
- **Enums**: Contém a enumeração **OrderStatus** para o status de pedidos.
- **pk**: Contém a classe de chave composta **OrderItemPk**.

#### Classes:
- **Category**: Representa uma categoria de produto.
- **Order**: Representa um pedido.
- **OrderItem**: Representa um item de pedido.
- **Payment**: Representa um pagamento associado a um pedido.
- **Product**: Representa um produto.
- **User**: Representa um usuário.

### 3. Repositories
Contém interfaces que estendem `JpaRepository` para acesso ao banco de dados.
- **CategoryRepository**: Repositório de categorias.
- **OrderRepository**: Repositório de pedidos.
- **OrderItemRepository**: Repositório de itens de pedidos.
- **PaymentRepository**: Repositório de pagamentos.
- **ProductRepository**: Repositório de produtos.
- **UserRepository**: Repositório de usuários.

### 4. Resources
Contém as classes responsáveis por expor as APIs RESTful.
- **CategoryResource**: Endpoints para categorias.
- **OrderResource**: Endpoints para pedidos.
- **ProductResource**: Endpoints para produtos.
- **UserResource**: Endpoints para usuários.

#### Exceptions:
- **exceptions/ResourceExceptionHandler.java**: Manipulador global de exceções.
- **exceptions/StandardError.java**: Classe para formatação de respostas de erro.

### 5. Services
Contém as classes responsáveis pela lógica de negócio.
- **CategoryServices**: Lógica de negócio para categorias.
- **OrderServices**: Lógica de negócio para pedidos.
- **ProductServices**: Lógica de negócio para produtos.
- **UserServices**: Lógica de negócio para usuários.

#### Exceptions:
- **exceptions/DatabaseException.java**: Exceção personalizada para erros no banco de dados.
- **exceptions/ResourceNotFoundException.java**: Exceção personalizada para recursos não encontrados.

## Tecnologias Utilizadas
- **Spring Boot 3**: Framework principal para criação da API RESTful.
- **JPA & Hibernate**: Para mapeamento objeto-relacional (ORM) e persistência de dados.
- **H2 Database**: Banco de dados em memória para testes e desenvolvimento.
  
## Como Executar o Projeto
1. Clone o repositório.
2. Importe o projeto em sua IDE (recomenda-se IntelliJ ou Eclipse).
3. Execute o arquivo principal da aplicação: `SpringBot3Application.java`.
4. O banco H2 será inicializado automaticamente em memória, e você pode acessar a API nos endpoints definidos.

## Próximos Passos
- Adicionar autenticação e autorização.
- Implementar novas funcionalidades para as entidades.
- Configurar o projeto para uso em um banco de dados relacional (MySQL, PostgreSQL, etc).

## Contribuição
Sinta-se à vontade para abrir Issues ou enviar Pull Requests para melhorias.

---

**Desenvolvido por:** Rodrigo Kikuchi Ferreira
