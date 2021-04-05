## Maps[](https://elixir-lang.org/getting-started/keywords-and-maps.html#maps)

Whenever you need a key-value store, maps are the “go to” data structure in Elixir. A map is created using the `%{}` syntax:

```elixir
map = %{:a => 1, 2 => :b}	# %{2 => :b, :a => 1}
map[:a]	# 1
map[2]	# :b
map[:c]	# nil
```

Compared to keyword lists, we can already see two differences:

-   Maps allow any value as a key.
-   Maps’ keys do not follow any ordering.

When all the keys in a map are atoms, you can use the keyword syntax for convenience:

```elixir
map = %{a: 1, b: 2}	# %{a: 1, b: 2}
```
