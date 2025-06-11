Limitações da PubMed
+++++++++++++++++++++

A ferramenta de busca do PubMed não lida com múltiplos termos de forma eficaz. A recuperação bem-sucedida de artigos depende dos autores declararem claramente todos os termos necessários no título, palavras-chave, resumo e corpo do texto do artigo. É importante observar que uma busca sem restrições no PubMed também analisa a seção de referências, o que pode levar a muitos FP. Logo, temos que restringir as buscas ao título e *abstract* ([Title/Abstract]) para contornar esse problema, possivelmente gerando vários FN. 

Além disso, LLMs e PubMed também podem produzir FNs se os artigos não forem de livre acesso ou estiverem ocultos na documentação da patente.

.. warning::
   Em qualquer pesquisa temos o comprometimento entre **filtrar muito** ou **filtrar pouco** ao fazermos uma pergunta (*query*). Para medirmos este fenômeno precisamos calcular a **Sensibilidade** e **Especificidade**, ou seja conhecer os FP e FN, tarefa que neste tipo de pesquisa pode ser muito difícil.



Concepts
============


Options
=======


Pathway ensemble
--------

LFC-FDR landascape
---------------

Chosing the Best Cutoff
-----------------



