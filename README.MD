# Atualização de uma pagina simples para html5 e css3 avançado.

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
