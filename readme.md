# Steps

1. Comment out the container for `mirror-to-gitea` as it will need the a toke from gitea to work.
2. Run the docker compose `docker compose up --build -d`
3. Create an account on `http://localhost:3000`
4. Create an API token in `Settings > Application > Generate new token`
5. Uncomment `mirror-to-gitea` and fill in the credentials
6. Run the `docker compose up --build -d` command again
