# Devtools console shows IEx console logs

add in `config/dev.exs`
```elixir
  config :my_app, MyAppWeb.Endpoint,
    live_reload: [
      interval: 1000,
      patterns: [...],
+     web_console_logger: true
    ]
```

add in `app.js`
```javascript
 + window.addEventListener("phx:live_reload:attached", ({detail: reloader}) => {
+   // enable server log streaming to client.
+   // disable with reloader.disableServerLogs()
+   reloader.enableServerLogs()
+ })
```

Source: [elixirstreams](https://www.elixirstreams.com/tips/stream_server_logs_to_console)

