---
language: 
  - zh
license: apache-2.0
widget:
- text: "生活的真谛是[MASK]。"
---
# Zhouwenwang-110M model (Chinese)，one model of [Fengshenbang-LM](https://github.com/IDEA-CCNL/Fengshenbang-LM).
We modify the original position code of longformer to rotational position coding，and on the basis of [chinese_roformer_L-12_H-768_A-12.zip](https://github.com/ZhuiyiTechnology/roformer), use 180G of data to continue training

## Usage
There is no structure of Longformer-base in [Transformers](https://github.com/huggingface/transformers), you can run follow code to get structure of Zhouwenwang-110M from [Fengshenbang-LM](https://github.com/IDEA-CCNL/Fengshenbang-LM)

 ```shell
 git clone https://github.com/IDEA-CCNL/Fengshenbang-LM.git
 ```

### Load Model
```python
from fengshen import LongformerModel    
from fengshen import LongformerConfig
from transformers import BertTokenizer

tokenizer = BertTokenizer.from_pretrained("IDEA-CCNL/longformer_base")
config = LongformerConfig.from_pretrained("IDEA-CCNL/longformer_base")
model = LongformerModel.from_pretrained("IDEA-CCNL/longformer_base")
```



## Citation
If you find the resource is useful, please cite the following website in your paper.

```
@misc{Fengshenbang-LM,
  title={Fengshenbang-LM},
  author={IDEA-CCNL},
  year={2021},
  howpublished={\url{https://github.com/IDEA-CCNL/Fengshenbang-LM}},
}
```