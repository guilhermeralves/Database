![banner_banco_de_dados_git](https://github.com/guilhermeralves/banco_de_dados/assets/54563385/b2bc7324-be7f-4207-bfa2-3ff1b2daf746)

# Principais Tópicos desse Artigo:

- Introdução ao Modelo Relacional
- Manipulação e Organização de Dados
- 





## Introdução ao Modelo Relacional

O modelo relacional é um método de organizar os dados usando tabelas compostas por linhas e colunas. Cada tabela representa uma entidade, e as relações entre essas entidades são definidas pelas chaves primárias, comumente chamadas de (Primary Key - PK) e estrangeiras (Foreign key - FK).

Os principais Componentes são:

Tabela: Também conhecida como relação, é a estrutura básica do modelo relacional. Cada tabela é composta por linhas (registros) e colunas (atributos ou campos).

Chave Primária (Primary Key): É um atributo ou conjunto de atributos que identifica exclusivamente cada registro em uma tabela. Garante a unicidade dos dados.

Chave Estrangeira (Foreign key): É um atributo em uma tabela que estabelece uma relação com a chave primária de outra tabela. É usada para criar associações entre tabelas.

Exemplo Modelo Relacional:

![ER_Banco_de_Dados_1](https://github.com/guilhermeralves/banco_de_dados/assets/54563385/857135e0-405e-44a0-bc73-6b16c31b2628)


Na Imagem a cima, temos uma explicação mais visual, Exemplo de um modelo relacional com 3 entidades: "Livro", "Autor" e "Editora". Podemos perceber, como já comentado, que a relação entre as entidades se dá através das Primary Key´s e Foreign Key´s. A entidade "Livro" se relaciona com a entidade "Autor" através da Foreign Key: "ID_Autor", já o relacionamento entre: "Livro" e "Editora" acontece por meio da Foreign Key: "ID_Editora".