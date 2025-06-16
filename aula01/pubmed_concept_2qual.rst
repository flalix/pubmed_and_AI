1 conceito e 2 qualificadores
+++++++++++++++++++++++++++++++



Conceito (definição)
------------------------

``Conceito`` pode ser uma palavra ou termo (como **Diabetes**) ou múltiplas palavras definindo um ``termo semântico`` como **heart disease** ou **cerebrovascular accident**.


Será que isto está certo?
--------------------------

diabetes ``AND`` young ``OR`` children

\

Sem dúvida que **está errado**.

Quando não há parêntesis o interpretador da *query* Pubmed vai da esquerda para direita:

  1. Primeiro pesquisa **diabetes** ``AND`` faz a intersecção com artigos contendo **young**
  2. Une estes resultados com todos os artigos contendo **children**, pois ``OR`` é união
  3. Mas, não queremos ``união`` com todos os artigos contendo **children**

O correto
------------


diabetes ``AND`` ( young ``OR`` children )

  1. Primeiro faz pesquisa e une todos os artigos contendo ``young`` e ``children``
  2. Depois faz a intersecção com o resultado da pesquisa do termo ``diabetes``
  3. O resultado são artigos de ``Crianças ou Jovens`` com ``Diabetes``.


.. tip::
   * Use sempre parêntesis ``onde há termos com concetor OR``
   * **concept1 AND (concept2 OR concept3)**
   * Dificilmente você vai querer o **concept3** União **concept1** ``AND`` **concept2**, se o desejar use:
   * (**concept1** ``AND`` **concept2**) OR (**concept3**)


