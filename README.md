# JEEBench(EMNLP 2023)
Repository for the code and dataset for the paper: "Have LLMs Advanced Enough? A Harder Problem Solving Benchmark For Large Language Models" accepted in EMNLP 2023 as a Main conference paper. https://aclanthology.org/2023.emnlp-main.468/

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
@inproceedings{arora-etal-2023-llms,
    title = "Have {LLM}s Advanced Enough? A Challenging Problem Solving Benchmark For Large Language Models",
    author = "Arora, Daman  and
      Singh, Himanshu  and
      {Mausam}",
    editor = "Bouamor, Houda  and
      Pino, Juan  and
      Bali, Kalika",
    booktitle = "Proceedings of the 2023 Conference on Empirical Methods in Natural Language Processing",
    month = dec,
    year = "2023",
    address = "Singapore",
    publisher = "Association for Computational Linguistics",
    url = "https://aclanthology.org/2023.emnlp-main.468",
    doi = "10.18653/v1/2023.emnlp-main.468",
    pages = "7527--7543",
    abstract = "The performance of large language models (LLMs) on existing reasoning benchmarks has significantly improved over the past years. In response, we present JEEBench, a considerably more challenging benchmark dataset for evaluating the problem solving abilities of LLMs. We curate 515 challenging pre-engineering mathematics, physics and chemistry problems from the highly competitive IIT JEE-Advanced exam. Long-horizon reasoning on top of deep in-domain knowledge is essential for solving problems in this benchmark. Our evaluation on various open-source and proprietary models reveals that the highest performance, even after using techniques like self-consistency, self-refinement and chain-of-thought prompting, is less than 40{\%}. The typical failure modes of GPT-4, the best model, are errors in algebraic manipulation, difficulty in grounding abstract concepts into mathematical equations accurately and failure in retrieving relevant domain-specific concepts. We also observe that by mere prompting, GPT-4 is unable to assess risk introduced by negative marking for incorrect answers. For this, we develop a post-hoc confidence-thresholding method over self-consistency, which enables effective response selection. We hope that our challenging benchmark will guide future re-search in problem-solving using LLMs.",
}
```


