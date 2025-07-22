# Introduction

This repository was created to deliver a minimal setup that can sync all your Github repositories for redundancy. After reading a post from someone who's account got banned from Github and losing access to all his/her repositories I decided to at least have a copy of everything running locally on my home server.

This repository uses Gitea instead of other open source solutions like Gitlab because it is designed to run on a Raspberry Pi. Currently I run it on a Raspberry Pi 5 with 8GB of RAM without any problems.

# Installation

1. Comment out the container for `mirror-to-gitea` as it will need the a toke from gitea to work.
2. Run the docker compose `docker compose up --build -d`
3. Create an account on `http://localhost:3000`
4. Create an API token in `Settings > Application > Generate new token`
5. Uncomment `mirror-to-gitea` and fill in the credentials
6. Run the `docker compose up --build -d` command again
