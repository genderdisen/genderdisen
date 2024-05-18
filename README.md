### Neural Disentanglement of Gender from Content Semantics for Fair and Effective Re-ranking

This repository includes the code and experimental details for the paper "Neural Disentanglement of Gender from Content Semantics for Fair and Effective Re-ranking". 
Recent empirical research indicates that while neural ranking methods perform well in retrieval effectiveness, they often amplify stereotypical biases, particularly gender biases. Current mitigation strategies focus on modifying training methods or balancing training data but generally overlook direct attention to gender as an attribute. This paper introduces a systematic approach that explicitly acknowledges gender within neural ranker representations. The proposed neural disentanglement method separates content semantics from gender information in neural representations, enabling the ranker to assess document relevance based on content alone. Extensive experiments demonstrate that (1) the disentanglement approach achieves competitive retrieval effectiveness compared to baselines and maintains consistency across queries with different gender associations, (2) it produces unbiased document lists that do not favor any gender, and (3) it effectively captures gender information independently of semantic content.

### Train

Training the minilm-L6 model:

Original model:

```
python my_train_original.py -vocab sentence-transformers/msmarco-MiniLM-L6-cos-v5 -pretrain sentence-transformers/msmarco-MiniLM-L6-cos-v5 -res <results_path> -save <checkpoint_save_path> -n_warmup_steps 160000 -batch_size 16 -attribute_dim 100 -optimizer adam -lr 3e-6
```

Disentangled Model:
```
python my_train_disentangled.py -vocab sentence-transformers/msmarco-MiniLM-L6-cos-v5 -pretrain sentence-transformers/msmarco-MiniLM-L6-cos-v5 -res <results_path> -save <checkpoint_save_path> -n_warmup_steps 160000 -batch_size 16 -attribute_dim 50 -optimizer adam -lr 3e-4
```
Training the bert-mini model:

Original Model:
```
python my_train_original.py -vocab prajjwal1/bert-mini -pretrain prajjwal1/bert-mini -res <results_path> -save <checkpoint_save_path> -n_warmup_steps 160000 -batch_size 16 -lr 3e-6 -max_query_len 32 -max_doc_len 221

```

disentabgled Model:
```
python my_train_disentangled.py -vocab prajjwal1/bert-mini -pretrain prajjwal1/bert-mini -res .<results_path> -save <checkpoint_save_path> -n_warmup_steps 160000 -batch_size 16 -attribute_dim 50 -optimizer 'adam' -lr 3e-5 -max_query_len 32 -max_doc_len 221 -alpha 1 -betta 1 -gamma 1
```


### inference

minilm


```
python inference_disentanglement.py -task ranking -model bert -max_input 600000000 -vocab sentence-transformers/msmarco-MiniLM-L6-cos-v5 -pretrain sentence-transformers/msmarco-MiniLM-L6-cos-v5  -checkpoint <checkpoint_save_path> -res <result_path> -max_query_len 32 -max_doc_len 221 -batch_size 256 -attribute_dim 50 -test queries=<test_query_path>,docs=<collection_path>,trec=<run_path>
```

bert-mini


```
python inference_disentanglement.py -task ranking -model bert -max_input 600000000 -vocab prajjwal1/bert-mini -pretrain prajjwal1/bert-mini -checkpoint ${save_path} -res ${res_path} -max_query_len 32 -max_doc_len 221 -batch_size 256 -attribute_dim 50 -test queries=<test_query_path>,docs=<collection_path>,trec=<run_path>
```

### evaluation

MRR

```
python calculate_mrr.py -qrels <qrels_path> -run <run_path>
```

ARaB

NFair

LIWC


