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
Availableing-bias.ipynb (same file's name with folder) answer the question contain bias don't use any methods
Cot.ipynb answer the question contain bias use cot
Zero-shot.ipynb answer the question contain bias use self_help
Few shot.ipynb answer the question contain bias use few_shot
Multi-agent debate.ipynb answer the question contain bias use multi-debate 
Self_help.ipynb answer the question contain bias use self_help
Reflexion.ipynb answer the question contain bias use reflexion
SACD.ipynb answer the question contain bias use our methods
```
