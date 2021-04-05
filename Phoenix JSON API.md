# [[Phoenix]] JSON API

## Start project

```sh
mix phx.new project_name --no-html --no-webpack --binary-id
```

-   Use `--no-html --no-webpack` to not generate HTML files or webpack config, since this is a JSON only API.
-   Use `--binary-id` to configure Ecto to use UUIDs as Primary IDs.


## Database Config

Make sure Postgres is running
![[Postgres on Docker Compose]]

```sh
docker-compose up -d
```

Now create the database

```sh
mix ecto.create
```

## Generate Schema

Using [[Phoenix Contexts]]

```
mix phx.gen.context Store Book books title:string isbn:text:unique description:text price:float authors:array:string
```

**Explained:**

-   `Store` is the context’s module name.
-   `Book` is the schema’s module name.
-   `books` is the Database table’s name.
-   The rest is field definitions. You can learn more about them on [https://hexdocs.pm/phoenix/Mix.Tasks.Phx.Gen.Schema.html](https://hexdocs.pm/phoenix/Mix.Tasks.Phx.Gen.Schema.html).

then apply the migrations to the database
```sh
mix ecto.migrate
```

## Generate REST Endpoints

```sh
mix phx.gen.json Store Book books title:string isbn:text:unique description:text price:float authors:array:string --no-context --no-schema
```

**Explained:**

-   The parameters `--no-context --no-schema` will ensure no context and schema are generated since we already have them from the previous step.

[**NOT YET FINISHED**](https://www.dairon.org/2020/07/06/simple-rest-api-with-elixir-phoenix.html)

Last step i took was running the migration.