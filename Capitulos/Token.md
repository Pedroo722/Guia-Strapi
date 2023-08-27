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

Adicionalmente, você pode escolher adicionar algum parametro ao seu comando GET, limitando o retorno de registro. Por exemplo, "/1" ou "/2" no final da sua url limitará o comando GET para agir apenas nos elementos da sua tabela com id = 1 ou id = 2

![id1](https://github.com/Pedroo722/Guia-Strapi/assets/132232273/edd5fdc0-e556-467e-ae6d-1c84738baffb)
![id2](https://github.com/Pedroo722/Guia-Strapi/assets/132232273/152c0cb3-7015-45e0-ab24-6699d95245e5)

### Status: 503 Bad Gateway

Aleatoriamente, ao clickar no *Send* pode ocorrer do seu request falhar. Retornando assim o status 502 e uma mensagem de erro do Replit: "Unable To Wake Up", no lugar onde deveria haver seus registros, como mostra a imagem.

![Error 503](https://github.com/Pedroo722/Guia-Strapi/assets/132232273/b4ac2929-a0b0-448a-8822-4a40b2dedfc2)

Isso ocorreu porque o seu servidor no replit parou de funcionar, para resolver isso, apenas volte no Shell do seu projeto e refaça o comando "npm run develop".

### POST

O segundo comando da API REST do Strapi é o comando POST, utilizado para criar um novo registro na sua coleção. Assim como no comando GET, será necessário preencher o cabeçalho superior com o url da sua API e o Token de acesso.

![POST_1](https://github.com/Pedroo722/Guia-Strapi/assets/132232273/15a82593-08c8-404f-bc82-dfc2d0760ee0)

Mas dessa vez, também será necessário preencher na aba "Body" (e no formato Json), um arquivo json contendo o id, as informações e atributos do novo registro a ser criado. Como mostra a image:

![POST_2](https://github.com/Pedroo722/Guia-Strapi/assets/132232273/d8141485-0085-4af9-a548-9dd326561dd6)

Com isso, na parte inferior da tela, o site retornará as informações do novo registro criado.

![Post_response](https://github.com/Pedroo722/Guia-Strapi/assets/132232273/bee06678-659a-4812-ae59-4f842af239fb)

### PUT

O comando PUT é utilizado para alterar um registro existente. Para isso será necessário especificar na url da sua API o registro especifico que deseja ser alterado.

![PUT_1](https://github.com/Pedroo722/Guia-Strapi/assets/132232273/f59f5dc8-da3e-42e4-8030-76bba221349c)

Enquanto que no Body, novamente será necessário criar um arquivo json. Mas dessa vez será necessário especificar somente os atributos que serão editados

![PUT_2](https://github.com/Pedroo722/Guia-Strapi/assets/132232273/c4a2aa67-83eb-4011-8e30-fd3b1edc11dc)

O postman retornará o novo registro editado, e você pode ainda realizar o comando GET novamente para verificar que o seu atributo foi mesmo editado. Como mostrá a imagem onde o telefone do terceiro registro foi alterado depois de realizarmos o comando GET:

![PUT_response_(GET)](https://github.com/Pedroo722/Guia-Strapi/assets/132232273/d3fb0630-5bec-4a31-9098-88524eb61471)

### DELETE

Por fim, o último comando da API REST é o comando DELETE, cuja funcionalidade é bem intuitiva. DELETE simplesmente deletará algum registro com base no valor especificado no url da sua API. Não havendo necessidade de se criar algum arquivo Json.

![DELETE](https://github.com/Pedroo722/Guia-Strapi/assets/132232273/24d52b3f-c834-4ce6-aa2d-0c3af0020a67)

Como resposta, o site retorna o registro deletado e o seus atributos.

![DELETE_response1](https://github.com/Pedroo722/Guia-Strapi/assets/132232273/90b4ac30-e4ae-47e0-9806-3b36032ba477)

Caso haja uma tentativa de deletar algum registro já deletado ou inexistente, será retornado null e o Status 404.

![DELETE_response2](https://github.com/Pedroo722/Guia-Strapi/assets/132232273/a812d28f-2285-4237-9649-535cc862fadb)

## Axios e Integração

Com isso podemos ver que o nosso Token de acesso está funcionando e ainda foi possivel checar os 4 comandos da API REST. Agora iremos ver como utilizar esses comandos junto da [biblioteca Axios para Javascript, para conseguirmos iniciar na integração entre o nosso Front-end e o nosso Back-end.](REST.md)
