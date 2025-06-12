# SmolVLM Image Description Demo

A simple web-based demo showcasing how to use llama.cpp server with the SmolVLM 500M model to generate image descriptions.

## Features

* Uses llama.cpp to serve the SmolVLM 500M Instruct GGUF model
* Easy setup with CPU or GPU support
* Web interface (`index.html`) for uploading images and receiving descriptions
* Customizable instruction prompts (e.g., switch to JSON output)

## Prerequisites

* **llama.cpp** installed and available in your PATH
* A supported GPU setup (optional, but recommended for performance)
* A modern web browser (Chrome, Firefox, Safari)

## Installation

1. Clone this repository:

   ```bash
   git clone https://github.com/your-username/smolvlm-image-description.git
   cd smolvlm-image-description
   ```
2. Install llama.cpp following the official instructions: [https://github.com/ggerganov/llama.cpp](https://github.com/ggerganov/llama.cpp)

## Running the Server

Launch the llama.cpp server with the SmolVLM 500M model:

```bash
llama-server -hf ggml-org/SmolVLM-500M-Instruct-GGUF
```

* To enable GPU acceleration (NVIDIA / AMD / Intel), add:

  ```bash
  -ngl 99
  ```

## Using the Demo

1. Open `index.html` in your web browser.
2. (Optional) Edit the instruction prompt directly in the HTML to change the response format, such as returning JSON:

   ```html
   <textarea id="instruction">
   Describe the following image in JSON format with keys: "caption", "tags".
   </textarea>
   ```
3. Click **Upload** to select an image.
4. Click **Send Image for description**.
5. View the generated description returned by the SmolVLM model.

## Customizing Instructions

You can modify the instruction prompt in `index.html` to tailor the output:

* **Plain text**: Give a natural language description
* **JSON**: Return structured data
* **Bullet points**: List key elements

```html
<textarea id="instruction">
Provide a detailed caption of the image.
</textarea>
```

## Examples

![Sample Output](assets/sample_output.png)

```json
{
  "caption": "A serene mountain lake surrounded by pine trees at sunset.",
  "tags": ["lake", "mountains", "sunset", "nature"]
}
```

## Troubleshooting

* **Server not found**: Ensure `llama-server` is installed and running.
* **GPU errors**: Verify your GPU drivers and compatibility with llama.cpp.
* **Slow performance**: Try disabling GPU flags or use a smaller model.

## Contributing

Contributions are welcome! Feel free to open issues or submit pull requests.

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.
