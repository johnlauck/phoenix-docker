# phoenix-docker
Basic Docker and Docker Compose setup for Phoenix, Elixir, and Postgres.

## Usage

1. Copy `docker-compose.yml` and `Dockerfile` to project directory
2. Run `docker-compose build`
3. Run `docker-compose run app` 
4. In docker shell, run `mix phx.new` with your preferred options. In some cases, particularly with an umbrella app, you'll probably want to move the docker files inside the umbrella directory and use that as the project root. 
5. Update `config/dev.exs` and `config/test.exs` to use docker Postgres, by setting `hostname: System.get_env("DB_1_PORT_5432_TCP_ADDR")`. 
6. Run `mix ecto.create`
5. `docker-compose up` will get things started.