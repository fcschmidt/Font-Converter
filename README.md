# Conversor de Fontes
[Primeira versão](https://github.com/fcschmidt/font-converter/tree/master/old/converterpixel), teste usando C# (2013).
[Segunda versão](https://github.com/fcschmidt/font-converter/tree/master/old/FonteConvertor), teste usando Java (2014).

## Unidades de medidas em CSS

Um pequeno projeto para treino da linguagem **Java** realizado na Universidade.
Esse aplicativo foi criado apenas com o intuito de fazer algumas conversões de unidades de medida do css de maneira simples e armazena-las.

**Oque são Unidade de Medidas CSS?**

As unidades de medida de comprimento CSS referem-se a medidas na horizontal ou na vertical (e em sentido mais amplo, em qualquer direção).

O formato para declarar o valor de uma unidade de medida CSS é um número com ou sem ponto decimal imediatamente precedido do sinal '+' (mais) ou do sinal '-' (menos), sendo o sinal '+' (mais) o valor "default" e imediatamente seguido por uma unidade identificadora (medida CSS válida - p.ex., px, em, deg, etc...). A unidade identificadora é opcional quando se declara um valor '0' (zero).

Algumas das propriedades CSS permitem que sejam declarados valores negativos para unidades de medida. A adoção de valores negativos podem complicar a formatação do elemento e devem ser usados com cautela. Se valores negativos não forem suportados pela aplicação de usuário, eles serão convertidos para o valor mais próximo suportado (e isso pode tornar-se desastroso para um layout).Veja abaixo as unidades disponíveis:


### Unidades de Comprimento

**Unidades Relativas**
* em
* ex

_as unidades relativas são referenciadas a outras unidades._

**Unidade relativa** - é aquela tomada em relação a uma outra medida. Folhas de estilos em Cascata que usam unidades de comprimento são mais apropriadas para ajustes de uso em diferentes tipos de mídia(p. ex., de uma tela de monitor para uma impressora laser).

**Unidades Absolutas**
* pt - point:1/72 in;
* pc - pica: 12 points ou 1/6 in;
* mm - milímetro: 1/10 cm;
* in - polegada: 2,54 cm; 
* px - pixel  

**Unidade absoluta** - é aquela que não esta referenciada a qualquer outra unidade e nem é herdada. São unidades de medida de comprimento definidas nos sistemas de medidas pela física e em fim são os conhecidos "centímetros, polegadas etc...). São indicadas para serem usadas quando as mídias de exibição são perfeitamente conhecidas.

**Unidades de Porcentagem**
* % - porcentagem

_O valor é tomado em relação:_

* **em:** ...ao tamanho da fonte ('font-size') herdada;
* **px:** ...ao dispositivo (midia) de exibição;
* **%:** ... a uma medida previamente definida.

_De todas as unidades, as recomendadas são as relativas, em especial **EMs**, que anteriormente seu tamanho era equivalente a altura da letra M em maiúscula, mas hoje, é igual a altura da letra do elemento em que se usa. Com esse tipo de medida, o autor mantém um controle relativo em relação ao tamanho da fonte padrão do usuário, onde pode especificar quanto maior ou menor se vê o texto na página. VOcê pode utilizar a unidade em também em qualquer propriedade CSS que admita medidas (margens, paddings,…), o que permite um desenho proporcional ao sistema do usuário._

_Mas por que não utilizar medidas absolutas? As unidades absolutas como px (pixel), cm (centímetros), pt (pontos), permitem um controle exato da aparência da página, sempre e quando, que seja vizualizada com o fim que ela foi projetada (onde se acaba a acessibilidade da página). Por exemplo, a unidade px tem um valor diferente dependendo da resolução da tela e do tipo de computador usuário. Assim, um sistema Windows mantém uma equivalência de 96px por polegada, e o Macintosh, 72 px por polegada. Se utilizarmos pt (pontos), no lugar de px (pixels) o tamanho dos pontos dependem da resolução do usuário._

### Unidades de medidas usadas nesse projeto: _PX (pixel), PT (point), EM, % (percentagem)_

1. **"Ems" (in):** A "in" é uma unidade expansível que é usado em meios documento da web. Um em é igual ao font-size atual, por exemplo, se o tamanho da fonte do documento é _12pt_, _1em_ é igual a _12pt_. Ems são escaláveis ​​na natureza, assim _2em_ seria igual _24pt_, .5em seria igual _6pt_, etc. Ems estão se tornando cada vez mais popular na web documentos devido à _escalabilidade e sua natureza **móvel-friendly** do dispositivo._

2. **Pixels (px):** Os pixels são unidades de tamanho fixo que são usados ​​na mídia de tela (ou seja, para ser lido na tela do computador). Um pixel é igual a um ponto na tela do computador (a menor divisão da resolução do ecrã). Muitos web designers usar unidades de pixel em documentos da web, a fim de produzir uma representação pixel-perfeito do seu site como ele é processado no navegador. _Um problema com a unidade de pixel é que ele não escala ascendente para os leitores com deficiência visual ou para baixo para ajustar dispositivos móveis._

3. **Os pontos (pt):** Pontos são tradicionalmente usados ​​na mídia impressa (qualquer coisa que está a ser impresso em papel, etc.). Um ponto é igual a _1/72_ de polegada. _Pontos são bem como pixels, na medida em que são unidades de tamanho fixo e não pode ser dimensionado em tamanho._

4. **Percentual (%):** A unidade cento é muito parecido com a unidade "em", salvo algumas diferenças fundamentais. Em primeiro lugar, o font-size atual é igual a _100%_ (ou seja, _12_ pontos = _100%_). _Ao usar o aparelho por cento, o seu texto permanece totalmente escalável para dispositivos móveis e para a acessibilidade._


**_Tabela e Equivalências_**

_Abaixo você pode ver uma tabela equivalente as medidas e seus valores aproximados, pois tudo depende do Navegador utilizado e também do Sistema Operacional:_

![Exemplo](http://i59.tinypic.com/21bjbs9.jpg)

**Formula utilizada para efetuar a conversão usando alguns valores como exemplo:**

**Converter PX para EM**
> * **Formula:** _tamanho em pixel / pixel pai_
> * **Exemplo:** _12px / 16px = .75em_

**Converter PX para %**
> * **Formula:**  _tamanho em pixel / pixel pai * 100_
> * **Exemplo:** _12px / 16px * 100 = 75%_

**Converter PX para PT**
> * **Formula:** _tamanho em pixels * (pontos por polegada / pixels por polegada)_
> * **Exemplo:** _16px * (72pt / 96px) = 12pt_

**Converter EM para PX**
> * **Formula:** _tamanho em EMs * pixel pai_
> * **Exemplo:** _.75em * 16px = 12px_

**Converter EM para %**
> * **Formula:** _tamanho em EMs * 100_
> * **Exemplo:** _.75em * 100 = 75%_
