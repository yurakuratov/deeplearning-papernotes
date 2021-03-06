- Ссылка на статью: [arXiv](https://arxiv.org/abs/1603.01354).

В данной статье описывается подход для разметки последовательности токенов
без использования сторонних признаков (в т.ч. без газетиров). Они получили state-of-the-art
результат на корпусах CoNLL-2003 (Named entity recognition) и WSJ (part-of-speech tagging).
В качестве модели они использовали Bidirectional-LSTM с CRF (conditional random field)
на выходе. На вход они подавали предобученные вектора слов и вектора слов
полученные с помощью character-level CNN (он и заменил ручной газетир).
Довольно интересно влияют вектора слов на качество NER - на предобученных
на word2vec F1=84.91, на GloVe F1=91.21. Без использования CRF на выходе - F1=89.36.

Схема сети: https://www.dropbox.com/s/iwffxxwspsf38qg/ner-lstm-cnn-crf.png?dl=0.
