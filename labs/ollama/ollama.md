# Ollama
[Ollama](https://docs.ollama.com/) is the easiest way to get up and running with large language models such as gpt-oss, Gemma 3, DeepSeek-R1, Qwen3 and more.

## General System Requirements
- Operating System: Ollama supports macOS, Linux, and Windows.
- Disk Space: A base installation needs about 4GB of free space, with additional space required for each model you download (e.g., a 7B parameter model is around 4-5GB).
- CPU: A modern multi-core processor is recommended. Ollama can run on CPU, but performance is significantly better with a compatible GPU.
- RAM: At least 8GB of RAM is the minimum, with 16GB or more recommended for better performance and to run larger models.

## Specific Model Requirements (RAM/VRAM)
The most crucial factor is the memory (RAM or VRAM) required by the specific model you intend to use. Generally, the memory requirement is slightly higher than the model's size.

| Model Size (Parameters)               | Recommended RAM/VRAM            |
|:--------------------------------------|:--------------------------------|
| 7B models (e.g., Mistral, Llama 2 7B) | At least 8GB of RAM or 8GB VRAM |
| 13B models                            | At least 16GB of RAM or VRAM    |
| 70B models (e.g., Llama 3 70B)        | At least 64GB of RAM or VRAM    |

## GPU Acceleration
A GPU is not strictly mandatory, but it is highly recommended for an efficient experience. Ollama automatically uses an available GPU if detected.

- NVIDIA GPUs are generally well-supported. Ensure you have the proper drivers and CUDA installed for the best performance.
- The amount of VRAM is more important than the GPU type itself. For example, a mid-range GPU with 8GB VRAM is suitable for 7B-13B models, while 16GB+ VRAM is necessary for 70B models with quantization.

You can manage and run these models via the command line, API, or various web UIs. You can explore different models and their specific details on the official Ollama Library.

## Quick Start
The system requirements for Ollama are flexible and vary significantly depending on the size of the specific LLM you plan to run. Ollama itself is lightweight, but the models require substantial RAM and VRAM (GPU memory) for efficient performance.

### Run in Container
Ollama can run in container runtime (Docker, Podman, or Kubernetes), for the service isolation. Use the following command to start the Ollama server, mapping port `11434` and mounting a local volume to persist your models.
```sh
podman run -d -p 11434:11434 -v ollama:/root/.ollama --name ollama docker.io/ollama/ollama:0.17.7
```

This is an additional considerations for Ollama container environment customization.
- Persistent Storage: The `-v ollama:/root/.ollama` flag creates a named volume to ensure your downloaded AI models remain saved even after the container is stopped or removed.
- GPU Access: If you have an NVIDIA GPU, you may need to add `--device nvidia.com/gpu=all` (depending on your Podman version and driver configuration) to enable hardware acceleration for faster performance.
- Resource Management: You can manage the container's lifecycle using standard docker/podman commands like `podman stop ollama` and `podman start ollama`.
- Environment Variables: You can pass variables like `OLLAMA_KEEP_ALIVE=-1` using the `-e` flag if you want to prevent the model from unloading from memory after inactivity.
- Integration: If you are running a frontend like Open WebUI, it can communicate with this container via `http://localhost:11434`

If Ollama container runs successfully, then, you can download a language model. In this example, we're going to use Qwen 2.5, a lightweight module for testing.
```sh
podman exec -it ollama ollama pull qwen2.5:0.5b
```

This is an example query.
```sh
curl -s http://localhost:11434/v1/chat/completions \
  -H "Content-Type: application/json" \
  -d '{
    "model":"qwen2.5:0.5b",
    "messages":[{"role":"user","content":"Explain Ollama in 1 sentence"}],
    "stream":false
  }' | jq
```

When your lab is finished, clean up the environment.
```sh
podman stop ollama
podman rm ollama
```

# Additional Resources

# References
- [Install Ollama on Linux](https://docs.ollama.com/linux)

