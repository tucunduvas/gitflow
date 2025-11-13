# Projeto de Layout com CSS Flexbox

Este é um projeto de estudo focado em demonstrar o uso do *CSS Flexbox* para criar um layout de página web estruturado e complexo. O projeto consiste em uma única página HTML (index.html) e uma folha de estilos (style.css) que trabalham juntas para organizar visualmente vários contêineres coloridos.

O objetivo principal é praticar o aninhamento de contêineres flex, o uso de diferentes direções (row e column) e o controle de alinhamento e justificação dos itens.

## Visualização

Para visualizar o resultado final, basta abrir o arquivo index.html em qualquer navegador web moderno.

(Recomendação: Adicione uma captura de tela do layout final aqui para referência rápida.)

## 📜 Estrutura do Projeto

O projeto é dividido em três seções principais, todas contidas dentro de um .container-geral.

### 1. .container-geral

* Este é o contêiner principal que envolve toda a página.
* Usa display: flex com flex-direction: column para empilhar as três seções principais verticalmente.
* align-items: center centraliza as seções na página.
* gap: 15px adiciona um espaçamento vertical entre cada seção.

### 2. Seção 1: .container-amarelo-1

* *HTML:* .container-amarelo-1 > .container-lilas > .container-laranja
* *CSS:*
    * .container-amarelo-1: Um contêiner flexível (row) que se estende por toda a largura (width: 100%).
    * .container-lilas: Usa flex: 1 para ocupar todo o espaço disponível dentro do contêiner amarelo. Também é um contêiner flex (row) que usa justify-content: center para centralizar seu filho.
    * .container-laranja: Um bloco de tamanho fixo (300px x 150px) centrado dentro do contêiner lilás.

### 3. Seção 2: .container-vermelho

* *HTML:* .container-vermelho > (.container-invisivel1 > 3x .retangulo-azul) + .retangulo-verde
* *CSS:*
    * .container-vermelho: Um contêiner flex (row) que usa justify-content: space-around para distribuir seus filhos horizontalmente com espaço igual ao redor deles.
    * flex-wrap: wrap permite que os itens quebrem para a linha seguinte em telas menores.
    * .container-invisivel1: Um contêiner flex (row) que agrupa os três retângulos azuis e os distribui com justify-content: space-around.

### 4. Seção 3: .container-amarelo-2

* *HTML:* .container-amarelo-2 > 2x (.invisivel2 > 2x (.container-laranja-2 > .retangulo-vermelho))
* *CSS:*
    * .container-amarelo-2: O layout mais complexo. É um contêiner flex (row) que usa justify-content: space-around e flex-wrap: wrap para organizar seus filhos.
    * .invisivel2: Existem dois desses contêineres. Cada um é um item flexível (flex: 1) com uma largura mínima (min-width: 250px), o que ajuda na quebra de linha. O mais importante é que ele usa flex-direction: column para empilhar seus filhos (os .container-laranja-2) verticalmente.
    * .container-laranja-2: Contêineres laranja que usam display: flex e align-items: flex-end para posicionar seu filho (.retangulo-vermelho) na parte inferior.

## 🚀 Conceitos de Flexbox Demonstrados

* *display: flex*: Transforma um elemento em um contêiner flex.
* *flex-direction: column*: Empilha os itens flex verticalmente (visto no .container-geral e .invisivel2).
* *flex-direction: row*: Organiza os itens flex horizontalmente (padrão, visto em todos os outros contêineres).
* *justify-content*: Controla o alinhamento horizontal (e.g., center, space-around, flex-start).
* *align-items*: Controla o alinhamento vertical (e.g., center, flex-end).
* *flex-wrap: wrap*: Permite que os itens "quebrem" para a próxima linha se não houver espaço suficiente.
* *flex: 1*: Permite que um item cresça para ocupar o espaço disponível.
* *gap*: Define o espaçamento entre os itens flex.
* *Aninhamento (Nesting)*: Demonstra como contêineres flex podem ser colocados dentro de outros contêineres flex, cada um com suas próprias regras de layout.

## 🛠️ Como Visualizar

1.  Salve o primeiro bloco de código como index.html.
2.  Salve o segundo bloco de código como style.css *na mesma pasta* que o index.html.
3.  Abra o arquivo index.html em seu navegador.

## 💻 Tecnologias Utilizadas

* *HTML5*: Para a estrutura semântica dos elementos.
* *CSS3: Para estilização, com foco principal no módulo **Flexbox*.