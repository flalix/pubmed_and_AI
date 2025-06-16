Pesquisando 2 palavras ou conceitos
++++++++++++++++++++++++++++++++++++

Há varias formas de se pesquisar 2 palavras ou 2 conceitos.


  1. <palavra1> <palavra2>
  2. <palavra1> AND <palavra2>
  3. <palavra1> OR <palavra2>

Aqui introduzimos os conectores booleanos ``AND`` e ``OR``


O conector ``AND`` significa ``e`` ou intersecção. *Query*: <conceito1> ``e`` <conceito2>

O conector ``OR`` significa ``ou`` ou união. *Query*: o <conceito1> ``ou`` <conceito2>

Onde *Query* significa indagar ou pesquisar.


Sem usar conector booleano
----------------------------

Pequisa I
==============

  1. Diabetes
  2. Heart Disease
  3. 'Heart Disease'
  4. heart disease
  5. heart diseases


Resultados I
==============

  1. Diabetes: 1,054,888 results
  2. Heart Disease: 1,661,926 results
  3. 'Heart Disease': 1,661,926 results
  4. 'heart disease': 1,661,926 results
  5. heart disease: 1,661,926 results
  6. heart diseases: 1,496,211 results

  
.. tip::
   Porque **meus resultados** podem ser diferentes dos **seus resultados**?

.. tip::
   As quatro primeiras pesquisas eram sobre ``heart disease``, porque a quinta pergunta gerou resultados diferentes?
   Qual a solução para este problema?


Pequisa II
============

  6. heart diseases kidney failure
  7. heart diseases AND kidney failure
  8. 'heart disease' AND 'kidney failure'


Resultados II
==============

  6. heart disease kidney failure: 36,626 results
  7. heart disease AND kidney failure: 36,626 results
  8. 'heart disease' AND 'kidney failure': 45,185 results

.. tip::
   As *queries* 6 a 8 são diferentes e as 2 primeiras geraram o mesmo resultado, quiçá por sorte. Isto se deve a cada palavra apareceram nos 36,626 resultados assim como os conceitos ``heart disease`` e ``kidney failure``. Porém, em 8) o resultado foi maior. Porque? Será que pegou mais termos MESH? Vá em *history* e consulte a explicação -> separação dos termos *heart* e *disease* assim como *kidney* e *failure*.


.. warning::
   Para pesquisar, use preferencialmente 
     1. os termos do dicionário MESH da PubMed
     2. letras em minúsculo ou maiúsculo, tanto faz
     3. o radical da palavra mais um ``*``

     exemplo: **heart disease***



Pequisa III
============

  9. 'heart disease' OR 'kidney failure'


Resultados II
==============

  9. 'heart disease' OR 'kidney failure': 1,906,740 results
    * heart disease: 1,660,518 results
    * kidney failure: 291,332 results
  10. heart disease OR kidney failure: 1,906,740 results

.. warning::
   Repare que ``heart disease`` OR ``kidney failure`` com ou sem aspas gera o mesmo resultado pois são conceitos do dicionário MESH. Mas, não tem significado usar o conector ``OR`` para unir dois conceitos diferentes. Em 9c temos a soma de 9a e 9b, um pouco menor, pois deve haver alguns poucos artigos de que tratam dois conceitos.

