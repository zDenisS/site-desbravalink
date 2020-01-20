Guia de estilo HTML5 e convenções de codificação
Convenções de codificação HTML
Os desenvolvedores da Web geralmente não sabem o estilo e a sintaxe de codificação a serem usados ​​no HTML.

Entre 2000 e 2010, muitos desenvolvedores da Web foram convertidos de HTML para XHTML.

Com o XHTML, os desenvolvedores foram forçados a escrever um código válido e "bem formado".

O HTML5 é um pouco mais desleixado quando se trata de validação de código.

Seja inteligente e à prova do futuro
Um uso consistente do estilo facilita a compreensão do HTML por outras pessoas.

No futuro, programas como leitores de XML podem querer ler seu HTML.

Usar uma sintaxe bem formada - "próxima ao XHTML" pode ser inteligente.

Sempre mantenha seu código organizado, limpo e bem formado.

Usar tipo de documento correto
Sempre declare o tipo de documento como a primeira linha do seu documento:

<!DOCTYPE html>
Se você deseja consistência com as letras minúsculas, pode usar:

<!doctype html>
Usar nomes de elementos em minúsculas
O HTML5 permite misturar letras maiúsculas e minúsculas nos nomes dos elementos.

Recomendamos o uso de nomes de elementos em minúsculas, porque:

Misturar nomes em maiúsculas e minúsculas é ruim
Os desenvolvedores normalmente usam nomes em minúsculas (como em XHTML)
Limpador de aspeto minúsculo
Minúsculas são mais fáceis de escrever
Mau:
<SECTION>
  <p>This is a paragraph.</p>
</SECTION>
Muito mal:
<Section>
  <p>This is a paragraph.</p>
</SECTION>
Boa:
<section>
  <p>This is a paragraph.</p>
</section>

Fechar todos os elementos HTML
No HTML5, você não precisa fechar todos os elementos (por exemplo, o <p>elemento).

Recomendamos fechar todos os elementos HTML.

Mau:
<section>
  <p>This is a paragraph.
  <p>This is a paragraph.
</section>
Boa:
<section>
  <p>This is a paragraph.</p>
  <p>This is a paragraph.</p>
</section>
Fechar elementos HTML vazios
No HTML5, é opcional fechar elementos vazios.

Permitido:
<meta charset="utf-8">
Também permitido:
<meta charset="utf-8" />
No entanto, a barra de fechamento (/) é NECESSÁRIA em XHTML e XML.

Se você espera que o software XML acesse sua página, é uma boa ideia manter a barra final!

Usar nomes de atributo em minúsculas
O HTML5 permite misturar letras maiúsculas e minúsculas nos nomes dos atributos.

Recomendamos o uso de nomes de atributo em minúsculas porque:

Misturar nomes em maiúsculas e minúsculas é ruim
Os desenvolvedores normalmente usam nomes em minúsculas (como em XHTML)
Limpador de aspeto minúsculo
Minúsculas são mais fáceis de escrever
Mau:
<div CLASS="menu">
Boa:
<div class="menu">
Citar valores de atributo
O HTML5 permite valores de atributos sem aspas.

Recomendamos citar valores de atributo porque:

Os desenvolvedores normalmente citam valores de atributo (como em XHTML)
Os valores citados são mais fáceis de ler
Você DEVE usar aspas se o valor contiver espaços
Muito mal:
Isso não funcionará, porque o valor contém espaços:

<table class=table striped>
Mau:
<table class=striped>
Boa:
<table class="striped">
Atributos da imagem
Sempre adicione o altatributo às imagens. Este atributo é importante quando a imagem, por algum motivo, não pode ser exibida. Além disso, sempre defina a largura e a altura da imagem. Reduz a tremulação porque o navegador pode reservar espaço para a imagem antes do carregamento.

Mau:
<img src="html5.gif">
Boa:
<img src="html5.gif" alt="HTML5" style="width:128px;height:128px">
Espaços e sinais de igualdade
O HTML5 permite espaços em torno de sinais de igual. Mas sem espaço é mais fácil de ler e agrupa melhor as entidades.

Mau:
<link rel = "stylesheet" href = "styles.css">
Boa:
<link rel="stylesheet" href="styles.css">
Evitar linhas de código longas
Ao usar um editor de HTML, é inconveniente rolar para a direita e para a esquerda para ler o código HTML.

Tente evitar linhas de código com mais de 80 caracteres.

Linhas em branco e recuo
Não adicione linhas em branco sem um motivo.

Para facilitar a leitura, adicione linhas em branco para separar blocos de códigos grandes ou lógicos.

Para facilitar a leitura, adicione dois espaços de recuo. Não use a tecla tab.

Não use linhas em branco e recuos desnecessários. Não é necessário recuar cada elemento:

Desnecessário:
<body>

  <h1>Famous Cities</h1>

  <h2>Tokyo</h2>

  <p>
    Tokyo is the capital of Japan, the center of the Greater Tokyo Area,
    and the most populous metropolitan area in the world.
    It is the seat of the Japanese government and the Imperial Palace,
    and the home of the Japanese Imperial Family.
  </p>

</body>
Melhor:
<body>

<h1>Famous Cities</h1>

<h2>Tokyo</h2>
<p>Tokyo is the capital of Japan, the center of the Greater Tokyo Area,
and the most populous metropolitan area in the world.
It is the seat of the Japanese government and the Imperial Palace,
and the home of the Japanese Imperial Family.</p>

</body>
Exemplo de tabela:
<table>
  <tr>
    <th>Name</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>A</td>
    <td>Description of A</td>
  </tr>
  <tr>
    <td>B</td>
    <td>Description of B</td>
  </tr>
</table>
Exemplo de lista:
<ul>
  <li>London</li>
  <li>Paris</li>
  <li>Tokyo</li>
</ul>
Omitindo <html> e <body>?
No HTML5, a <html>tag e a <body>tag podem ser omitidas.

O código a seguir será validado como HTML5:

Exemplo
<!DOCTYPE html>
<head>
  <title>Page Title</title>
</head>

<h1>This is a heading</h1>
<p>This is a paragraph.</p>
No entanto, não recomendamos omitir <html>a <body>tag e.

O <html>elemento é a raiz do documento. É o local recomendado para especificar o idioma da página:

<!DOCTYPE html>
<html lang="en-US">
A declaração de um idioma é importante para aplicativos de acessibilidade (leitores de tela) e mecanismos de pesquisa.

Omitir <html>ou <body>pode travar o software DOM e XML.

A omissão <body>pode produzir erros em navegadores mais antigos (IE9).

Omitindo <head>?
No HTML5, a tag <head> também pode ser omitida.

Por padrão, os navegadores adicionam todos os elementos anteriores <body>a um <head> elemento padrão .

Você pode reduzir a complexidade do HTML, omitindo a <head>tag:

Exemplo
<!DOCTYPE html>
<html>
<title>Page Title</title>

<body>
  <h1>This is a heading</h1>
  <p>This is a paragraph.</p>
</body>

</html>
No entanto, não recomendamos omitir a <head>tag.

A omissão de tags não é familiar para desenvolvedores da web. Ele precisa de tempo para ser estabelecido como uma diretriz.

Meta Data
O <title>elemento é necessário no HTML5. Torne o título o mais significativo possível:

<title>HTML5 Syntax and Coding Style</title>
Para garantir a interpretação adequada e a indexação correta do mecanismo de pesquisa, o idioma e a codificação de caracteres devem ser definidos o mais cedo possível em um documento:

<!DOCTYPE html>
<html lang="en-US">
<head>
  <meta charset="UTF-8">
  <title>HTML5 Syntax and Coding Style</title>
</head>
Definindo a janela de exibição
O HTML5 introduziu um método para permitir que os web designers assumam o controle sobre a janela de exibição, por meio da <meta>tag.

A janela de visualização é a área visível do usuário de uma página da web. Varia de acordo com o dispositivo e será menor em um telefone celular do que na tela do computador.

Você deve incluir o seguinte <meta>elemento de janela de visualização em todas as suas páginas da web:

<meta name="viewport" content="width=device-width, initial-scale=1.0">
Um <meta>elemento de janela de visualização fornece instruções ao navegador sobre como controlar as dimensões e a escala da página.

A parte width = width do dispositivo define a largura da página para seguir a largura da tela do dispositivo (que variará dependendo do dispositivo).

A parte inicial-scale = 1.0 define o nível de zoom inicial quando a página é carregada pela primeira vez pelo navegador.

Aqui está um exemplo de uma página da web sem a meta tag da viewport e a mesma página da web com a meta tag da viewport:

Dica: Se você estiver navegando nesta página com um telefone ou tablet, poderá clicar nos dois links abaixo para ver a diferença.




Sem a metatag da viewport



Com a metatag da viewport

Comentários em HTML
Comentários breves devem ser escritos em uma linha, assim:

<!-- This is a comment -->
Comentários que abrangem mais de uma linha devem ser escritos assim:

<!--
  This is a long comment example. This is a long comment example.
  This is a long comment example. This is a long comment example.
-->
Comentários longos são mais fáceis de observar se forem recuados em dois espaços.

Folhas de estilo
Use uma sintaxe simples para vincular a folhas de estilo (o atributo type não é necessário):

<link rel="stylesheet" href="styles.css">
Regras curtas podem ser escritas compactadas, assim:

p.intro {font-family: Verdana; font-size: 16em;}
Regras longas devem ser escritas em várias linhas:

body {
  background-color: lightgrey;
  font-family: "Arial Black", Helvetica, sans-serif;
  font-size: 16em;
  color: black;
}
Coloque o suporte de abertura na mesma linha do seletor
Use um espaço antes do suporte de abertura
Use dois espaços de recuo
Use ponto e vírgula após cada par de valor de propriedade, incluindo o último
Use aspas somente em valores se o valor contiver espaços
Coloque o suporte de fechamento em uma nova linha, sem espaços à esquerda
Evite linhas com mais de 80 caracteres
Carregando JavaScript em HTML
Use uma sintaxe simples para carregar scripts externos (o atributo type não é necessário):

<script src="myscript.js">
Acessando elementos HTML com JavaScript
Uma conseqüência do uso de estilos HTML "desarrumados" pode resultar em erros de JavaScript.

Essas duas instruções JavaScript produzirão resultados diferentes:

Exemplo
var obj = getElementById("Demo")

var obj = getElementById("demo")
Visite o Guia de estilos JavaScript .

Usar nomes de arquivo em letras minúsculas
Alguns servidores da Web (Apache, Unix) diferenciam maiúsculas de minúsculas dos nomes de arquivos: "london.jpg" não pode ser acessado como "London.jpg".

Outros servidores da Web (Microsoft, IIS) não diferenciam maiúsculas de minúsculas: "london.jpg" pode ser acessado como "London.jpg" ou "london.jpg".

Se você usa uma combinação de letras maiúsculas e minúsculas, precisa ser extremamente consistente.

Se você mudar de um servidor que não diferencia maiúsculas de minúsculas para um servidor que diferencia maiúsculas de minúsculas, até pequenos erros irão quebrar sua web!

Para evitar esses problemas, sempre use nomes de arquivos em letras minúsculas.

Extensões de arquivo
Os arquivos HTML devem ter uma extensão .html ou .htm .

Os arquivos CSS devem ter uma extensão .css .

Os arquivos JavaScript devem ter uma extensão .js .

Diferenças entre .htm e .html
Não há diferença entre as extensões .htm e .html. Ambos serão tratados como HTML por qualquer navegador ou servidor da web.

As diferenças são culturais:

.htm "cheira" a sistemas DOS antigos, nos quais o sistema limitava as extensões a 3 caracteres.

.html "cheira" a sistemas operacionais Unix que não tinham essa limitação.

Diferenças técnicas
Quando um URL não especifica um nome de arquivo (como https://www.w3schools.com/css/), o servidor retorna um nome de arquivo padrão. Os nomes de arquivos padrão comuns são index.html, index.htm, default.html e default.htm.

Se o seu servidor estiver configurado apenas com "index.html" como nome de arquivo padrão, seu arquivo deverá ser nomeado "index.html", não "index.htm".

No entanto, os servidores podem ser configurados com mais de um nome de arquivo padrão e, normalmente, você pode configurar quantos nomes de arquivos padrão forem necessários.

De qualquer forma, a extensão completa dos arquivos HTML é .html, e não há motivo para não ser usada.
