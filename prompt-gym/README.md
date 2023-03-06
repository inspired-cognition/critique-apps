# Prompt Gym

by [Inspired Cognition](https://inspiredco.ai)

Recently, many AI-based applications are based on large language models and *prompting*, where you write a textual prompt and the model generates a response. However, app engineers and researchers are often faced with a hard decision of *which prompt to use* and *which model to use it with*.

 [Prompt Gym](prompt-gym.ipynb) is a Jupyter notebook that demonstrates how to simply play around with prompts for text generation, testing **different models** and **different prompts** and evaluating according to **different criteria**.

<p align="center">
<img src="prompt-gym.png"  width="256" height="256">
</p>

In the example here we test two different companies' text generation models, [OpenAI's GPT-3](https://openai.com/blog/gpt-3-apps/), and [Cohere's text generation models](https://cohere.ai/generate). Evaluation of the models is done with the [Inspired Cognition Critique](https://docs.inspiredco.ai/critique/) tool for text generation evaluation. We demonstrate the case for text summarization on 10 examples from the [CNN-DailyMail dataset](https://huggingface.co/datasets/cnn_dailymail). But you can swap in whatever models, prompts, metrics, and data that you would like to try on other tasks too!

By the end of the exploration, you will have a **comprehensive report** of which prompts and models work well along a number of axes, like the actual table below that was generated from this notebook:

| Model | Prompt | UniEval (Relevance) | UniEval (Consistency) | UniEval (Coherence) | UniEval (Fluency) | BartScore (Coverage) | Length Ratio |
| --- | --- | --- | --- | --- | --- | --- | --- |
| cohere_command_xlarge | standard | 0.9144 | 0.8998 | 0.9085 | 0.9474 | -3.1686 | 1.1700 |
| openai_davinci_003 | concise | 0.9063 | 0.8328 | 0.9373 | 0.8819 | -3.0728 | 2.5300 |
| cohere_command_xlarge | complete | 0.8978 | 0.9146 | 0.9299 | 0.9371 | -3.3028 | 1.3867 |
| openai_davinci_003 | standard | 0.8974 | 0.8760 | 0.9489 | 0.9232 | -3.1167 | 2.6200 |
| cohere_command_xlarge | tldr | 0.8954 | 0.8753 | 0.9086 | 0.9557 | -3.3080 | 1.0000 |
| cohere_command_xlarge | concise | 0.8899 | 0.9006 | 0.9109 | 0.9475 | -3.3431 | 0.9333 |
| openai_gpt_3.5_turbo | standard | 0.8628 | 0.9129 | 0.9757 | 0.8902 | -3.0634 | 2.6233 |
| openai_davinci_003 | complete | 0.8568 | 0.9153 | 0.9412 | 0.9347 | -3.1098 | 2.6667 |
| openai_davinci_003 | tldr | 0.8232 | 0.9242 | 0.9490 | 0.9504 | -3.0339 | 2.5700 |
| openai_gpt_3.5_turbo | tldr | 0.8008 | 0.8856 | 0.9430 | 0.8988 | -3.1236 | 2.6000 |
| openai_gpt_3.5_turbo | complete | 0.7859 | 0.8820 | 0.9509 | 0.9045 | -3.0904 | 2.6967 |
| openai_gpt_3.5_turbo | concise | 0.7108 | 0.8712 | 0.8674 | 0.8798 | -3.0555 | 2.6033 |

Some pointers into how to do **further exploration** into the results, such as finding examples where a particular method is doing well or poorly, or where one method is outperforming the other.

**[Click through to the notebook now and try it out!](prompt-gym.ipynb)**

If you want to discuss more, you can join the [Inspired Cognition Discord](https://discord.com/invite/vJHdpCBqWN) or get in touch through our [contact page](https://inspiredco.ai/contact/), we love talking about applications of generative AI!