Esta é uma Aplicação formulada com Frontend em Vite, com Backend em Laravel, com Base de
Dados pelo MySQL e a estilização com Tailwind, com dados a buscar em Rest Api.

A aplicação tem por objetivo administrar os agendamentos de consulta e os dados tanto de clientes
como de médicos de uma clínica genérica.

Para acessar o projeto, deve-se fazer os comandos no projeto Frontend: “npm i react”, “ npm i
tailwindcss” e “npm i postcss”. e no backend “npm i".

E, após, conectar a base de dados do MySql já é possível mexer no projeto.

A primeira rota acessar é a página Home, em que é possível fazer o Login ou criar um novo Login em
“signup”, caso pretenda, pode clicar no símbolo no início do header, que redirecionará para a página
Home.

Aplicação têm a lógica de autenticação de user em que por meio de um Context, é providenciado um
Token ao user registado, em que, ao definir o user_type (adm, client ou doctor), este é armazenado
juntamente com os dados preenchidos, na base de dados, diferenciado as permissões dos users de
acordo com o user_type.

Cada tipo de user acede à uma page diferente: adm, client ou doctor, em que nelas, tem uma nav lateral que permite navegar entre a aplicação.
No adm é possível ver, adicionar e deletar users, doctors e pacientes (esta última não
implementada), bem como fazer agendamentos (não implementado).

No Doctor é possível ver os agendamentos e a lista de fármacos (não implementado).
Enquanto que no Client é possível ver os agendamentos e marcar algum (não implementado).

Os dados preenchidos nos forms de cada página são enviados ao Backend por meio de chamadas
Axios, em que lá são recebidas e tratadas pelos controladores devidos, que fazem inclusive as
Queries à base de dados.
