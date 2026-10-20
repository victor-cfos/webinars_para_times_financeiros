# Prompts para reproduzir os 20 gráficos · Webinar #1 · CFOs.AI

Cada prompt é autocontido: traz os dados fictícios inline, o tipo de gráfico, as cores em hex, fontes, eixos, rótulos e layout, e pede duas saídas: (a) um script Python executável (matplotlib) e (b) um HTML com Tailwind CSS via CDN + Chart.js ou SVG. Copie o bloco inteiro e cole em qualquer IA. Planilha correspondente: `dashboards-financeiros-cfosai.xlsx`.

## 01 · Colunas

Aba: `01 Colunas` · Pergunta: Qual regional gerou mais receita no ano?

```text
Você é especialista em visualização de dados financeiros. Crie um gráfico de colunas verticais com o título "Receita líquida por regional · 2026" e o subtítulo "Qual regional gerou mais receita no ano?".
DADOS (fictícios; unidade: R$ mil). Use exatamente estes valores, sem inventar outros:
| Regional | Receita líquida |
|---|---|
| Norte | 4200 |
| Nordeste | 5850 |
| Centro-Oeste | 3900 |
| Sudeste | 9700 |
| Sul | 6400 |
ESPECIFICAÇÃO DO GRÁFICO:
- Uma coluna por regional, na ordem da tabela, todas na cor #EF4517; largura das colunas ~60% do espaço de cada categoria.
- Eixo Y começando em zero, formato de milhar, título do eixo "R$ mil"; grade horizontal fina; sem grade vertical.
- Rótulo de valor acima de cada coluna (ex.: 9.700), 11 px, cor #1A1A1A. Sem legenda (série única).
IDENTIDADE VISUAL (CFOs.AI):
- Paleta: laranja principal #EF4517; tons de laranja para séries extras #F47D5D, #F9B4A2, #FCDAD1; cinzas para referência/secundário #BFBFBF e #8C8C8C; textos em #1A1A1A e #595959. Não use outras cores.
- Fundo branco (#FFFFFF) no gráfico e na página; sem bordas no gráfico, sem sombras, sem 3D, sem gradientes.
- Fonte: Calibri (fallback: Arial, sans-serif) em todo o gráfico.
- Título do gráfico: 18 px, negrito, cor #1A1A1A, alinhado à esquerda. Subtítulo logo abaixo: 13 px, cor #595959.
- Textos de eixos e legendas: 11–12 px, cor #595959. Linhas de eixo finas em #BFBFBF; linhas de grade finas em #E6E6E6; sem marcas de escala (ticks).
- Wordmark "CFOs.AI" no canto superior direito, texto em negrito na cor #EF4517. Rodapé à esquerda: "Fonte: dados fictícios · CFOs.AI" em 10 px, cor #8C8C8C.
- Números em formato brasileiro nos rótulos (ponto como separador de milhar e vírgula decimal; ex.: 1.234; 12,5%).
- Proporção 16:9 (960 × 540 px), margens generosas e nada de elementos decorativos extras.
ENTREGUE DUAS SAÍDAS, cada uma em um bloco de código separado e completo:
(a) Python: um único script executável (matplotlib + numpy, sem outras dependências), com os dados declarados no próprio script, que aplica todas as especificações acima e salva o gráfico em "colunas.png" (dpi 200, fundo branco). Ao final, chame plt.close().
(b) HTML: um único arquivo .html autocontido que carrega Tailwind CSS via CDN (<script src="https://cdn.tailwindcss.com"></script>) e Chart.js 4 via CDN (https://cdn.jsdelivr.net/npm/chart.js); mostre o gráfico em um card branco centralizado (max-w-4xl, padding generoso, sem sombra), com título, subtítulo, wordmark e rodapé em HTML, e as mesmas cores, fontes e dados.
Não explique demais: entregue o código pronto para rodar.
```

## 02 · Barras horizontais

Aba: `02 Barras horizontais` · Pergunta: Quais despesas mais pesam no resultado?

```text
Você é especialista em visualização de dados financeiros. Crie um gráfico de barras horizontais ordenadas com o título "Despesas operacionais por natureza · 2026" e o subtítulo "Quais despesas mais pesam no resultado?".
DADOS (fictícios; unidade: R$ mil). Use exatamente estes valores, sem inventar outros:
| Natureza da despesa | Valor |
|---|---|
| Pessoal e encargos | 3150 |
| Tecnologia e software | 1240 |
| Marketing e mídia | 980 |
| Aluguel e facilities | 760 |
| Serviços de terceiros | 640 |
| Viagens e deslocamentos | 310 |
| Outras despesas | 220 |
ESPECIFICAÇÃO DO GRÁFICO:
- Barras horizontais ordenadas do maior (no topo) para o menor (embaixo).
- Destaque: a maior barra ("Pessoal e encargos") em #EF4517; todas as outras em cinza claro #BFBFBF.
- Nomes das categorias à esquerda; eixo X a partir de zero com título "R$ mil" e grade vertical fina.
- Rótulo de valor no fim de cada barra (ex.: 3.150), 11 px, cor #1A1A1A. Sem legenda.
IDENTIDADE VISUAL (CFOs.AI):
- Paleta: laranja principal #EF4517; tons de laranja para séries extras #F47D5D, #F9B4A2, #FCDAD1; cinzas para referência/secundário #BFBFBF e #8C8C8C; textos em #1A1A1A e #595959. Não use outras cores.
- Fundo branco (#FFFFFF) no gráfico e na página; sem bordas no gráfico, sem sombras, sem 3D, sem gradientes.
- Fonte: Calibri (fallback: Arial, sans-serif) em todo o gráfico.
- Título do gráfico: 18 px, negrito, cor #1A1A1A, alinhado à esquerda. Subtítulo logo abaixo: 13 px, cor #595959.
- Textos de eixos e legendas: 11–12 px, cor #595959. Linhas de eixo finas em #BFBFBF; linhas de grade finas em #E6E6E6; sem marcas de escala (ticks).
- Wordmark "CFOs.AI" no canto superior direito, texto em negrito na cor #EF4517. Rodapé à esquerda: "Fonte: dados fictícios · CFOs.AI" em 10 px, cor #8C8C8C.
- Números em formato brasileiro nos rótulos (ponto como separador de milhar e vírgula decimal; ex.: 1.234; 12,5%).
- Proporção 16:9 (960 × 540 px), margens generosas e nada de elementos decorativos extras.
ENTREGUE DUAS SAÍDAS, cada uma em um bloco de código separado e completo:
(a) Python: um único script executável (matplotlib + numpy, sem outras dependências), com os dados declarados no próprio script, que aplica todas as especificações acima e salva o gráfico em "barras.png" (dpi 200, fundo branco). Ao final, chame plt.close().
(b) HTML: um único arquivo .html autocontido que carrega Tailwind CSS via CDN (<script src="https://cdn.tailwindcss.com"></script>) e Chart.js 4 via CDN (https://cdn.jsdelivr.net/npm/chart.js) (indexAxis: 'y'); mostre o gráfico em um card branco centralizado (max-w-4xl, padding generoso, sem sombra), com título, subtítulo, wordmark e rodapé em HTML, e as mesmas cores, fontes e dados.
Não explique demais: entregue o código pronto para rodar.
```

## 03 · Colunas agrupadas

Aba: `03 Colunas agrupadas` · Pergunta: Em que trimestre o realizado se afastou do orçamento?

```text
Você é especialista em visualização de dados financeiros. Crie um gráfico de colunas agrupadas com o título "EBITDA orçado vs. realizado por trimestre · 2026" e o subtítulo "Em que trimestre o realizado se afastou do orçamento?".
DADOS (fictícios; unidade: R$ mil). Use exatamente estes valores, sem inventar outros:
| Trimestre | Orçado | Realizado |
|---|---|---|
| T1 | 1800 | 1720 |
| T2 | 2000 | 2090 |
| T3 | 2150 | 1980 |
| T4 | 2400 | 2510 |
ESPECIFICAÇÃO DO GRÁFICO:
- Para cada trimestre, duas colunas lado a lado: "Orçado" em cinza #BFBFBF (referência) e "Realizado" em laranja #EF4517.
- Pequeno espaço entre as colunas do mesmo grupo e espaço maior entre trimestres.
- Eixo Y a partir de zero, formato de milhar, título "R$ mil"; grade horizontal fina.
- Rótulos de valor acima de cada coluna em 10 px, cor #595959. Legenda embaixo, centralizada.
IDENTIDADE VISUAL (CFOs.AI):
- Paleta: laranja principal #EF4517; tons de laranja para séries extras #F47D5D, #F9B4A2, #FCDAD1; cinzas para referência/secundário #BFBFBF e #8C8C8C; textos em #1A1A1A e #595959. Não use outras cores.
- Fundo branco (#FFFFFF) no gráfico e na página; sem bordas no gráfico, sem sombras, sem 3D, sem gradientes.
- Fonte: Calibri (fallback: Arial, sans-serif) em todo o gráfico.
- Título do gráfico: 18 px, negrito, cor #1A1A1A, alinhado à esquerda. Subtítulo logo abaixo: 13 px, cor #595959.
- Textos de eixos e legendas: 11–12 px, cor #595959. Linhas de eixo finas em #BFBFBF; linhas de grade finas em #E6E6E6; sem marcas de escala (ticks).
- Wordmark "CFOs.AI" no canto superior direito, texto em negrito na cor #EF4517. Rodapé à esquerda: "Fonte: dados fictícios · CFOs.AI" em 10 px, cor #8C8C8C.
- Números em formato brasileiro nos rótulos (ponto como separador de milhar e vírgula decimal; ex.: 1.234; 12,5%).
- Proporção 16:9 (960 × 540 px), margens generosas e nada de elementos decorativos extras.
ENTREGUE DUAS SAÍDAS, cada uma em um bloco de código separado e completo:
(a) Python: um único script executável (matplotlib + numpy, sem outras dependências), com os dados declarados no próprio script, que aplica todas as especificações acima e salva o gráfico em "agrupadas.png" (dpi 200, fundo branco). Ao final, chame plt.close().
(b) HTML: um único arquivo .html autocontido que carrega Tailwind CSS via CDN (<script src="https://cdn.tailwindcss.com"></script>) e Chart.js 4 via CDN (https://cdn.jsdelivr.net/npm/chart.js); mostre o gráfico em um card branco centralizado (max-w-4xl, padding generoso, sem sombra), com título, subtítulo, wordmark e rodapé em HTML, e as mesmas cores, fontes e dados.
Não explique demais: entregue o código pronto para rodar.
```

## 04 · Colunas empilhadas

Aba: `04 Colunas empilhadas` · Pergunta: Quanto cada canal contribui para o total do trimestre?

```text
Você é especialista em visualização de dados financeiros. Crie um gráfico de colunas empilhadas com o título "Receita por canal e trimestre · 2026" e o subtítulo "Quanto cada canal contribui para o total do trimestre?".
DADOS (fictícios; unidade: R$ mil). Use exatamente estes valores, sem inventar outros:
| Trimestre | Loja | Online | B2B | Total |
|---|---|---|---|---|
| T1 | 2100 | 1200 | 900 | 4200 |
| T2 | 2050 | 1450 | 950 | 4450 |
| T3 | 2200 | 1700 | 1000 | 4900 |
| T4 | 2600 | 2050 | 1150 | 5800 |
ESPECIFICAÇÃO DO GRÁFICO:
- Uma coluna por trimestre empilhando de baixo para cima: Loja (#EF4517), Online (#F47D5D), B2B (#F9B4A2).
- Eixo Y a partir de zero, formato de milhar, título "R$ mil"; grade horizontal fina.
- Rótulo de valor no centro de cada segmento (texto branco sobre #EF4517, #1A1A1A sobre os tons claros) e o total acima de cada coluna em negrito.
- Linhas brancas finas separando os segmentos. Legenda embaixo, centralizada.
IDENTIDADE VISUAL (CFOs.AI):
- Paleta: laranja principal #EF4517; tons de laranja para séries extras #F47D5D, #F9B4A2, #FCDAD1; cinzas para referência/secundário #BFBFBF e #8C8C8C; textos em #1A1A1A e #595959. Não use outras cores.
- Fundo branco (#FFFFFF) no gráfico e na página; sem bordas no gráfico, sem sombras, sem 3D, sem gradientes.
- Fonte: Calibri (fallback: Arial, sans-serif) em todo o gráfico.
- Título do gráfico: 18 px, negrito, cor #1A1A1A, alinhado à esquerda. Subtítulo logo abaixo: 13 px, cor #595959.
- Textos de eixos e legendas: 11–12 px, cor #595959. Linhas de eixo finas em #BFBFBF; linhas de grade finas em #E6E6E6; sem marcas de escala (ticks).
- Wordmark "CFOs.AI" no canto superior direito, texto em negrito na cor #EF4517. Rodapé à esquerda: "Fonte: dados fictícios · CFOs.AI" em 10 px, cor #8C8C8C.
- Números em formato brasileiro nos rótulos (ponto como separador de milhar e vírgula decimal; ex.: 1.234; 12,5%).
- Proporção 16:9 (960 × 540 px), margens generosas e nada de elementos decorativos extras.
ENTREGUE DUAS SAÍDAS, cada uma em um bloco de código separado e completo:
(a) Python: um único script executável (matplotlib + numpy, sem outras dependências), com os dados declarados no próprio script, que aplica todas as especificações acima e salva o gráfico em "empilhadas.png" (dpi 200, fundo branco). Ao final, chame plt.close().
(b) HTML: um único arquivo .html autocontido que carrega Tailwind CSS via CDN (<script src="https://cdn.tailwindcss.com"></script>) e Chart.js 4 via CDN (https://cdn.jsdelivr.net/npm/chart.js); mostre o gráfico em um card branco centralizado (max-w-4xl, padding generoso, sem sombra), com título, subtítulo, wordmark e rodapé em HTML, e as mesmas cores, fontes e dados.
Não explique demais: entregue o código pronto para rodar.
```

## 05 · Empilhadas 100%

Aba: `05 Empilhadas 100%` · Pergunta: O mix de canais está mudando ao longo dos anos?

```text
Você é especialista em visualização de dados financeiros. Crie um gráfico de colunas empilhadas 100% com o título "Mix de receita por canal · 2023–2026" e o subtítulo "O mix de canais está mudando ao longo dos anos?".
DADOS (fictícios; unidade: R$ mil). Use exatamente estes valores, sem inventar outros:
| Ano | Loja | Online | B2B | Total | % Loja | % Online | % B2B |
|---|---|---|---|---|---|---|---|
| 2023 | 6960 | 2640 | 2400 | 12000 | 58,0% | 22,0% | 20,0% |
| 2024 | 6760 | 3640 | 2600 | 13000 | 52,0% | 28,0% | 20,0% |
| 2025 | 6580 | 4620 | 2800 | 14000 | 47,0% | 33,0% | 20,0% |
| 2026 | 6150 | 5700 | 3150 | 15000 | 41,0% | 38,0% | 21,0% |
ESPECIFICAÇÃO DO GRÁFICO:
- Uma coluna por ano, cada uma somando 100%, empilhando de baixo para cima: Loja (#EF4517), Online (#F47D5D), B2B (#F9B4A2).
- Calcule as participações a partir dos valores em R$ mil (as % da tabela servem de conferência).
- Eixo Y de 0% a 100% com marcas a cada 20%; grade horizontal fina.
- Rótulo da participação no centro de cada segmento com 1 casa decimal (ex.: 41,0%); texto branco sobre #EF4517 e #1A1A1A sobre os tons claros.
- Linhas brancas finas separando os segmentos. Legenda embaixo, centralizada.
IDENTIDADE VISUAL (CFOs.AI):
- Paleta: laranja principal #EF4517; tons de laranja para séries extras #F47D5D, #F9B4A2, #FCDAD1; cinzas para referência/secundário #BFBFBF e #8C8C8C; textos em #1A1A1A e #595959. Não use outras cores.
- Fundo branco (#FFFFFF) no gráfico e na página; sem bordas no gráfico, sem sombras, sem 3D, sem gradientes.
- Fonte: Calibri (fallback: Arial, sans-serif) em todo o gráfico.
- Título do gráfico: 18 px, negrito, cor #1A1A1A, alinhado à esquerda. Subtítulo logo abaixo: 13 px, cor #595959.
- Textos de eixos e legendas: 11–12 px, cor #595959. Linhas de eixo finas em #BFBFBF; linhas de grade finas em #E6E6E6; sem marcas de escala (ticks).
- Wordmark "CFOs.AI" no canto superior direito, texto em negrito na cor #EF4517. Rodapé à esquerda: "Fonte: dados fictícios · CFOs.AI" em 10 px, cor #8C8C8C.
- Números em formato brasileiro nos rótulos (ponto como separador de milhar e vírgula decimal; ex.: 1.234; 12,5%).
- Proporção 16:9 (960 × 540 px), margens generosas e nada de elementos decorativos extras.
ENTREGUE DUAS SAÍDAS, cada uma em um bloco de código separado e completo:
(a) Python: um único script executável (matplotlib + numpy, sem outras dependências), com os dados declarados no próprio script, que aplica todas as especificações acima e salva o gráfico em "empilhadas100.png" (dpi 200, fundo branco). Ao final, chame plt.close().
(b) HTML: um único arquivo .html autocontido que carrega Tailwind CSS via CDN (<script src="https://cdn.tailwindcss.com"></script>) e Chart.js 4 via CDN (https://cdn.jsdelivr.net/npm/chart.js); mostre o gráfico em um card branco centralizado (max-w-4xl, padding generoso, sem sombra), com título, subtítulo, wordmark e rodapé em HTML, e as mesmas cores, fontes e dados.
Não explique demais: entregue o código pronto para rodar.
```

## 06 · Linhas

Aba: `06 Linhas` · Pergunta: O caixa melhora ou piora ao longo do ano? Fica acima do mínimo?

```text
Você é especialista em visualização de dados financeiros. Crie um gráfico de linhas com o título "Saldo de caixa no fim do mês · 2026" e o subtítulo "O caixa melhora ou piora ao longo do ano? Fica acima do mínimo?".
DADOS (fictícios; unidade: R$ mil). Use exatamente estes valores, sem inventar outros:
| Mês | Saldo de caixa | Caixa mínimo |
|---|---|---|
| Jan | 3200 | 2500 |
| Fev | 2950 | 2500 |
| Mar | 2700 | 2500 |
| Abr | 2850 | 2500 |
| Mai | 3100 | 2500 |
| Jun | 2600 | 2500 |
| Jul | 2400 | 2500 |
| Ago | 2750 | 2500 |
| Set | 3050 | 2500 |
| Out | 3400 | 2500 |
| Nov | 3300 | 2500 |
| Dez | 3900 | 2500 |
ESPECIFICAÇÃO DO GRÁFICO:
- Série "Saldo de caixa": linha contínua #EF4517, 2,5 px, com marcadores circulares preenchidos na mesma cor e rótulo do valor acima de cada ponto (10 px, #595959).
- Série "Caixa mínimo": linha tracejada cinza #8C8C8C, 1,25 px, sem marcadores (é a referência).
- Eixo X com os meses (Jan a Dez); eixo Y a partir de zero, formato de milhar, título "R$ mil"; grade horizontal fina.
- Legenda embaixo, centralizada.
IDENTIDADE VISUAL (CFOs.AI):
- Paleta: laranja principal #EF4517; tons de laranja para séries extras #F47D5D, #F9B4A2, #FCDAD1; cinzas para referência/secundário #BFBFBF e #8C8C8C; textos em #1A1A1A e #595959. Não use outras cores.
- Fundo branco (#FFFFFF) no gráfico e na página; sem bordas no gráfico, sem sombras, sem 3D, sem gradientes.
- Fonte: Calibri (fallback: Arial, sans-serif) em todo o gráfico.
- Título do gráfico: 18 px, negrito, cor #1A1A1A, alinhado à esquerda. Subtítulo logo abaixo: 13 px, cor #595959.
- Textos de eixos e legendas: 11–12 px, cor #595959. Linhas de eixo finas em #BFBFBF; linhas de grade finas em #E6E6E6; sem marcas de escala (ticks).
- Wordmark "CFOs.AI" no canto superior direito, texto em negrito na cor #EF4517. Rodapé à esquerda: "Fonte: dados fictícios · CFOs.AI" em 10 px, cor #8C8C8C.
- Números em formato brasileiro nos rótulos (ponto como separador de milhar e vírgula decimal; ex.: 1.234; 12,5%).
- Proporção 16:9 (960 × 540 px), margens generosas e nada de elementos decorativos extras.
ENTREGUE DUAS SAÍDAS, cada uma em um bloco de código separado e completo:
(a) Python: um único script executável (matplotlib + numpy, sem outras dependências), com os dados declarados no próprio script, que aplica todas as especificações acima e salva o gráfico em "linhas.png" (dpi 200, fundo branco). Ao final, chame plt.close().
(b) HTML: um único arquivo .html autocontido que carrega Tailwind CSS via CDN (<script src="https://cdn.tailwindcss.com"></script>) e Chart.js 4 via CDN (https://cdn.jsdelivr.net/npm/chart.js); mostre o gráfico em um card branco centralizado (max-w-4xl, padding generoso, sem sombra), com título, subtítulo, wordmark e rodapé em HTML, e as mesmas cores, fontes e dados.
Não explique demais: entregue o código pronto para rodar.
```

## 07 · Área

Aba: `07 Área` · Pergunta: Como evoluiu a receita recorrente ao longo do ano?

```text
Você é especialista em visualização de dados financeiros. Crie um gráfico de área com o título "Receita recorrente mensal (MRR) · 2026" e o subtítulo "Como evoluiu a receita recorrente ao longo do ano?".
DADOS (fictícios; unidade: R$ mil). Use exatamente estes valores, sem inventar outros:
| Mês | MRR |
|---|---|
| Jan | 820 |
| Fev | 845 |
| Mar | 870 |
| Abr | 910 |
| Mai | 935 |
| Jun | 960 |
| Jul | 1010 |
| Ago | 1050 |
| Set | 1080 |
| Out | 1130 |
| Nov | 1170 |
| Dez | 1230 |
ESPECIFICAÇÃO DO GRÁFICO:
- Área única preenchida com #EF4517 a 25% de opacidade e linha superior sólida #EF4517 de 2,25 px.
- Eixo Y a partir de zero, formato de milhar, título "R$ mil"; grade horizontal fina. Eixo X com os meses, com a área encostada nas bordas.
- Rótulo destacado só no último ponto (Dez: 1.230) em negrito #EF4517. Sem legenda.
IDENTIDADE VISUAL (CFOs.AI):
- Paleta: laranja principal #EF4517; tons de laranja para séries extras #F47D5D, #F9B4A2, #FCDAD1; cinzas para referência/secundário #BFBFBF e #8C8C8C; textos em #1A1A1A e #595959. Não use outras cores.
- Fundo branco (#FFFFFF) no gráfico e na página; sem bordas no gráfico, sem sombras, sem 3D, sem gradientes.
- Fonte: Calibri (fallback: Arial, sans-serif) em todo o gráfico.
- Título do gráfico: 18 px, negrito, cor #1A1A1A, alinhado à esquerda. Subtítulo logo abaixo: 13 px, cor #595959.
- Textos de eixos e legendas: 11–12 px, cor #595959. Linhas de eixo finas em #BFBFBF; linhas de grade finas em #E6E6E6; sem marcas de escala (ticks).
- Wordmark "CFOs.AI" no canto superior direito, texto em negrito na cor #EF4517. Rodapé à esquerda: "Fonte: dados fictícios · CFOs.AI" em 10 px, cor #8C8C8C.
- Números em formato brasileiro nos rótulos (ponto como separador de milhar e vírgula decimal; ex.: 1.234; 12,5%).
- Proporção 16:9 (960 × 540 px), margens generosas e nada de elementos decorativos extras.
ENTREGUE DUAS SAÍDAS, cada uma em um bloco de código separado e completo:
(a) Python: um único script executável (matplotlib + numpy, sem outras dependências), com os dados declarados no próprio script, que aplica todas as especificações acima e salva o gráfico em "area.png" (dpi 200, fundo branco). Ao final, chame plt.close().
(b) HTML: um único arquivo .html autocontido que carrega Tailwind CSS via CDN (<script src="https://cdn.tailwindcss.com"></script>) e Chart.js 4 via CDN (https://cdn.jsdelivr.net/npm/chart.js) (type line com fill: true); mostre o gráfico em um card branco centralizado (max-w-4xl, padding generoso, sem sombra), com título, subtítulo, wordmark e rodapé em HTML, e as mesmas cores, fontes e dados.
Não explique demais: entregue o código pronto para rodar.
```

## 08 · Pizza

Aba: `08 Pizza` · Pergunta: Como a receita do ano se divide entre os canais?

```text
Você é especialista em visualização de dados financeiros. Crie um gráfico de pizza com o título "Receita anual por canal · 2026" e o subtítulo "Como a receita do ano se divide entre os canais?".
DADOS (fictícios; unidade: R$ mil). Use exatamente estes valores, sem inventar outros:
| Canal | Valor (R$ mil) | % do total |
|---|---|---|
| Loja | 6150 | 41,0% |
| Online | 5700 | 38,0% |
| B2B | 3150 | 21,0% |
Total: 15.000
ESPECIFICAÇÃO DO GRÁFICO:
- Pizza com 3 fatias no sentido horário a partir das 12h: Loja #EF4517, Online #F9B4A2, B2B #BFBFBF.
- Separadores brancos de 1,5 px entre as fatias; sem destacar/explodir fatias.
- Rótulo de % em cada fatia (sem casas decimais), negrito, cor #1A1A1A. Legenda à direita com o nome do canal.
IDENTIDADE VISUAL (CFOs.AI):
- Paleta: laranja principal #EF4517; tons de laranja para séries extras #F47D5D, #F9B4A2, #FCDAD1; cinzas para referência/secundário #BFBFBF e #8C8C8C; textos em #1A1A1A e #595959. Não use outras cores.
- Fundo branco (#FFFFFF) no gráfico e na página; sem bordas no gráfico, sem sombras, sem 3D, sem gradientes.
- Fonte: Calibri (fallback: Arial, sans-serif) em todo o gráfico.
- Título do gráfico: 18 px, negrito, cor #1A1A1A, alinhado à esquerda. Subtítulo logo abaixo: 13 px, cor #595959.
- Textos de eixos e legendas: 11–12 px, cor #595959. Linhas de eixo finas em #BFBFBF; linhas de grade finas em #E6E6E6; sem marcas de escala (ticks).
- Wordmark "CFOs.AI" no canto superior direito, texto em negrito na cor #EF4517. Rodapé à esquerda: "Fonte: dados fictícios · CFOs.AI" em 10 px, cor #8C8C8C.
- Números em formato brasileiro nos rótulos (ponto como separador de milhar e vírgula decimal; ex.: 1.234; 12,5%).
- Proporção 16:9 (960 × 540 px), margens generosas e nada de elementos decorativos extras.
ENTREGUE DUAS SAÍDAS, cada uma em um bloco de código separado e completo:
(a) Python: um único script executável (matplotlib + numpy, sem outras dependências), com os dados declarados no próprio script, que aplica todas as especificações acima e salva o gráfico em "pizza.png" (dpi 200, fundo branco). Ao final, chame plt.close().
(b) HTML: um único arquivo .html autocontido que carrega Tailwind CSS via CDN (<script src="https://cdn.tailwindcss.com"></script>) e Chart.js 4 via CDN (https://cdn.jsdelivr.net/npm/chart.js) (pie); mostre o gráfico em um card branco centralizado (max-w-4xl, padding generoso, sem sombra), com título, subtítulo, wordmark e rodapé em HTML, e as mesmas cores, fontes e dados.
Não explique demais: entregue o código pronto para rodar.
```

## 09 · Rosca

Aba: `09 Rosca` · Pergunta: Qual o peso de cada componente no CPV?

```text
Você é especialista em visualização de dados financeiros. Crie um gráfico de rosca (donut) com o título "Composição do custo dos produtos vendidos · 2026" e o subtítulo "Qual o peso de cada componente no CPV?".
DADOS (fictícios; unidade: R$ mil). Use exatamente estes valores, sem inventar outros:
| Componente | Valor (R$ mil) | % do total |
|---|---|---|
| Matéria-prima | 4300 | 51,2% |
| Mão de obra direta | 2100 | 25,0% |
| Frete | 950 | 11,3% |
| Embalagem | 620 | 7,4% |
| Outros | 430 | 5,1% |
Total: 8.400
ESPECIFICAÇÃO DO GRÁFICO:
- Rosca com furo central de ~58% do raio; fatias no sentido horário a partir das 12h, na ordem da tabela, com cores #EF4517, #F47D5D, #F9B4A2, #BFBFBF, #8C8C8C.
- Separadores brancos de 1,5 px entre as fatias.
- No centro, o total "R$ 8.400 mil" em negrito 22 px #1A1A1A e a palavra "CPV" em 12 px #595959 logo abaixo.
- Rótulo de % sobre cada fatia (sem casas decimais) e legenda à direita com nome e valor.
IDENTIDADE VISUAL (CFOs.AI):
- Paleta: laranja principal #EF4517; tons de laranja para séries extras #F47D5D, #F9B4A2, #FCDAD1; cinzas para referência/secundário #BFBFBF e #8C8C8C; textos em #1A1A1A e #595959. Não use outras cores.
- Fundo branco (#FFFFFF) no gráfico e na página; sem bordas no gráfico, sem sombras, sem 3D, sem gradientes.
- Fonte: Calibri (fallback: Arial, sans-serif) em todo o gráfico.
- Título do gráfico: 18 px, negrito, cor #1A1A1A, alinhado à esquerda. Subtítulo logo abaixo: 13 px, cor #595959.
- Textos de eixos e legendas: 11–12 px, cor #595959. Linhas de eixo finas em #BFBFBF; linhas de grade finas em #E6E6E6; sem marcas de escala (ticks).
- Wordmark "CFOs.AI" no canto superior direito, texto em negrito na cor #EF4517. Rodapé à esquerda: "Fonte: dados fictícios · CFOs.AI" em 10 px, cor #8C8C8C.
- Números em formato brasileiro nos rótulos (ponto como separador de milhar e vírgula decimal; ex.: 1.234; 12,5%).
- Proporção 16:9 (960 × 540 px), margens generosas e nada de elementos decorativos extras.
ENTREGUE DUAS SAÍDAS, cada uma em um bloco de código separado e completo:
(a) Python: um único script executável (matplotlib + numpy, sem outras dependências), com os dados declarados no próprio script, que aplica todas as especificações acima e salva o gráfico em "rosca.png" (dpi 200, fundo branco). Ao final, chame plt.close().
(b) HTML: um único arquivo .html autocontido que carrega Tailwind CSS via CDN (<script src="https://cdn.tailwindcss.com"></script>) e Chart.js 4 via CDN (https://cdn.jsdelivr.net/npm/chart.js) (doughnut, cutout 58%); mostre o gráfico em um card branco centralizado (max-w-4xl, padding generoso, sem sombra), com título, subtítulo, wordmark e rodapé em HTML, e as mesmas cores, fontes e dados.
Não explique demais: entregue o código pronto para rodar.
```

## 10 · Dispersão

Aba: `10 Dispersão` · Pergunta: Mais investimento comercial vem acompanhado de mais receita nova?

```text
Você é especialista em visualização de dados financeiros. Crie um gráfico de dispersão (scatter) com linha de tendência com o título "Investimento em marketing vs. receita nova · 2026" e o subtítulo "Mais investimento comercial vem acompanhado de mais receita nova?".
DADOS (fictícios; unidade: R$ mil). Use exatamente estes valores, sem inventar outros:
| Mês | Investimento em marketing | Receita nova |
|---|---|---|
| Jan | 80 | 410 |
| Fev | 95 | 450 |
| Mar | 110 | 520 |
| Abr | 105 | 480 |
| Mai | 130 | 590 |
| Jun | 150 | 640 |
| Jul | 140 | 600 |
| Ago | 165 | 700 |
| Set | 180 | 760 |
| Out | 175 | 720 |
| Nov | 200 | 820 |
| Dez | 220 | 880 |
ESPECIFICAÇÃO DO GRÁFICO:
- Cada mês é um ponto: X = investimento em marketing, Y = receita nova. Marcadores circulares de 8 px em #EF4517 com borda branca fina.
- Linha de tendência linear (mínimos quadrados) tracejada cinza #8C8C8C, 1,25 px, legendada "Tendência linear".
- Eixo X de 60 a 240 com título "Investimento em marketing (R$ mil)"; eixo Y de 300 a 950 com título "Receita nova (R$ mil)"; grade fina nos dois eixos.
- Rótulo com o nome do mês ao lado de cada ponto em 9 px, cor #595959. Legenda embaixo.
IDENTIDADE VISUAL (CFOs.AI):
- Paleta: laranja principal #EF4517; tons de laranja para séries extras #F47D5D, #F9B4A2, #FCDAD1; cinzas para referência/secundário #BFBFBF e #8C8C8C; textos em #1A1A1A e #595959. Não use outras cores.
- Fundo branco (#FFFFFF) no gráfico e na página; sem bordas no gráfico, sem sombras, sem 3D, sem gradientes.
- Fonte: Calibri (fallback: Arial, sans-serif) em todo o gráfico.
- Título do gráfico: 18 px, negrito, cor #1A1A1A, alinhado à esquerda. Subtítulo logo abaixo: 13 px, cor #595959.
- Textos de eixos e legendas: 11–12 px, cor #595959. Linhas de eixo finas em #BFBFBF; linhas de grade finas em #E6E6E6; sem marcas de escala (ticks).
- Wordmark "CFOs.AI" no canto superior direito, texto em negrito na cor #EF4517. Rodapé à esquerda: "Fonte: dados fictícios · CFOs.AI" em 10 px, cor #8C8C8C.
- Números em formato brasileiro nos rótulos (ponto como separador de milhar e vírgula decimal; ex.: 1.234; 12,5%).
- Proporção 16:9 (960 × 540 px), margens generosas e nada de elementos decorativos extras.
ENTREGUE DUAS SAÍDAS, cada uma em um bloco de código separado e completo:
(a) Python: um único script executável (matplotlib + numpy, sem outras dependências), com os dados declarados no próprio script, que aplica todas as especificações acima e salva o gráfico em "dispersao.png" (dpi 200, fundo branco). Ao final, chame plt.close().
(b) HTML: um único arquivo .html autocontido que carrega Tailwind CSS via CDN (<script src="https://cdn.tailwindcss.com"></script>) e Chart.js 4 via CDN (https://cdn.jsdelivr.net/npm/chart.js) (scatter); mostre o gráfico em um card branco centralizado (max-w-4xl, padding generoso, sem sombra), com título, subtítulo, wordmark e rodapé em HTML, e as mesmas cores, fontes e dados.
Não explique demais: entregue o código pronto para rodar.
```

## 11 · Bolhas

Aba: `11 Bolhas` · Pergunta: Quais unidades combinam escala, rentabilidade e tamanho de equipe?

```text
Você é especialista em visualização de dados financeiros. Crie um gráfico de bolhas com o título "Unidades de negócio: receita, margem e equipe · 2026" e o subtítulo "Quais unidades combinam escala, rentabilidade e tamanho de equipe?".
DADOS (fictícios; unidade: R$ mil). Use exatamente estes valores, sem inventar outros:
| Unidade | Receita (R$ mil) | Margem EBITDA | Colaboradores (nº) |
|---|---|---|---|
| Varejo | 9800 | 14% | 420 |
| Atacado | 6200 | 9% | 160 |
| E-commerce | 5100 | 18% | 95 |
| Serviços | 2400 | 26% | 110 |
| Franquias | 1800 | 31% | 25 |
| Exportação | 3300 | 12% | 60 |
ESPECIFICAÇÃO DO GRÁFICO:
- X = Receita (R$ mil), Y = Margem EBITDA (%), tamanho (área) da bolha proporcional ao nº de colaboradores.
- Bolhas em #EF4517 com 65% de opacidade e borda #EF4517 de 1 px; a maior bolha com ~70 px de diâmetro.
- Nome da unidade no centro da bolha (ou ao lado, se ela for pequena) em 10 px negrito, cor #1A1A1A.
- Eixo X de 0 a 12.000 (passo 2.000) com título "Receita (R$ mil)"; eixo Y de 0% a 40% (passo 10%) com título "Margem EBITDA"; grade fina.
- Nota pequena no canto inferior direito: "Tamanho da bolha = nº de colaboradores", cor #8C8C8C. Sem legenda.
IDENTIDADE VISUAL (CFOs.AI):
- Paleta: laranja principal #EF4517; tons de laranja para séries extras #F47D5D, #F9B4A2, #FCDAD1; cinzas para referência/secundário #BFBFBF e #8C8C8C; textos em #1A1A1A e #595959. Não use outras cores.
- Fundo branco (#FFFFFF) no gráfico e na página; sem bordas no gráfico, sem sombras, sem 3D, sem gradientes.
- Fonte: Calibri (fallback: Arial, sans-serif) em todo o gráfico.
- Título do gráfico: 18 px, negrito, cor #1A1A1A, alinhado à esquerda. Subtítulo logo abaixo: 13 px, cor #595959.
- Textos de eixos e legendas: 11–12 px, cor #595959. Linhas de eixo finas em #BFBFBF; linhas de grade finas em #E6E6E6; sem marcas de escala (ticks).
- Wordmark "CFOs.AI" no canto superior direito, texto em negrito na cor #EF4517. Rodapé à esquerda: "Fonte: dados fictícios · CFOs.AI" em 10 px, cor #8C8C8C.
- Números em formato brasileiro nos rótulos (ponto como separador de milhar e vírgula decimal; ex.: 1.234; 12,5%).
- Proporção 16:9 (960 × 540 px), margens generosas e nada de elementos decorativos extras.
ENTREGUE DUAS SAÍDAS, cada uma em um bloco de código separado e completo:
(a) Python: um único script executável (matplotlib + numpy, sem outras dependências), com os dados declarados no próprio script, que aplica todas as especificações acima e salva o gráfico em "bolhas.png" (dpi 200, fundo branco). Ao final, chame plt.close().
(b) HTML: um único arquivo .html autocontido que carrega Tailwind CSS via CDN (<script src="https://cdn.tailwindcss.com"></script>) e Chart.js 4 via CDN (https://cdn.jsdelivr.net/npm/chart.js) (bubble); mostre o gráfico em um card branco centralizado (max-w-4xl, padding generoso, sem sombra), com título, subtítulo, wordmark e rodapé em HTML, e as mesmas cores, fontes e dados.
Não explique demais: entregue o código pronto para rodar.
```

## 12 · Radar

Aba: `12 Radar` · Pergunta: Em quais dimensões estamos mais distantes da meta?

```text
Você é especialista em visualização de dados financeiros. Crie um gráfico de radar (teia) com o título "Maturidade da área financeira (0 a 5)" e o subtítulo "Em quais dimensões estamos mais distantes da meta?".
DADOS (fictícios; unidade: notas de 0 a 5). Use exatamente estes valores, sem inventar outros:
| Dimensão | Atual | Meta 2027 |
|---|---|---|
| Fechamento contábil | 3.5 | 4.5 |
| Planejamento (FP&A) | 2.5 | 4.0 |
| Tesouraria | 4.0 | 4.5 |
| Controles internos | 3.0 | 4.0 |
| Dados e BI | 2.0 | 4.0 |
| Automação | 1.5 | 3.5 |
ESPECIFICAÇÃO DO GRÁFICO:
- Seis eixos, um por dimensão, na ordem da tabela, começando no topo e seguindo no sentido horário.
- Escala radial de 0 a 5 com anéis a cada 1 ponto, grade fina #E6E6E6, números da escala em 9 px #595959.
- Série "Atual": linha #EF4517 de 2,5 px com marcadores circulares e preenchimento #EF4517 a 15% de opacidade.
- Série "Meta 2027": linha tracejada cinza #8C8C8C de 1,25 px, sem preenchimento e sem marcadores.
- Rótulos das dimensões fora do círculo em 11 px #1A1A1A. Legenda embaixo.
IDENTIDADE VISUAL (CFOs.AI):
- Paleta: laranja principal #EF4517; tons de laranja para séries extras #F47D5D, #F9B4A2, #FCDAD1; cinzas para referência/secundário #BFBFBF e #8C8C8C; textos em #1A1A1A e #595959. Não use outras cores.
- Fundo branco (#FFFFFF) no gráfico e na página; sem bordas no gráfico, sem sombras, sem 3D, sem gradientes.
- Fonte: Calibri (fallback: Arial, sans-serif) em todo o gráfico.
- Título do gráfico: 18 px, negrito, cor #1A1A1A, alinhado à esquerda. Subtítulo logo abaixo: 13 px, cor #595959.
- Textos de eixos e legendas: 11–12 px, cor #595959. Linhas de eixo finas em #BFBFBF; linhas de grade finas em #E6E6E6; sem marcas de escala (ticks).
- Wordmark "CFOs.AI" no canto superior direito, texto em negrito na cor #EF4517. Rodapé à esquerda: "Fonte: dados fictícios · CFOs.AI" em 10 px, cor #8C8C8C.
- Números em formato brasileiro nos rótulos (ponto como separador de milhar e vírgula decimal; ex.: 1.234; 12,5%).
- Proporção 16:9 (960 × 540 px), margens generosas e nada de elementos decorativos extras.
ENTREGUE DUAS SAÍDAS, cada uma em um bloco de código separado e completo:
(a) Python: um único script executável (matplotlib + numpy, sem outras dependências), com os dados declarados no próprio script, que aplica todas as especificações acima e salva o gráfico em "radar.png" (dpi 200, fundo branco). Ao final, chame plt.close().
(b) HTML: um único arquivo .html autocontido que carrega Tailwind CSS via CDN (<script src="https://cdn.tailwindcss.com"></script>) e Chart.js 4 via CDN (https://cdn.jsdelivr.net/npm/chart.js) (radar); mostre o gráfico em um card branco centralizado (max-w-4xl, padding generoso, sem sombra), com título, subtítulo, wordmark e rodapé em HTML, e as mesmas cores, fontes e dados.
Não explique demais: entregue o código pronto para rodar.
```

## 13 · Histograma

Aba: `13 Histograma` · Pergunta: Em quais faixas de dias se concentram os recebimentos?

```text
Você é especialista em visualização de dados financeiros. Crie um gráfico de histograma (faixas já agrupadas) com o título "Distribuição do prazo de recebimento das faturas · 2026" e o subtítulo "Em quais faixas de dias se concentram os recebimentos?".
DADOS (fictícios; unidade: quantidade de faturas). Use exatamente estes valores, sem inventar outros:
| Faixa (dias) | Nº de faturas |
|---|---|
| 0–15 | 42 |
| 16–30 | 118 |
| 31–45 | 96 |
| 46–60 | 51 |
| 61–75 | 24 |
| 76–90 | 12 |
| > 90 | 7 |
Total de faturas: 350
ESPECIFICAÇÃO DO GRÁFICO:
- Os dados já estão agrupados em faixas de 15 dias: desenhe uma barra por faixa, sem recalcular as faixas.
- Barras encostadas (separação branca de ~1 px), cor #EF4517.
- Eixo X com os rótulos das faixas e título "Prazo de recebimento (dias)"; eixo Y a partir de zero com título "Nº de faturas"; grade horizontal fina.
- Rótulo da contagem acima de cada barra em 11 px #1A1A1A. Sem legenda.
IDENTIDADE VISUAL (CFOs.AI):
- Paleta: laranja principal #EF4517; tons de laranja para séries extras #F47D5D, #F9B4A2, #FCDAD1; cinzas para referência/secundário #BFBFBF e #8C8C8C; textos em #1A1A1A e #595959. Não use outras cores.
- Fundo branco (#FFFFFF) no gráfico e na página; sem bordas no gráfico, sem sombras, sem 3D, sem gradientes.
- Fonte: Calibri (fallback: Arial, sans-serif) em todo o gráfico.
- Título do gráfico: 18 px, negrito, cor #1A1A1A, alinhado à esquerda. Subtítulo logo abaixo: 13 px, cor #595959.
- Textos de eixos e legendas: 11–12 px, cor #595959. Linhas de eixo finas em #BFBFBF; linhas de grade finas em #E6E6E6; sem marcas de escala (ticks).
- Wordmark "CFOs.AI" no canto superior direito, texto em negrito na cor #EF4517. Rodapé à esquerda: "Fonte: dados fictícios · CFOs.AI" em 10 px, cor #8C8C8C.
- Números em formato brasileiro nos rótulos (ponto como separador de milhar e vírgula decimal; ex.: 1.234; 12,5%).
- Proporção 16:9 (960 × 540 px), margens generosas e nada de elementos decorativos extras.
ENTREGUE DUAS SAÍDAS, cada uma em um bloco de código separado e completo:
(a) Python: um único script executável (matplotlib + numpy, sem outras dependências), com os dados declarados no próprio script, que aplica todas as especificações acima e salva o gráfico em "histograma.png" (dpi 200, fundo branco). Ao final, chame plt.close().
(b) HTML: um único arquivo .html autocontido que carrega Tailwind CSS via CDN (<script src="https://cdn.tailwindcss.com"></script>) e Chart.js 4 via CDN (https://cdn.jsdelivr.net/npm/chart.js) (bar com barPercentage 1 e categoryPercentage 1); mostre o gráfico em um card branco centralizado (max-w-4xl, padding generoso, sem sombra), com título, subtítulo, wordmark e rodapé em HTML, e as mesmas cores, fontes e dados.
Não explique demais: entregue o código pronto para rodar.
```

## 14 · Cascata (ponte do EBITDA)

Aba: `14 Cascata` · Pergunta: O que explica a variação do EBITDA de um ano para o outro?

```text
Você é especialista em visualização de dados financeiros. Crie um gráfico de cascata (waterfall / ponte do EBITDA) com o título "Ponte do EBITDA · 2025 → 2026" e o subtítulo "O que explica a variação do EBITDA de um ano para o outro?".
DADOS (fictícios; unidade: R$ mil). Use exatamente estes valores, sem inventar outros:
| Etapa | Tipo | Valor | Acumulado |
|---|---|---|---|
| EBITDA 2025 | total inicial | 7800 | 7800 |
| Volume de vendas | variação | +1450 | 9250 |
| Preço | variação | +820 | 10070 |
| Mix de produtos | variação | -310 | 9760 |
| Custo de insumos | variação | -960 | 8800 |
| Despesas com pessoal | variação | -540 | 8260 |
| Eficiência operacional | variação | +390 | 8650 |
| EBITDA 2026 | total final (calculado) | 8650 | 8650 |
ESPECIFICAÇÃO DO GRÁFICO:
- Colunas na ordem da tabela. "EBITDA 2025" e "EBITDA 2026" são colunas cheias que partem do zero.
- As variações são colunas flutuantes: cada uma começa onde terminou o acumulado anterior e vai até o novo acumulado.
- Cores: totais em #EF4517; aumentos em laranja claro #F9B4A2; reduções em cinza #BFBFBF.
- Linhas conectoras horizontais finas (#BFBFBF, 0,75 px, tracejadas) ligando o topo de cada coluna ao início da próxima.
- Rótulos: totais com o valor (ex.: 7.800) em negrito; variações com sinal (ex.: +1.450 e −960) em 10 px #1A1A1A.
- Eixo Y a partir de zero, formato de milhar, título "R$ mil"; grade horizontal fina. Rótulos do eixo X podem quebrar em 2 linhas.
- Legenda embaixo com três itens: Total, Aumento, Redução.
IDENTIDADE VISUAL (CFOs.AI):
- Paleta: laranja principal #EF4517; tons de laranja para séries extras #F47D5D, #F9B4A2, #FCDAD1; cinzas para referência/secundário #BFBFBF e #8C8C8C; textos em #1A1A1A e #595959. Não use outras cores.
- Fundo branco (#FFFFFF) no gráfico e na página; sem bordas no gráfico, sem sombras, sem 3D, sem gradientes.
- Fonte: Calibri (fallback: Arial, sans-serif) em todo o gráfico.
- Título do gráfico: 18 px, negrito, cor #1A1A1A, alinhado à esquerda. Subtítulo logo abaixo: 13 px, cor #595959.
- Textos de eixos e legendas: 11–12 px, cor #595959. Linhas de eixo finas em #BFBFBF; linhas de grade finas em #E6E6E6; sem marcas de escala (ticks).
- Wordmark "CFOs.AI" no canto superior direito, texto em negrito na cor #EF4517. Rodapé à esquerda: "Fonte: dados fictícios · CFOs.AI" em 10 px, cor #8C8C8C.
- Números em formato brasileiro nos rótulos (ponto como separador de milhar e vírgula decimal; ex.: 1.234; 12,5%).
- Proporção 16:9 (960 × 540 px), margens generosas e nada de elementos decorativos extras.
ENTREGUE DUAS SAÍDAS, cada uma em um bloco de código separado e completo:
(a) Python: um único script executável (matplotlib + numpy, sem outras dependências), com os dados declarados no próprio script, que aplica todas as especificações acima e salva o gráfico em "cascata.png" (dpi 200, fundo branco). Ao final, chame plt.close(). Implemente a cascata com ax.bar usando o parâmetro bottom (base invisível).
(b) HTML: um único arquivo .html autocontido que carrega Tailwind CSS via CDN (<script src="https://cdn.tailwindcss.com"></script>) e Chart.js 4 via CDN (https://cdn.jsdelivr.net/npm/chart.js) (barras flutuantes: cada dado como [início, fim]); mostre o gráfico em um card branco centralizado (max-w-4xl, padding generoso, sem sombra), com título, subtítulo, wordmark e rodapé em HTML, e as mesmas cores, fontes e dados.
Não explique demais: entregue o código pronto para rodar.
```

## 15 · Gantt (fechamento mensal)

Aba: `15 Gantt` · Pergunta: Quais etapas do fechamento acontecem ao mesmo tempo até o D+8?

```text
Você é especialista em visualização de dados financeiros. Crie um gráfico de Gantt (cronograma em barras horizontais) com o título "Cronograma do fechamento mensal (dias úteis)" e o subtítulo "Quais etapas do fechamento acontecem ao mesmo tempo até o D+8?".
DADOS (fictícios; unidade: dias úteis). Use exatamente estes valores, sem inventar outros:
| Etapa | Responsável | Início (dia útil) | Duração (dias) | Fim (dia útil) |
|---|---|---|---|---|
| Corte de faturamento e vendas | Faturamento | 1 | 1 | 1 |
| Conciliações bancárias | Tesouraria | 1 | 2 | 2 |
| Provisões e apropriações | Contabilidade | 2 | 2 | 3 |
| Inventário e custo dos estoques | Custos | 2 | 3 | 4 |
| Impostos e apurações | Fiscal | 3 | 2 | 4 |
| Consolidação e eliminações | Contabilidade | 4 | 2 | 5 |
| Revisão analítica (DRE/BP) | Controladoria | 5 | 2 | 6 |
| Relatório gerencial | FP&A | 6 | 2 | 7 |
| Reunião de resultados | CFO | 8 | 1 | 8 |
ESPECIFICAÇÃO DO GRÁFICO:
- Uma barra horizontal por etapa, na ordem da tabela de cima para baixo. A barra vai de (Início − 1) até (Início − 1 + Duração) no eixo X; ex.: início 2 e duração 3 ocupa de 1 a 4 (D2 a D4).
- Barras em #EF4517, cantos levemente arredondados (raio 3 px), com a duração escrita dentro em branco negrito (ex.: "3 d").
- Nome da etapa à esquerda; o responsável em cinza #8C8C8C, entre parênteses após o nome.
- Eixo X de 0 a 9 com marcas inteiras rotuladas D+0 … D+9 (a marca k = fim do dia útil k), título "Dias úteis após o fim do mês (fim do dia)" e grade vertical fina #E6E6E6.
- Linha vertical tracejada #8C8C8C em x = 8 com o texto "Meta: resultado no D+8". Sem legenda.
IDENTIDADE VISUAL (CFOs.AI):
- Paleta: laranja principal #EF4517; tons de laranja para séries extras #F47D5D, #F9B4A2, #FCDAD1; cinzas para referência/secundário #BFBFBF e #8C8C8C; textos em #1A1A1A e #595959. Não use outras cores.
- Fundo branco (#FFFFFF) no gráfico e na página; sem bordas no gráfico, sem sombras, sem 3D, sem gradientes.
- Fonte: Calibri (fallback: Arial, sans-serif) em todo o gráfico.
- Título do gráfico: 18 px, negrito, cor #1A1A1A, alinhado à esquerda. Subtítulo logo abaixo: 13 px, cor #595959.
- Textos de eixos e legendas: 11–12 px, cor #595959. Linhas de eixo finas em #BFBFBF; linhas de grade finas em #E6E6E6; sem marcas de escala (ticks).
- Wordmark "CFOs.AI" no canto superior direito, texto em negrito na cor #EF4517. Rodapé à esquerda: "Fonte: dados fictícios · CFOs.AI" em 10 px, cor #8C8C8C.
- Números em formato brasileiro nos rótulos (ponto como separador de milhar e vírgula decimal; ex.: 1.234; 12,5%).
- Proporção 16:9 (960 × 540 px), margens generosas e nada de elementos decorativos extras.
ENTREGUE DUAS SAÍDAS, cada uma em um bloco de código separado e completo:
(a) Python: um único script executável (matplotlib + numpy, sem outras dependências), com os dados declarados no próprio script, que aplica todas as especificações acima e salva o gráfico em "gantt.png" (dpi 200, fundo branco). Ao final, chame plt.close(). Implemente com ax.barh usando o parâmetro left (= Início − 1).
(b) HTML: um único arquivo .html autocontido que carrega Tailwind CSS via CDN (<script src="https://cdn.tailwindcss.com"></script>) e Chart.js 4 via CDN (https://cdn.jsdelivr.net/npm/chart.js) (barras flutuantes com indexAxis: 'y') ou SVG puro; mostre o gráfico em um card branco centralizado (max-w-4xl, padding generoso, sem sombra), com título, subtítulo, wordmark e rodapé em HTML, e as mesmas cores, fontes e dados.
Não explique demais: entregue o código pronto para rodar.
```

## 16 · Slopegraph

Aba: `16 Slopegraph` · Pergunta: Quais linhas ganharam e quais perderam margem?

```text
Você é especialista em visualização de dados financeiros. Crie um gráfico de slopegraph (gráfico de inclinação) com o título "Margem bruta por linha de produto · 2025 vs. 2026" e o subtítulo "Quais linhas ganharam e quais perderam margem?".
DADOS (fictícios; unidade: % da receita). Use exatamente estes valores, sem inventar outros:
| Linha de produto | 2025 | 2026 |
|---|---|---|
| Linha A | 18% | 24% |
| Linha B | 22% | 21% |
| Linha C | 15% | 19% |
| Linha D | 27% | 23% |
| Linha E | 12% | 16% |
ESPECIFICAÇÃO DO GRÁFICO:
- Duas colunas verticais imaginárias: 2025 à esquerda e 2026 à direita (rótulos "2025" e "2026" em negrito no topo).
- Para cada linha de produto, um segmento de reta ligando a margem de 2025 à de 2026, com marcadores circulares nas duas pontas.
- Cores: linhas que melhoraram em laranja (Linha A #EF4517, Linha C #F47D5D, Linha E #F9B4A2); linhas que pioraram em cinza (Linha B #BFBFBF, Linha D #8C8C8C).
- Rótulos à esquerda do ponto de 2025 ("Linha A 18%") e à direita do ponto de 2026 ("24%"), 11 px, cor #1A1A1A; afaste verticalmente se colidirem.
- Escala vertical de 10% a 30%, sem eixo Y visível e sem grade. Sem legenda (os rótulos identificam as linhas).
IDENTIDADE VISUAL (CFOs.AI):
- Paleta: laranja principal #EF4517; tons de laranja para séries extras #F47D5D, #F9B4A2, #FCDAD1; cinzas para referência/secundário #BFBFBF e #8C8C8C; textos em #1A1A1A e #595959. Não use outras cores.
- Fundo branco (#FFFFFF) no gráfico e na página; sem bordas no gráfico, sem sombras, sem 3D, sem gradientes.
- Fonte: Calibri (fallback: Arial, sans-serif) em todo o gráfico.
- Título do gráfico: 18 px, negrito, cor #1A1A1A, alinhado à esquerda. Subtítulo logo abaixo: 13 px, cor #595959.
- Textos de eixos e legendas: 11–12 px, cor #595959. Linhas de eixo finas em #BFBFBF; linhas de grade finas em #E6E6E6; sem marcas de escala (ticks).
- Wordmark "CFOs.AI" no canto superior direito, texto em negrito na cor #EF4517. Rodapé à esquerda: "Fonte: dados fictícios · CFOs.AI" em 10 px, cor #8C8C8C.
- Números em formato brasileiro nos rótulos (ponto como separador de milhar e vírgula decimal; ex.: 1.234; 12,5%).
- Proporção 16:9 (960 × 540 px), margens generosas e nada de elementos decorativos extras.
ENTREGUE DUAS SAÍDAS, cada uma em um bloco de código separado e completo:
(a) Python: um único script executável (matplotlib + numpy, sem outras dependências), com os dados declarados no próprio script, que aplica todas as especificações acima e salva o gráfico em "slope.png" (dpi 200, fundo branco). Ao final, chame plt.close().
(b) HTML: um único arquivo .html autocontido que carrega Tailwind CSS via CDN (<script src="https://cdn.tailwindcss.com"></script>) e Chart.js 4 via CDN (https://cdn.jsdelivr.net/npm/chart.js) (line) ou SVG puro; mostre o gráfico em um card branco centralizado (max-w-4xl, padding generoso, sem sombra), com título, subtítulo, wordmark e rodapé em HTML, e as mesmas cores, fontes e dados.
Não explique demais: entregue o código pronto para rodar.
```

## 17 · Barras divergentes

Aba: `17 Barras divergentes` · Pergunta: Quais áreas gastaram acima do orçado e quais economizaram?

```text
Você é especialista em visualização de dados financeiros. Crie um gráfico de barras divergentes (horizontais, a partir do zero) com o título "Desvio das despesas vs. orçamento por área · 2026" e o subtítulo "Quais áreas gastaram acima do orçado e quais economizaram?".
DADOS (fictícios; unidade: R$ mil e % sobre o orçado). Use exatamente estes valores, sem inventar outros:
| Área | Orçado (R$ mil) | Realizado (R$ mil) | Desvio % |
|---|---|---|---|
| Tecnologia | 1500 | 1680 | +12,0% |
| Comercial | 2400 | 2604 | +8,5% |
| Logística | 1800 | 1921 | +6,7% |
| Operações | 3200 | 3341 | +4,4% |
| Financeiro | 900 | 886 | -1,6% |
| Recursos Humanos | 1100 | 1066 | -3,1% |
| Marketing | 1300 | 1219 | -6,2% |
| Jurídico | 600 | 541 | -9,8% |
ESPECIFICAÇÃO DO GRÁFICO:
- Desvio % = Realizado ÷ Orçado − 1 (já calculado). Uma barra horizontal por área, na ordem da tabela (maior estouro no topo).
- Barras saindo de uma linha vertical de zero (#595959, 1 px): desvios positivos (gastou acima) para a direita em #EF4517; negativos (economizou) para a esquerda em cinza #BFBFBF.
- Nomes das áreas alinhados à esquerda, fora da área das barras (não sobre o zero).
- Rótulo com sinal e 1 casa decimal na ponta de cada barra (ex.: +12,0% e −9,8%), 11 px #1A1A1A.
- Eixo X de −15% a +15% com marcas a cada 5% e título "Desvio vs. orçado"; grade vertical fina.
- Legenda embaixo: "Acima do orçado" e "Abaixo do orçado".
IDENTIDADE VISUAL (CFOs.AI):
- Paleta: laranja principal #EF4517; tons de laranja para séries extras #F47D5D, #F9B4A2, #FCDAD1; cinzas para referência/secundário #BFBFBF e #8C8C8C; textos em #1A1A1A e #595959. Não use outras cores.
- Fundo branco (#FFFFFF) no gráfico e na página; sem bordas no gráfico, sem sombras, sem 3D, sem gradientes.
- Fonte: Calibri (fallback: Arial, sans-serif) em todo o gráfico.
- Título do gráfico: 18 px, negrito, cor #1A1A1A, alinhado à esquerda. Subtítulo logo abaixo: 13 px, cor #595959.
- Textos de eixos e legendas: 11–12 px, cor #595959. Linhas de eixo finas em #BFBFBF; linhas de grade finas em #E6E6E6; sem marcas de escala (ticks).
- Wordmark "CFOs.AI" no canto superior direito, texto em negrito na cor #EF4517. Rodapé à esquerda: "Fonte: dados fictícios · CFOs.AI" em 10 px, cor #8C8C8C.
- Números em formato brasileiro nos rótulos (ponto como separador de milhar e vírgula decimal; ex.: 1.234; 12,5%).
- Proporção 16:9 (960 × 540 px), margens generosas e nada de elementos decorativos extras.
ENTREGUE DUAS SAÍDAS, cada uma em um bloco de código separado e completo:
(a) Python: um único script executável (matplotlib + numpy, sem outras dependências), com os dados declarados no próprio script, que aplica todas as especificações acima e salva o gráfico em "divergentes.png" (dpi 200, fundo branco). Ao final, chame plt.close().
(b) HTML: um único arquivo .html autocontido que carrega Tailwind CSS via CDN (<script src="https://cdn.tailwindcss.com"></script>) e Chart.js 4 via CDN (https://cdn.jsdelivr.net/npm/chart.js) (indexAxis: 'y', cor por barra); mostre o gráfico em um card branco centralizado (max-w-4xl, padding generoso, sem sombra), com título, subtítulo, wordmark e rodapé em HTML, e as mesmas cores, fontes e dados.
Não explique demais: entregue o código pronto para rodar.
```

## 18 · Mapa de calor

Aba: `18 Mapa de calor` · Pergunta: Onde e quando a receita se concentra? Há sazonalidade?

```text
Você é especialista em visualização de dados financeiros. Crie um gráfico de mapa de calor (heatmap) em matriz com o título "Receita por regional e mês · 2026" e o subtítulo "Onde e quando a receita se concentra? Há sazonalidade?".
DADOS (fictícios; unidade: R$ mil). Use exatamente estes valores, sem inventar outros:
| Regional | Jan | Fev | Mar | Abr | Mai | Jun | Jul | Ago | Set | Out | Nov | Dez |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| Norte | 310 | 295 | 330 | 345 | 360 | 350 | 340 | 365 | 375 | 390 | 420 | 520 |
| Nordeste | 420 | 400 | 445 | 460 | 470 | 455 | 450 | 480 | 495 | 520 | 560 | 695 |
| Centro-Oeste | 300 | 290 | 315 | 320 | 335 | 340 | 330 | 345 | 330 | 325 | 330 | 340 |
| Sudeste | 690 | 660 | 720 | 750 | 780 | 770 | 760 | 800 | 820 | 860 | 950 | 1140 |
| Sul | 480 | 455 | 500 | 515 | 530 | 520 | 505 | 535 | 545 | 560 | 600 | 655 |
ESPECIFICAÇÃO DO GRÁFICO:
- Matriz com as regionais nas linhas (ordem da tabela) e os meses Jan–Dez nas colunas; cada célula é um retângulo com o valor escrito no centro.
- Escala de cor contínua de uma só cor: branco #FFFFFF no menor valor da matriz até laranja #EF4517 no maior (interpolação linear).
- Texto do valor em 11 px: #1A1A1A nas células claras e branco nas células com mais de 60% da intensidade.
- Separadores brancos de 2 px entre as células; nomes das regionais à esquerda e meses no topo, em #595959.
- Coluna extra à direita com o total anual de cada regional em negrito (sem cor de fundo).
- Barra de legenda horizontal pequena abaixo da matriz indicando "menor → maior".
IDENTIDADE VISUAL (CFOs.AI):
- Paleta: laranja principal #EF4517; tons de laranja para séries extras #F47D5D, #F9B4A2, #FCDAD1; cinzas para referência/secundário #BFBFBF e #8C8C8C; textos em #1A1A1A e #595959. Não use outras cores.
- Fundo branco (#FFFFFF) no gráfico e na página; sem bordas no gráfico, sem sombras, sem 3D, sem gradientes.
- Fonte: Calibri (fallback: Arial, sans-serif) em todo o gráfico.
- Título do gráfico: 18 px, negrito, cor #1A1A1A, alinhado à esquerda. Subtítulo logo abaixo: 13 px, cor #595959.
- Textos de eixos e legendas: 11–12 px, cor #595959. Linhas de eixo finas em #BFBFBF; linhas de grade finas em #E6E6E6; sem marcas de escala (ticks).
- Wordmark "CFOs.AI" no canto superior direito, texto em negrito na cor #EF4517. Rodapé à esquerda: "Fonte: dados fictícios · CFOs.AI" em 10 px, cor #8C8C8C.
- Números em formato brasileiro nos rótulos (ponto como separador de milhar e vírgula decimal; ex.: 1.234; 12,5%).
- Proporção 16:9 (960 × 540 px), margens generosas e nada de elementos decorativos extras.
ENTREGUE DUAS SAÍDAS, cada uma em um bloco de código separado e completo:
(a) Python: um único script executável (matplotlib + numpy, sem outras dependências), com os dados declarados no próprio script, que aplica todas as especificações acima e salva o gráfico em "heatmap.png" (dpi 200, fundo branco). Ao final, chame plt.close(). Use ax.imshow com um LinearSegmentedColormap de branco para #EF4517.
(b) HTML: um único arquivo .html autocontido que carrega Tailwind CSS via CDN (<script src="https://cdn.tailwindcss.com"></script>) e nenhuma biblioteca de gráficos: monte a matriz com <table> ou CSS grid do Tailwind (ou SVG puro), calculando a cor de cada célula em JavaScript; mostre o gráfico em um card branco centralizado (max-w-4xl, padding generoso, sem sombra), com título, subtítulo, wordmark e rodapé em HTML, e as mesmas cores, fontes e dados.
Não explique demais: entregue o código pronto para rodar.
```

## 19 · Pareto

Aba: `19 Pareto` · Pergunta: Quais poucos motivos explicam a maior parte do valor devolvido?

```text
Você é especialista em visualização de dados financeiros. Crie um gráfico de Pareto (colunas + linha de % acumulado em eixo secundário) com o título "Devoluções por motivo · 2026" e o subtítulo "Quais poucos motivos explicam a maior parte do valor devolvido?".
DADOS (fictícios; unidade: R$ mil). Use exatamente estes valores, sem inventar outros:
| Motivo da devolução | Valor devolvido | % do total | % acumulado |
|---|---|---|---|
| Atraso na entrega | 420 | 36,8% | 36,8% |
| Produto avariado | 310 | 27,2% | 64,0% |
| Erro de faturamento | 180 | 15,8% | 79,8% |
| Pedido duplicado | 95 | 8,3% | 88,2% |
| Especificação incorreta | 70 | 6,1% | 94,3% |
| Arrependimento do cliente | 40 | 3,5% | 97,8% |
| Outros | 25 | 2,2% | 100,0% |
Total: 1.140
ESPECIFICAÇÃO DO GRÁFICO:
- Colunas com o valor devolvido por motivo, já ordenadas do maior para o menor ("Outros" por último), cor #EF4517, rótulo do valor dentro do topo da coluna em branco negrito.
- Linha do % acumulado no eixo Y secundário (direita, 0% a 100%, passo 20%), cor #404040, 1,5 px, marcadores circulares brancos com borda #404040 e rótulos de % (sem decimais) acima de cada ponto.
- Linha horizontal de referência tracejada cinza #8C8C8C em 80% no eixo secundário, com o texto "80%" à direita.
- Eixo Y principal (esquerda) de 0 a 500 com título "R$ mil"; grade horizontal fina só do eixo principal.
- Rótulos do eixo X podem quebrar em 2 linhas. Legenda embaixo: "Valor devolvido" e "% acumulado".
IDENTIDADE VISUAL (CFOs.AI):
- Paleta: laranja principal #EF4517; tons de laranja para séries extras #F47D5D, #F9B4A2, #FCDAD1; cinzas para referência/secundário #BFBFBF e #8C8C8C; textos em #1A1A1A e #595959. Não use outras cores.
- Fundo branco (#FFFFFF) no gráfico e na página; sem bordas no gráfico, sem sombras, sem 3D, sem gradientes.
- Fonte: Calibri (fallback: Arial, sans-serif) em todo o gráfico.
- Título do gráfico: 18 px, negrito, cor #1A1A1A, alinhado à esquerda. Subtítulo logo abaixo: 13 px, cor #595959.
- Textos de eixos e legendas: 11–12 px, cor #595959. Linhas de eixo finas em #BFBFBF; linhas de grade finas em #E6E6E6; sem marcas de escala (ticks).
- Wordmark "CFOs.AI" no canto superior direito, texto em negrito na cor #EF4517. Rodapé à esquerda: "Fonte: dados fictícios · CFOs.AI" em 10 px, cor #8C8C8C.
- Números em formato brasileiro nos rótulos (ponto como separador de milhar e vírgula decimal; ex.: 1.234; 12,5%).
- Proporção 16:9 (960 × 540 px), margens generosas e nada de elementos decorativos extras.
ENTREGUE DUAS SAÍDAS, cada uma em um bloco de código separado e completo:
(a) Python: um único script executável (matplotlib + numpy, sem outras dependências), com os dados declarados no próprio script, que aplica todas as especificações acima e salva o gráfico em "pareto.png" (dpi 200, fundo branco). Ao final, chame plt.close(). Use ax.twinx() para o eixo secundário.
(b) HTML: um único arquivo .html autocontido que carrega Tailwind CSS via CDN (<script src="https://cdn.tailwindcss.com"></script>) e Chart.js 4 via CDN (https://cdn.jsdelivr.net/npm/chart.js) (gráfico misto bar + line, com eixo y1 à direita); mostre o gráfico em um card branco centralizado (max-w-4xl, padding generoso, sem sombra), com título, subtítulo, wordmark e rodapé em HTML, e as mesmas cores, fontes e dados.
Não explique demais: entregue o código pronto para rodar.
```

## 20 · Linhas indexadas (base 100)

Aba: `20 Linhas indexadas` · Pergunta: O que cresceu mais rápido desde o início de 2025?

```text
Você é especialista em visualização de dados financeiros. Crie um gráfico de linhas indexadas (base 100) com o título "Receita, despesas e clientes · base 100 = T1/2025" e o subtítulo "O que cresceu mais rápido desde o início de 2025?".
DADOS (fictícios; unidade: R$ mil, nº de clientes e índice (base 100)). Use exatamente estes valores, sem inventar outros:
| Trimestre | Receita (R$ mil) | Despesas operacionais (R$ mil) | Clientes ativos (nº) | Receita (índice) | Despesas (índice) | Clientes (índice) |
|---|---|---|---|---|---|---|
| T1/25 | 4200 | 1500 | 1250 | 100,0 | 100,0 | 100,0 |
| T2/25 | 4350 | 1540 | 1300 | 103,6 | 102,7 | 104,0 |
| T3/25 | 4500 | 1600 | 1320 | 107,1 | 106,7 | 105,6 |
| T4/25 | 4800 | 1700 | 1400 | 114,3 | 113,3 | 112,0 |
| T1/26 | 4900 | 1780 | 1470 | 116,7 | 118,7 | 117,6 |
| T2/26 | 5150 | 1850 | 1520 | 122,6 | 123,3 | 121,6 |
| T3/26 | 5400 | 1950 | 1610 | 128,6 | 130,0 | 128,8 |
| T4/26 | 5800 | 2050 | 1700 | 138,1 | 136,7 | 136,0 |
ESPECIFICAÇÃO DO GRÁFICO:
- Índice = valor do trimestre ÷ valor do T1/25 × 100 (já calculado; recalcule a partir dos valores brutos para conferir).
- Três linhas com marcadores pequenos: Receita (índice) em #EF4517 2,75 px; Despesas (índice) em cinza #8C8C8C 2 px; Clientes (índice) em laranja claro #F9B4A2 2 px.
- Linha horizontal de referência fina #BFBFBF em 100.
- Eixo Y de 90 a 145 (passo 10) com título "Índice (T1/25 = 100)"; eixo X com os trimestres; grade horizontal fina.
- Rótulo no último ponto de cada linha com o nome curto e o índice (ex.: "Receita 138,1"), na cor da linha. Legenda embaixo.
IDENTIDADE VISUAL (CFOs.AI):
- Paleta: laranja principal #EF4517; tons de laranja para séries extras #F47D5D, #F9B4A2, #FCDAD1; cinzas para referência/secundário #BFBFBF e #8C8C8C; textos em #1A1A1A e #595959. Não use outras cores.
- Fundo branco (#FFFFFF) no gráfico e na página; sem bordas no gráfico, sem sombras, sem 3D, sem gradientes.
- Fonte: Calibri (fallback: Arial, sans-serif) em todo o gráfico.
- Título do gráfico: 18 px, negrito, cor #1A1A1A, alinhado à esquerda. Subtítulo logo abaixo: 13 px, cor #595959.
- Textos de eixos e legendas: 11–12 px, cor #595959. Linhas de eixo finas em #BFBFBF; linhas de grade finas em #E6E6E6; sem marcas de escala (ticks).
- Wordmark "CFOs.AI" no canto superior direito, texto em negrito na cor #EF4517. Rodapé à esquerda: "Fonte: dados fictícios · CFOs.AI" em 10 px, cor #8C8C8C.
- Números em formato brasileiro nos rótulos (ponto como separador de milhar e vírgula decimal; ex.: 1.234; 12,5%).
- Proporção 16:9 (960 × 540 px), margens generosas e nada de elementos decorativos extras.
ENTREGUE DUAS SAÍDAS, cada uma em um bloco de código separado e completo:
(a) Python: um único script executável (matplotlib + numpy, sem outras dependências), com os dados declarados no próprio script, que aplica todas as especificações acima e salva o gráfico em "indexadas.png" (dpi 200, fundo branco). Ao final, chame plt.close().
(b) HTML: um único arquivo .html autocontido que carrega Tailwind CSS via CDN (<script src="https://cdn.tailwindcss.com"></script>) e Chart.js 4 via CDN (https://cdn.jsdelivr.net/npm/chart.js); mostre o gráfico em um card branco centralizado (max-w-4xl, padding generoso, sem sombra), com título, subtítulo, wordmark e rodapé em HTML, e as mesmas cores, fontes e dados.
Não explique demais: entregue o código pronto para rodar.
```
