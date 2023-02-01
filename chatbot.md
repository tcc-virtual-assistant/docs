# Chatbot 

## Ávila é um chatbot interativo construído com processamento de linguagem natural (NLP) e aprendizagem profunda (deep learning).

Nós usamos três bibliotecas para o seu desenvolvimento, sendo elas:
- NLTK; 
- NumPy;
- PyTorch;

## NLTK (Natural Language Toolkit)
O NLTK é uma biblioteca para trabalhar com dados de linguagem natural/humana e foi utilizado no projeto para o processo de lematização (lemmatization) e stemização (stemming). A lematização consiste em separar a frase de input e colocar esses dados (que podem ser palavras, números, símbolos) em uma lista de strings. 
Já a stemização tem a função de transformar os verbos conjugados para o verbo no infinitivo, para as palavras em inglês é utilizado o PorterStemmer e para as palavras em português nltk.stem.RSLPStemmer.
![image](https://user-images.githubusercontent.com/101810029/216030661-5c1752be-d83c-47c5-bb0c-7fd8d2293749.png)

![image](https://user-images.githubusercontent.com/101810029/216031230-236c9607-0a86-4537-a721-3220ead67787.png)</br>
a função bag_of_words recebe as listas de strings tokenizadas e stemetizadas e identifica quais dessas strings recebidas se encontram no padrão pré estabelecido de perguntas (patterns, arquivo json), se a string tiver uma correspondente ela recebe o numero 1, se não, o numero 0. A comparação é feita com todas as patterns de todas as tags, a que mais tiver compatibilidade (receber 1) irá ser assimilada com a devida resposta pré estabelecida na tag. A biblioteca utilizada para conversão de string em float e atribuição de 0 e 1 é a numpy.

## NumPy (Numeral Python)
A NumPy é uma biblioteca utilizada para realizar cálculos matemáticos de alto nível envolvendo arrays e matrizes.
Nós a utilizamos na função da bag of words, linhas 26 e 29 (imagem acima)

Essas funções são chamadas no arquivo train.py, onde é passado todas as perguntas pré definidas (patterns) para a função de tokenização e adicionadas a uma lista com a sua tag referente, exemplo: [['comer', 'almoçar'],'restaurante'].
O mesmo ocorre com a stemização, que transforma todas as strings da lista obtida na tokenização. Após o processo, a 'bag_of_words' é chamada com o mesmo propósito das anteriores.
![image](https://user-images.githubusercontent.com/101810029/216058014-7cfe34ba-e2f3-49d9-a4c6-2e734af8e9a1.png)

## PyTorch ( ? )
O PyTorch é um framework de aprendizado de máquina (machine learning) para criar redes neurais. O primeiro uso das funcionalidades foi para realizar o treinamento de dados.
