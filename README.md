## Running the container
1. Make sure docker and docker compose is installed to your system
2. Create empty folder and copy paste `docker-compose.yaml` to that folder
3. Change `INITIAL_ADMIN_EMAIL` and `INITIAL_ADMIN_PASSWORD` to your needs inside `docker-compose.yaml`
4. Create new network called `application_network` using `docker create network` command
5. Run Docker container using `docker compose up -d` command
6. You can access the portal at `http://localhost:81` _// im not sure lmao_

## Notes 
If accessing `http://localhost:81` not work on your local machine, change `"127.0.0.1:81:81"` inside `docker-compose.yaml` to `"81:81"`

## Extra
If on vps, pipe your vps to your machine like this:
```bash
ssh -L 8081:localhost:81 hostname@ip_address
```

Then access the nginx portal at `http://localhost:8081` in your machine.
