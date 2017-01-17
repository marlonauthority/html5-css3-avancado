# Atualização de uma pagina simples para html5 e css3 avançado.

## Verificar as funcionalidades novas
> Entre no site "caniuse.com" e verifique se as funcionalidades que você queira implementar está disponível e/ou suporta o seu navegador padrão.


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


#### Border-Radius
Implementado para colocar bordas arredondadas em elementos.
A sintaxe é: border-radius rx rx rx rx;


## Transform
Está propriedade permite o controle da posição do elemento sem afetar o fluxo da pagína.
Seu uso é simples basta especificar o tipo de transformação.
`transform: rotate(30deg)` -> Rotaciona em 30 graus.
`transform: scale(1.5)` -> Aumenta sua escala x 1.5
`transform: skew(20deg)` -> Entorta o elemento, fazendo crescer ou diminuir em 20 graus.
`transform: translate(10px, 50px)` -> Faz um translado de 10 pixels para direita e 50 para cima.

* Para transformações em 3D é usado 3 eixos para definir o tamanho dos nossos objetos: X, Y e Z.
  * translatex - eixo X
  * translatey - eixo Y
  * translatez - profundidade
Também é necesário especificar a perspectiva `(perspective)` para definir a distancia que o usuário estaá da tela para que possamos fazer o cálculo de projeção do 3D. Outro pronto importante é a anfulação que o usuário está olhando, o que causa diferentes efeitos de perspectiva. Para lidar com essa diferença usamos a propriedade `perspective-origin`
