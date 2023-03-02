# Prompt Gym

by [Inspired Cognition](https://inspiredco.ai)

Recently, many AI-based applications are based on large language models and *prompting*, where you write a textual prompt and the model generates a response. However, app engineers and researchers are often faced with a hard decision of *which prompt to use* and *which model to use it with*.

 [Prompt Gym](prompt-gym.ipynb) is a Jupyter notebook that demonstrates how to simply play around with prompts for text generation, testing **different models** and **different prompts** and evaluating according to **different criteria**.

<p align="center">
<img src="prompt-gym.png"  width="256" height="256">
</p>

In the example here we test two different companies' text generation models, [OpenAI's GPT-3](https://openai.com/blog/gpt-3-apps/), and [Cohere's text generation models](https://cohere.ai/generate). Evaluation of the models is done with the [Inspired Cognition Critique](https://docs.inspiredco.ai/critique/) tool for text generation evaluation. We demonstrate the case for text summarization on 10 examples from the [CNN-DailyMail dataset](https://huggingface.co/datasets/cnn_dailymail). But you can swap in whatever models, prompts, metrics, and data that you would like to try on other tasks too!

By the end of the exploration, you will have a **comprehensive report** of which prompts and models work well along a number of axes, like the actual table below that was generated from this notebook:

| Model | Prompt | UniEval (Consistency) | UniEval (Coherence) | UniEval (Fluency) | UniEval (Relevance) | BartScore (Coverage) | Length Ratio |
| --- | --- | --- | --- | --- | --- | --- | --- |
| cohere_medium | standard | 0.7466 | 0.4006 | 0.8869 | 0.3438 | -3.4095 | 2.5533 |
| cohere_medium | tldr | 0.5006 | 0.2967 | 0.8539 | 0.3312 | -3.1348 | 2.5800 |
| cohere_medium | concise | 0.8542 | 0.6115 | 0.9140 | 0.6167 | -3.4220 | 2.4500 |
| cohere_medium | complete | 0.8331 | 0.4845 | 0.8825 | 0.5214 | -3.1689 | 2.6767 |
| openai_babbage_001 | standard | 0.9409 | 0.9036 | 0.8782 | 0.7975 | -3.4083 | 2.0800 |
| openai_babbage_001 | tldr | 0.8728 | 0.9072 | 0.9593 | 0.8145 | -3.5234 | 1.0200 |
| openai_babbage_001 | concise | 0.9483 | 0.9365 | 0.8669 | 0.8431 | -3.2528 | 2.2800 |
| openai_babbage_001 | complete | 0.9306 | 0.8278 | 0.8634 | 0.6951 | -3.2720 | 2.2633 |
| openai_ada_001 | standard | 0.6750 | 0.7270 | 0.8850 | 0.8174 | -3.6719 | 2.0067 |
| openai_ada_001 | tldr | 0.7999 | 0.7122 | 0.7973 | 0.6728 | -3.7436 | 1.5300 |
| openai_ada_001 | concise | 0.7776 | 0.7439 | 0.8106 | 0.5852 | -3.6096 | 2.3600 |
| openai_ada_001 | complete | 0.7732 | 0.5008 | 0.7332 | 0.3283 | -3.5246 | 2.4567 |

Some pointers into how to do **further exploration** into the results, such as finding examples where a particular method is doing well or poorly, or where one method is outperforming the other.

**[Click through to the notebook now and try it out!](prompt-gym.ipynb)**

If you want to discuss more, you can join the [Inspired Cognition Discord](https://discord.com/invite/vJHdpCBqWN) or get in touch through our [contact page](https://inspiredco.ai/contact/), we love talking about applications of generative AI!