## Criando meu Token

Volte para o Dashboard inicial Vá em **Global Settings** > **API Token**. Chegando nessa página, clique em *Create API Token*.

Token duration fica como Unlimited e Token type fica como Full access. Exemplo:
![Token_Exemplo](https://github.com/Pedroo722/Guia-Strapi/assets/132232273/0efff72f-ae08-4cc5-8077-03fd329b76c9)
![image](https://github.com/Pedroo722/Guia-Strapi/assets/132232273/64a913ad-4b09-4787-8ee6-855d941a592d)

Com isso clique em salvar e então copie e guarde o codigo do seu Token em algum lugar. Por razões de segurança, você só pode ver o Token uma única vez, então guarde em um lugar seguro.

## Teste com postman

Agora um passo mais opcional para testarmos se o nosso Token está mesmo utilizável. Abra em uma nova guia o seguinte url:

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

Agora clique em Header e só preencha como feito na foto:
- GET: [url da sua coleção do Strapi. No meu caso: "https://back.pedrohenriq1921.repl.co/api/clientes"]
- Na segunda Key, a primeira linha com "Authorization" e a segunda com "Bearer [Token]". 

![PreenchidoPostman](https://github.com/Pedroo722/Guia-Strapi/assets/132232273/58ec7be6-fa90-4590-bc8e-eb4ef876b7a6)

E por fim só clicar no botão *Send* no canto superior da tela. Com isso na caixa inferior da tela, deve aparecer os registros que foram anotados na sua coleção.

![registros](https://github.com/Pedroo722/Guia-Strapi/assets/132232273/b1ccf42b-acdb-4a87-bdd5-67575680a57e)
![registros2](https://github.com/Pedroo722/Guia-Strapi/assets/132232273/178baac3-2bb8-49ca-ba28-4fb0611d99a8)

Você pode adicionar "/1" ou "/2" na url da sua API para limitar o comando GET apenas ao elemento da sua tabela com id = 1 ou id = 2

![id1](https://github.com/Pedroo722/Guia-Strapi/assets/132232273/edd5fdc0-e556-467e-ae6d-1c84738baffb)
![id2](https://github.com/Pedroo722/Guia-Strapi/assets/132232273/152c0cb3-7015-45e0-ab24-6699d95245e5)

Com isso finalizamos o teste inicial do nosso Token de acesso. [Agora iremos ver como utilizar os comandos da nossa REST API para conseguir adicionar, remover e alterar registros na nossa coleção.](REST.md)
