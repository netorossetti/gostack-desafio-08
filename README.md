# gostack-desafio-08
Fundamentos React-Native

<h2><a id="user-content-rocket-sobre-o-desafio" class="anchor" aria-hidden="true" href="#rocket-sobre-o-desafio"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a><g-emoji class="g-emoji" alias="rocket" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/1f680.png">🚀</g-emoji> Sobre o desafio</h2>
<p>Nesse desafio, você desenvolverá uma nova aplicação, a GoMarketplace. Dessa vez é hora de você praticar o que você aprendeu até agora no React Native junto com o TypeScript, utilizando rotas, Async Storage e a Context API.</p>
<h3><a id="user-content-template-da-aplicação" class="anchor" aria-hidden="true" href="#template-da-aplicação"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Template da aplicação</h3>
<p>Para te ajudar nesse desafio, criamos para você um modelo que você deve utilizar como um template do Github.</p>
<p>O template está disponível na seguinte url: <strong><a href="https://github.com/Rocketseat/gostack-template-fundamentos-react-native">Acessar Template</a></strong></p>
<p><strong>Dica</strong>: Caso não saiba utilizar repositórios do Github como template, temos um guia em <strong><a href="https://github.com/Rocketseat/bootcamp-gostack-desafios/tree/master/faq-desafios">nosso FAQ</a>.</strong></p>
<p>Agora navegue até a pasta criada e abra no Visual Studio Code, lembre-se de executar o comando <code>yarn</code> no seu terminal para instalar todas as dependências.</p>
<h3><a id="user-content-utilizando-uma-fake-api" class="anchor" aria-hidden="true" href="#utilizando-uma-fake-api"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Utilizando uma fake API</h3>
<p>Antes de tudo, para que você tenha os dados para exibir em tela, criamos um arquivo que você poderá utilizar como fake API para te prover esses dados.</p>
<p>Para isso, deixamos instalado no seu package.json uma dependência chamada <code>json-server</code>, e um arquivo chamado <code>server.json</code> que contém os dados para uma rota <code>/products</code>. Para executar esse servidor você pode executar o seguinte comando:</p>
<div class="highlight highlight-source-js position-relative" data-snippet-clipboard-copy-content="  yarn json-server server.json -p 3333
"><pre>  <span class="pl-s1">yarn</span> <span class="pl-s1">json</span><span class="pl-c1">-</span><span class="pl-s1">server</span> <span class="pl-s1">server</span><span class="pl-kos">.</span><span class="pl-c1">json</span> <span class="pl-c1">-</span><span class="pl-s1">p</span> <span class="pl-c1">3333</span></pre></div>
<h3><a id="user-content-layout-da-aplicação" class="anchor" aria-hidden="true" href="#layout-da-aplicação"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Layout da aplicação</h3>
<p>Essa aplicação possui um layout que você pode seguir para conseguir visualizar o seu funcionamento.</p>
<p>O layout pode ser acessado através da página do Figma, no <a href="https://www.figma.com/file/VgK3hsmyGbqiGu9FdqfUzF/GoMarketplace?node-id=0%3A1" rel="nofollow">seguinte link</a>.</p>
<p>Você precisará de uma conta (gratuita) no Figma pra inspecionar o layout e obter detalhes de cores, tamanhos, etc.</p>
<h3><a id="user-content-funcionalidades-da-aplicação" class="anchor" aria-hidden="true" href="#funcionalidades-da-aplicação"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Funcionalidades da aplicação</h3>
<p>Agora que você já está com o template clonado e pronto para continuar, você deve verificar os arquivos da pasta <code>src</code> e completar onde não possui código, com o código para atingir os objetivos de cada rota.</p>
<ul>
<li><strong><code>Listar os produtos da fake API</code></strong>: Sua página <code>Dashboard</code> deve ser capaz de exibir uma listagem através de uma tabela, com os campos <code>title</code>, <code>image_url</code> e <code>price</code>.</li>
</ul>
<p><strong>Dica</strong>: Você pode utilizar a função <a href="https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/NumberFormat" rel="nofollow">Intl</a> para formatar os valores. Dentro da pasta <code>utils</code> no template você encontrará um código para te ajudar.</p>
<ul>
<li><strong><code>Adicionar itens ao carrinho</code></strong>: Em toda sua aplicação, você deve utilizar o Contexto chamado <code>cart</code> que deixamos disponível. Você vai precisar completar as funcionalidades dentro de <code>hooks/cart.tsx</code> para que você consiga adicionar itens ao carrinho.</li>
</ul>
<p><strong>Dica</strong>: No seu contexto de carrinho, utilize uma propriedade chamada <code>quantity</code> para controlar quantos desse item existem no seu carrinho.</p>
<p><strong>Dica 2</strong>: Caso um produto que você está adicionando já exista no carrinho, apenas altere a quantidade dele no seu contexto para evitar itens duplicados.</p>
<ul>
<li>
<p><strong><code>Exibir itens do carrinho</code></strong>: Na página <code>Cart</code> você deve exibir todos os itens do carrinho, junto com a quantidade, valor único, valor subtotal dos itens e total de todos os items.</p>
</li>
<li>
<p><strong><code>Aumentar quantidade de itens do carrinho</code></strong>: Na página <code>Cart</code> você deve permitir que o usuário aumente a quantidade de itens do mesmo produto, para isso você pode utilizar a função <code>increment</code> dentro do seu contexto em <code>/src/hooks/cart.tsx</code>.</p>
</li>
<li>
<p><strong><code>Diminuir quantidade de um item do carrinho</code></strong>: Na página <code>Cart</code> você deve permitir que o usuário decremente a quantidade de itens do mesmo produto, para isso você pode utilizar a função <code>decrement</code> dentro do seu contexto em <code>/src/hooks/cart.tsx</code>.</p>
</li>
<li>
<p><strong><code>Exibir valor total dos itens no carrinho</code></strong>: Tanto na página <code>Dashboard</code>, quanto na página <code>Cart</code> você deve exibir o valor total de todos os itens que estão no seu carrinho.</p>
</li>
</ul>
<h3><a id="user-content-específicação-dos-testes" class="anchor" aria-hidden="true" href="#específicação-dos-testes"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.775 3.275a.75.75 0 001.06 1.06l1.25-1.25a2 2 0 112.83 2.83l-2.5 2.5a2 2 0 01-2.83 0 .75.75 0 00-1.06 1.06 3.5 3.5 0 004.95 0l2.5-2.5a3.5 3.5 0 00-4.95-4.95l-1.25 1.25zm-4.69 9.64a2 2 0 010-2.83l2.5-2.5a2 2 0 012.83 0 .75.75 0 001.06-1.06 3.5 3.5 0 00-4.95 0l-2.5 2.5a3.5 3.5 0 004.95 4.95l1.25-1.25a.75.75 0 00-1.06-1.06l-1.25 1.25a2 2 0 01-2.83 0z"></path></svg></a>Específicação dos testes</h3>
<p>Em cada teste, tem uma breve descrição do que sua aplicação deve cumprir para que o teste passe.</p>
<p>Caso você tenha dúvidas quanto ao que são os testes, e como interpretá-los, dé uma olhada em <strong><a href="https://github.com/Rocketseat/bootcamp-gostack-desafios/tree/master/faq-desafios">nosso FAQ</a>.</strong></p>
<p>Para esse desafio, temos os seguintes testes:</p>
<ul>
<li>
<p><strong><code>should be able to list the products</code></strong>: Para que esse teste passe, sua aplicação deve permitir que sejam listados na sua tela <code>Dashboard</code>, todos os produtos que são retornadas do Fake API. Essa listagem deve exibir o <code>title</code> e o <code>price</code> que deve ser formatado utilizando a função <code>Intl</code>.</p>
</li>
<li>
<p><strong><code>should be able to add a product to the cart</code></strong>: Para que esse teste passe, você deve permitir que seja possível adicionar produtos da sua <code>Dashboard</code> ao carrinho, utilizando o contexto de <code>cart</code> disponibilizado.</p>
</li>
<li>
<p><strong><code>should be able to list the products on the cart</code></strong>: Para que esse teste passe, você deve permitir que seja possível listar os produtos que estão salvos no contexto do seu carrinho na página <code>Cart</code>, nessa página exiba o nome do produto e o subtotal total de cada produto (price * quantity).</p>
</li>
<li>
<p><strong><code>should be able to calculate the cart total</code></strong>: Para que esse teste passe, tanto na página <code>Dashboard</code>, tanto na página <code>Cart</code> você deve exibir o valor total de todos os itens que estão no seu carrinho.</p>
</li>
</ul>
<p><strong>Dica</strong>: Para calcular o total de todos os itens, você pode utilizar o <a href="https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Array/reduce" rel="nofollow">reduce</a> para somar todos os valores e retornar o valor total.</p>
<ul>
<li><strong><code>should be able to show the total quantity of itens in the cart</code></strong>: Para que esse teste passe, tanto na página <code>Dashboard</code>, tanto na página <code>Cart</code> você deve exibir o número total de itens que estão no seu carrinho.</li>
</ul>
<p><strong>Dica</strong>: Para calcular o total de todos os itens, você pode utilizar o <a href="https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Array/reduce" rel="nofollow">reduce</a> para somar todos os valores e retornar o valor total.</p>
<p><strong>Dica 2</strong>: Utilize o useMemo para armazenar o valor total do carrinho que você calculou.</p>
<ul>
<li>
<p><strong><code>should be able to increment product quantity on the cart</code></strong>: Para que esse teste passe, você deve permitir que seja possível incrementar a quantidade de um produto do seu carrinho, utilizando o contexto de <code>cart</code> disponibilizado.</p>
</li>
<li>
<p><strong><code>should be able to decrement product quantity on the cart</code></strong>: Para que esse teste passe, você deve permitir que seja possível decrementar a quantidade de um produto do seu carrinho, utilizando o contexto de <code>cart</code> disponibilizado.</p>
</li>
</ul>
<p><strong>Dica</strong>: Ao decrementar a quantidade de um produto, não permita que ele seja decrementado para um valor negativo, sendo a quantidade mínima 1 para estar no carrinho.</p>
<ul>
<li>
<p><strong><code>should be able to navigate to the cart</code></strong>: Para que esse teste passe, no seu componente <code>FloatingCart</code> na Dashboard, você deve permitir que ao clicar no botão de carrinho com o testID de <code>navigate-to-cart-button</code>, o usuário seja redirecionado para a página <code>Cart</code>.</p>
</li>
<li>
<p><strong><code>should be able to add products to the cart</code></strong>: Para que esse teste passe, no seu arquivo onde contém o contexto do carrinho, você deve permitir que a função <code>addToCart</code> adicione um novo item ao carrinho.</p>
</li>
<li>
<p><strong><code>should be able to increment quantity</code></strong>: Para que esse teste passe, no seu arquivo onde contém o contexto do carrinho, você deve permitir que a função <code>increment</code> incremente em <code>1</code> unidade a quantidade de um item que está armazenado no contexto.</p>
</li>
<li>
<p><strong><code>should be able to decrement quantity</code></strong>: Para que esse teste passe, no seu arquivo onde contém o contexto do carrinho, você deve permitir que a função <code>decrement</code> decremente em <code>1</code> unidade a quantidade de um item que está armazenado no contexto.</p>
</li>
<li>
<p><strong><code>should store products in AsyncStorage while adding, incrementing and decrementing</code></strong>: Para que esse teste passe, no seu arquivo onde contém o contexto do carrinho você deve permitir que todas as atualizações que você fizer no carrinho, sejam salvas no AsyncStorage. Por exemplo, ao adicionar um item ao carrinho, adicione-o também no AsyncStorage. Lembre de também atualizar o valor do AsyncStorage quando você incrementar ou decrementar a quantidade de um item.</p>
</li>
<li>
<p><strong><code>should load products from AsyncStorage</code></strong>: Para que esse teste passe, no seu arquivo onde contém o contexto do carrinho, você deve permitir que todos os produtos que foram adicionados sejam buscados do AsyncStorage.</p>
</li>
</ul>
