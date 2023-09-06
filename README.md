# Como adicionar token automático na variável de ambiente usando Insomnia

## Como colocar o token na variável de ambiente de forma automática
A ideia principal: em vez de passar o valor do token manualmente nas minhas variáveis de ambiente, preciso buscar esse token a partir da resposta de uma outra requisição - (no caso, na requisição de logar).

Abrindo as minhas variáveis de ambiente, na propriedade que eu quero obter o dado, dou um Ctrl + barra de espaço entre aspas duplas. Vai abrir um leque de opções. Seleciono: "Response -> Body Attribute".

![image](https://user-images.githubusercontent.com/60934938/207662182-dc8e4bc7-4a45-4f0d-820d-daa7444a0277.png)

Após selecionar essa opção, vai ficar como uma tag vermelha, não tem problema. Clica nessa tag e um formulário será aberto. 
Os campos são: Function to Perform, Attribute, Request, Filter (JSONPath or XPath), Trigger Behavior e Live Preview.

![image](https://user-images.githubusercontent.com/60934938/207662236-5b2dc64e-c597-4a5d-b7c2-823ba5c86255.png)


Depois de definir qual a requisição vai retornar os resultados que precisa, no meu caso, [Sessions] Post Create (login), no campo Filter virá os dados de resposta. Colocando apenas $ vai mostrar todos os dados que obtivemos da resposta. Para pegar apenas o token, no meu caso, basta $.token.

Em Trigger Behavior diz quando a resposta vai ser reenviada, no meu caso, sempre que necessário.

Em Live Preview você observa como os dados estão chegando. Útil para ver qual a propriedade que precisamos para filtrar. Basta deixar apenas o $.


![image](https://user-images.githubusercontent.com/60934938/207662332-57ca5ba1-2f1d-41d9-925c-df395909ed2d.png)


Pronto! Agora nas minhas requisições, posso colocar a variável de ambiente token e sempre que eu fizer login, o token vai ser aplicado automaticamente. Isso evita que eu precise copiar o token depois de fazer o login, ir nas variáveis de ambiente e substituir o token antigo pelo novo.

![image](https://user-images.githubusercontent.com/60934938/207662407-ad66b78b-8b0f-4cf6-baad-d8dc00e33fea.png)

![image](https://user-images.githubusercontent.com/60934938/207662449-4486b7df-cf40-4575-ba58-1830dfb2054e.png)


<a href="https://marciofrancalima.com.br/blog/como-adicionar-token-autom%C3%A1tico-na-vari%C3%A1vel-de-ambiente-usando-insomnia/">Mias informações</a>

# Como fazer documenção de api

<a href="https://github.com/jeovanedossantossantos/desafio-chefao/tree/main/documentacao">Tutorial</a>

# Variaveis no Insomina

- [x] <a href="https://medium.com/@felipeb4c/como-agilizar-as-requests-usando-postman-e-insomnia-com-o-uso-de-vari%C3%A1veis-de-ambiente-d8016273a1b0">Variaveisno insomnia</a>

- [x] Abra o Insomnia(Avá?! É mesmo?).
- [x] Com ele aberto vá até a sua Collection.

![image](https://user-images.githubusercontent.com/60934938/221416960-90f0a55f-a20d-483f-bf4f-5321c477a65b.png)

- [x] Vá até ‘No Environment’ e clique em Manage Environments.

![image](https://user-images.githubusercontent.com/60934938/221417001-143c2397-af9a-47e6-8cde-3e686f14e53e.png)

- [x] Irá aparecer uma tela escrito Base Environments e nele você pode criar as suas variáveis. Você pode criar quantas variáveis quiser e armazenar os valores que desejar, desde que siga um regra, a estrutura tem que ser em JSON. Veja o exemplo:

![image](https://user-images.githubusercontent.com/60934938/221417022-83a166d1-37f7-4a0d-ab6c-aa0df4c836c0.png)

- [x] E agora, como usa? Bom é bem simples, basta você escrever o nome da variável que você criou e apertar Ctrl + Espaço. Ou simplesmente não escrever nada, apertar Ctrl + Espaço e ele mostrará todas as variáveis que você tem disponível. Vejá como aparece:

![image](https://user-images.githubusercontent.com/60934938/221417042-53bb5ff0-55a4-48be-80c6-45c5975c866d.png)

- [x] No final você vai ter algo parecido com isso:

![image](https://user-images.githubusercontent.com/60934938/221417072-57aea4c5-ce14-43df-a481-a9f29ff123a5.png)


