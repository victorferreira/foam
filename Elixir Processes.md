Processes in Elixir have two basic properties:

- A Process ID (PID)
- A message queue

## spawning new processes

```elixir
spaw(fn -> do_something() end)
```
