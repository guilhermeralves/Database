![banner_banco_de_dados_git](https://github.com/guilhermeralves/banco_de_dados/assets/54563385/b2bc7324-be7f-4207-bfa2-3ff1b2daf746)

# Principais Tópicos desse Artigo:

- Introdução ao Modelo Relacional.
- Manipulação e Organização de Dados.
- Linguagem de Manipulação Padrão.
-  

## Introdução ao Modelo Relacional

O modelo relacional é um método de organizar os dados usando tabelas compostas por linhas e colunas. Cada tabela representa uma entidade, e as relações entre essas entidades são definidas pelas chaves primárias, comumente chamadas de (Primary Key - PK) e estrangeiras (Foreign key - FK).

Os principais Componentes são:

Tabela: Também conhecida como Entidade, é a estrutura básica do modelo relacional. Cada tabela é composta por linhas (registros) e colunas (atributos ou campos).

Chave Primária (Primary Key): É um atributo ou conjunto de atributos que identifica exclusivamente cada registro em uma tabela. Garante a unicidade dos dados.

Chave Estrangeira (Foreign key): É um atributo em uma tabela que estabelece uma relação com a chave primária de outra tabela. É usada para criar associações entre tabelas.

Exemplo do Modelo Relacional:

![ER_Banco_de_Dados_1](https://github.com/guilhermeralves/banco_de_dados/assets/54563385/857135e0-405e-44a0-bc73-6b16c31b2628)


Na Imagem a cima, temos uma explicação mais visual, Exemplo de um modelo relacional com 3 entidades: "Livro", "Autor" e "Editora". Podemos perceber, como já comentado, que a relação entre as entidades se dá através das Primary Key´s e Foreign Key´s. A entidade "Livro" se relaciona com a entidade "Autor" através da Foreign Key: "ID_Autor", já o relacionamento entre: "Livro" e "Editora" acontece por meio da Foreign Key: "ID_Editora".

## Manipulação e Organização de Dados

Em qualquer modelo de banco de dados, será necessário o auxílio de um SGBD (Sistema de Gerenciamento de Banco de Dados). Ele é o Software responsável por várias tarefas essenciais relacionadas ao armazenamento, organização, manipulação e proteção dos dados.

Alguns Exemplos de SGBDs:

- Microsoft SQL Management Studio
- MySql
- PostgreSQL
- Oracle DataBase

![Exemplos_SGBD´s](https://github.com/guilhermeralves/banco_de_dados/assets/54563385/6615ad6a-b77d-4c3e-ae5f-53175efef236)

Dentre as Responsabilidades de um SGBD, encontra-se:

- Criação e Definição de Esquemas: O SGBD permite criar a estrutura do banco de dados, incluindo a definição de tabelas, índices, restrições e relacionamentos entre os dados.

- Recuperação de Dados: Permite recuperar dados de maneira eficiente através de consultas.

- Manipulação de Dados: Possibilita a inserção, atualização e exclusão de dados no banco de dados, garantindo a integridade e consistência dos dados.

- Controle de Concorrência: Garante que múltiplos usuários possam acessar e manipular os dados simultaneamente de forma segura e consistente, evitando problemas como leituras sujas, escritas sujas e conflitos de atualização.

- Implementação de Restrições de Integridade: O SGBD impõe regras de integridade referencial para garantir que os dados permaneçam consistentes e precisos, como chaves primárias, chaves estrangeiras e restrições de verificação.

- Backup e Recuperação: Fornece recursos para fazer backup regular dos dados e recuperá-los em caso de falhas, garantindo a segurança e disponibilidade dos dados.

- Segurança e Controle de Acesso: O SGBD oferece recursos para controlar o acesso aos dados, incluindo autenticação, autorização e criptografia, garantindo que apenas usuários autorizados possam acessar e manipular os dados.

Essas são apenas algumas das responsabilidades fundamentais, Em resumo, o SGBD atua como uma camada intermediária entre os usuários/aplicativos e os dados armazenados, facilitando o gerenciamento eficiente e seguro dos dados.

## Linguagem de Manipulação Padrão

### SQL (Structure Query Language)

Com a criação dos SGBD´s, e a popularização dos Bancos de Dados Relacionais, foi necessário a construção de uma linguagem padrão para qualquer projeto que envolvesse os Bancos de Dados Relacionais. Foi criado então a SQL (Structure Query Language), que permite a execução de diversas operações sobre os dados armazenados, tais como consulta, inserção, atualização e exclusão.

Principais Componentes do SQL:

 - DDL (Data Definition Language)

Utilizada para definir e modificar a estrutura dos objetos no banco de dados, como tabelas e índices.
    Comandos principais:
        CREATE: Cria novos objetos, como tabelas e índices.
        ALTER: Modifica a estrutura de objetos existentes.
        DROP: Exclui objetos do banco de dados.
        TRUNCATE: Remove todos os registros de uma tabela, mas mantém a estrutura intacta.

 - DML (Data Manipulation Language)

Utilizada para manipular os dados dentro das tabelas.
    Comandos principais:
        SELECT: Consulta dados no banco de dados.
        INSERT: Insere novos registros.
        UPDATE: Atualiza registros existentes.
        DELETE: Exclui registros.

 - DCL (Data Control Language)

Utilizada para controlar o acesso aos dados.
    Comandos principais:
        GRANT: Concede permissões aos usuários.
        REVOKE: Revoga permissões dos usuários.

 - TCL (Transaction Control Language)

Utilizada para gerenciar transações no banco de dados, garantindo que as operações sejam realizadas de forma consistente e segura.
    Comandos principais:
        COMMIT: Confirma as transações realizadas.
        ROLLBACK: Desfaz transações não confirmadas.
        SAVEPOINT: Define pontos de salvamento dentro de uma transação.

