# 🚢 Docker-Compose

This repository only holds the docker-compose file [📄](compose.yaml) that builds the whole backend stack as defined here:

![Image of the whole infrastructure](infrastructure.svg)

## 📂 Dependent Repositories

- 📂 `/middleware` : [`Backend-Interface`](https://github.com/Emotion2Emoji-LMU-ACP-WS24-25/Backend-Interface)
- 📂 `/imageGeneration` : [`Backend-StableDiffusion`](https://github.com/Emotion2Emoji-LMU-ACP-WS24-25/Backend-StableDiffusion)
- 📂 `/visionModel` : [`Backend-PaliGemma-2`](https://github.com/Emotion2Emoji-LMU-ACP-WS24-25/Backend-PaliGemma-2)
- 📂 `/llm` : [`Backend-Mistral`](https://github.com/Emotion2Emoji-LMU-ACP-WS24-25/Backend-Mistral)
- 📂 `/frontend` : [`Frontend-Flutter`](https://github.com/Emotion2Emoji-LMU-ACP-WS24-25/Frontend-Flutter)


## 🛠️ Job
Example:
```json
{
  "_id": {
    "$oid": "6758a254a304107814afd00e"
  },
  "frontImagePath": "uploads/demo/2024_12_10-20_19-front-51394850.jpg",
  "backImagePath": "uploads/demo/2024_12_10-20_19-back-51394850.jpg",
  "prompt": "A male with blonde hair, green eyes, strongly expressing happy emotion, wearing a balck shirt, a rocky cliff with grass growing out of it in the background, icon emoji",
  "status": "completed",
  "resultImagePath": "/app/emojis/6758a254a304107814afd00e.png",
  "uploadDate": "2024-12-10",
  "uploadTime": "20:19:32",
  "__v": 0
}
```

### ✅ Job Status
![Image of the whole infrastructure](status.svg)

## ⚙️ Setup & Build

To get the whole project with the correct folder structure use `git clone --recurse-submodules git@github.com:Emotion2Emoji-LMU-ACP-WS24-25/Docker-Compose.git [path]` with `path` being the optional custom path to clone the repo into.

`docker-compose up --build` : Brings up the whole stack including a persistent MongoDB Container, the "Middleware" (i.e. [`Backend-Interface`](https://github.com/Emotion2Emoji-LMU-ACP-WS24-25/Backend-Interface)) as well as the dependent VLM, LLM and Stable Diffusion (i.e. [`Backend-StableDiffusion`](https://github.com/Emotion2Emoji-LMU-ACP-WS24-25/Backend-StableDiffusion)) applications.

Use `-d` to run the docker-compose detached.

Expose backend port 3000 using ngrok with a static URL, following the instructions [here](https://dashboard.ngrok.com/get-started/setup/docker). Once set up, add the static URL to the .env file in the Flutter frontend.
