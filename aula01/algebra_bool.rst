Álgebra de Bool
++++++++++++++++++++++


Vocês verão em breve que a PubMed (basicamente o SQL) utiliza a álgebra booleana para mostrar resultados.

Na verdade o que ela está fazendo são operações com conjutos (união e interseção).

A seguir vemos alguns conceitos básicos da Álgebra Booleana.


Lógica AND
--------------

A lógica **AND** funciona como a Interseção entre conjuntos. 
Ou seja, Interseção(A,B) = A AND B = somente os elementos comuns em A e B.
Como exemplo, na PubMed, você escreve um *query* = pneumonia AND woman. O SQL irá buscar:
  - todos os papers que contém 'pneumonia' = A
  - todos os papers que contém 'woman' = B
  - e depois fará a interseção


Dado que x e y são as respostas de cada paper ao *query* formulado, apresentamos o resultado x **AND** y, ou seja, pode-se observar na **tabela verdade** abaixo que se e somente se x=True e y=True que a **Interseção** será True.

.. list-table:: 
   :widths: 5 5 5
   :header-rows: 1

   * - x
     - y
     - x ^ y
   * - F
     - F
     - F
   * - F
     - T
     - F
   * - T
     - F
     - F
   * - T
     - T
     - T



Lógica OR
--------------

A lógica **OR** funciona como a União entre conjuntos. 
Ou seja, União(A,B) = A OR B = todos os elementos em A e B, sem repetição
Como exemplo, na PubMed, você escreve um *query* = young AND children. O SQL irá buscar:
  - todos os papers que contém 'young' = A = todos artigos contendo **jovens**
  - todos os papers que contém 'children' = B = todos artigos contendo **criança**
  - e depois fará a União


Dado que x e y são as respostas de cada paper ao *query* formulado, apresentamos o resultado x **OR** y, ou seja, pode-se observar na **tabela verdade** abaixo que se x=True ou y=True basta para a **União** ser True.


.. list-table:: 
   :widths: 5 5 5
   :header-rows: 1

   * - x
     - y
     - x ^ y
   * - F
     - F
     - F
   * - F
     - T
     - T
   * - T
     - F
     - T
   * - T
     - T
     - T


Ver
====

http://carol.dimap.ufrn.br/logicwiki/index.php?title=%C3%81lgebra_Booleana
