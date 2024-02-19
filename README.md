# PromptL-I-N-K

Modified from the original ULTRA implementation, which can be found here: [https://github.com/DeepGraphLearning/ULTRA](https://github.com/DeepGraphLearning/ULTRA)

Please download ultra/rspmm files from the ULTRA repository.

The Original Ingram Datasets will be automatically downloaded on the first run.

#### Call LLMs for prompt graph

```python script/llm_relgraph.py```

#### Pretrain GNN model

```torchrun --nproc_per_node=3 script/pretrain.py -c /path/to/config/transductive/pretrain_3g.yaml --gpus [0,1,2]```

#### FewShot-Evaluation

```python script/run_fewshot.py -c /path/to/config/inductive/inference.yaml --gpus [0] --ckpt /path/to/ultra/ckpts/ultra_3g.pth -d FBIngram:100,WKIngram:100,NLIngram:100```

Thanks for the source code and datasets provided by ULTRA team.
