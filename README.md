# Praca domowa ZUM - NLP

Do swojego projektu użyładm danych z Kaggle - Sentiment140 dataset with 1.6 million tweets
link do danych - https://www.kaggle.com/datasets/kazanova/sentiment140?resource=download

Jest to dataset do analizy sentymentu, zawiera 1 600 000 tweetów wyodrębnionych za pomocą twitter api. Tweety zostały opatrzone etykietami (0 = negatywne, 4 = pozytywne), natomiast dla lepszej czytelności zdecydowałam się zmienić na 0 = negatywne, 1 = pozytywne. Dane są w jednym pliku .csv, pierwotnie plik zawierał 6 kolumn, natomiast na potrzeby tego zadania korzystam jedynie z kolumn 'sentiment' i 'text'.

W moim projekcie wykorzystuję model analizy sentymentu oparty na sieci konwolucyjnej (CNN). Model ten został zbudowany w oparciu o architekturę warstw Embedding, Conv1D, GlobalMaxPooling1D i Dense.

## Architektura Modelu

Model składa się z następujących warstw:

1. **Warstwa Embedding**
2. **Warstwa Konwolucyjna (Conv1D)**: Zastosowano 128 filtrów konwolucyjnych o rozmiarze 5 z funkcją aktywacji ReLU.
3. **Warstwa GlobalMaxPooling1D**
4. **Warstwa Gęsta (Dense)**

<img width="413" alt="image" src="https://github.com/HochtaubelM/ZUM_zadanie_praca_domowa_nlp/assets/116303087/980afb06-b1d5-49c3-9c91-34fa2eb97dbe">

## Trenowanie Modelu:
Model został trenowany przez 5 epok na danych treningowych.
Osiągnął dokładność na zbiorze treningowym około 86%.
Na zbiorze walidacyjnym osiągnął dokładność około 81%.

Macierz pomyłek:

<img width="680" alt="image" src="https://github.com/HochtaubelM/ZUM_zadanie_praca_domowa_nlp/assets/116303087/c293fcdd-111e-4fd2-9dc7-9f82c6978f36">








