Recursos de Aplicativos de IA
+++++++++++++++++++++++++++++++

Os aplicativos de IA em sites públicos (livres ou pagos) permitem que usuários façam várias operações distintas, após se logarem no mesmo *site*.


Principais aplicativos:

  * Google AI: https://aistudio.google.com/
  * Chat-GPT: https://chatgpt.com/
  * Perplexity: https://www.perplexity.ai/
  * Ainda há LLama (Meta), Claude (AWS), entre outras iniciativas abertas ou pagas.

Perguntas & Respostas
-----------------------

O usuário pode fazer perguntas e continuar questionando (dialogando). A cada resposta há o ícone de cópia (só texto ou texto marcado (*markdown*)) que copia o conteúdo da resposta para a memória, e pode-se, p.ex., colá-la num editor de texto.


  * O que é uma mitocôndria?
  * Onde fica a Guatemala?
  * Qual a forma de governo dos países baixos na Europa?


Resumos
---------

Um LLM tem capacidade fazer resumos, pois é uma máquina semântica e generativa (capacidade de criar). Logo, pode-se pedir para o aplicativo Resumir (Sumarizar ou *Summarize*) um texto. Sempre que possível acrescente um contexto. No primeiro exemplo pedimos para o aplicativo de LLM "ir na PubMed" e com dado ID, obter o abstract e resumi-lo. Sim, ele consegue fazer isto! É extraordinário.


  * Get PMID 37567824 in PubMed and Summarize the abstract.
  * Summarize this text: <text>
  * Summarize this text: <text> + "Context: xxxxx"
  * Faça um resumo da história "Branca de Neve e os sete anões"

Context
===========

Ao escrevermos um texto, este pode se referir a tópicos diferentes no conhecimento humano, logo após o texto deve-se acrescentar **"Contexto:" mais o texto do contexto**.

P.ex.: Resumir o contrato e apresentar seus principais tópicos: <contrato>. Contexto: este é um contrato de compra e venda de um apartamento no Brasil".


Tradução
-----------

Uma das primeiras funções na criação de um **Transformer** foi a tradução, uma vez que se pode, neste modelo neural, comparar duas frases de comprimentos diferentes. Como uma dada frase em Inglês pode ter comprimento diferente que em Francês, uma RNN teria dificuldades de comparar e gerar uma tradução. No entanto, pode-se treinar um LLM com frases de comprimentos diferentes. No caso de uma tradução, treinamos um LLM oferecendo uma frase em inglês e dizendo que esta é similar a outra frase em francês. Logo, o LLM treinado para tradução mapeia frases em inglês no espaço de embeddings em francês, e pode, com este treinamento, retornar a tradução.


  * Traduza do Inglês para o Português: <texto>
  * Traduza do Português para o Alemão: <texto>
  * Translate from English to Spanish: <texto>

Exemplo <texto>: Rheumatoid arthritis (RA) is described as a chronic, systemic inflammatory disease with an autoimmune basis. It primarily targets peripheral joints in a symmetrical pattern. Despite significant progress in understanding RA’s physiological mechanisms, its underlying cause remains elusive.

.. warning::
   Há diversos outros tradutores, como: https://translate.google.com/ 

.. warning::
   Há suporte para a língua inglesa Grammarly (pago): https://app.grammarly.com/


Correção gramatical
---------------------

No caso de correção gramatical, p.ex. no Inglês Britânico, dado um texto, o LLM gera os embeddings preditivos e compara com o que foi escrito no texto. Se uma dada palavra não estiver correta ou este verificar a falta de uma vírgula, apresenta o resultado como uma possível correção.

  * Please review and fix this text in British English: <text>

<text>: A mitochondrion (pl. mitochondria) is an organele found in the cells of most eukaryotes, such as animals, plants and fungi. Mitochondria have a doble membrane structure and use aerobic respiration to generate adenosine triphosphate (ATP), which is used throughout the cell as an source of chemical energy.

.. note::
   Nós humanos pedimos **por favor** (*please*), mas isto é desnecessário ao se fazer uma pergunta a um LLM.

.. warning::
   Porém, as empresas (e soluções) estão aprendendo muito com nossas indagações (*queries*). Logo, sempre que possível, o usuário educadamente deve reportar um **Errro** ou **Acerto**. Como, "*I think I disagree with your answer, because ...*"" ou "*Well done, Chat-GPT, great answer*". Com estes *feedbacks* as empressas aprimoram suas máquinas de LMM.



Multimodal
-------------

Algumas soluções de LLM tem a capacidade de gerar imagens, sons e até filmes.


  * Desenhe um coelhinho sambando na praia de Ipanema

Perplexity:

  * Draw an astronaut visiting the Skylab (the old Nasa's space station)

.. image:: ../images/astronaut.png
  :align: center
  :width: 50%
  :alt: Astronaut and Skylab

\


Gráficos & Cálculos
---------------------

Alguns LLMs tem a capacidade de fazer cálculos, gerar gráficos e até fazer análise matemáticas ou financeiras.


  * Faça uma tabela de número de cromossomos versus espécies e mostre as 10 primeiras espécies com maior número de cromossomos.
  * Faça um gráfico de barras com o PIB das 10 nações mais ricas do mundo seguido das 10 nações mais pobres.
  * Faça um gráfico de barras com o PIB das 10 nações mais ricas do mundo seguido das 10 nações mais pobres usando Seaborn.
  * Faça um gráfico de barras com o PIB das 10 nações mais ricas do mundo seguido das 10 nações mais pobres usando Plotly.
   * Pode mostrar o gráfico?
   * Pode mostrar o código em Python?
  * Você pode `subir` (*upload*) tabelas em Excel ou CSV/TSV e pedir para o aplicativo analisar



Código gerado
-----------------

Provavelmente todos LLMs têm a capacidade de gerar códigos em diferentes linguagens de programação com muita acurácia. Por exemplo, conseguem gerar códigos em C, Java, Java-Script, HTM-CSS, Python, R, Ruby, etc. Importante, se algum código estiver incorreto ou incompleto, continue dialogando e orientando a máquina, o resultado, usualmente, é incrível.

  * Código gerado em Seaborn (Python) por Chat-GPT (Junho 2025)

| import seaborn as sns
| import matplotlib.pyplot as plt
| import pandas as pd

| # Dados do PIB em trilhões (ricas) e bilhões (pobres convertidos para trilhões)

| data = {'País': ['EUA', 'China', 'Alemanha', 'Japão', 'Índia','Reino Unido', 'França', 'Itália', 'Brasil', 'Canadá',  'São Tomé e Príncipe', 'Comoros', 'Eritreia', 'Lesoto', 'Gâmbia',  'Cabo Verde', 'R. Centro-Africana', 'Burundi', 'Djibouti', 'Libéria'], 
|           'PIB (trilhões US$)': [27.361, 17.795, 4.456, 4.213, 3.550, 3.340, 3.031, 2.255, 2.174, 2.140, 0.00081, 0.00145, 0.00225, 0.00230, 0.00269, 0.00276, 0.00282, 0.00429, 0.00433, 0.00476], 
|           'Grupo': ['Ricos'] * 10 + ['Pobres'] * 10
| }

df = pd.DataFrame(data)

# Ordenar os países por PIB
df_sorted = df.sort_values(by='PIB (trilhões US$)', ascending=False)

| # Plot com Seaborn
| plt.figure(figsize=(12, 8))
| sns.barplot(data=df_sorted, x='PIB (trilhões US$)', y='País', hue='Grupo', dodge=False, palette='Set2')
| plt.title('PIB das 10 Nações Mais Ricas e 10 Mais Pobres (2023)', fontsize=14)
| plt.xlabel('PIB (trilhões de dólares americanos)')
| plt.ylabel('País')
| plt.legend(title='Grupo Econômico')
| plt.tight_layout()
| plt.grid(True, axis='x', linestyle='--', alpha=0.6)
| plt.show()

