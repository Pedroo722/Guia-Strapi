## Criando meu Token

Volte para o Dashboard inicial Vá em **Global Settings** > **API Token**. Chegando nessa página, clique em *Create API Token*.

Token duration fica como Unlimited e Token type fica como Full access. Exemplo:
![Token_Exemplo](https://github.com/Pedroo722/Guia-Strapi/assets/132232273/0efff72f-ae08-4cc5-8077-03fd329b76c9)
![image](https://github.com/Pedroo722/Guia-Strapi/assets/132232273/64a913ad-4b09-4787-8ee6-855d941a592d)

Com isso clique em salvar e então copie e guarde o codigo do seu Token em algum lugar. Por razões de segurança, você só pode ver o Token uma única vez, então guarde em um lugar seguro.

## Teste da API REST com postman

Agora um passo mais opcional para testarmos se o nosso Token está mesmo utilizável, e aproveitando iremos ver os comandos da API REST do Strapi, que serão utilizados quando formos realizar a integração do nosso Back-end com o Front-end. Primeiramente, abra em uma nova guia o seguinte url:

 https://www.postman.com/

No canto superior, clique em sign in e entre com alguma conta do google.

Depois de entrar, vá em Workspaces no menu a esquerda. Clique em *Create Your Workspace*.

![WorkspaceMenu](https://github.com/Pedroo722/Guia-Strapi/assets/132232273/dffc2a1a-3c66-4111-9bd9-fed9a97987ad)

Escolha o template Blank Workspace. Na opção de "Who can access your Worskpace", pode deixar como "Team". Então cliquem em "Create".

![TestePostma1](https://github.com/Pedroo722/Guia-Strapi/assets/132232273/17f76857-3ca9-4702-b4e0-3707ccd13fae)
![TestePostman2](https://github.com/Pedroo722/Guia-Strapi/assets/132232273/de9850e0-863d-43cb-8010-9def0495c7ab)

Nessa nova pagina, na abazinha do canto superior da tela. Do lado de 'Overview' clique no +

![image](https://github.com/Pedroo722/Guia-Strapi/assets/132232273/2339b2ee-15ae-4408-9e8a-802de9f8287e)
![image](https://github.com/Pedroo722/Guia-Strapi/assets/132232273/50bdd3a8-54b8-4447-8468-fe1a7c66ea7f)

### GET

O primeiro comando da API REST que iremos testar é o comando 'GET'. Utilizado para retornar os registros de nossa coleção. Por padrão retornando todos os registros públicos.

Para realizar o comando no Postman, clique em *Header* e então só preencha como feito na foto, usando o url da sua API:
- GET: [url da sua coleção do Strapi. No meu caso: "https://back.pedrohenriq1921.repl.co/api/clientes"]
- Na segunda Key, a primeira linha com "Authorization" e a segunda com "Bearer [Token]". 
![PreenchidoPostman](https://github.com/Pedroo722/Guia-Strapi/assets/132232273/58ec7be6-fa90-4590-bc8e-eb4ef876b7a6)

E por fim só clicar no botão *Send* no canto superior da tela. Com isso na caixa inferior da tela, você verá o status do seu request, se o código for 200, sua requisição deu certo. Logo deve aparecer os registros que foram anotados na sua coleção, como mostrá a imagem.

![registros](https://github.com/Pedroo722/Guia-Strapi/assets/132232273/b1ccf42b-acdb-4a87-bdd5-67575680a57e)
![registros2](https://github.com/Pedroo722/Guia-Strapi/assets/132232273/178baac3-2bb8-49ca-ba28-4fb0611d99a8)

Adicionalmente, você pode escolher adicionar algum parametro ao seu comando GET, limitando o retorno de registro. Por exemplo, "/1" ou "/2" no final da sua url limitará o comando GET para agir apenas nos elementoe da sua tabela com id = 1 ou id = 2

![id1](https://github.com/Pedroo722/Guia-Strapi/assets/132232273/edd5fdc0-e556-467e-ae6d-1c84738baffb)
![id2](https://github.com/Pedroo722/Guia-Strapi/assets/132232273/152c0cb3-7015-45e0-ab24-6699d95245e5)

### Status: 503 Bad Gateway

Aleatoriamente, ao clickar no *Send* pode ocorrer do seu request falhar. Retornando assim o status 502 e uma mensagem de erro do Replit: "Unable To Wake Up", no lugar onde deveria haver seus registros, como mostra a imagem.

![Error 503](https://github.com/Pedroo722/Guia-Strapi/assets/132232273/b4ac2929-a0b0-448a-8822-4a40b2dedfc2)

Isso ocorreu porque o seu servidor no replit parou de funcionar, para resolver isso, apenas volte no Shell do seu projeto e refaça o comando "npm run develop".

### POST

O segundo comando da API REST do Strapi é o comando POST, utilizado para criar um novo registro na sua coleção. Assim como no comando GET, será necessário preencher o cabecário superior com o url da sua API e o Token de acesso.

![POST_1](https://github.com/Pedroo722/Guia-Strapi/assets/132232273/4a547432-ef30-40d5-b24e-974809c0fe59)

Mas dessa vez

### PUT

### DELETE

Com isso podemos ver que o nosso Token de acesso está funcionando. [Agora iremos ver como utilizar os comandos da nossa REST API para conseguir adicionar, remover e alterar registros na nossa coleção.](REST.md)
