Montando *queries* complexos
+++++++++++++++++++++++++++++

A seguir vamos apresentar a técnica mais fácil e segura de se montar uma *query* complexa.

Dividindo para conquistar
--------------------------


Vamos supor que queremos pesquisar:

**Hipertensão Arterial em jovens, crianças ou recém-nascidos**

Como fazer?
============

Criando várias pesquisas:
  1. arterial hypertension [All Fields]
  2. arterial hypertension [Title/Abstract]
  3. young [Title/Abstract]
  4. cildren [Title/Abstract]
  5. newborn [Title/Abstract]

\

.. image:: ../images/pubmed_arterial_hyp_advanced_query_5histories.png
  :align: center
  :width: 90%
  :alt: PubMed and AI

\

Concatenando com termos lógicos

.. image:: ../images/pubmed_arterial_hyp_advanced_query_2345.png
  :align: center
  :width: 80%
  :alt: PubMed and AI

\

Repare como é mais fácil montar os ANDs e ORs. Jovens, Crianças e Neonatos ficam entre parentesis e utilizam a cláusula OR para se UNIR todos eles. Já **hipertensão arterial** fica de fora, seguida do conector booleano AND, pois queremos esta patologia neste grupo / faixa etária.

Então funcionou? Tudo Correto?

Sempre há erros - estude os resultados
-------------------------------------------

Vamos analisar os resultado,

\

.. image:: ../images/pubmed_arterial_hyp_advanced_title_abst_result_study.png
  :align: center
  :width: 90%
  :alt: PubMed and AI

\

Vemos que aparecem palavaras que não havíamos pesquisado como **childhood**, **neonate**, **infant**, e **adolescent**.

Logo, podemos melhorar nossa pesquisa adiconando estas palavras. E ao final teremos váriso ORs encadeados.

Aqui trocamos **children** e **childhood** por **child*** (com um asterístico ao fim).


.. tip::
   **pesquisa final** - todas com [title/abstract]

   * #2 - arterial hypertension
   * #3 - young
   * #5 - newborn
   * #7 - child*
   * #8 - infant*
   * #9 - neonat*

\

.. image:: ../images/pubmed_arterial_hyp_advanced_query02_add_terms.png
  :align: center
  :width: 90%
  :alt: PubMed and AI

\

.. warning::
   **Query** - #2 AND (#3 OR #5 OR #7 OR #8 OR #9)

\


Resultado final
================

Passamos de 2911 artigos para 3909. Descobrimos, possivelmente, 998 FN!

\

.. image:: ../images/pubmed_arterial_hyp_advanced_query02_results.png
  :align: center
  :width: 90%
  :alt: PubMed and AI

\






