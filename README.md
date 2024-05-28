![banner_banco_de_dados_git](https://github.com/guilhermeralves/banco_de_dados/assets/54563385/b2bc7324-be7f-4207-bfa2-3ff1b2daf746)

# Principais Tópicos desse Artigo:

- Introdução ao Modelo Relacional
- Manipulação e Organização de Dados
- Linguagem de Manipulação Padrão
- Modelagem do Banco de Dados
- Principais Conceitos
- Formas de Normalização e Padronização

Obs: Para facilitar a navegação, caso queira ler sobre algum tópico específico, basta copiar o nome do tópico de interesse, apertar o comando "Ctrl + F" e Colar na pesquisa para ir direto ao Tópico!


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

SQL (Structure Query Language) 

Com a criação dos SGBD´s, e a popularização dos Bancos de Dados Relacionais, foi necessário a construção de uma linguagem padrão para qualquer projeto que envolvesse os Bancos de Dados Relacionais. Foi criado então a SQL (Structure Query Language), que permite a execução de diversas operações sobre os dados armazenados, tais como consulta, inserção, atualização e exclusão.

![subconjuntos-sql](https://github.com/guilhermeralves/banco_de_dados/assets/54563385/7cf47898-023e-4457-bb6e-0b4cadef8a73)

Principais Componentes do SQL:

### DDL (Data Definition Language)

Utilizada para definir e modificar a estrutura dos objetos no banco de dados, como tabelas e índices.

Comandos principais:

- CREATE: Cria novos objetos, como tabelas e índices.
- ALTER: Modifica a estrutura de objetos existentes.
- DROP: Exclui objetos do banco de dados.
- TRUNCATE: Remove todos os registros de uma tabela, mas mantém a estrutura intacta.

### DML (Data Manipulation Language)

Utilizada para manipular os dados dentro das tabelas.

Comandos principais:

- SELECT: Consulta dados no banco de dados.
- INSERT: Insere novos registros.
- UPDATE: Atualiza registros existentes.
- DELETE: Exclui registros.

### DCL (Data Control Language)

Utilizada para controlar o acesso aos dados.

Comandos principais:

- GRANT: Concede permissões aos usuários.
- REVOKE: Revoga permissões dos usuários.

### TCL (Transaction Control Language)

Utilizada para gerenciar transações no banco de dados, garantindo que as operações sejam realizadas de forma consistente e segura.

Comandos principais:

- COMMIT: Confirma as transações realizadas.
- ROLLBACK: Desfaz transações não confirmadas.
- SAVEPOINT: Define pontos de salvamento dentro de uma transação.

### DBA (DataBase Administrator)

É o profissional responsável pela administração e gerenciamento do banco de dados, suas príncipais responsabilidades são:

- Criação, Instalação, Configuração e Manutenção:

Ajudar na criação da arquitetura do banco de dados direcionado ao projeto específico, fazer instalações físicas e tambem configurações no SGBD envolvido e Gerenciar a manutenção do banco de dados sendo responsável pela boa performance na requisição de dados ou seja no tempo de resposta do servidor à aplicação.

- Backup e Recuperação de Dados:

Planejar e Implementar estratégias de backup e recuperação de dados mantendo a proteção e integridade dos dados guardados, disponíveis sempre que solicitados.

- Seurança:

Configurar e arquitetar permissões de acessos, controlando assim quem pode acessar os dados e executar comandos no banco de dados.

- Suporte Técnico e Solução de Problemas:

Ofereçer Suporte Técnico a equipe e usuários do banco de dados, trazendo desempenho e resolução de problemas relacionados ao banco de dados.

## Modelagem do Banco de Dados

![header_banco_de_dados_sql](https://github.com/guilhermeralves/banco_de_dados/assets/54563385/0bc52081-505f-41d8-813e-eb889b9c4cf6)

A organização e modelagem de um Banco de Dados é feita à partir de 3 níveis de abstração dos dados coletados através do cliente final. Esses 3 níveis são:

- Externo (Visão do Usuário)

No nível de abstração Externo é feito o levantamento das informações fornecidas pelo cliente, indentificado quais serão os tipos de dados guardados os tipos de usuários que farão requisições ao banco e quais permissões serão utilizadas para cada tipo de usuário.

- Conceitual (Visão Lógica)

No Nível Conceitual é feito o processo de "Normalização" de todas as informações fornecidas pelo cliente e a identificação dos tipos dos dados por termos técnicos como: dados tipo texto, numero, Quantidade e identificação das entidades, atributos, linhas, relacionamentos e restrições. Trazendo uma visão abrangente e coesa criando assim a arquitetura que irá suprir as demandas do sistema.

- Interno (Visão Física)

O nível de abstração Interno é responsável por identificar como será o armazenamento físico dos dados, tipos de disco de Armazenamento, HDD´s ou SSD´s, Quais serão os Índices Útilizados, como será a estrutura física, qual será as configurações mínimas e recomendadas para suprir o SGBD e o Banco de Dados em funcionamento, quais serão os particionamentos nos discos, todas essas etapas serão direcionadas ao desempenho e a minimização do tempo de resposta à requisição da aplicação.

## Principais Conceitos

Os principais conceitos que serão estudados são: 

- Tabelas (Relações ou Entidades)

Conjuntos de informações, elementos do mundo real distinguíveis.

- Linhas (Elementos ou Registros)
        
Cada linha refere-se a um determinado elemento real.

- Colunas (Atributos ou Propriedades)

São todos os dados referentes a um determindado elemento.

Tipos de Atributos:

- Simples: dado único, sem divisão.
Exemplo: CPF "005.326.548.38", impossível dividir.

- Composto: Dado composto, com sub-divisão.
Exemplo: Endereço "Rua, Número, Cidade" duas ou mais informações.

- MonoValorado: atributo de valor único para aquele elemento.
Exemplo: "Nome, CPF"

- MultiValorado: Atributo com possíveis valores.
Exemplo: "Telefone, Endereço pode ser residencial ou comercial"

- Nulo: Atributo com ausencia de valor.

- Devirado: Atributos que podem derivar outros atributos.
Exemplo: "Data de Nascimento -> Idade"

- Domínios
São todos os tipos de dados possíveis de cada Coluna.

## Formas de Normalização e Padronização

As formas normais são princípios e técnicas de design utilizadas para estruturar bancos de dados relacionais de maneira eficiente e minimizar a redundância e dependências indesejadas. A normalização é o processo de organizar os dados.

### Primeira Forma Normal (1FN)

As regras para que uma tabela não venha à ferir a 1FN são:

- As tabelas contém somente atributos simples.

- Não contém atributos totalizadores ou Derivados, aqueles que pode ser derivados de outros atributos.

- Não contém atributos repetidos.

- Todas as linhas são diferentes em relação a chave primária.


A seguir temos um exemplo de uma tabela que não fere as regras da 1FN:

![banco_de_dados_git](https://github.com/guilhermeralves/banco_de_dados/assets/54563385/ccb1499f-44ab-4909-92e6-daceb5cfcd91)

Pode-se perceber que nenhum dos cadastros realizados nesse tabela estão ferindo as regras da Primeira Forma Normal (1FN), estão dentro dos padrões:

- O atributo "cpf" é o Primary Key (PK) da entidade "aluno", esse atributo é único na tabela para cada registro.

- Não temos nenhum atributo 'Composto' ou seja, dados que podem ser separados.

- Nenhum atributo se repete ao longo dos cadastros.

- Tambem não temos atributos derivados.

Porém ao adicionar mais atributos, temos uma tabela que já não faz mais parte da Primeira Forma Normal (1FN)

![Captura de tela 2024-05-28 125906](https://github.com/guilhermeralves/banco_de_dados/assets/54563385/5656c29c-f4f2-4818-ba56-30a7dc176ac1)

Podemos perceber que o atributo "endereco" tem registros compostos.

Uma forma de transformar as condições para que essa tabela esteja enquadrada na 1FN, seria dividir os registros do atributo "endereco" em novos atributos compostos por registros simples. Dessa forma a tabela teria novos atributos como: "rua", "numero", "cidade" e "estado" e cada um desses novos atributos teriam registros simples, enquadrando-se na 1FN.

![Captura de tela 2024-05-28 162154](https://github.com/guilhermeralves/banco_de_dados/assets/54563385/c5611030-922e-434f-818d-509296821b84)

Uma segunda opção seria criar uma nova tabela para guardar essas informações sobre o atributo endereço, nessa opção teriamos duas tabelas facilitando a busca pelas informações e ainda mantendo a cultura da 1FN.

![Captura de tela 2024-05-28 153622](https://github.com/guilhermeralves/banco_de_dados/assets/54563385/f61e5ca4-3c28-4bcd-89dc-04ef417a800d)

Nessa segunda opção vemos também que a entidade "endereco" se relaciona com a entidade "aluno" através da Primary Key "id_endereco" que pode ser encontrada como uma Foreign Key na entidade "aluno".