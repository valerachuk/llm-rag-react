## Running Ollama with Docker

Use the following command to run Open WebUI with bundled Ollama:

`docker run -d -p 3000:8080 --gpus=all -v ollama:/root/.ollama -v open-webui:/app/backend/data --name open-webui --restart always ghcr.io/open-webui/open-webui:ollama`

- See docs: https://docs.openwebui.com/#installing-open-webui-with-bundled-ollama-support
- See list of available models: https://ollama.com/library

## GitLab handbook source:

See: https://gitlab.com/gitlab-com/content-sites/handbook
