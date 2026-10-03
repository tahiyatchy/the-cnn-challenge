# AI Usage

## AI Tools Used
* **Google Gemini 3.1 Pro**
* **Gemini 2.5 Flash** (As Google Colab Assistant)

---

## Representative Ways AI Assisted

1. Suggesting a list of potential models to try and why they might be suitable for training on an image dataset of only 2400 samples.
2. Suggesting ways to develop a training stage with finetuning.
3. Catching mismatched parameters due to remnants from the previous model that were overlooked after the model was replaced, e.g. code that assumes a grayscale input when the model is supposed to take RGB input, but was not used to implement code fixes.

---

## Ineffective / Incorrect AI Suggestions

When reusing code across models, the Gemini assistant built into Google Colab assisted in explaining errors thrown by  inconsistencies like attributes which existed for one model but not the other, such as ResNet not having an attribute classifier like ConvNeXt-Tiny, which is used in the latter’s training code. However, the suggested fixes were rejected because, while being technically correct in that the code would run, they contradict mechanisms selected to carry out training. Because the Gemini Colab Assistant prioritizes execution without errors, something which may seem like a banal rewrite may completely change the program's behavior, or at least add style faux pas like redundant imports throughout the notebook.

## Key Human-Made Experimental Decision

One key experimental decision I made was to include data augmentation to the preprocessing stage and implementing it. Additionally, I decided which CNN architectures would be implemented and how based on further reading of documentation and main papers after receiving a list of suggestions from Gemini 3.1 Pro. 
