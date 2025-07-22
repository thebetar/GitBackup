# Introduction

This repository was created to deliver a minimal setup that can sync all your Github repositories for redundancy. After reading a post from someone who's account got banned from Github and losing access to all his/her repositories I decided to at least have a copy of everything running locally on my home server.

This repository uses Gitea instead of other open source solutions like Gitlab because it is designed to run on a Raspberry Pi. Currently I run it on a Raspberry Pi 5 with 8GB of RAM without any problems.

# Installation

- Comment out the container for `mirror-to-gitea` as it will need the a token from gitea to work.
- Run the docker compose `docker compose up --build -d`
- Create an account on `http://localhost:3000`
- Create an API token in `Settings > Application > Generate new token`, the token only needs `read` access to **users** and `write` access to **repositories**
- Generate a token for your Github account in `Settings > Developer settings > Personal access tokens > Fine-grained tokens` , this token only needs `read` access to **repositories** it is good to keep these tokens minimal to prevent disaster when a third-party gets access to your token.
- Create a `.env` file from the base template of the `.env.example` file and fill in your Github username, Github Access token and Gitea API token
- Uncomment `mirror-to-gitea` and fill in the credentials
- Run the `docker compose up --build -d` command again
