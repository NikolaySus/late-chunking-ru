# late-chunking-ru

### ИССЛЕДОВАНИЕ ВЛИЯНИЯ ПОЗДНЕГО ФРАГМЕНТИРОВАНИЯ ДОКУМЕНТОВ НА КАЧЕСТВО ПОЛНОТЕКСТОВОГО ПОИСКА В КОЛЛЕКЦИИ РУССКОЯЗЫЧНЫХ ТЕКСТОВ С ИСПОЛЬЗОВАНИЕМ ЯЗЫКОВЫХ МОДЕЛЕЙ ДЛЯ СОЗДАНИЯ ЭМБЕДДИНГОВ /  RESEARCH ON THE IMPACT OF LATE DOCUMENT CHUNKING ON THE QUALITY OF FULL-TEXT SEARCH IN A COLLECTION OF RUSSIAN-LANGUAGE TEXTS USING LANGUAGE MODELS FOR CREATING EMBEDDINGS

Исследование проводилось по метрикам качества поиска при K = 5. Поиск проводится по фрагментам текстов, поэтому в результатах поиска берётся первое вхождение каждого текста, ведь несколько фрагментов одного текста могут попасть в результаты поиска по запросу.

### Подготовка к запуску ноутбуков:

* Установите пакеты из [requirements.txt](requirements.txt).
* Скачайте [данные](https://drive.google.com/file/d/1F07Hjit8OAGcKjJcZ4CwFrlOWhhkqXi1/view?usp=sharing) и распакуйте в директорию [ai-forever-ria-news-retrieval](ai-forever-ria-news-retrieval). Если хотите пропустить крайне ресурсозатратный этап в [data-to-emb.ipynb](data-to-emb.ipynb), то можете скачать [данные с готовыми эмбеддингами](https://sharedby.blomp.com/7E6IJ6) (осторожно, архив весит 27,4 ГБ, а в распакованном виде 45,4 ГБ).

### Порядок просмотра/запуска ноутбуков:

* [data-info.ipynb](data-info.ipynb) — ноутбук для понимания, что из себя представляет датасет
* [data-to-emb.ipynb](data-to-emb.ipynb) — ноутбук для генерации эмбеддингов фрагментов текстов и запросов
* [emb-fix-record.ipynb](emb-fix-record.ipynb) — ноутбук для исправления особенности датасета
* [emb-to-qdrant.ipynb](emb-to-qdrant.ipynb) — ноутбук для занесения эмбеддингов фрагментов текстов в векторную БД qdrant
* [qdrant-to-stats.ipynb](qdrant-to-stats.ipynb) — ноутбук для измерения качества поиска по фрагментам текстов/текстам

results/результаты
```
{chunks_embedded_trad}
  MNDCG_K=0.6870302533259881
  MAP_K=0.6542466666666595
{chunks_embedded_new}
  MNDCG_K=0.8500745753240168
  MAP_K=0.8270649999999947
CPU times: total: 3min 58s
Wall time: 8h 4min 52s
```

citations/цитаты
```
@article{gunther2024late,
  title={Late Chunking: Contextual Chunk Embeddings Using Long-Context Embedding Models},
  author={G{\"u}nther, Michael and Mohr, Isabelle and Williams, Daniel J and Wang, Bo and Xiao, Han},
  journal={arXiv preprint arXiv:2409.04701},
  year={2024}
}
```
