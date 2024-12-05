# Docker-Compose

This repository only holds the docker-compose file [📄](compose.yaml) that builds the whole backend stack as defined here:

![Image of the whole infrastructure](infrastructure.svg)

## Dependent Repositories

- 📂 `/middleware` : [`Backend-Interface`](https://github.com/Emotion2Emoji-LMU-ACP-WS24-25/Backend-Interface)
- 📂 `/imageGeneration` : [`Backend-StableDiffusion`](https://github.com/Emotion2Emoji-LMU-ACP-WS24-25/Backend-StableDiffusion)

  ... more to come

## Commands

To get the whole project with the correct folder structure use `git clone --recurse-submodules git@github.com:Emotion2Emoji-LMU-ACP-WS24-25/Docker-Compose.git [path]` with `path` being the optional custom path to clone the repo into.

`docker-compose up --build` : Brings up the whole stack including a persistent MongoDB Container, the "Middleware" (i.e. [`Backend-Interface`](https://github.com/Emotion2Emoji-LMU-ACP-WS24-25/Backend-Interface)) as well as the dependent LLama 3.2 Vision and Stable Diffusion (i.e. [`Backend-StableDiffusion`](https://github.com/Emotion2Emoji-LMU-ACP-WS24-25/Backend-StableDiffusion)) applications.

Use `-d` to run the docker-compose detached.
