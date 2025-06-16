Pesquisando com IA
++++++++++++++++++++

Como perguntar?
-----------------

Inicialmente fizemos as seguintes perguntas de como indagar um LLM:

  * Como consultar um LLM em linguagem natural e obter respostas reproduzíveis sem alucinações? 
  * Como obter uma resposta positiva ou negativa para inferir se um conceito existe na literatura biomédica ou não?

Abaixo, mostramos a consulta básica (sempre em inglês!) mesclando um **conceito** a uma **doença**:

“Is the <concept> related to the <disease>?” 

Ou,

“Is the <disease> related to the <concept>?”

 No caso dos LLMs, um usuário faz uma pergunta em linguagem natural e o LLM a responde em linguagem natural. No entanto, se as respostas forem frases ordenadas com muitos parágrafos, como podemos inferir se a resposta tem um tom positivo (Sim) ou negativo (Não)? Resumindo, temos duas alternativas:
 
   a. calcular a **análise de sentimento** de cada resposta (como um texto completo ou dividindo e ponderando os parágrafos), ou
   b. **adicionar um preâmbulo** à pergunta que oriente o LLM a começar a responder com um "Sim" ou "Não", pois um LLM é uma máquina semântica.
   
O primeiro método resulta em muitas incertezas, pois a resposta consiste em muitos parágrafos, alguns com sentimentos positivos e outros com sentimentos negativos (resultados não mostrados aqui). Após muitas simulações, o processo usando um <preâmbulo> produziu resultados consistentes e demonstrou que, além de ser uma ferramenta semântica, o Gemini conseguia raciocinar e organizar a resposta da maneira que perguntamos.

Dado um **conceito**, pode-se formular a seguinte consulta:

“Is <concept> related to <disease>?”

E a máquina responderá a esta pergunta, escreverá explicações e um parágrafo de conclusão. 

Pergunte Sim ou Não (preâmbulo)
------------------------------------

Portanto, para obter um Sim ou Não, é necessário adicionar um preâmbulo:

“Answer in the first line, Yes or No; Is <concept> related to <disease>?”


Essa abordagem funciona bem de acordo com muitos testes implementados, e aprendemos que é possível tentar introduzir mais classes qualitativas do que **Yes** ou **No**, mas a resposta é modelo dependente. Observe os novos termos no preâmbulo:

“Answer in the first line Yes, Possible, Low evidence, or No; Is <concept> related to <disease>?”

Dependendo do LLM selecionado, a resposta retornará apenas **Yes** ou **No**; outros modelos podem retornar **Yes**, **Possible**, **Low evidence** ou **No**. Além disso, ao introduzir este preâmbulo, perde-se a explicação se a máquina decidir responder apenas brevemente. Aqui, novamente, pode-se melhorar adicionando "e explicar": 

“Answer in the first line Yes, Possible, Low evidence, or No, and explain: Is <concept> related to <disease>?”

Por fim, é necessário adicionar **contextos** à consulta para ajudar o LLM a se concentrar e melhorar a reprodutibilidade. Os **contextos** direcionam a máquina para um subespaço definido dentro do hiperespaço de embeddings. Portanto, o formato final proposto é:


“Answer in the first line Yes, Possible, Low evidence, or No, and explain: Is <concept> related to <disease>? Context: <disease_context> + <concept_concept>.”

Vamos fazer um exemplo em português.

Responda na primeira linha Sim, Possível, Pouca evidência ou Não, e explique: a "tempestade de citocinas" é causa fundamental das "mortes em COVID-19"? Contexto: a COVID-19 foi a pandemia que se iniciou em fins de 2019 e atingiu o planeta inteiro matando mais de 6 milhões de pessoas. A "tempestade de citocinas" é o disparo massivo de interleucinas inflamatórios, principalmente IL6, quando em casos graves de COVID-19.


Respostas do Gemma 3 27B (da Google)
------------------------------------

https://aistudio.google.com/

Ao entrar escolha: Gemma 3 27B e baixe a temperatura para 0.1

Copie esta pergunta na caixa de query e <run>

Resposta
=========

Sim, Possível.

A "tempestade de citocinas", especialmente o aumento descontrolado de IL-6 e outras citocinas pró-inflamatórias, é um fator *importante* na patogênese da COVID-19 grave e, consequentemente, nas mortes associadas. No entanto, **não é a única causa fundamental**.

**Explicação:**

*   **Inflamação Descontrolada:** O SARS-CoV-2, em casos graves, induz uma resposta imune exagerada, levando à "tempestade de citocinas". Essa tempestade de citocinas causa inflamação sistêmica, dano tecidual (principalmente nos pulmões), síndrome do desconforto respiratório agudo (SDRA), coagulopatia e disfunção de múltiplos órgãos.
*   **Correlação com Gravidade:** Níveis elevados de IL-6 e outras citocinas estão fortemente correlacionados com a gravidade da doença e maior risco de morte.
*   **Alvos Terapêuticos:** Medicamentos que bloqueiam a IL-6 (como o tocilizumabe) demonstraram reduzir a mortalidade em alguns pacientes com COVID-19 grave, o que reforça o papel da interleucina na doença.
*   **Outros Fatores:** A COVID-19 é uma doença complexa. Outros fatores contribuem para a gravidade e mortalidade, incluindo:
    *   Carga viral inicial
    *   Idade e comorbidades do paciente (diabetes, doenças cardíacas, obesidade, etc.)
    *   Resposta imune individual
    *   Formação de microtrombos
    *   Disfunção endotelial
    *   Variantes do vírus

Portanto, a tempestade de citocinas é um componente crucial da patologia da COVID-19 grave, mas a morte geralmente resulta de uma combinação de fatores, e não apenas da inflamação descontrolada.



Respostas do Chat-GPT
----------------------

https://openai.com/

Copie esta pergunta na caixa de query e <run>

Resposta
=========

Pouca evidência
Embora a "tempestade de citocinas" — também conhecida como tempestade de citocinas — esteja associada a casos graves de COVID-19, especialmente com níveis elevados de IL-6, ela não é considerada a causa fundamental das mortes. A COVID-19 é uma doença complexa, com múltiplos mecanismos patológicos, incluindo trombose, lesão endotelial, disfunção imunológica e falência multiórgãos. A tempestade de citocinas contribui significativamente para a gravidade, mas isolá-la como causa primária das mortes carece de evidência conclusiva e ignora a multifatorialidade do desfecho fatal.


Desacordo
------------

.. warning::
   Chat-GPT não está de acordo com Gemma!


Desafios
------------

.. note::
   1. Será que uma indagação estruturada em linguagem natural em Português gera os mesmos resultados que em Inglês?
   2. Compare os resultados entre o Gemma e o Chat-GPT
   3. Faça uma pergunta sua.
   4. Escolha outra ferramenta e faça perguntas: use o Perplexity (https://www.perplexity.ai/)
   5. Como você verificaria se uma dada resposta está correta?

.. tip::
   **Pergunta em Inglês**
   Answer in the first line Yes, Possible, Low evidence or No, and explain: is the cytokine storm a fundamental cause of COVID-19 deaths? Context: COVID-19 was a pandemic that began in late 2019 and affected the entire planet, killing more than 6 million people. The cytokine storm is the massive release of inflammatory interleukins, mainly IL6, in severe cases of COVID-19.



