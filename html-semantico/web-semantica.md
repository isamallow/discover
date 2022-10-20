# Web Semântica

## O que é?
- Adicionar significado à uma linguagem
- No caso do HTML, para dar significado ao conteúdo

## Web Semântica

- Cada site é único, entretanto, existe padrões ou convenções, que nós identificamos intecionalmente ou não intencionalmente.

- Exemplo: identifica logo, cabeçalho, conteúdo, etc.

- Ao usar uma marcação semântica consistente, para identificar corretamente os elementos a apresentá-los aos visitantes da página.

- Isso se torna extremamente relevante para acessibilidade, ou seja, para visitantes que precisam usar leitores de página, por exemplo. Com uma página desorganizada, fica complexo para o visitante com necessidades especiais, fazer um bom uso da nossa página.

- Além disso, os motores de busca dão preferência para sistes que estão com sua semântica em dia. Um site bem estruturado e e organizado é um site melhor encontrado na web.

# HTML5 Semântico

# As tags

- Elas que irão ajudar a criar um HTML semântico, pois algumas tags tem significados específicos e orientações claras sobre onde devem ficar na página e o motivo dela existir.

- blockquote = um bloco citação e depois tag <cite> e coloca quem está citando

# Seções comuns em documentos HTML

- cabeçallho <header>
- navegação <nav>
- conteúdo principal <main>
- barra lateral <aside>
- rodapé <footer>

## Header

- <header></header>

### Onde utilizar?

- quando no início da página é visto como global
- Pode ser usado em outros elementos semânticos como article, section.
- múltiplos headers
- não possui atributos específicos
- não pode colocar header dentro de outro header, nem usar dentro do footer

## Nav

- Seção da página que vai apontar pra outra página
- Não necessariamente todos os links da páginas estarão só no nav
- Pode ter mais de um nav na página
- Não possuem atributos específicos, somente os globais

## Main

- A tag main é para um conteúdo único da sua página, portanto, você vai utilizá-la apenas uma vez por página, e vai ser colocada direto do body, e não é legal deixar em qualquer outro lugar além de logo depois do body, entendemos a tag main como o foco central da página, o conteúdo principal da aplicação, então geralmente dentro dessa tag, não vamos deixar o nosso menu.


## Article

- a tag article vai criar blocos de conteúdo que estejam relacionados
- composição independente do documento
- não possui atributos específicos apenas os globais

## Aside

- A tag aside é para conteúdos levemente relacionados ao conteúdo principal, como explicações do conteúdo, glossários, links extras, biografia do autor, informações de perfil e etc.
- atributos apenas globais

## Footer

- rodapé da página
- fica no final da página e vai geralmente ter informações do autor da página, copyright, contato, sitemap, voltar ao topo, etc
- atributos apenas globais

## Section

- seções na página
- coloca um título e depois o conteúdo
- pode ser usada dentro de um article
- não possui atributos específicos, somente os globais

## Elementos genéricos, não semânticos

- em ambos se usa atributos globais como id e class para entregar maior significado
- o span é usado quando não se acha um elemento de texto semântico 
- div se usa quando não se acha um elemento de bloco semântico