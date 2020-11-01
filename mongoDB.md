# INTRODUÇÃO AO MongoDB

O MongoDB foi criado para garantir uma certa dinâmica. Por isso, foi pensado em Big Data, sendo capaz de suportar seu escalonamento tanto vertical quanto horizontal. Além disso, usa replica sets, que permitem que ele seja capaz de lidar com um grande volume de informações.Seu uso é orientado para documentos em JSON, permitindo que tabelas e colunas sejam criadas previamente. 

## COMANDOS DO MongoDB

>### DATABASES
- show dbs: lista todos os bancos de dados, o alias desse comando é show databases;
- use [nome-do-banco]: selecionar um banco de dados, ex.: use admin;
- db: verifica qual o banco de dados em uso no momento;
- use terminalroot: cria um banco de dados, mas só passa a existir efetivamente quando você cria uma collection e insere algum dado nela, se não o mesmo não estará disponível quando você listar os bancos, deixará de existir;
- db.dropdatabase(): apaga um banco de dados, usar após selecionar use nome-do-banco que deseja;

>### COLLECTIONS 
- show collections: Mostra as collections;
- createcollection(): Cria uma collection, protótipo dela é createcollection("nomedatabela", opções), exemplo: db.createcollection("minhacolecao").
- db.nome_da_colecao.find().pretty(): Ler todos os dados de uma coleção, ex.: db.system.users.find().pretty() , ler todos os dados da coleção system.users, equivalente à select * from tabela. essa saída sairá formatada, se quiser os dados numa única linha, use sem o método .pretty(): db.system.users.find();
- db.nome_da_colecao.insert(): Insere dados numa coleção, ex.: db.minhacolecao.insert( { "_id" : 0, "site" : "terminal root", "url" : "terminalroot.com.br", "content" : "sobre mongodb" } );
- db.nome_da_colecao.update(consulta, o_que_atualizar, opções): Atualiza(update) dados em um documento(campo), ex.: db.minhacolecao.update({'content':'sobre mongodb'},{$set:{'content':'mongodb definitivo tutorial'}}), altera o documento de nome content que tem o valor: sobre mongodb por mongodb definitivo tutorial;
- db.nome_da_colecao.drop(): Deleta uma coleção, ex.: db.minhacolecao.drop(), deleta a coleção minhacolecao.
db.dados.remove({"mail": "james@brown.org"}) - Remove um documento( linha em SQL ) que possui uma coluna( campo em SQL ) mail igual à james@brown.org.

### REFERÊNCIAS
1. _https://www.luiztools.com.br/post/tutorial-mongodb-para-iniciantes-em-nosql/_
2. _https://www.devmedia.com.br/introducao-ao-mongodb/30792_
3. _https://terminalroot.com.br/2020/02/mongodb.html_
4. _http://paulodutrainfo.com.br/alguns-comandos-basicos-mongodb_