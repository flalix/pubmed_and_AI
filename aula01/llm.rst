O que são LLMs?
++++++++++++++++

Em Deep Learning foram propostos vários modelos, como vemos abaixo. Neste capítulos vamos nos ater a **Transformers**, um modelo utilizado para o treinamento de Grandes Modelos de Linguagem, ou **Large Language Models** (**LLM**).


Tipos de modelos de Deep Learning
-----------------------------------

  * Convolutional Neural Networks (CNNs) - as redes convolucionais são muito utilizadas para classificação de imagens
  * Recurrent Neural Networks (RNNs) - menos usadas, a redes recorrentes foram trocadas por Transformes
  * Generative Adversarial Networks (GANs) - redes generativas, muito utilizadas para gerar texto, imagens, áudios, vídeos e códigos como Python ou C.
  * Deep Belief Networks (DBNs) - modelo generativo utilizado para clasficação e extração de características
  * Transformers - o modelo mais utilizado, atualmente, usado para treinamento de LLMs
  * Autoencoders - redes onde a saída é igual a entrada, servem para fazer a redução de dimensionalidade, extração de características e compressão  de dados.
  * Graphical Neural Network (GNN) - este é um novo modelo, existe desde ~2021, é a nova grande revolução em Deep Learning, muito utilizado em drug discovery e cheminformatics.

LLMs
------

Os LLMs ou Large Language Model são modelos ultra-sofisticados de Deep Learning que têm a capacidade de *compreender* e **gerar** textos semelhantes a seres humanos. Os LLMs são criados, atualmente, sobre o modelo de **Transformers**. Estas redes neurais estão sendo treinadas utilizando-se um massivo *corpus*, como todo o texto da internet e mais todos os livros e artigos disponíveis, além de outras mídias (imagens, vídeos, sons, códigos de computadores, etc). Como são baseadas em *embeddings* cada conceito no `espaço de embeddings` é uma dimensão, logo para treinar vários **Transformers em paralelo** há bilhões de parâmetros a serem analisados. Portanto, o treinamento é demorado e custoso (em equipamento e energia elétrica), mas a LLM final é finita e responde em alta velocidade.  


ver: https://www.youtube.com/watch?v=wjZofJX0v4M


Fundamentalmente, os LLMs funcionam prevendo a próxima palavra em uma sequência, dadas as palavras anteriores. Eles não "pensam" ou "entendem" no sentido humano, mas são notavelmente bons em imitar padrões de linguagem humana.

Uma vez treinado, um LMM aceita perguntas e responde na forma de **predições**, ou seja possíveis tokens encadeados formando uma frase. Porém, a cada predição (um token) o sistema encontra um conjunto de possíveis tokens dentro de uma distribuição probabilística. Usualmente ele retorna o token com maior probabilidade. Este leque de tokens probabilisticos se encontram no espaço de embedings, e de acordo com que diminuímos a Teperatura do algoritmo, diminuímos **este leque** e somente 1 ou poucos tokens são retornados por vez. Isto faz com que as respostas sejam mais sistemáticas e menos variávies ou halucinógenas.


O que podemos fazer com uma LLM?
-------------------------------------

  * Análise de Sentimento: p.ex. pode-se perguntar se um parágrafo é Negativo (ou Triste), Neutro, ou Positivo (ou Alegre)
  * Análise de toxicidade: se o texto é hostil
  * Traduções, Correção de Erros, Apoio à escrita, Completar textos
  * Resumir textos (além de resumir, tem que gerar o resumo == IA Generativa)
  * Reconhecimento de entidades nomeadas (define se palavras ou um conjunto de palavras denota uma Pessoa, Data, Organização, etc)
  * Detecção de SPAM
  * Recuperação de Informação (achar os documentos mais relevantes dado um query)
  * Respoder perguntas
  * Autocompletar um texto ou parágrafo


Desafio
---------------

.. warning::
   Dados que um LLM pode *entender*, classificar e resumir textos, além de encontrar conceitos no hiper-espaço de **embeddings**: - SERÁ QUE UM LLM É MELHOR AO PESQUISAR ARTIGOS CIENTÍFICOS QUE SISTMAS ESPECIALIZADOS COMO A PubMed?



Refinamento
---------------

.. image:: ../images/llama.png
  :align: right
  :width: 20%
  :alt: Llama model


Uma característica interessante de uma LLM é que podemos treiná-la de maneira geral e disponibilizá-la a pesquisadores de usuários, como o modelo Llama da empresa Meta AI (https://ai.meta.com/blog/meta-llama-3/).

Logo, uma vez de posse de uma super LLM, podemos retreiná-la para uma específica tarefas. Por exemplo, diferentes grupos treinaram um dado LLM e depois refinaram o mesmo com todos os abstracts da PubMed. Este tipo de operação, o refinamento, ainda está sendo estudado para se entender o ganho e acurácia do mesmo.



