# Ollama

[Ollama](https://docs.ollama.com/) is the easiest way to get up and running with large language models such as gpt-oss, Gemma 3, DeepSeek-R1, Qwen3 and more.


The system requirements for Ollama are flexible and vary significantly depending on the size of the specific LLM you plan to run. Ollama itself is lightweight, but the models require substantial RAM and VRAM (GPU memory) for efficient performance.

## General System Requirements

- Operating System: Ollama supports macOS, Linux, and Windows.
- Disk Space: A base installation needs about 4GB of free space, with additional space required for each model you download (e.g., a 7B parameter model is around 4-5GB).
- CPU: A modern multi-core processor is recommended. Ollama can run on CPU, but performance is significantly better with a compatible GPU.
- RAM: At least 8GB of RAM is the minimum, with 16GB or more recommended for better performance and to run larger models.

## Specific Model Requirements (RAM/VRAM)
The most crucial factor is the memory (RAM or VRAM) required by the specific model you intend to use. Generally, the memory requirement is slightly higher than the model's size.

|Model Size (Parameters) | 	Recommended RAM/VRAM |
|:-----------------------|:----------------------|
|7B models (e.g., Mistral, Llama 2 7B)	| At least 8GB of RAM or 8GB VRAM |
|13B models	| At least 16GB of RAM or VRAM |
|70B models (e.g., Llama 3 70B)	| At least 64GB of RAM or VRAM |

## GPU Acceleration
A GPU is not strictly mandatory, but it is highly recommended for an efficient experience. Ollama automatically uses an available GPU if detected.

- NVIDIA GPUs are generally well-supported. Ensure you have the proper drivers and CUDA installed for the best performance.
- The amount of VRAM is more important than the GPU type itself. For example, a mid-range GPU with 8GB VRAM is suitable for 7B-13B models, while 16GB+ VRAM is necessary for 70B models with quantization.

You can manage and run these models via the command line, API, or various web UIs. You can explore different models and their specific details on the official Ollama Library.


# Additional resources
[Install Ollama on Linux](https://docs.ollama.com/linux)

