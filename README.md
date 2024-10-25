# late-chunking-ru
### ИССЛЕДОВАНИЕ ВЛИЯНИЯ ПОЗДНЕГО ФРАГМЕНТИРОВАНИЯ ДОКУМЕНТОВ НА КАЧЕСТВО ПОЛНОТЕКСТОВОГО ПОИСКА В КОЛЛЕКЦИИ РУССКОЯЗЫЧНЫХ ТЕКСТОВ С ИСПОЛЬЗОВАНИЕМ ЯЗЫКОВЫХ МОДЕЛЕЙ ДЛЯ СОЗДАНИЯ ЭМБЕДДИНГОВ /  RESEARCH ON THE IMPACT OF LATE DOCUMENT CHUNKING ON THE QUALITY OF FULL-TEXT SEARCH IN A COLLECTION OF RUSSIAN-LANGUAGE TEXTS USING LANGUAGE MODELS FOR CREATING EMBEDDINGS

Исследование проводилось по метрикам качества поиска при K = 5. Поиск проводится по фрагментам документов, поэтому в результатах поиска берётся первое вхождение каждого документа, ведь несколько фрагментов одного документа могут попасть в результаты поиска по запросу.

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
