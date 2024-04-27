# Running Llama3 on NAS

This is a simple instruction on how to locally run Llama3 on your NAS using [Open WebUI](https://github.com/open-webui/open-webui) and [Ollama](https://github.com/ollama/ollama). 

## Hardware

- **[UGREEN NASync DXP480T Plus](https://www.kickstarter.com/projects/urgreen/ugreen-nasync-next-level-storage-limitless-possibilities?ref=9q75gj)**
  - CPU: Intel® Core™ i5-1235U Processor (12M Cache, up to 4.40 GHz, 10 Cores 12 Threads)
  - RAM: 8G

## Setup Instructions

### 1. Create Necessary Directories

Open a terminal and run the following commands to create directories for your AI models and the web interface:

```sh
$ mkdir -p /home/ansonhe/AI/ollama
$ mkdir -p /home/ansonhe/AI/Llama3/open-webui
```

### 2. Deploy Using Docker

Copy the provided `docker-compose.yml` file to your directory, then start the services using Docker:

```sh
$ sudo docker-compose up -d
```

### 3. Access the Web Interface

Open web browser and enter `YOUR_NAS_IP:8080`

### 4. Configure Ollama Models

In the web interface, change the Ollama Models address to `0.0.0.0:11434`.

![config](https://raw.githubusercontent.com/ansonhe97/rawimages/master/img/config.png)

### 5. Download the Llama3 Model

Download the Llama3 Model **`ollama run llama3:8b`**, (Only using 8b versions here since performance limitations on NAS)

![download](https://raw.githubusercontent.com/ansonhe97/rawimages/master/img/llama3-download.png)

### 6. Set Llama3 as the Default Model

After the model has been downloaded, you can select Llama3 as your default model and host it locally.

![llama3](https://raw.githubusercontent.com/ansonhe97/rawimages/master/img/llama3-hello.png)

## Performance Considerations

Please note that the CPU of the NAS may still face limitations when running large language models (LLMs) due to its processing capabilities.

