# Ollama Installation Guide

1. To install Ollama on your Ubuntu or other Linux, type following command on your terminal. [Ollama Download document is here](https://ollama.com/download).

    ```bash
    curl -fsSL https://ollama.com/install.sh | sh
    ```

1. To check if Ollama is installed, go to the following URL on your browswer. [This YouTube video has better explanations](https://youtu.be/91npmOxCL-c).

    [http://localhost:11434](http://localhost:11434)

1. Download a model for Ollama. For other models, check [Ollama Libary site](https://ollama.com/library). [Check about Phi-4 on this Youtube video](https://youtu.be/aYvt9czdgbU).

    ```bash
    ollama pull vanilj/Phi-4
    ```

1. Test Ollama on Terminal

    ```bash
    ollama run vanilj/Phi-4
    ```

1. Exit from Ollama console.

    ```bash
    /bye
    ```

1. To run on your brower, run OpenWebUI locally using Docker with GPU. [OpenWebUI document is here](https://docs.openwebui.com/getting-started/quick-start).

    ```bash
    docker run -d -p 3000:3000 --network host --gpus all -v open-webui:/app/backend/data \
    -e OLLAMA_BASE_URL=http://localhost:11434 \
    -e DEVICE_TYPE=cuda \
    -e PORT=3000 \
    --name open-webui \
    --restart always \
    ghcr.io/open-webui/open-webui:cuda
    ```

    If your device doesn't use Cuda, use the following command

    ```bash
    docker run -d -p 3000:3000 -v open-webui:/app/backend/data -e OLLAMA_BASE_URL=http://localhost:11434 -e DEVICE_TYPE=cpu -e PORT=3000 --name open-webui --restart always ghcr.io/open-webui/open-webui:main
    ```

1. Open OpenWebUI on your browser.

    [http://localhost:3000](http://localhost:3000)
