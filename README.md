# Self-Adaptive Cognitive Debiasing for Large Language Models in Decision-Making
You can run this project easy following these step.

Before run any ipynb file you should add you openai-api-key or llama3-70b-key to file.

### API
We use gpt3.5-0125 and gpt-4o from openai, you can use your keys.

We use llama3-70b from groq, its free you can get the keys from Groq.

### Get Data
First, you can download the original dataset from the link in the dataset paper.

Then you should make a new folder named data and add the original dataset.

You can get a jsonl after you run the ```data_process.ipynb```

The jsonl while buile in data files.

### Evaluate
You can run any Bias type and DeBias methods use the jsonl file that get in the first step.

First add the openai-key in file start.
```
client = OpenAI(
    api_key="",
)
```
Then you can run the any file that you need.


### Get Result
Run the judge_correct.ipynb you can get the accuracy of the ans.

### File Descroption
In every domain and any Bias type (same in paper), you can see many files.
```
availableing-bias.ipynb(same name with folder) answer the question contain bias don't use any methods
cot.ipynb answer the question contain bias use cot 
few shot.ipynb answer the question contain bias use few_shot
few shot1.ipynb answer the question contain bias use few_shot
multi-debate.ipynb answer the question contain bias use multi-debate 
self_help.ipynb answer the question contain bias use self_help
reflexion.ipynb answer the question contain bias use reflexion
our_methods.ipynb answer the question contain bias use our methods
without_think.ipynb and without_while.ipynb the ablation study
ground_true.ipynb get the origin answer without any bias
judge_correct.ipynb get the accuracy of methods
```
