Here are some findings that I noted while collecting resources for russian lmentry tasks.

## Table of contents
1. [nouns_by_category](#nouns_by_category)
2. [homophones](#homophones)
3. [lmentry_words_ru](#lmentry_words_ru)
4. [phonetically_unambiguous_words](#phonetically_unambiguous_words)
5. [plurals](#plurals)
6. [rhyme_groups](#rhyme_groups)
7. [simple_sentences](#simple_sentences)

## nouns_by_category
In the original file there are 5 categories: animals, items of clothing, fruit, furniture, vehicles. However, there are some problems:

1. There are more semantic categories listed in the Russian National Corpus (RNC).
They include:
- животные
- растения
- вещества и материалы
- пространство и место
- здания и сооружения
- инструменты и приспособления
a. инструменты
b. механизмы и приборы
c. транспортные средства
d. оружие
e. музыкальные инструменты
f. мебель
g. посуда
h. одежда и обувь
- еда и напитки
- тексты

Surely, not all categories should necessarily be used, but it has to be mentioned that there are more than 5 different categories.

2. Undoubtedly, words in each category should reflect that category as accurately as possible. Nevertheless, there are some differences between English and Russian languages. For example, I wouldn't say that "mango" and "pineapple" are the first fruit that come to mind than russian people (including me) think about fruit in general. And as far as I'm concerned "watermelon" doesn't apply to fruits, as many people know. Ofcourse, it's just my assumption that should be proved by linguistic research. But at this stage of work I think such words should be excluded from the list. 

3. Translation difficulty is another issue. Some English words aren't easy to translate to Russian using one noun only without changing its meaning. It particularly concerns such words as "bookcase" ("книжный шкаф"/"этажерка"), "truck" and "van" ("грузовик" и "фургон"; фургон - это грузовой автомобиль)

Some other notes:
1. In the "animals" category in the original json-file, only domestic animals are indicated ("cat", "chicken", "cow", "dog" etc). A search in the RNC corpus among the most frequent words returns both domestic and wild animals. Possibly, it makes sense to separate them. Perhaps, in the final version of the work it is worth taking only one category: either only domestic, or only wild. The same issue applies to the “vehicles” category, since the corpus data can be divided into land and water vehicles. Now I include both of them, but may be later I'll take only one.

2. Shall I use letter "ё" while selecting words for the tasks? Currently I don't.

3. The category "растения" in RNC can be divided by 2: trees and flowers.

4. The category "вещества и материалы" mentioned in RNC includes a wide variety of words: "вода", "хлеб" (more associated with "food" category), "дождь", "стул" (more associated with "furniture" category) and others. So, I decided not to include it in the tasks.

The same applies to the categories "пространство и место", "инструменты", "механизмы и приборы" which are quite abstract and involve words with diverse semantics.

The category "здания и сооружения" is also heterogeneous and can be divided into numerous cateories: residential or non-residential, open or closed, heated or unheated and so on. I don't include it.

5. Among the words in the "одежда и обувь" category it is possible to find some subcategories: shoes, hats, some outdated names of clothing ("мундир", "шинель", "картуз" etc). I chose only "traditional" clothes.

6. In the category "еда и напитки" I examine separately food and drinks, so there are 2 subcategories now. I suppose it makes sense. The category "food" itself seems to be heterogeneous
too. There can be distinguished such categories as ready food, fruit, vegetables, fish, meat... I'll fix this problem either by dividing "еда" category into subcategories or including only some of the subcategories, e.g. fruit and vegetables.

## simple_sentences
Simple sentences are extarcted from the PARus dataset. 

I extracted all the sentences from all json-files - test, train, val - and merged them into one csv-file.

Total number of sentences: 

The simplicity of sentences might be checked taking into account quantitative (length of the text, sentences, words) parameters.
