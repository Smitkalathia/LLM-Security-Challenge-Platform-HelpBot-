# How to Run - HelpBot LLM Prompt Injection CTF Challenge

Each challenge level is a Flask web application paired with an Ollama LLM service, orchestrated via Docker Compose.

## Prerequisites

- [Docker](https://docs.docker.com/get-docker/) and [Docker Compose](https://docs.docker.com/compose/install/) installed on your machine.
- At least 5 GB of RAM allocated to the machine or VM running the challenge.
- An internet connection (required on first run to pull the `llama3.2:3b` model, approximately 2 GB).

## Running a Challenge

Navigate into the desired level directory and run a single command:

### Level 1 - No Protections

```bash
cd level1
docker-compose up --build
```

Open [http://localhost:5000](http://localhost:5000) in your browser.

### Level 2 - Limited Protections (Input/Output Filtering)

```bash
cd level2
docker-compose up --build
```

Open [http://localhost:5000](http://localhost:5000) in your browser.

### Level 3 - Fully Protected

```bash
cd level3
docker-compose up --build
```

Open [http://localhost:5000](http://localhost:5000) in your browser.

## Notes

- On first run, the `llama3.2:3b` model will be downloaded automatically. This may take a few minutes depending on your connection. Subsequent runs use the cached model.
- Wait until you see "Model ready!" in the terminal output before using the chat interface. If you send a message before the model finishes loading, you will see a connection error.
- Only run one level at a time, or change the host port mapping in `docker-compose.yml` to avoid conflicts.
- To stop the challenge, press `Ctrl+C` in the terminal, then run `docker-compose down`.
- If you encounter a port conflict on 11434, stop any locally running Ollama instance first with `sudo systemctl stop ollama`.
- The flag for each level is stored as an environment variable in the Flask container. In Levels 1 and 2, it is also embedded in the LLM's system prompt. In Level 3, the flag is not in the system prompt.
