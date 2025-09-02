# Error: pull model manifest: 412

If you see this message when trying to install a model:

<figure><img src=".gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

…it means your current Ollama version is outdated and doesn’t support the model you're trying to install.

***

**✅ How to fix it**

1. Go to the official download page:\
   https://ollama.com/download
2. Download and install the latest version for your operating system.
3.  Once updated, open a terminal and try pulling the model again:

    ```
    ollama pull <modelname>
    ```

After the update, you should be able to install the model without any issues.
