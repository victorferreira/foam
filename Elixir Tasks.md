## Tasks

## spawning a new task

```elixir
task = Task.async(fn -> do_some_work() end)
result = Task.await(task)
```

