# Failed to get a valid response from Ollama (HTTP Status: 500)

### Error message

`llama runner process has terminated: error loading model: unable to locate cpu buffer`

***

### What it means

This usually happens when **Ollama can't allocate enough memory** to load the model. If you're running on CPU with limited RAM, it may not be able to create the necessary buffer for the model.

### How to fix it

**Try using a smaller model**, such as:

* **TinyLLaMA** (638 MB)
* **Gemma 3B:1b** (815 MB)

These use less memory and typically work fine even on systems without a dedicated GPU.

{% hint style="info" %}
Tip: Always save your work before trying a larger model. If it doesn’t load, no harm done — just try a lighter one.
{% endhint %}

