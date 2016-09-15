# exgen-plug-simple

A simple Plug-based web app in Elixir.

## Exgen

To create a new copy of this app, use [Exgen](https://github.com/rwdaigle/exgen):

```bash
$ mix exgen.new new_dir \
    -t https://github.com/rwdaigle/exgen-plug-simple.git \
    --app-name my_app --module MyApp
```

## Running

Once the app has been generated w/ Exgen, install its dependencies:

```bash
$ mix deps.get
```

Then start the app using iex:

```bash
$ iex -S mix
iex(1)>
```

Load [localhost:4000](http://localhost:4000) in your browser. You will see the basic text-response defined for the root path:

> Hello there!

## Extending

To begin adding your own endpoints, open `lib/<%= app_name %>/router.ex` and start defining simple paths:

```elixir
get "/status" do
  conn
  |> put_resp_content_type("text/html")
  |> send_resp(200, "OK")
end
```
