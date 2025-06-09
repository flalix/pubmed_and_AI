História e Início
+++++++++++++++++++

Introdução
------------

É muito difícil e complicado explicar o que é Intelgiência Artiticial (IA) nos dias atuais (2025). Mas, vamos tentar explicar com história e exemplos. Uma vez que é necessário um bom conhecimento de matemática e aprendizado de máquina (*Machine Learning*), nós não vamos nos aprofundar e tentar mostrar de maneira metafórica os conceitos. Por fim, mostraremos como utilizar a IA focando em recuperação de informações científicas, em especial, biomédicas.


História
-----------


.. image:: ../images/jamonycajal.png
  :align: left
  :width: 50%
  :alt: jamonycajal


.. image:: ../images/neuron.png
  :align: right
  :width: 45%
  :alt: Neuron

Na década de 1870, o cientista Santiago Jamón y Cajal, espanhol, desenhou os primeiros neurônios e criou a neurologia. Seus trabalhos foram fundamentais para diversas áreas de Biologia e da Medicina e também serviram de modelo aos primeiros **Neurônios Artificiais**.

ref: https://www.linkedin.com/pulse/art-science-santiago-ram%C3%B3n-y-cajal-tim-vancamp/

https://blogs.scientificamerican.com/illusion-chasers/santiago-ramon-y-cajal-the-young-artist-who-grew-up-to-invent-neuroscience/

\
\

Na década de 1940 von Neuman e Alan Turing *desenharam* e propuseram o primeiro computador. Em 1946 foi construído o ENIAC (Electronic Numerical Integrator and Computer). Naquele momento, possivelmente, alguns cientistas entendeream que o mesmo tinha um severo fator limitante: seus cálculos eram seriais. Em 1943 Warren McCulloch e Walter Pitts propuseram um **neurônio artificial**, sua vantagem: processamento paralelo.

O modelo de McCulloch e Pitts mimetiza um neurônio de Cajal, tendo várias entradas (*inputs*) um corpo celular (Soma) que faz uma operação como adição e uma saída φ que é uma função de transformação ou normalização (função(soma entradas) --> saída ou *output), como vemos no desenho abaixo.

.. image:: ../images/neuron_model.png
  :align: center
  :width: 60%
  :alt: Neuron Model

ref: https://en.wikipedia.org/wiki/Artificial_neuron

A seguir em 1949, Touring, precocemente imaginou que a máquina, ainda que primitiva, poderia ser *inteligente*. E propôs o **Teste de Touring** (ver https://en.wikipedia.org/wiki/Turing_test). Feliz ou infelizmente, John McCarthy cunhou o termo **Inteligência Artificial**, mas o correto é a denominação **Aprendizado de Máquina** (*Machine Learning* ou ML).

\
\

Em 1957, Frank Rosenblatt, monta o prmeiro circuito elétrico que mimetizava o **Neurônio Artificial**. Daí para frente o planeta estava pronto para sair da *Era Industrial* e entrar na *Era da Informação*. Porém, a evolução dos computadores seriais foi ótima e exponencial, sendo que no início dos anos 80, devido a minituarização dos circuitos eletrônicos, surge a micro informática e os computadores pessoais. Já a teoria e desenvolvimento do circuitos neurais artificiais passou pela grande crise denominada o **Inverno da IA** (de ~1970-1990).

ref: https://iatracker.com.br/glossario/o-que-e-xor-problem/

https://en.wikipedia.org/wiki/AI_winter. 


Linha do Tempo
---------------

.. image:: ../images/ai_timeline.jpg
  :align: center
  :width: 90%
  :alt: AI timeline

\

ref: Bellini V, Cascella M, Cutugno F, Russo M, Lanza R, Compagnone C, Bignami EG. Understanding basic principles of Artificial Intelligence: a practical guide for intensivists. Acta Biomed. 2022 Oct 26;93(5):e2022297. doi: 10.23750/abm.v93i5.13626. PMID: 36300214; PMCID: PMC9686179.

Do ínicio dos anos 90 até 2012 há a primeira era tecnologica da IA, conhecida como Deep-Learning (DL). DL é o encadeamento de neurônios em várias camadas. Ou seja, à esquerda há a *entrada) ou *input*, à direita há a *saída* ou *output* e no meio as camadas de *neurônios escondidas* denominadas *hidden layers*. 

Um esquema de ANN,


.. image:: ../images/ann.jpg
  :align: center
  :width: 90%
  :alt: AI timeline

\


A **grande sacada** foi como *ajustar os pesos* de cada neurônio (valores sobre as funções dos neurônios) e ir modificando os mesmos de forma que o *output* fosse igual ou próximo a determnados valores. Portanto, na etapa de treinameto de uma ANN, neurônios importante vão se aproximando do peso 1, e neurônios menos importantes ficam no intervalo de pesos entre 0.1 e 0.9 e aqueles que não colaboram com o resultado são desligados, ficando com peso igual a zero. A técnica é levar os valores de entrada para cada camada, passando por cada neurônio e calculando a função neural, num algoritmo denominado "feedforward". Os neurônio de saída (*output*) preditos, são confrontados com o resultado desejado (p.ex.: entrada 1, 3, 5 -> São, entradas 2, 4, 6 --> Doente). O erro é mensurado numa função denominada *Custo*. O erro é propagado de volta (*backpropagation*), até a que a função de custo atinja um mínimo. Neste momento a rede estará treinada e pronta para se analisar se funciona com novos dados (dados de teste). O que se armazena, ao final, é a topologia da rede e os pesos encontrados que minimizaram a função custo.

Caso a função da ANN seja o de um classificador então a rede se ajusta para acertar o *output* de classificção, como: 1) doente ou são, 2) rico, médio, pobre, 3) 5 níveis de inflamação, etc). Já se a função da ANN é de calcular uma regressão, o *output* torna-se, p.ex., 50 valores discretos de uma função matemática num determinado domínio de valores. Como exemplo: a) ajustar a uma parábola, b) um pedaço de curva qualquer, c) semi-círculo.

Mas, como se define **Doente** e **São** numa ANN? Isto é simples, denominamos **one-hot encoding**, ou seja, basta numerar os valores categóricos: **encode**: Doente:0, São:1 e **decode**: 0:Doente e 1:São. Agora a ANN pode trabalhar, pois só há números.


A seguir mostramos um modelo de simulação de uma *Artificial Neural Network* (ANN) utilizando tensorflow (uma das ferramentas para programação de ANNs).

\

.. image:: ../images/playground_tensorflow.png
  :align: center
  :width: 90%
  :alt: AI timeline

\

Vamos Simular? https://playground.tensorflow.org/


