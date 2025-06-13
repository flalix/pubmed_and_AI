Limitações da PubMed
+++++++++++++++++++++


Limitações
-------------

A ferramenta de busca do PubMed não lida com múltiplos termos de forma eficaz. A recuperação bem-sucedida de artigos depende dos autores declararem claramente todos os termos necessários no título, palavras-chave, resumo e corpo do texto do artigo. É importante observar que uma busca sem restrições no PubMed também analisa a seção de referências, o que pode levar a muitos FP. Logo, temos que restringir as buscas ao título e *abstract* ([Title/Abstract]) para contornar esse problema, possivelmente gerando vários FN. 

Além disso, LLMs e PubMed também podem produzir FNs se os artigos não forem de livre acesso ou estiverem ocultos na documentação da patente.

.. warning::
   Em qualquer pesquisa temos o comprometimento entre **filtrar muito** ou **filtrar pouco** ao fazermos uma pergunta (*query*). Para medirmos este fenômeno precisamos calcular a **Sensibilidade** e **Especificidade**, ou seja conhecer os FP e FN, tarefa que neste tipo de pesquisa pode ser muito difícil.


Dicas
-------

1. Utilizar o mínimo número de termos possíveis

Exeplo errado
-----------------

hipertension AND systemic AND cardio AND (CVA OR cerebrovascular accident) AND deaths


Motivo
------------

  a. muitos termos podem levar a muitos FN
  b. use radicais seguidos de asterístico: card*
  c. use ao máximo palavras sinônimas concatenadas com OR: cerebr* OR brain*
  d. pesquise cada conceito e utilize a numeração das pesquisas: #1 AND #2 AND (#3 OR #4 OR #5)
  e. não use plural
  f. tente usar termos MESH, vá escrevendo o que deseja na tela inicial da PubMed que ela retorna os termos possíveis.


2. Nunca acredite que uma primeira pesquisa está pronta

Importante
----------------

as primeiras pesquisas nunca são boas


Dicas de como pesquisar
-------------------------


  a. Construa uma pesquisa (*query*) na PubMed
  b. Analise as referências de retorno
  c. Anote novos conceitos e palavras sinônimas ou homológas
  d. Refaça a pesquisa
  e. Pesquise com IA: anote novos conceitos e palavras sinônimas ou homológas
  f. Refaça a pesquisa: inclusa novos conceitos e sinônios usando **OR**
  g. Estude a melhoria de cada passo / resultados
  h. Estude se há FP: artigos trazidos errados (se sim, refaça a pesquisa usando cláusula NOT)
  i. Se você não é um especialista na área é praticamente impossível analisar FN
  j. Sempre que possível peça ajuda a pessoas mais experientes na área
  k. Nunca ache que sua pesquisa terminou e está ótima: sempre há algo para melhorar


