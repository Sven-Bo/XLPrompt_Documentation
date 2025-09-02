# Do I need a powerful computer to run local AI with XLlama?

That’s probably one of the first questions that comes to mind, and it’s a good one.

Here’s what’s going on under the hood: **XLlama is built on top of Ollama**, which handles the actual model loading and execution. Ollama itself uses a backend called **llama.cpp**, designed to run models locally on your machine.

So when you ask “what kind of computer do I need,” the real answer is:\
**It depends on the model you choose.**

***

#### Lighter models, lighter requirements

Some models are small and efficient. Others are massive and hungry for memory. If you're just getting started or working on a regular laptop, here’s the rule of thumb:

* If your laptop isn’t older than **5 or 6 years** and you have at least **8GB of RAM**, you're good to go for **small models**
* You **don’t need a dedicated GPU** to get started. Small models like **TinyLLaMA** (around 638 MB) or **Gemma 3B:1b** (around 815 MB) can run on the **CPU**
* Things might run a bit slower on CPU, but they still work fine for basic use

***

#### What happens with bigger models?

Once you go beyond the small ones, like 13B or larger, you’ll start to need more power:

* **More RAM** (16GB or more recommended)
* Ideally a **dedicated GPU** with enough **VRAM** (8GB or more)
* A system that can handle heavier memory loads without slowing down

In short, the bigger the model, the more your system needs to keep up.

***

#### So… will it work?

Most likely, yes, especially if you start small. XLlama won’t break anything. If a model is too large, it either won’t load or will run very slowly.

Just save your work first — especially any open Excel files — and give it a try. Better safe than sorry 😉
