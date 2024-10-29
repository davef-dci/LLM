To setup a Python 3.12 virtual environment for running tutorials
with an Nvidia CUDA-capable card and then running a local
instance of an LLM and RAG:

Reference video:
https://www.youtube.com/watch?v=Ylz779Op9Pw&t=621s

Reference 'blog post:
https://towardsdatascience.com/how-to-improve-llms-with-rag-abdc132f76ac

1. sudo apt install python3.12-venv
1. sudo ubuntu-drivers autoinstall
1. sudo apt install nvidia-cuda-toolkit
2. python -m venv tutorials
3. source tutorials/bin/activate
4. ./tutorials/bin/pip install numpy torch -OR-
4. ./tutorials/bin/pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu124
5. test with
```
import torch
print(torch.cuda.is_available())
print(torch.cuda.get_device_name(0))
```

6. ./tutorials/bin/pip install llama-index llama-index-embeddings-huggingface peft optimum bitsandbytes
7. cd tutorials
8. git clone https://github.com/PanQiWei/AutoGPTQ.git
9. cd AutoGPTQ
10. python setup.py build
11. python setup.py install

 do the stuff

5. deactivate

## Hosting Ollama on an Nvidia Jetson AGX Orin Dev Kit

https://thenewstack.io/how-to-get-started-running-small-language-models-at-the-edge/

