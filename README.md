# smolvlm-image-description

![image](https://github.com/user-attachments/assets/02e5884a-f9e6-4847-882b-226a8e72e59e)

This repository is a simple demo for how to use llama.cpp server with SmolVLM 500M to get image description.

How to setup
1.Install llama.cpp
2.Run llama-server -hf ggml-org/SmolVLM-500M-Instruct-GGUF
Note: you may need to add -ngl 99 to enable GPU (if you are using NVidia/AMD/Intel GPU)
Note (2): You can also try other models here
3.Open index.html
4.Optionally change the instruction (for example, make it returns JSON)
5.Upload photo
5.Click on "Send Image for description" and enjoy
