# Case iFood · Executivo de Vendas Farmer

Apresentação interativa criada para um case de processo seletivo na área de contas estratégicas do iFood. Em vez de slides estáticos, o resultado é uma página única em que o leitor filtra a carteira, abre a ficha de cada restaurante, muda premissas e vê o efeito nos números.

> Projeto de estudo, sem vínculo com o iFood. Os dados são os do enunciado do case e servem apenas para demonstração.

## Sumário

- [Para que serve](#para-que-serve)
- [Como abrir](#como-abrir)
- [Como navegar](#como-navegar)
- [O que cada aba faz](#o-que-cada-aba-faz)
- [Principais achados](#principais-achados)
- [Regras e fórmulas usadas](#regras-e-fórmulas-usadas)
- [Limitações e pontos de atenção](#limitações-e-pontos-de-atenção)
- [Detalhes técnicos](#detalhes-técnicos)
- [Autor](#autor)

## Para que serve

O case pede uma análise de carteira de restaurantes parceiros e propostas de ação. A página responde a cinco perguntas:

1. **Carteira:** quem cresce, quem cai e por quê? Quem atender primeiro? Como chegar a +15% em pedidos?
2. **Funil:** onde o cliente desiste dentro da loja e o que orientar ao parceiro?
3. **Mercado:** onde a cidade tem demanda que a carteira ainda não cobre?
4. **Maquinona e Totem:** quantas abordagens são necessárias para bater a meta de captação?
5. **Relacionamento:** como agir em três situações do dia a dia de um Executivo Farmer?

A ideia central é que cada número possa ser explorado. O leitor não recebe só a conclusão, ele consegue testar a premissa por trás dela.

## Como abrir

**No computador:** baixe o arquivo `index.html` e dê dois cliques. Ele abre em qualquer navegador moderno (Chrome, Edge, Firefox, Safari), sem instalar nada e sem servidor. Sem internet, a página funciona normalmente, apenas com a fonte padrão do sistema.

**Online, com GitHub Pages:** em **Settings → Pages**, escolha a branch `main` e a pasta raiz. O GitHub gera um endereço no formato `https://<usuario>.github.io/case-ifood-dados/`.

## Como navegar

- Cinco abas no topo: Carteira, Funil, Mercado, Maquinona e Totem, Quick questions.
- As setas **←** e **→** do teclado trocam de aba.
- Cada aba tem um endereço direto: `#carteira`, `#funil`, `#mercado`, `#expansao` e `#postura`.
- Ao passar o mouse sobre barras e etiquetas, aparecem os valores exatos.
- A página segue o tema claro ou escuro do sistema e se adapta ao celular.

## O que cada aba faz

### 1 · Carteira

- **Números do mês:** pedidos, contas em queda, contas crescendo e concentração nas cinco maiores contas.
- **Crescimento por alavanca:** variação de pedidos totais e de pedidos com Frete Grátis, Cupom e PBB.
- **Agenda de consultorias:** três faixas de prioridade. Clicar em um restaurante abre a ficha dele.
- **Tabela da carteira:** filtros (em queda, crescendo, sem variação, perdeu Frete Grátis, 500 pedidos ou mais sem PBB), busca por nome e ordenação. A coluna de variação mostra uma barra divergente: laranja para queda e azul para alta.
- **Ficha do restaurante:** compara mês anterior e atual para pedidos e cada alavanca, e traz uma causa provável e uma ação sugerida, geradas por regras.
- **Simulador de +15%:** três controles, um por frente de trabalho, com cenários prontos (conservador, base e agressivo). Mostra quanto cada frente entrega e quanto falta para a meta.
- **Pontos de atenção nos dados:** linhas repetidas, dados parados e o efeito disso no crescimento. Uma caixa de seleção remove as linhas suspeitas de todos os números da aba.

### 2 · Funil

- Barras com a taxa de cada etapa sobre as visitas, com um traço que marca a taxa do período anterior.
- Dois controles respondem a "e se o parceiro melhorar?": mais visitas que viram visualização, e parte dos abandonos na revisão do pedido que volta a comprar.
- Duas listas: o que o funil mostra e o que orientar ao parceiro.

### 3 · Mercado

- Gráfico de barras com três visões: pedidos na cidade, parceiros na carteira e pedidos por parceiro.
- Barras azuis marcam culinárias com parceiro na carteira, e barras laranja marcam culinárias sem nenhum.
- Etiquetas de leitura: **espaço** (muita demanda por parceiro), **disputada** (pouca demanda por parceiro) e **sem parceiro**.

### 4 · Maquinona e Totem

- Calculadora com quatro controles: meta de Maquinona, meta de Totem, conversão por abordagem e dias úteis.
- Resultado: abordagens necessárias de cada produto, total no mês e ritmo por dia útil.
- Plano de quatro semanas e ferramentas de apoio.

### 5 · Quick questions

Três situações de relacionamento, cada uma respondida em três passos: pedido de dados de concorrentes, feedback sobre meta não batida e parceiro que cresce e ainda reclama.

## Principais achados

- A carteira passou de **48.069 para 56.381 pedidos (+17,3%)**.
- **19 contas caíram** (−3.284 pedidos). **12 delas desligaram o Frete Grátis** e, juntas, perderam 2.054 pedidos. A causa mais clara da queda é essa.
- Os pedidos com PBB cresceram **32,7%**, mais que o volume total.
- A meta de +15% equivale a **8.457 pedidos**. Há 12 contas de alto volume que ainda não usam PBB.
- No funil, as visitas subiram 54,18%, mas a conversão final caiu de 27,33% para 25,26%. São 2,07 pontos percentuais a menos, ou 7,57% em termos relativos.
- No mercado, **Açaí e Padaria** têm muita demanda por parceiro, enquanto **Pizza e Hambúrguer** são disputados. Dez culinárias da cidade não têm nenhum parceiro na carteira.
- Com 33% de conversão, as metas de 9 Maquinonas e 7 Totens pedem **50 abordagens**, cerca de 2,3 por dia útil.

## Regras e fórmulas usadas

**Classificação das contas**
- Em queda: variação de pedidos menor que zero. Crescendo: maior que zero.
- Alavanca desligada: tinha uso no mês anterior e hoje tem zero.
- Etiquetas na tabela: *Ligou*, *Desligou*, *Subiu*, *Caiu*, *Igual* e *Sem uso*.

**Agenda**
- Prioridade 1, recuperar: todas as contas em queda.
- Prioridade 2, destravar volume: contas sem queda, com 500 pedidos ou mais e sem PBB.
- Prioridade 3, escalar e proteger: os oito maiores crescimentos fora da prioridade 2.

**Simulador de +15%** (os três grupos não se sobrepõem, então os ganhos podem ser somados)
- Meta = 15% dos pedidos do mês atual.
- Frente 1 = perda das contas em queda × percentual recuperado.
- Frente 2 = pedidos das contas da prioridade 2 × ganho esperado com PBB.
- Frente 3 = pedidos das contas que crescem, fora da frente 2, × ganho esperado.

**Simulador do funil**
- Pedidos concluídos = visitas × taxa de visualização × (sacola ÷ visualizações) × (revisão ÷ sacola) × (taxa de conclusão + abandono × parte recuperada).

**Mercado**
- Pedidos por parceiro = pedidos da cidade na culinária ÷ parceiros da carteira nela.
- Leitura: 10 mil ou mais indica espaço, 2.500 ou menos indica disputa. Esses cortes são uma regra de leitura minha, não um dado do case.

**Captação**
- Abordagens de cada produto = meta ÷ conversão, arredondado para cima.
- Ritmo diário = total de abordagens ÷ dias úteis.

## Limitações e pontos de atenção

- **Os percentuais do simulador de +15% são hipóteses para discussão,** não resultados medidos. Servem para testar se a meta fecha e quanto cada premissa pesa.
- **Linhas que parecem repetidas.** Os pares G/M e AG/AN são idênticos em todas as colunas, e S/X e AI/AQ têm os mesmos pedidos. Se M, X, AN e AQ forem repetição, o crescimento cai de 17,3% para 15,3%.
- **Dado possivelmente parado.** Cinco restaurantes pequenos (BE a BI) têm pedidos idênticos nos dois meses.
- **Parceiros por culinária** foram lidos de um gráfico do enunciado e somam 96, enquanto a carteira da planilha tem 55 restaurantes. As duas carteiras não são a mesma, então o cruzamento é por culinária, não por restaurante.
- **Culinárias sem demanda de cidade.** Dezenove lojas do gráfico são de culinárias que a tabela da cidade não traz, e para elas não há como calcular demanda por parceiro.
- **Maquinona e taxas.** A página não afirma que as taxas são menores. As condições variam por negociação, e a comparação com a taxa atual do parceiro deve somar mensalidade, taxa por transação, antecipação e marketing.

## Detalhes técnicos

- **HTML, CSS e JavaScript puros** em um único arquivo, sem frameworks e sem bibliotecas externas. A única chamada externa é a fonte do Google Fonts, com alternativa local.
- Os dados da carteira ficam embutidos no próprio arquivo, na constante `RAW`. Cada linha traz: restaurante, pedidos do mês atual, pedidos do mês anterior, variação, e uso de Frete Grátis, Cupom e PBB nos dois meses.
- Tema claro e escuro automáticos, layout responsivo, foco visível no teclado e abas com a semântica de acessibilidade adequada.
- Gráficos desenhados com CSS, sem canvas.

## Autor

Victor · [github.com/VictorChantre08](https://github.com/VictorChantre08)
