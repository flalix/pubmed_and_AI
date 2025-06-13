Webservices: Python
+++++++++++++++++++++


**Web Service** é uma forma arguição na Web (Internet) onde um usuário faz uma pergunta em texto puro, controlada, e um *site* (URL - endereço geral da internet) responde.

Ou seja, empresas, comércios, jornais, bases de dados, entre outros, podem construir e disponibilizar seus **Web Services** para responder sistematicamente a informações de usuários.


.. Note::
   **Web Service** é composto:

   * Host: um servidor central que armazena o **Web Service** e disponiliza o serviço
   * Dicionário: um dicionário que apresenta a URL, e diversas formas fixas de se perguntar
   * Usuário: na outra ponta o usuário, que tem que conhecer o serviço e saber como perguntar e processar as respostas


Em BioMedicina, vários bancos de dados (como NCBI, KEGG, Reactome, Ensembl, COSMIC, etc) disponibilizam um **Web Service** e usuários ou aplicativos podem fazer até algumas dezenas de perguntas por segundo para obter informações técnicas e científicas.


As plataformas de IA também disponibilizam seus **Web Services**. Este é um ponto nevrálgico do **negócio**. As políticas das plataformas de IA é de convidar a todos a utilizarem seus serviços. Mas, aqueles usuários e empresas que têm necessidades de fazer milhares de perguntas num período, ou prestam serviços e fazem milhões de perguntas por dia, são convidados a pagar uma taxa por milhões e tokens processados. Pequenos usuários que fazem 2, 5, ou 10 perguntas num dia estão isentos de taxas.

Exemplo WS-Gemini
--------------------
   
Somente a título de curiosidade e para poucos, como um exemplo técnico, apresentamos um código de **Web Service** para fazer consultas a qualquer modelo de LLM da Google. O mesmo pode ser consultado para as outras plataformas como Chat-GPT, Perplexity, Claude, LLama, etc.

.. Note::
   Código para acess Google Web Service em: https://github.com/flalix/google_webservice


Como testar o WS-Gemini?
-------------------------

  * Baixe ou faça um clone do endereço GitHub acima
  * Suba os arquivos para o Google-Drive
  * O arquivo de params.yaml é um arquivo de configuração, obrigatório editá-lo:

    * entre no site da `IA da Google <https://aistudio.google.com>`_ e se logue
    * copie a chave de acesso: API_KEY
    * edite no params.yaml: seu email e a chave copiada API_KEY
    * nunca mostre esta chave de acesso: com ela o Google é capaz de cobrar taxas de uso
    * caso alguém a tenha, pode usá-la e você pagar a conta!
   
  * Vá no google-drive e abra o notebook **webservice_google_AI.ipynb**
  * Rode o código e bom aprendizado.


   