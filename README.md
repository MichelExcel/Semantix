# Semantix
Processo Seletivo

Código desenvolvido para o processo seletiva da empresa Semantix em Jan/2019. 

Na solução utilizei apenas a base ‘Aug 04 to Aug 31, ASCII format, 21.8 MB gzip compressed’, já que a base ‘Aug 04 to Aug 31, ASCII format, 21.8 MB gzip compressed’ estava solicitando login para a realização do download.

A base analisada não possui uma estruturação muito simples. Os dados não apresentam um separador como em um CSV, por exemplo, o que dificulta bastante a quebra das informações. 

Também há várias quebras de padrões como a existência de aspas no meio das requisições, traços nos campos bytes retornados, variação entre sites e IPs e etc. 

Tentei então optar pelo uso de expressões regulares para resolver estes problemas, mas a regex já estava com várias linhas e ainda assim seguia não contemplando todas as possibilidades existentes entre os quase 2 milhões de registros.

Isso me forçou a criar funções em Python "puro" para separar os dados e então convertê-los em matriz e posteriormente em dataframe para a realização das análises com a library pandas.

Entendo que não seja uma solução totalmente em PySpark, mas as respostas esperadas foram encontradas e muitos conceitos estão demonstrados no código.
