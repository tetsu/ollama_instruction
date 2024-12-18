# Ollama Installation Guide

1. To install Ollama on your Ubuntu or other Linux, type following command on your terminal. [Ollama Download document is here](https://ollama.com/download).

    ```bash
    curl -fsSL https://ollama.com/install.sh | sh
    ```

1. To check if Ollama is installed, go to the following URL on your browswer. [This YouTube video has better explanations](https://youtu.be/91npmOxCL-c).

    [localhost:11434](localhost:11434)

1. Download a model for Ollama. [Check about Phi-4 on this Youtube video](https://youtu.be/aYvt9czdgbU).

    ```bash
    ollama pull vanilj/Phi-4
    ```

1. Run Ollama on Terminal

    ```bash
    ollama run vanilj/Phi-4
    ```

1. To run on your brower, run OpenWebUI locally using Docker. [OpenWebUI document is here](https://docs.openwebui.com/getting-started/quick-start).

    ```bash
    docker pull ghcr.io/open-webui/open-webui:main
    docker run -d -p 3000:8080 --gpus all -v open-webui:/app/backend/data --name open-webui ghcr.io/open-webui/open-webui:cuda
    ```

1. Open OpenWebUI on your browser.

    [localhost:3000](localhost:3000)