# Formulários

### Para que serve?

* capturar dados de entrada (input)
* interação
* controle

### Pré-requisitos

* básico HTML

### Dominar

* estilização
* validação
* controles customizados
* javascript

### <form>

* elemento que definirá um formulário
* é cum container estilo <section> e <footer>

#### Atributos básicos

* action (pra onde o formulário será submetido)
* method (o método: POST ou GET)


`Obs: não pode criar um form dentro de outro form`

### <fieldset>

* agrupamento de campos que tenham o mesmo propósito
* semântico
* acessibilidade

#### Atributos especiais

* disable
    - desabilita todos os elementos internos
    - não serão enviados ao submeter o formulário
* form
    - o id de um formulário ao qual esse fieldset pertence
    - não precisa estar dentro do formulário
* name
    - nome do grupo do fieldset

<legend>    
    - nome do agrupamento que aparece na tela
    - primeiro elemento dentro do fieldset

```html
    <form id="contato" action="" name="input-contact">
      <button>Enviar</button>
      </form>

      <fieldset form="contato"> 
      <legend> Contato </legend>
      <label for="">Nome</label>
      <input type="text">
      </fieldset>
   ```
      
#### <label>

* associar e identificar uma (ou mais) tags de entrada de dados
* acessibilidade
* você poderá clicar para mudar o foco de entrada de dados

##### Atributos

- for
  - para fazer a conexão entre a label e a tag de entrada de dados
  - é feita via id do input
  - só funciona com elementos específicos
     - button, input (not hidden), meter, output, progress, select, textarea

     ```html
     <label for="nome">
      Nome:
      </label>
       <input id="nome type="text">
       ```
### <button>

* representa um botão
* usado para enviar formulários
* é estilizado pelo user agent (navegador)

#### Atributos comuns

- type
    - submit
    - reset
    - button
- autofocus
- disabled
- name
- value
- form

### Datalist

* lista de valores como sugestão a uma tag <input>
* valores sugestivos e não obrigatórios
* usuários poderão selecionar um dos valores, ou colocar um valor diferente da sugestão

```html
<input type="text" 
list="fruitdata"
placeholder="Escolha uma fruta" />
>
<datalist id="fruitdata">
  <option>apple</option>
  <option>banana</option>
  <option>mango</option>
  <option>orange</option>
  <option>cherry</option>
  </datalist>
  ```

#### list

* um atributo que recebe como valor o id de um <datalist> residente no mesmo documento

#### Tipos de input suportados

* text, search, url, tel, email, date, month, week, time, datetime-local, number, range e color

* valores de datalist que não são compatíveis com o tipo do <input> não apresentados

#### Tipos de input não suportados (conforme especificação)

* hidden, password, checkbox, radio, file, ou qualquer tipo de button

`Verificar a compatibilidade com o browser!`

### <input>

* um dos mais usados em formulários
* aceita os mais diversos tipos de dados
* um dos mais poderosos e complexos
* elevado número de combinações

#### Atributos

* type
* name
* id

#### Atributos comuns

* autocomplete = busca dado que você usou com frequência
* autofocus = atributo boolean, somente um input pode receber esse atributo
* disabled = desabilita o input
* readonly = aspecto diferente do disabled (quase todos)
* value
* name
* form = interliga ao formulário (quase todos)
* required (quase todos) = o input se torna obrigatório
* placeholder (password, search, tel, text, url)

`Obs: não trocar o label pelo placeholder`


### <input type="password">

* colocar uma senha de maneira segura
* esconde o que está sendo digitado no campo
* o estilo da apresentação do campo, depende do user agent

#### Atributos

- minlenght / maxlenght
    * o número mínimo e/ou máximo de caracteres para este campo
- size
    * o número aceitável de caracteres que esse campo deverá conter
- pattern
    * expressão regular para validar o que está sendo digitado no campo
    * altamente recomendado o uso de um padrão de segurança alta de senhas
    * exemplo: queremos que a senha contenha caracteres hexadecimais com o limite mínimo de 4 e no máximo 8 caracteres
        * pattern="[0-9a-fA-F]{4, 8}"    
- title = ajuda na acessibilidade
- placeholder 
    * mostra um exemplo de texto a ser digitado no campo
- readonly / disabled
    * atributo booleano indicando se o campo está habilitado ou não
- required
    * o campo será obrigatório
- inputmode
    * poderá alterar o uso do teclado em smartphones
    * exemplo: queremos que o cliente só adicione números
        * inputmode="numeric"
- autocomplete
    * on: permite a sugestão de: new-password ou current-password
    * off: desabilita a opção de autocompletar
    * new-password: o navegador poderá sugerir uma nova senha

### <input type="email">

* espera que o usuário digite um email
* irá validar se o valor digitado é um email

#### Atributos

- placeholder
- readonly / disabled
- value
- required
- multiple
    * o campo iriá receber 1 ou mais emails, separado por vírgulas
* minlenght / maxlenght
    * o mínimo e/ou máximo valor que o campo irá conter
* size
    * valor numérico indicando quantos caracteres esse campo deveria conter, modificando o tamanho para o usuário
- pattern
    * uso de expressão regular para validar o campo
    * exemplo: o usuário só poderá colocar email do domínio rocketseat.com.br
        * pattern="[.+@rocketseat\.com\.br]"
- list
    * o id de uma tag <datalist> que está no mesmo documento
    * <datalist> irá conter uma lista de valores pré-definidos a fim de sugerir ao usuário, quais valores estão disponíveis
        * os valores do <datalist> que não forem compatíveis com o campo, não serão apresentados como sugestão

### <input type="url">

* espera que o usuário digite uma url
* irá invalidar se o valor digitado é uma url

#### Atributos

- placeholder
- readonly / disabled
- value
- required
- minlenght / maxlenght
- size
- pattern
    * exemplo: o usuário só poderá colocar domínio .com.br
        * pattern="*\.com\.br\/.*"
- list
- spellcheck
    * habilitar a verificação ortográfica para este input


### <input type="file">

* usuário poderá escolher 1 ou mais arquivos para enviar no formulário

#### Atributos

- value
    * contém o arquivo a ser enviado
- accept
    * descreve que tipos de arquivos serão aceitos
    * exemplo: .doc, docx, .pdf, audio/*, image/png, .png
- files
    * a lista de arquivo ou arquivos
- multiple
    * permite o envio de múltiplos arquivos

#### Envio dos arquivos

Para o envio dos arquivos o formulário deverá utilizar o método POST e atributo enctype como "multipart/form-data".

### <input type="color">

* interface para selecionar a cor
* color picker

#### Atributos

- value: RGB
    * se inválido, a cor preta será exibida
- list

### <input type="checkbox">

* caixas que podem ser marcadas
* selecionar um valor para ser enviado
* se não selecionado, não será enviado nenhum dado

#### Atributos

- globais
- value
    * o valor que aquele campo contém
    * se não tiver presente, o padrão é 'on'
- checked
    * para deixar o campo marcado por padrão

#### Marcar múltiplos valores

- usaremos o atributo 'name' com o mesmo nome para os diversos campos

### <input type="hidden">

- invisível ao usuário
- será enviado com o formulário
- não receberá foco
- leitores de tela não percebem esse campo

```html
<input type="hidden" id="timestamp" name="timestamp" value="123456789">
```

### <input type="radio">

* projetado para selecionar uma única opção de um grupo de opções

#### Atributos essenciais

- checked
    * indica que o campo foi marcado
- value
    * valor que aquele campo contém

### <textarea>

* mais de uma linha
* útil para textos grandes

#### Atributos

- id
- name
- rows e cols
- maxlenght e minlenght
- wrap

`outros comuns aos <input>s`
` autocomplete, autofocus, disabled, placeholder, readonly, form, required`

### <select>

* contole que fornece menu de opções

#### <option>

* contém as opções a serem selecionadas
* atributos necessários: value

#### Atributos únicos

- multiple
    * habilita múltiplas opções
- size
    * quantidade de opções visíveis

#### <optgroup>

* agrupamento dos options dentro do <select>

### <input type="search">

* para campos de busca
* é igual ao campo do tipo 'text' mas poderá ser um pouco diferente dependendo do user agent

#### Atributos

- list / <datalist>
- pattern
    * exemplo pattern="[0-9]{2}"
- arial-label
    * quando não tem o label
  
### <input type="number">

* entrada de números

#### Atributos

- min/max
- step
    * pula números
- list

### <input type="range">

* controle para selecionar um valor numérico
* slider ou dial control

#### Atributos

- min/max
- step
- value

### Outros campos interessantes

* porém não tem um bom suporte
* https://caniuse.com

<input type="date">

<input type="datetime-local">

<input type="month">

<input type="time">

<input type="week">

### Desenhando formulários

* pensar nos requisitos
* ajuda a definr as necessidades

Dicas:
    * simples e focado
    * somente dados necessários
    * verifique o que te agrada