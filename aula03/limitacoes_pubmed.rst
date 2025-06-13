Limitações da PubMed
+++++++++++++++++++++


Limitações
-------------

A ferramenta de busca do PubMed não lida com múltiplos termos de forma eficaz. A recuperação bem-sucedida de artigos depende dos autores declararem claramente todos os termos necessários no título, palavras-chave, resumo e corpo do texto do artigo. É importante observar que uma busca sem restrições no PubMed também analisa a seção de referências, o que pode levar a muitos FP. Logo, temos que restringir as buscas ao título e *abstract* ([Title/Abstract]) para contornar esse problema, possivelmente gerando vários FN. 

Além disso, LLMs e PubMed também podem produzir FNs se os artigos não forem de livre acesso ou estiverem ocultos na documentação da patente.

.. warning::
   Em qualquer pesquisa temos o comprometimento entre **filtrar muito** ou **filtrar pouco** ao fazermos uma pergunta (*query*). Para medirmos este fenômeno precisamos calcular a **Sensibilidade** e **Especificidade**, ou seja conhecer os FP e FN, tarefa que neste tipo de pesquisa pode ser muito difícil.


Exemplo errado
-----------------

hipertension AND systemic AND cardio AND (CVA OR cerebrovascular accident) AND deaths


Motivo
------------

  a. muitos termos podem levar a muitos FN
  b. use radicais seguidos de asterístico: card*
  c. use ao máximo palavras sinônimas concatenadas com OR: cerebr* OR brain*
  d. pesquise cada conceito e utilize a numeração das pesquisas: #1 AND #2 AND (#3 OR #4 OR #5)
  e. não use plural
  f. tente usar termos MESH, vá escrevendo o que deseja na tela inicial da PubMed que ela vai autocompletando possíves termos controlados.



Importante
----------------

| As primeiras pesquisas nunca são boas.
| Nunca acredite que 2 ou 3 pesquisas são boas e suficientes, sem análise mais profundas.


Dicas de como pesquisar
-------------------------

  * Construa uma pesquisa (*query*) na PubMed
  * Utilize, quando possível, o mínimo número de termos
  * Analise as referências de retorno
  * Anote novos conceitos e palavras sinônimas ou homológas
  * Refaça a pesquisa
  * Pesquise com IA: anote novos conceitos e palavras sinônimas ou homológas
  * Refaça a pesquisa: inclua novos conceitos e sinônios usando **OR**
  * Estude a melhoria de cada passo / resultados
  * Estude se há FP: artigos trazidos errados (se sim, refaça a pesquisa usando cláusula NOT)
  * Se você não é um especialista na área é praticamente impossível analisar FN (referências que deveriam ter aparecido)
  * Sempre que possível peça ajuda a pessoas mais experientes na área
  * Nunca ache que sua pesquisa terminou e está ótima: sempre há algo para melhorar
  * Nunca diga **boa sorte**! Sorte é **acaso**. Estude, estude muito: **bom trabalho**




