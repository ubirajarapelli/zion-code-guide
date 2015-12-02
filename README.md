# Ziontics Code Guide
Guia de código para os desenvolvedores da Zion TICs. - [www.ziontics.com.br](http://www.zionsoftware.com.br/site/)

> Se você trabalha com uma equipe, o código escrito precisa parecer que foi produzido por uma pessoa.
> _- Diego Eis_

Este guia tem como objetivo padronizar a escrita e a produção de códigos entre os desenvolvedores da Zion TICs, com o intuito de melhorar a qualidade na produção de código, aumentando a produtividade, assim refletindo na entrega dos projetos.

Este documento é um documento "vivo", assim em constante atualização, e tais atualizacões devem ser feitas por os desenvolvedores participantes e sua leitura e contribuição são fortemente recomendadas para uma melhora colaborativa.

## Primeiros passos

### Padronização 
Utilize esse [`.editorconfig`](/.editorconfig) em todos os projetos da Zion TICs. 

> O EditorConfig ajuda desenvolvedores a definir e manter estilos de códigos consistentes entre diferentes editores e IDEs. 

**Como funciona:** Baixe e instale o plugin do EditorConfig em seu editor ou IDE, e coloque o arquivo _.editorconfig_ na pasta raiz do projeto.

Mais informações acesse o site do [EditorConfig](http://editorconfig.org/)

### HTML

#### DOCTYPE
Utilizamos a instrução para a versão em HTML5.

```
<!DOCTYPE html>
<html>
	<head></head>
	<body></body>
</html>
```

#### Language
Não esqueça de definir o idioma, comumente utilizamos `lang="pt-br"`.

```
<html lang="pt-br">
```
> Para encontrar a listagem de códigos das linguagens, acesse a [documentação oficial do W3C](http://www.w3.org/International/questions/qa-choosing-language-tags).

#### Encoding
Utilizamos o UTF-8 como padrão da tabela Unicode de caracteres.

```
<head>
  <meta charset="UTF-8">
</head>
```

#### Sintaxe do Markup
- **Identação:** 2 espaços (Soft-tabs), relaxa, o `.editorconfig` está aí pra fazer isso por nós.
- **Atributos:** Sempre utlize aspas duplas `""`, nunca utilize aspas simples.
- **Elementos viúvos:** Não inclua barra invertida em elemntos _self-closed_ `<hr>`, `<br>`.

```
<!DOCTYPE html>
<html lang="pt-br">
  <head>
  	<meta charset="UTF-8">
    <title>Page title</title>
  </head>
  <body>
    <h1 class="hello-world">Hello, world!</h1>
    <img src="images/company-logo.png" alt="Company">
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.<br> Praesent sed enim sed velit ultricies interdum. <br>Suspendisse eget magna lorem. In congue ipsum quis egestas commodo. Nulla nisl ligula, iaculis a dapibus eget, porttitor eu diam.<br> Cras non nisl enim. Vestibulum eu libero commodo, mollis dolor luctus, elementum libero. </p>
  </body>
</html>
```
#### Insersão de CSS

Inserimos a tag `<link>` dentro `<head></head>` do documento.

 - O atributo `type` não precisa ser especificado, mas não esqueça do `rel="stylesheet"`.

```
<link rel="stylesheet" href="stylesheet.css">
```

#### Insersão de Javascript

Inserimos a tag `<script>` antes do fechamento da tag `</body>`.  

- O atributo `type` não precisa ser especificado.

```
	<script src="script.js"></script>
</body>
</html>
```
#### Ordem de declaração dos atributos

Seguimos esta ordem de declaração de atributos no markup, assim facilitando a compreensão.

 - `class`
 - `id`
 - `data-*`
 - `for`, `type`, ou `href`
 - `src`, `for`, `type`, `href`
 - `title`, `alt`
 - `aria-*`, `role`

