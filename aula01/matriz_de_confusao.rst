Matriz de Confusão
+++++++++++++++++++++

Resumo
--------

Quando fazemos uma pesquisa (*query*) na PubMed aparecem, p.ex., 100 referências, e obviamente o restante (milhões de referências) não aparecem. Relativo às referências que aparecem dizemos que o resultado foi **positivo** e com relação às que não aparecem o resultado foi **negativo**.

Mas, em ciência, qualquer pesquisa tem seus erros!

Aos erros para resultados positivos, denominamos de **Falsos Positivos**. Ou seja, positivos que não deveriam estar lá, foram encontrados mas estão errados.

Aos erros para resultados negativos, denominamos de **Falsos Negativos**. Ou seja, negativos que não deveriam estar lá, não foram encontrados mas estão corretos, deveriam ser positivos.


Logo, podemos desejar uma **matriz de confusão**.


.. list-table:: 
   :widths: 25 25 25
   :header-rows: 1

   * - 
     - True
     - False
   * - Positive
     - True Positive (TP)
     - False Positive (FP)
   * - Negative
     - False Negative (FN)
     - True Negative (TN)



Exemplo fictício: vamos pesquisar o conceito "Hipertensão Arterial"  (*Arterial Hypertension*) no PubMed.

O *engine* encontrou 653308 artigos científicos! Mas, vamos supor que 300 estão errados, eram relativos à nefrologia ou câncer. E vamos supor que descobrimos que o *engine* não trouxe 103 artigos corretos. Logo, tempos 300 FP e 103 FN.

Logo, a matriz de confusão ficará assim

.. list-table:: 
   :widths: 15 15 15
   :header-rows: 1

   * - 
     - True
     - False
   * - Positive
     - 653308-300
     - 300
   * - Negative
     - 103
     - 38 Milhoes - 653308 - 103

