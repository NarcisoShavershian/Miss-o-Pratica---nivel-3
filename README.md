                                 missao pratica - nivel 3
Meu primeiro framework  Criação de front-end web com base em React JS ou Next JS, com utilização de bases de teste JSON, em memória, para ambas as plataformas.
bjetivos da prática

A partir dos objetivos listados abaixo, no final do projeto, você terá criado duas versões de um front-end web, com base nas React JS e Next JS, tornando-se capacitado para lidar com contextos reais de aplicação das tecnologias abordadas:

Explorar a sintaxe Type Script na implementação de entidades e controladores, para projetos React JS e Next JS;
Criar um front-end para Web completo, baseado em componentes reutilizáveis, através do React JS;
Criar um front-end para Web completo, baseado em componentes reutilizáveis, através do Next JS;
Utilização do Next JS para a definição de uma API no estilo REST, de uso interno, com acesso via função fetch, oferecida no ambiente padrão do Java Script.
Materiais necessários para a prática

Computador com acesso à internet;
Editor de código Visual Studio Code;
Ambiente de desenvolvimento NodeJS;
Navegador de internet instalado no computador.
Desenvolvimento da prática

Vamos colocar a mão na massa ?! Siga as instruções abaixo para desenvolver esta missão.

         👉 1º Procedimento | Lista de Livros no React JS

Crie o projeto e inicie o ambiente de desenvolvimento:
a) Abrir uma linha de comandos

b) Executar npx create-react-app livros-react --template typescript

c) Entrar no diretório do projeto criado, executando cd livros-react

d) Abra o Visual Studio Code, executando o código .\

No ambiente de desenvolvimento do Visual Studio Code, crie a estrutura básica do projeto:
a) Adicione uma pasta com o nome do modelo

b) Criar, na pasta modelo , os arquivos " Editora.ts " e " Livro.ts " (TypeScript)

c) Adicione uma pasta com o nome de controle

d) Criar, na pasta controle , " ControleEditora.ts " e " ControleLivros.ts "

e) Incluir as dependências do Bootstrap no arquivo index.html , encontrado na pasta public

f) Criar os arquivos " LivroDados.js " e " LivroLista.js " (JavaScript) em src

Codifique as entidades do sistema (Editora e Livro):
a) No arquivo Editora.ts , crie a classe Editora , com os campos codEditora , numérico, e nome , do tipo texto

b) No arquivo Livro.ts , criar a classe Livro , composta dos campos: codigo e codEditora , numéricos, título e resumo , ambos do tipo texto, e autores , como um vetor de texto

Codifique o driver de editoras, no arquivo ControleEditora.ts :
a) Importar uma classe Editora

b) Definir uma variável editoras , como Array<Editora> , contendo ao menos três elementos, no formato JSON

c) Crie uma classe ControleEditora , contendo os métodos getNomeEditora e getEditoras

d) Implementar o método getEditoras , com o retorno do vetor editoras

e) Implementar o método getNomeEditora , recebendo codEditora , do tipo numérico, e retornando o nome da editora, através de uma operação filter sobre o vetor editoras

Codifique o driver de livros, no arquivo ControleLivros.ts :
a) Importar um livro de aula

b) Definir a variável livros , como Array<Livro> , contendo ao menos três elementos, no formato JSON

c) Criar uma classe ControleLivro , contendo os métodos obterLivros , incluir e excluir

d) Implementar o método obterLivros , com o retorno do vetor livros

e) Implementar o método incluir , receber um objeto do tipo Livro , que terá o código trocado pelo código mais alto do vetor, incrementado de um, e depois será adicionado ao vetor

f) Implementar o método excluir , receber um código numérico, que irá encontrar o índice do livro com o código fornecido, através de findIndex , e removê-lo com o uso de splice

Codifique o componente LivroLista , no arquivo LivroLista.js :
a) Instanciar um driver de livros, com o nome controleLivro , e um de editoras, com o nome controleEditora

b) Definir o componente auxiliar LinhaLivro , com parâmetro props , para a recepção dos atributos livro e excluir , a partir da aplicação do seletor

c) Definir em LinhaLivro o atributo nomeEditora , invocando o método getNomeEditora , com a passagem de codEditora , atributo do livro

d) No retorno do componente, deverá ser fornecida uma linha de tabela , ou tr, com os valores dos atributos do livro nas tags td

e) Abaixo do título, na célula primeiro, adicione um botão de exclusão , com a coleta de um método que será fornecido no atributo excluir

f) Exibir os autores como uma lista HTML , efetuando a geração dos itens através do método map , e tendo como chave o valor de índice

g) Definir o componente LivroLista , exportado por padrão, sem parâmetros

h) Em LivroLista , defina as propriedades livros , do tipo vetor, e carregado , booleana, através de useState

i) Utilização do Hook useEffect , que deve alimentar livros com a chamada para obterLivros , do driver, e alterar carregado para true , tendo ainda como balizador o atributo carregado

j) Aumentar o método excluir , estilo arrow function, que deve receber o código do livro, invocar o método excluir do driver , e definir o valor de carregado como false , para forçar o redesenho da página

k) Nenhum retorno do componente deve ser fornecido na área principal ( main ), contendo o título da página e uma tabela para exibição dos livros

l) Utilizar o método map , de livros , para a geração das linhas de dados como componentes do tipo LinhaLivro , tendo como configurações o livro atual do vetor, excluir invocando o método excluir de LivroList, com a passagem do código do livro corrente, e chave associada ao código do livro

Altere o arquivo App.tsx , retornando em App o componente LivroLista ;

Verifique os resultados obtidos através de um navegador, lembrando de testar a funcionalidade da exclusão do livro.
        
           👉 2º Procedimento | Página de Cadastro e Navegação no React JS

Ajuste das rotas de navegação do sistema livros-react:
a) Adicione o pacote de navegação com npm instal react-router-dom

b) Definir o componente LivroDados , em LivroDados.js , inicialmente com o retorno de uma tag main e uma mensagem de "Olá mundo", devendo ser exportado por padrão

c) Alterar o arquivo App.tsx , com a adição das rotas e menu de navegação

d) Nenhum retorno do componente deve ser fornecido um BrowserRouter , onde as rotas, na divisão Routes , serão a raiz , apontando para LivroLista , e dados , apontando para LivroDados

e) Antes da divisão Routes, defina o menu de navegação, com tag nav , formatado pelo BootStrap , e utilize elementos do tipo Link , no lugar das âncoras, para acesso às rotas definidas

Implemente o componente LivroDados , no arquivo LivroDados.js :
a) Instanciar um driver de livros, com o nome controleLivro , e um de editoras, com o nome controleEditora

b) Em LivroDados , defina o vetor opcoes , invocando o método getEditoras , com o mapeamento de codEditora para valor e nome para texto

c) Definir as propriedades titulo , resumo e autores , todo o texto, através de useState , além de codEditora , iniciado com a posição zero de opcoes

d) Aumentar o atributo navegar , receber o Hook useNavigate

e) Definir o método tratarCombo , tendo o evento como parâmetro, onde deve ocorrer a chamada para setCodEditora , com a passagem do valor de um combo de seleção ( target do evento) convertido para número

f) Definir o método incluir , com a recepção de um evento, que primeiro deve eliminar o comportamento padrão com preventDefault , em seguida instanciar um livro com código valendo zero, o valor das propriedades de estado, e autores separados por linha ( split ), invocar o método incluir do driver de livros , e navegar para a página de listagem, na raiz

g) Nenhum retorno do componente deve ser fornecido a área principal ( main ), contendo o título da página e um formulário para inclusão do livro, sendo composto dos campos referentes às propriedades de estado , com ligação através de value e onChange

h) Utilizar uma lista de seleção (combo) para as editoras, com as opções oferecidas pelo método map , de opcoes , e associando onChange ao método tratarCombo

i) Relacionar o evento onSubmit , do formulário, ao método incluir , além de adicionar um botão de submissão ao final

Verifique os resultados obtidos através de um navegador, lembrando de testar uma nova funcionalidade de inclusão de livros.
           
           
           👉 3º Procedimento | Criação do Aplicativo com Next JS

Crie o aplicativo e configure o ambiente:
a) Executar o comando npx create-next-app livros-next --typescript

b) Entrar no diretório do projeto criado, executando cd livros-next

c) Abra o Visual Studio Code, executando o código .\

d) No ambiente de edição, crie um diretório (pasta) com o nome classes , e copie os diretórios modelo e controle , do projeto livros-react , com seus respectivos arquivos Type Script, para dentro do novo diretório

e) Criar o diretório de componentes , e dentro dele adicionar os arquivos para componentes auxiliares, com os nomes " LinhaLivro.tsx " e " Menu.tsx "

f) No diretório pages/api , crie os diretórios com os nomes editoras e livros

g) No diretório editoras , crie os arquivos " [codEditora].ts " e " index.ts "

h) No diretório livros , crie os arquivos " [codigo].ts " e " index.ts "

Implemente uma API de gerenciamento de editores via HTTP:
a) Codificar o arquivo index.ts , no diretório pages/api/editoras , iniciando com a definição de uma instância exportável de ControleEditora, com o nome controleEditora

b) Definir a assinatura para tratamento das transferências, cujo formato deve ser export default (req: NextApiRequest, res: NextApiResponse) => { }

c) Implementar o tratamento de requisições, respondendo no método GET com status 200 e o vetor de editores, obtidos via método getEditoras , de controleEditoras , no formato JSON

d) Tratar o status 405 , para método não permitido, e 500 , para exceção ocorrida no servidor

e) Codificar o arquivo [codEditora].ts , no diretório pages/api/editoras

f) Importe o driver de editores instanciado em index.ts, utilizando o comando import {controleEditora} from '.'

g) Definir a assinatura para tratamento das obrigações, cujo formato deve ser export default (req: NextApiRequest, res: NextApiResponse) => { }

h) Implementar o tratamento de requisições, respondendo no método GET com status 200 e um objeto JSON como o nome da editora, obtido através de getNomeEditora , tendo como parâmetro codEditora , fornecido na URL de acesso e recuperado via req.query , convertido para number

i) Tratar o status 405 , para método não permitido, e 500 , para exceção ocorrida no servidor

Teste uma API nova
a) Iniciar a execução do aplicativo através do comando npm run dev

b) Abrir o endereço http://localhost:3000/api/editoras no navegador

c) Abrir o endereço http://localhost:3000/api/editoras/3 no navegador
Implemente uma API de gerenciamento de editores via HTTP:
a) Codificar o arquivo index.ts , no diretório pages/api/livros , iniciando com a definição de uma instância exportável de ControleLivro, utilizando o nome controleLivro

b) Definir a assinatura para tratamento das transferências, cujo formato deve ser export default (req: NextApiRequest, res: NextApiResponse) => { }

c) Implementar o tratamento de requisições, respondendo no método GET com status 200 e o vetor de livros, obtidos via método obterLivros , de controleLivro , no formato JSON

d) Responder ao método POST com a captura dos dados do livro, fornecido no corpo da requisição, no formato JSON , a partir de req.body , inclusão no vetor de livros via método incluir , de controleLivros , e retorno para o chamador com status 200 e mensagem de sucesso no formato JSON

e) Tratar o status 405 , para método não permitido, e 500 , para exceção ocorrida no servidor

f) Codificar o arquivo [codigo].ts , no diretório pages/api/livros

g) Importe o driver de livros instanciado em index.ts, utilizando o comando import {controleLivro} from '.'

h) Definir a assinatura para tratamento das transferências, cujo formato deve ser export default (req: NextApiRequest, res: NextApiResponse) => { }

i) Implementar o tratamento de requisições, respondendo ao DELETE com a captura do código fornecido na URL , via req.query , exclusão do livro no vetor, via método excluir de controleLivro , e retornar ao chamador com status 200 e mensagem de sucesso no formato JSON

j) Tratar o status 405 , para método não permitido, e 500 , para exceção ocorrida no servidor

Teste a nova API, efetuando uma consulta no navegador a partir do endereço http://localhost:3000/api/livros , onde deve ser retornado o vetor de livros no formato JSON , e opcionalmente testar os demais métodos ( POST e DELETE ) via Postman, Boomerang, ou outra ferramenta para envio de requisições
Habilite o Bootstrap no aplicativo Next JS:
a) Parar o aplicativo livros-next, esteja em execução, e execute o comando npm install bootstrap

b) Alterar o conteúdo de _app.tsx para o que é apresentado a seguir, com a importação da folha de estilo do Bootstrap, deixando-a disponível para todos os componentes
Implemente o componente LinhaLivro , no arquivo LinhaLivro.tsx :
a) Comece com a definição de uma instância de ControleEditora , com o nome controleEditora , utilizado internamente para diminuir a quantidade de chamadas assíncronas, já que os dados de editores não são dinâmicos

b) Definir uma interface LinhaLivroProps , com o atributo livro , do tipo Livro , e método excluir() , do tipo void 

c) Definir o componente exportável LinhaLivro , com parâmetro props , para a recepção dos atributos livro e excluir , a partir do seletor, utilizando export const LinhaLivro: React.FC<LinhaLivroProps> = (props) => { }

d) Copiar o corpo da função LinhaLivro , encontrado no arquivo LivroLista.js , do projeto livros-react , para o corpo da nova função, o que se justifica pelo fato de que apenas a assinatura é modificada para uso no Next JS

Implemente o componente Menu.tsx , de acordo com as instruções a seguir:
a) Defina o componente com export const Menu: React.FC = () => { }

b) Retornar o menu de navegação, com tag nav , formatado pelo BootStrap

c) Utilização de elementos do tipo Link , da biblioteca next/link

d) Através do atributo href , de Link , forneça acesso para as páginas index , LivroLista e LivroDados , como opções do menu de navegação

Altere o componente Home , no arquivo index.tsx :
a) Sem retorno, mantenha a div inicial, com classe CSS container

b) No componente Head , altere o título para "Loja Next"

c) Aumentar um componente Menu após Head

d) Após o menu, defina a área principal ( main ), com estilo estilos.main , e dentro dela criar um título h1 , com estilo estilos.title e texto Página Inicial

e) Apagar todo o restante da página original
Implemente o componente LivroLista , no arquivo LivroLista.tsx :
a) Importar os estilos com importar estilos de '../styles/Home.module.css'

b) Defina uma constante com o nome baseURL , do tipo texto, utilizando o valor "http://localhost:3000/api/livros"

c) Criar a função obter , assíncrona , no estilo arrow function, com a chamada para baseURL , via fetch , e retorno da resposta no formato JSON

d) Criar a função excluirLivro , assíncrona , no estilo arrow function, tendo o parâmetro codigo , numérico, com a chamada para baseURL/codigo via fetch , no modo DELETE , e retornar do campo ok da resposta, trazendo sucesso ou falha

e) Em LivroLista , defina as propriedades livros , do tipo Array<Livro> , e carregado , booleana, através de useState

f) Utilizar o Hook useEffect , que deve fazer a chamada para obterLivros , assíncrona, alimentando a propriedade de livros de estado no retorno, via operador then , e alterar carregado para true , tendo ainda como balizador o atributo carregado

g) Aumentar o método excluir , estilo arrow function, que deve receber o código do livro, invocar a função excluir , assíncrona, e no retorno definir o valor de carregado como false , para forçar o redesenho da página

h) Nenhum retorno do componente deve ser fornecido um div , formatado com estilos.container , e dentro dela um componente Head , equivalente ao que foi utilizado na página Home, um componente Menu , e a área main , contendo o título da página e uma tabela para exibição dos livros

i) Utilizar o método map , de livros , para a geração das linhas de dados como componentes do tipo LinhaLivro , tendo como configurações o livro atual do vetor, excluir invocando o método excluir de LivroList, com a passagem do código do livro corrente, e chave associada ao código do livro

Implemente o componente LivroDados , no arquivo LivroDados.tsx
a) Importar os estilos com importar estilos de '../styles/Home.module.css'

b) Definir um objeto do tipo ControleEditora, com o nome controleEditora

c) Defina uma constante com o nome baseURL , do tipo texto, utilizando o valor "http://localhost:3000/api/livros"

d) Criar a função incluirLivro , assíncrona , no estilo arrow function, tendo o parâmetro livro , do tipo Livro, com a chamada para baseURL via fetch , no modo POST , incluindo o tipo de conteúdo como informação do header e o livro no body , convertido com JSON.stringfy . O retorno da função será o campo ok da resposta, queda sucesso ou falha

e) Em LivroDados , defina o vetor opcoes , invocando o método getEditoras , com o mapeamento de codEditora para valor e nome para texto

f) Definir as propriedades titulo , resumo e autores , todo o texto, através de useState , além de codEditora , iniciado com a posição zero de opcoes

g) Aumentar o atributo navegar , receber o Hook useNavigate

h) Defina o método tratarCombo , tendo como parâmetro o evento , do tipo React.ChageEvent<HTMLSelectElement> , onde deve ocorrer a chamada para setCodEditora , passando value , da lista, convertido para number

i) Definir o método incluir , apresentando como parâmetro um evento do tipo React.FormEvent<HTMLFormElement> , que primeiro deve eliminar o comportamento padrão com preventDefault , em seguida instanciar um livro com código valendo zero, o valor das propriedades de estado, e autores separados por linha ( split ), invocar a função inclui, assíncrona, e, no retorno dela, navegar para a página LivroLista , através do sistema de navegação do Next JS , com a chamada para Router.push

j) Nenhum retorno do componente deve ser fornecido um div , formatado com estilos.container , e dentro dela um componente Head , equivalente ao que foi utilizado na página Home, um componente Menu , e a área main , contendo o título da página e o formulário para inclusão do livro

k) Implementar o formulário referente aos campos utilizados para definir as propriedades de estado , com ligação através de value e onChange

l) Utilizando uma lista de seleção (combo) para as editoras, com as opções oferecidas pelo método map , de opcoes , e associando onChange ao método tratarCombo

m) Relacionar o evento onSubmit , do formulário, ao método incluir , além de adicionar um botão de submissão ao final

A execução do projeto deverá fornecer as mesmas funcionalidades do livro-reagir, bem como aparência muito semelhante, mas agora com o gerenciamento da base de livros a partir da API interna, acessada de forma assíncrona, via fetch;
Verifique os resultados obtidos através de um navegador.
