<style>
    /* Use the following CSS code if you want to have a class per icon */
ul { padding-left:20px; list-style:none; }
li { margin-bottom:10px; }
li:before {    
    content: "📂";
    margin:0 5px 0 -15px;
}
</style>

# Docker-Compose

This repository only holds the docker-compose file [📄](compose.yaml) that builds the whole backend stack as defined here:

![Image of the whole infrastructure](infrastructure.svg)

## Dependent Repositories

- `/middleware` : [🧭 `Backend-Interface`](https://github.com/Emotion2Emoji-LMU-ACP-WS24-25/Backend-Interface)

... more to come

## Commands

`docker-compose up --build` : Brings up the whole stack including a persistent MongoDB Container, the "Middleware" (i.e. [`Backend-Interface`](https://github.com/Emotion2Emoji-LMU-ACP-WS24-25/Backend-Interface)) as well as the dependent LLama 3.2 Vision and Stable Diffusion applications

Use `-d` to run the docker-compose detached.
