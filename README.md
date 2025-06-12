# smolvlm-image-description

![Demo Image](https://github.com/user-attachments/assets/02e5884a-f9e6-4847-882b-226a8e72e59e)

A simple demo showing how to use the **llama.cpp** server with the **SmolVLM 500M** model to generate image descriptions.

## How to setup

1. **Install llama.cpp**
2. **Run the server**:

   ```bash
   llama-server -hf ggml-org/SmolVLM-500M-Instruct-GGUF
   ```

   * To enable GPU acceleration (NVIDIA/AMD/Intel), add the `-ngl 99` flag.
   * Feel free to try other GGUF models hosted on the llama.cpp hub.
3. **Open** `index.html` in your web browser.
4. **(Optional)** Edit the instruction prompt in `index.html` (for example, to return JSON).
5. **Upload** a photo.
6. **Click** **Send Image for description** and enjoy!
