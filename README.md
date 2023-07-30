# KV

# Install latest version of erlang and elixir via asdf

```
git clone https://github.com/asdf-vm/asdf.git ~/.asdf
. $HOME/.asdf/asdf.sh
asdf plugin add erlang
asdf plugin add elixir
asdf list-all erlang
asdf list-all elixir
```

find the latest available version then install

```
asdf install erlang xx.xx.x
asdf install elixir x.xx.x-otp-yy
```

## Set project version

```
asdf local erlang 26.0.2
asdf local elixir 1.15.4-otp-26
```

## Execute simple.exs

```
elixir simple.exs
```

## Compile this kv lib

```
cd kv
mix compile
mix test
mix test test/kv_test.exs:5
```

## Configure database

configure database in config/dev.exs, then


```
cd server
mix ecto.create
```

## Run server

```
mix phx.server
```

## Installation

If [available in Hex](https://hex.pm/docs/publish), the package can be installed
by adding `kv` to your list of dependencies in `mix.exs`:

```elixir
def deps do
  [
    {:kv, "~> 0.1.0"}
  ]
end
```

Documentation can be generated with [ExDoc](https://github.com/elixir-lang/ex_doc)
and published on [HexDocs](https://hexdocs.pm). Once published, the docs can
be found at <https://hexdocs.pm/kv>.

