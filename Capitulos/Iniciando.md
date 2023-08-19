# Criando meu projeto Strapi

De inicio, não tem segredo. Somente seguir passo a passo da [documentação do Professor Hugo](https://prism-longship-bba.notion.site/Strapi-a1582570ea6e4946a9ad5197b256a239#90f7276673cc47e7888bbfc7532cb935) e o seu [vídeo tutorial de instação.](https://www.youtube.com/watch?v=U-Lf6A_ZCEM).

Passo a passo:
- Crie um replit em branco e o nomei-o (como "Back" por exemplo). É importante o uso de alguma ferramenta como o replit, pois a intalação do Strapi no ambiente de desenvolvimento local implicaria alguns problemas que dificultariam o desenvolvimento. Por hora, significa a hospedagem do nosso Back-end será limitada ao replit.
- Agora no Shell, realizem o comando: 'npx create-strapi-app@latest my-project'. Que será usado para preparar o ambiente de desenvolvimento do Strapi. "my-project" será o nome da sua pasta. Logo pode ser alterado para algum outro nome que acharem melhor (como "backend" por exemplo.)
- Para a instalação, escolha a versão 16_x do Node.js, e então escolha a opção recomendada "Quickstart". Espere um pouco até terminar a nossa instalação.

Saberá que a instalação terminou quando sua tela estiver assim:

![InstalacaoStrapi1](https://github.com/Pedroo722/Guia-Strapi/assets/132232273/cbb8ccf8-9c5e-49ac-96d2-4672c1dacb15)
![InstalacaoStrapi2](https://github.com/Pedroo722/Guia-Strapi/assets/132232273/69ff284a-9710-44c8-a872-1c56f4302d11)

- Depois da instalação, realizem o comando 'cd backend/' (cd de "Change Directory", e backend sendo o nome da sua pasta). Isso é importante pois os dois comandos a seguir precisam serem executados na nossa pasta do backend.
- Agora, ainda no shell, realize o comando: 'npm run build'. Que será utilizado para criar a nossa admin UI. O processo estará terminado quando aparecer uma mensagem no shell escrita "Admin UI built successfully". (Espere alguns segundos e veja se também aparece linhas http de GET das páginas html do Strapi)
- Após isso, aperte Ctrl+C para matar o nosso projeto.
- Finalmente, realize o comando: 'npm run develop' (Antes disso, novamente faça o comando 'cd backend/' caso não esteja mais na pasta backend). O processo estará terminado quando aparecer uma mensagem no shell escrita "localhost:1337/admin".

Quando termina, sua tela deve estar mais ou menos assim:

![image](https://github.com/Pedroo722/Guia-Strapi/assets/132232273/a3746931-96ed-4608-aa9d-e990090eee77)
![image](https://github.com/Pedroo722/Guia-Strapi/assets/132232273/6927378b-3831-4073-a733-13cd7115f47a)

Com isso, você deve ter finalizado a instalado e criação do seu projeto Strapi corretamente. Agora só falta abrir a url do webview em uma nova aba (Pode só copiar e colar o link, mas tem um botãozinho par aisso do lado url).

No meu caso o url ficou: "https://back.pedrohenriq1921.repl.co" ("back" sendo do nome dado ao replit em branco).

Com isso, você deve estár na página inicial do Strapi, onde já podemos [criar o admin do módulo administrativo e partir para e a criação das nossas coleções.](Colecoes.md)

## Bug no Replit: Unable To Wake Up

É bastante comum que você se depare com essa tela de erro ao tentar abrir o url do seu webview. Isso ocorre porque o replit não conseguiu realizar o comando HTTP de GET das páginas html do Strapi.

![UnableToWakeUp](https://github.com/Pedroo722/Guia-Strapi/assets/132232273/dc671c49-910c-44ef-9d5d-e617996450b3)

Para resolver isso basta apenas voltar no passo a passo e novamente realizar os comandos 'npm run build' e então 'npm run develop' no Shell do projeto replit. E dessa vez espere até que as mensagens de GET aparecam no Shell. Como mostra a imagem:

![GETHttp](https://github.com/Pedroo722/Guia-Strapi/assets/132232273/e4bebc67-7aa1-4b63-b980-941eb916ae19)


