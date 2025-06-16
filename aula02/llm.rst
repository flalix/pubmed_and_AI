O que são LLMs?
++++++++++++++++

Em Deep Learning foram propostos vários modelos, como vemos a seguir. 


Tipos de modelos de Deep Learning
-----------------------------------

Neste capítulos vamos nos ater a **Transformers**, um modelo utilizado para o treinamento de Grandes Modelos de Linguagem, ou **Large Language Models** (**LLM**). Porém, há diversos tipos de topologias (ou modelos de ANNs). A princípio, cada uma foi criada para uma determinada função (como classificar imagens), mas hoje já se sabe que se pode *misturar* modelos para se adquirir melhor acurácia em diversas funções, como vemos aqui:

  * Convolutional Neural Networks (CNNs) - as redes convolucionais são muito utilizadas para classificação de imagens
  * Recurrent Neural Networks (RNNs) - menos usadas atualmente, a redes recorrentes foram trocadas por Transformes
  * Generative Adversarial Networks (GANs) - redes generativas, muito utilizadas para gerar texto, imagens, áudios, vídeos e códigos como Python ou C.
  * Deep Belief Networks (DBNs) - modelo generativo utilizado para classificação e extração de características
  * Transformers - o modelo mais utilizado, atualmente, usado para treinamento de LLMs
  * Autoencoders - redes onde a saída é igual a entrada, servem para fazer a redução de dimensionalidade, extração de características e compressão  de dados.
  * Graphical Neural Network (GNN) - este é um novo modelo, existe desde ~2021, é a nova grande revolução em Deep Learning, muito utilizado em drug discovery e cheminformatics.


LLMs
------

Os LLMs ou Large Language Model são modelos ultrassofisticados de Deep Learning que têm a capacidade de *compreender* e **gerar** textos semelhantes a seres humanos. Os LLMs são treinados, atualmente, baseados em modelos de **Transformers**. Os **Transformes** são redes neurais complexas, e estão sendo utilizadas para treinar um massivo *corpus* (conjunto de textos), como todo o texto da internet, mais todos os livros e artigos disponíveis, além de outras mídias (imagens, vídeos, sons, códigos de computadores, etc). Como são baseadas em *embeddings* cada conceito no `espaço de embeddings` é uma dimensão, logo para treinar vários **Transformers em paralelo** há bilhões de parâmetros a serem analisados. Portanto, o treinamento é demorado e custoso (em equipamento e energia elétrica), mas a LLM final é finita e responde em alta velocidade.  

| para quem quiser conhecer mais:
| https://www.datacamp.com/tutorial/how-transformers-work
| https://www.youtube.com/watch?v=wjZofJX0v4M


Fundamentalmente, os LLMs funcionam prevendo a próxima palavra em uma sequência de palavras, dadas as palavras anteriores e posteriores (mimetizam *LSTM*, *long short-term memory*). Eles não "pensam" ou "entendem" no sentido humano, mas são notavelmente bons em imitar padrões de linguagem humana.

Uma vez treinado, um LMM aceita perguntas e responde na forma de **predições**, ou seja possíveis tokens encadeados formando uma frase. Porém, o modelo não encontra uma predição exata no hiperespaço de **embeddings**, mas sim um conjunto de possíveis embeddings sendo que cada termo decodificado (embedding -> token) tem uma probabilidade. Usualmente ele define como resultado (predição) o token com maior probabilidade. Este leque de tokens probabilísticos vieram de um subespaço de embeddings, e de acordo com que diminuímos a Temperatura do algoritmo, diminuímos **este leque** e somente um ou poucos embeddings são trazidos e decodificados. Isto faz com que as respostas sejam mais sistemáticas e menos variáveis ou alucinógenas.

.. tip::
   Relembrando: uma palavra é transformada num token e um token (*palavra raiz ou simplificada*) é transformada em um número único denominado embedding. O espaço de todas as palavras transformadas é o hiperespaço de embeddings.


O que podemos fazer com um LLM?
-------------------------------------

  * Análise de Sentimento: p.ex. pode-se perguntar se um parágrafo é Negativo (ou Triste), Neutro, ou Positivo (ou Alegre)
  * Análise de toxicidade: se o texto é hostil
  * Traduções, Correção de Erros, Apoio à escrita, Completar textos
  * Resumir textos (além de resumir, tem que gerar o resumo == IA Generativa)
  * Reconhecimento de entidades nomeadas (define se palavras ou um conjunto de palavras denota uma Pessoa, Data, Organização, etc)
  * Detecção de SPAM
  * Recuperação de Informação (achar os documentos mais relevantes dado um query)
  * Responder perguntas
  * Autocompletar um texto ou parágrafo


Desafio
-----------

.. warning::
   Sabido que um LLM pode *entender*, classificar e resumir textos, além de encontrar conceitos no hiper-espaço de **embeddings**: - SERÁ QUE UM LLM É A MELHOR AO PESQUISAR ARTIGOS CIENTÍFICOS QUE SISTEMAS ESPECIALIZADOS COMO A PubMed?


Refinamento
---------------

.. image:: ../images/llama.png
  :align: right
  :width: 20%
  :alt: Llama model


Uma característica interessante de uma LLM é que podemos treiná-la de maneira geral e disponibilizá-la a pesquisadores de usuários, como o modelo Llama da empresa Meta AI (https://ai.meta.com/blog/meta-llama-3/).

Logo, uma vez de posse de uma super LLM, podemos retreiná-la para tarefas específicas. Por exemplo, diferentes grupos treinaram um dado LLM e depois refinaram o mesmo, p.ex., com todos os *abstracts* da PubMed. Este tipo de operação, o **refinamento**, ainda está sendo estudado para se entender o ganho e acurácia do mesmo.

