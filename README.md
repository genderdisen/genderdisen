### Neural Disentanglement of Gender from Content Semantics for Fair and Effective Re-ranking

This repository includes the code and experimental details for the paper "Neural Disentanglement of Gender from Content Semantics for Fair and Effective Re-ranking". 
Recent empirical research indicates that while neural ranking methods perform well in retrieval effectiveness, they often amplify stereotypical biases, particularly gender biases. Current mitigation strategies focus on modifying training methods or balancing training data but generally overlook direct attention to gender as an attribute. This paper introduces a systematic approach that explicitly acknowledges gender within neural ranker representations. The proposed neural disentanglement method separates content semantics from gender information in neural representations, enabling the ranker to assess document relevance based on content alone. Extensive experiments demonstrate that (1) the disentanglement approach achieves competitive retrieval effectiveness compared to baselines and maintains consistency across queries with different gender associations, (2) it produces unbiased document lists that do not favor any gender, and (3) it effectively captures gender information independently of semantic content.

## Results of stereotypical gender bias reduction on 215 gender-neutral query set, comparing with the state of the art baselines.
<div align="center">
<table style="font-size: smaller;">
  <thead>
    <tr>
      <th></th>
      <th colspan="6">Cut-off 10</th>
    </tr>
    <tr>
      <th></th>
      <th>MRR</th>
      <th>ARaB-tc&#8595;</th>
      <th>ARaB-tf&#8595;</th>
      <th>ARaB-bool&#8595;</th>
      <th>NFaIR&#8593;</th>
      <th>LIWC&#8595;</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Original Model</td>
      <td>0.1602</td>
      <td>0.3183</td>
      <td>0.1374</td>
      <td>0.1101</td>
      <td>0.8107</td>
      <td>1.023</td>
    </tr>
    <tr>
      <td>Advbert</td>
      <td>0.0093</td>
      <td>0.0304</td>
      <td>0.0022</td>
      <td>0.0008</td>
      <td>0.9854</td>
      <td>0.1134</td>
    </tr>
    <tr>
      <td>EDBT</td>
      <td>0.167</td>
      <td>0.1994</td>
      <td>0.0867</td>
      <td>0.0689</td>
      <td>0.8453</td>
      <td>0.8545</td>
    </tr>
    <tr>
      <td>CODER</td>
      <td>0.0152</td>
      <td>0.0254</td>
      <td>0.0240</td>
      <td>0.0313</td>
      <td>0.9336</td>
      <td>0.4114</td>
    </tr>
    <tr>
      <td>Light Weight</td>
      <td></td>
      <td></td>
      <td></td>
      <td></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td>Ours</td>
      <td>0.1877</td>
      <td>0.0737</td>
      <td>0.0460</td>
      <td>0.0567</td>
      <td>0.8664</td>
      <td>0.8404</td>
    </tr>
    <tr>
      <th></th>
      <th colspan="6">Cut-off 20</th>
    </tr>
    <tr>
      <th></th>
      <th>MRR</th>
      <th>ARaB-tc&#8595;</th>
      <th>ARaB-tf&#8595;</th>
      <th>ARaB-bool&#8595;</th>
      <th>NFaIR&#8593;</th>
      <th>LIWC&#8595;</th>
    </tr>
    <tr>
      <td>Original Model</td>
      <td>0.1658</td>
      <td>0.2635</td>
      <td>0.1142</td>
      <td>0.0920</td>
      <td>0.8274</td>
      <td>0.7966</td>
    </tr>
    <tr>
      <td>Advbert</td>
      <td>0.0103</td>
      <td>0.0289</td>
      <td>0.0028</td>
      <td>0.0016</td>
      <td>0.9824</td>
      <td>0.1101</td>
    </tr>
    <tr>
      <td>EDBT</td>
      <td>0.1722</td>
      <td>0.1674</td>
      <td>0.0725</td>
      <td>0.0576</td>
      <td>0.8564</td>
      <td>0.6426</td>
    </tr>
    <tr>
      <td>CODER</td>
      <td>0.0155</td>
      <td>0.0351</td>
      <td>0.0263</td>
      <td>0.0311</td>
      <td>0.9348</td>
      <td>0.3491</td>
    </tr>
    <tr>
      <td>Light Weight</td>
      <td></td>
      <td></td>
      <td></td>
      <td></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td>Ours</td>
      <td>0.1941</td>
      <td>0.0574</td>
      <td>0.0350</td>
      <td>0.0422</td>
      <td>0.8722</td>
      <td>0.7170</td>
    </tr>
  </tbody>
</table>
</div>div>
## Results of stereotypical gender bias reduction on 1765 gender-neutral query set, comparing with the state of the art baselines.
<div align="center">
<table style="font-size: smaller;">
  <thead>
    <tr>
      <th></th>
      <th colspan="6">Cut-off 10</th>
    </tr>
    <tr>
      <th></th>
      <th>MRR</th>
      <th>ARaB-tc&#8595;</th>
      <th>ARaB-tf&#8595;</th>
      <th>ARaB-bool&#8595;</th>
      <th>NFaIR&#8593;</th>
      <th>LIWC&#8595;</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Original Model</td>
      <td>0.2673</td>
      <td>0.1535</td>
      <td>0.0721</td>
      <td>0.0611</td>
      <td>0.7066</td>
      <td>1.5599</td>
    </tr>
    <tr>
      <td>Advbert</td>
      <td>0.0081</td>
      <td>0.0051</td>
      <td>0.0018</td>
      <td>0.000267</td>
      <td>0.9657</td>
      <td>0.2374</td>
    </tr>
    <tr>
      <td>EDBT</td>
      <td>0.2814</td>
      <td>0.0506</td>
      <td>0.0256</td>
      <td>0.0218</td>
      <td>0.7396</td>
      <td>1.4368</td>
    </tr>
    <tr>
      <td>CODER</td>
      <td>0.0021</td>
      <td>0.1507</td>
      <td>0.0721</td>
      <td>0.0663</td>
      <td>0.8404</td>
      <td>0.7199</td>
    </tr>
    <tr>
      <td>Light Weight</td>
      <td>0.2756</td>
      <td></td>
      <td>0.0195</td>
      <td>0.0174</td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td>Ours</td>
      <td>0.2969</td>
      <td>0.0805</td>
      <td>0.0131</td>
      <td>0.0178</td>
      <td>0.7623</td>
      <td>1.4521</td>
    </tr>
    <tr>
      <th></th>
      <th colspan="6">Cut-off 20</th>
    </tr>
    <tr>
      <th></th>
      <th>MRR</th>
      <th>ARaB-tc&#8595;</th>
      <th>ARaB-tf&#8595;</th>
      <th>ARaB-bool&#8595;</th>
      <th>NFaIR&#8593;</th>
      <th>LIWC&#8595;</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Original Model</td>
      <td>0.2726</td>
      <td>0.0721</td>
      <td>0.0641</td>
      <td>0.0538</td>
      <td>0.722</td>
      <td>1.3001</td>
    </tr>
    <tr>
      <td>Advbert</td>
      <td>0.0099</td>
      <td>0.0025</td>
      <td>0.0003</td>
      <td>0.0014</td>
      <td>0.9642</td>
      <td>0.2283</td>
    </tr>
    <tr>
      <td>EDBT</td>
      <td>0.2868</td>
      <td>0.0256</td>
      <td>0.0192</td>
      <td>0.0152</td>
      <td>0.7527</td>
      <td>1.1809</td>
    </tr>
    <tr>
      <td>CODER</td>
      <td>0.0025</td>
      <td>0.1490</td>
      <td>0.0716</td>
      <td>0.0663</td>
      <td>0.8407</td>
      <td>0.6467</td>
    </tr>
    <tr>
      <td>Light Weight</td>
      <td></td>
      <td></td>
      <td></td>
      <td></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td>Ours</td>
      <td>0.3023</td>
      <td>0.0131</td>
      <td>0.0313</td>
      <td>0.0052</td>
      <td>0.7658</td>
      <td>1.2767</td>
    </tr>
  </tbody>
</table>
<div>

# Performance of the original, and disentangled models on male, and female affiliated queries.

<div style="center;">
  <table style="font-size: x-small; width: 50%; margin: 0 auto; border-collapse: collapse;">
    <caption>Performance of the original, and disentangled models on male, and female affiliated queries.</caption>
    <thead>
      <tr>
        <th></th>
        <th colspan="3">Cut-off 10</th>
        <th colspan="3">Cut-off 20</th>
      </tr>
      <tr>
        <th></th>
        <th>Male</th>
        <th>Female</th>
        <th>&#916;</th>
        <th>Male</th>
        <th>Female</th>
        <th>&#916;</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>Original Model</td>
        <td>0.3939</td>
        <td>0.3178</td>
        <td>19.3196</td>
        <td>0.4002</td>
        <td>0.3242</td>
        <td>0.1899</td>
      </tr>
      <tr>
        <td>Disentangled Model</td>
        <td>0.4093</td>
        <td>0.3511</td>
        <td>14.2194</td>
        <td>0.4146</td>
        <td>0.3572</td>
        <td>0.1384</td>
      </tr>
      <tr>
        <td>Improvement</td>
        <td>3.9096</td>
        <td>10.4783</td>
        <td>-26.3991</td>
        <td>3.5982</td>
        <td>10.1789</td>
        <td>-27.1195</td>
      </tr>
    </tbody>
  </table>
</div>

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


