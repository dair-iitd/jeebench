# JEEBench(EMNLP 2023)
Repository for the code and dataset for the paper: "Have LLMs Advanced Enough? A Harder Problem Solving Benchmark For Large Language Models" accepted in EMNLP 2023 as a Main conference paper. 

![respresentative](https://github.com/dair-iitd/jeebench/assets/45387992/d0d14064-bce9-4b58-ac3f-87fef18fcff3)

## Dataset 

To access the dataset, unzip the dataset.zip file. This contains the dataset, few-shot examples and responses collected from GPT models along with extracted answers. 
The dataset contains questions from Physics, Chemistry and Mathematics collected from JEE Advanced 2016 to 2023. The breakdown with respect to subject type and response type is as follows:

<img src="https://github.com/dair-iitd/jeebench/assets/45387992/592af8bc-6a5f-457e-a8d8-806046e0463a" alt="drawing" width="500"/>


## Quick example

To run a baseline such as GPT-3.5 with zero-shot Chain of Thought on the first 10 questions of the dataset using 2 parallel requests, run:
`python inference.py --model gpt-3.5-turbo --mode CoT --max_questions 1 --num_procs 2`

To evaluate your results, use the code provided in compute_metrics.py:
`python compute_metrics.py`

## Baselines
![image](https://github.com/dair-iitd/jeebench/assets/45387992/3d79ba50-d4a3-4ba5-9a84-32b74ae5a887)


## Citation

If you use our dataset in your research, please cite it using the following
```latex
@misc{arora2023llms,
      title={Have LLMs Advanced Enough? A Challenging Problem Solving Benchmark For Large Language Models}, 
      author={Daman Arora and Himanshu Gaurav Singh and Mausam},
      year={2023},
      eprint={2305.15074},
      archivePrefix={arXiv},
      primaryClass={cs.CL}
}
```


