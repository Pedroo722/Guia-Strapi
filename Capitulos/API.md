## Registros de Exemplo

No passo anterior, foi criado uma coleção chamada "Clientes", que foi configurada para armazenar 3 valores diferentes: Nome, Email e Telefone.

Agora para servir de exemplo no nosso teste da API, iremos primeiro adicionar 2 registros a nossa coleção. No Dashboard do Strapi, vá em **Content Manager**. Clique na coleção anteriormente criada e depois clique em *Create new entry* no canto superior direito da tela. Com isso vá e adicione dois regitros a sua coleção. Depois marque a opção Publish em cada um, que será necessário para tornar os registros visíveis para a nossa API

No meu exemplo, foram adicionados na coleção Clientes 2 registros, "Roberto" e "Ana":

![2Entries](https://github.com/Pedroo722/Guia-Strapi/assets/132232273/d1e1a6fc-ea21-4e97-b104-8ea2cb623195)


## Permissões da Coleção

Para acessar a sua API, você só precisa mudar no link do Dashboard inicial "/admin" por "/api/[Nome_da_coleção]".

Por exemplo, o link do meu dashboard inicial é "https://back.pedrohenriq1921.repl.co/admin". Logo o link para a API da minha coleção Clientes ficou "https://back.pedrohenriq1921.repl.co/api/clientes". 

No entanto, se você tentar acessar o link da sua API agora, a página mostrará o Erro 403 Forbidden. Ainda não é possivel acessar as informações pois ainda não alteramos as permissões necessárias.

![image](https://github.com/Pedroo722/Guia-Strapi/assets/132232273/4a6f2f0d-c235-4f20-ae98-537376d9abf1)

Para consertar isso. Vá no Dashboard do Strapi, vá no painel **Settings** > **USERS & PERMISSIONS PLUGIN** > **Roles**. Chegando nessa página

![Roles](https://github.com/Pedroo722/Guia-Strapi/assets/132232273/62b607fe-ebda-4f84-80c6-de382533b697)

Clique para editar a opção *Public*, depois disso vá até a coleção criada. Por hora, apenas marque as opções *find* e *findOne*

![PublicRole](https://github.com/Pedroo722/Guia-Strapi/assets/132232273/30f1209e-2be8-480c-95ba-c427cdfecbae)
![image](https://github.com/Pedroo722/Guia-Strapi/assets/132232273/8dea22d8-6132-4fbf-ab08-a89efdc2800e)

Com isso a nossa página da API deve estar mostrando com sucesso os registros da nossa tabela.

![APISuccess](https://github.com/Pedroo722/Guia-Strapi/assets/132232273/3d638ecd-8d26-4705-b2a4-d752aa429fc9)

Agora volte no settings e desmaca *find* e *findOne*. A gente queria ver funcionado, mas a conselho do Professor André, precisaremos trabalhar com autenticação e permissões por questões de segurança. Por isso agora iremos criar um [Token de acesso para fazer a nossa API funcionar](Token.md).
