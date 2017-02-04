# Atualização de uma pagina simples para html5 e css3 avançado.

## Verificar as funcionalidades novas
> Entre no site "caniuse.com" e verifique se as funcionalidades que você queira implementar, se está disponível e/ou suporta em seu navegador padrão.


## Medidas relativas
 `rem` -> Usa o tamanho da fonte como base.
> 1,25rem = 1,25x tamanho da fonte.
Se a fonte do navegador for de 20px: 20px x 1,25 = 25px

 `ch` -> Usa a largura do caractere da fonte.
> 1ch = largura do caractere "zero" da fonte utilizada.

 `em` -> Usa o tamanho da fonte do pai como base.


## Position

`Relative` -> Usa a sí mesmo como posição.

`Absolute` -> Quebra o fluxo da pagína, e é sempre relativo ao primeiro pai dele que possuir um position definido. Senão definirmos para o pai, o filho estará posicionado em relação à tela do navegador.

`Fixed` -> Também quebra o fluxo da pagína, e como o nome seu diz ficará sempre fixo porém se referenciando a janela do navegador, diferente do absolute.

`Static` -> É o valor padrão de todos os elementos, grosseiramente seria dizer que o elemento com position - static não tem posição definida.


### Border-Radius
Implementado para colocar bordas arredondadas em elementos.
* A sintaxe é: `border-radius rx rx rx rx;`


## Transform
Está propriedade permite o controle da posição do elemento sem afetar o fluxo da pagína.
Seu uso é simples basta especificar o tipo de transformação.

* `transform: rotate(30deg)` -> Rotaciona em 30 graus.
* `transform: scale(1.5)` -> Aumenta sua escala x 1.5
* `transform: skew(20deg)` -> Entorta o elemento, fazendo crescer ou diminuir em 20 graus.
* `transform: translate(10px, 50px)` -> Faz um translado de 10 pixels para direita e 50 para cima.

* Para transformações em 3D é usado 3 eixos para definir o tamanho dos nossos objetos: X, Y e Z.
  * translatex - eixo X
  * translatey - eixo Y
  * translatez - profundidade
Também é necesário especificar a perspectiva `(perspective)` para definir a distancia que o usuário estaá da tela para que possamos fazer o cálculo de projeção do 3D. Outro pronto importante é a anfulação que o usuário está olhando, o que causa diferentes efeitos de perspectiva. Para lidar com essa diferença usamos a propriedade `perspective-origin`

##Gradientes
É possível criar efeitos visuais de gradientes utilizando a propriedade `background-image` passando como parâmetro `linear-gradient()`
Exemp: `background-image: linear-gradient(to bottom, red, black);` -> Cria um gradiente começando vermelho em cima indo em direção ao final "bottom" de cor preta.

Também é possível criar gradientes radiais:
`background-image: radial-gradient(yellow, red);`

## Seletores
* `~` -> `Depois` (Selecionando todos "Irmão")
Exemplo: li ~ li {margin-top 1em;}
Em uma lista de li's estamos apenas aplicando o margin-top apos o segundo li (elemento).

* `+` -> `Logo Depois` (Similar ao `~` mas seleciona imediatamente depois de outro elemento e não todos "Irmão Adjacente").

* `>` -> Pega o elemento pai e filho, deixando de lado ancestral de descendente.

## Pseudoclasses
É uma maneira melhor de selecionar elementos pela estrutura, as pseudoclasses são chamadas com os "`:`" (`dois pontos`):
  * `:odd`
  * `:even`

Na linguagem que estamos usando, generalizamos essas pseudoclasses com "`:nth-child()`". Dessa maneira, podemos estilizar não só as linhas pares ou ímpares:
  * `:nth-child(odd)` - linhas ímpares;
  * `:nth-child(even)` - linhas pares;
  * `:nth-child(3)` - terceira linha;
  * `:first-child` - primeira linha;
  * `:last-child` - última linha.

Também podemos inserir fórmulas dentro do `:nth-child()` como `nth-child(2n)` que nada mais é do que as linhas pares. Ou `nth-child(2n+1)`, que são as ímpares.

Generalizando: `:nth-child(xn + c)`
Em que:
 -  x é a periodicidade, de quantos em quantos elementos será aplicado o estilo;
 -  c é o ponto de partida;
 -  n é a variável, que começa em 0 (zero).

## Pseudoelementos
Assim como as pseudo-classes permite aplicar estilos em partes de um documento.
* `::after` -> Permite alterar/adicionar conteúdo no inicio do elemento.
* `::before` -> Permite alterar/adicionar conteúdo no final do elemento.

## Função calc()
A função calc() permite que se definam valores CSS com uso de expressões matemáticas, ou seja, o valor adotado para a propriedade é o resultado de uma expressão matemática.

Os operadores matemáticos válidos são: + (soma), - (subtração), * (multiplicação) e / (divisão). As unidades de medida CSS válidas na expressão matemática são as unidades CSS para: comprimento, ângulo, tempo, frequência e números inteiros e fracionários.

A função calc() traz três grandes vantagens para nosso código.
  * A primeira é a legibilidade: podemos deixar algumas contas explícitas, facilitando o entendimento e a manutenção do código.

  * A segunda é o poder: conseguimos criar layouts que não eram possíveis sem JavaScript antes, como elementos que ocupam um espaço que outros deixaram sobrando.

  * A terceira é a flexibilidade: como podemos misturar unidades nas contas, conseguimos deixar nosso layout ainda mais flexível, com um comportamento adequado em tamanhos de tela diferentes e com fontes diferentes.

## Tabelas
Segue:
  * Tudo inicia com a tag `table`.
  * Para indicar linhas usamos a tag `tr`.
  * No cabeçalho usamos a tag `thead` -> as colunas de dentro do cabeçalho indicamos com a tag `th`.
  * No corpo usamos a tag `tbody` -> e as colunas usamos a tag `td`
  * No footer também podemos usar a tag `tfooter`. "opcional"


## Transition
CSS transitions permite que as mudanças nos valores das propriedades CSS ocorram suavemente sobre uma duração especificada.

A propriedade transition possui quatro propriedades para você configurar:

* transition-property ->Nome da propriedade CSS sobre a qual o efeito da transição vai ser aplicado. É obrigatória na declaração pois caso seja omitida, não existirá uma propriedade para se aplicar o efeito da transição.
* transition-duration -> Duração do efeito em segundos (o padrão é 0)
* transition-timing-function -> Forma como a transição progride no tempo (o padrão é ease).
  - linear, ease, ease-in, ease-out e ease-in-out;
* transition-delay -> Define a partir de quanto tempo (em segundos) o efeito da transição vai se iniciar (o padrão é 0).


## Animation
Com CSS3, conseguimos criar animações que podem substituir imagens animadas, animações em Flash e JavaScript em muitas páginas web
Um keyframe descreve como o elemento que vai ser animado, deve ser renderizado em uma determinada fase, durante a sequência da animação.

Ou seja, cada keyframe contém uma ou mais propriedades CSS que vão ser aplicadas no elemento que será ser animado e, a animação se encarrega de mudar de um keyframe para outro, aplicando a transição entre as mudanças de CSS.

A sintaxe para a criação de keyframes é a seguinte:

* ```@keyframes nomedaanimacao {
      seletores-keyframe { estilo css para esse determinado keyframe; }
      }```

Com a animação criada nos keyframes, precisamos vinculá-la a algum seletor, caso contrário a animação não terá nenhum efeito. Para fazer isso, temos que declarar pelo menos duas propriedades que são obrigatórias:

o nome da animação (igual ao especificado nos keyframes);
a duração da animação (se não for declarada, a animação não se inicia pois o valor padrão é 0).

* Propriedades
  - animation-name: Nome da animação especificada nos @keyframes;
  - animation-duration: Quanto tempo, em segundos ou milisegundos, durará um ciclo da animação (o padrão é 0).
  - animation-timing-function: Forma como a animação progride no tempo (o padrão é ease). Do mesmo modo que a propriedade transition, pode ser usada de duas maneiras: uma é utilizando alguns valores já pré-definidos que são: `linear, ease, ease-in, ease-out e ease-in-out;`
  - animation-delay: Define a partir de quanto tempo a animação vai se iniciar (o padrão é 0).
  - animation-iteration-count: Determina o número de vezes que a animação vai se repetir (o padrão é 1). Podemos deixar a animação repetindo infinitamente, basta especificar o valor infinite.
  - animation-direction: Especifica se ao final da animação, ela deve reiniciar seu fluxo normalmente (normal), que é o padrão, ou voltar no sentido inverso (reverse).
  - animation-play-state: Define se a animação está rodando (running), que é o padrão, ou pausada (paused).
