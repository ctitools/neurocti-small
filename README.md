

# neurocti-small

![asian-hacker-512](https://github.com/ctitools/neurocti-small/assets/750019/30b6afa8-ee24-4e6b-a47c-f39191cc114b)


This repository shows you how to use the [neurocti-small](https://huggingface.co/ctitools/neurocti-small) model.
It is a [LoRA](https://arxiv.org/abs/2106.09685) adapter on top of [llama-3-8b-instruct](https://huggingface.co/meta-llama/Meta-Llama-3-8B-Instruct).

Please note that this is currently still the small model based on llama-3-8B-instruct and we are re-training on a bigger model.
So, it makes sense to try this model out, but then switch to the bigger one to leverage the bigger model's capabilities.

# Using it

## Transformers library

(coming)

## oobabooga

(https://github.com/oobabooga/text-generation-webui)

Go to the `Models` tab and then enter `ctitools/neurocti-small` into the "Download model or LoRA" field. Press "Download"
Then refresh the "Loras" dropdown box and then apply the Lora adapter.

<img width="1482" alt="Screenshot 2024-06-14 at 09 33 14" src="https://github.com/ctitools/neurocti-small/assets/750019/f9caa3d3-63dc-439a-836e-1720b090c4cd">

Go to the chat interface and make sure that the instruct-chat option is selected
<img width="1482" alt="Screenshot 2024-06-14 at 09 37 10" src="https://github.com/ctitools/neurocti-small/assets/750019/78968bee-959c-4825-aa95-618fcc3e93da">


Note that due to the smaller size (llama-3-8B based), the model sometimes get's it wrong. In that case, just repeat your question in the chat, like so:

<img width="1482" alt="Screenshot 2024-06-14 at 09 54 11" src="https://github.com/ctitools/neurocti-small/assets/750019/e3f99875-4872-4db3-b89f-4f98540623c5">

### JSON mode

In oobabooga, switch to the `Parameters` tab and select a JSON grammar. Also make sure that your prompt contains something like `Write the answer in JSON format`. It also helps to give examples (few-shot prompting).

