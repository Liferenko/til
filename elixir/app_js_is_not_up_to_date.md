## priv/static/assets/app.js issue


When I tried to use forked Excalidraw - I noticed that my JS board is not updated even when I'm using custom libraty in package.json


First of all I need to find who's in charge for app.js file.
Here is what hexdocs said:
> Your JavaScript is typically placed at "assets/js/app.js" and esbuild will extract it to "priv/static/assets/app.js"...
source - https://hexdocs.pm/phoenix/asset_management.html

#### Solution
seems like there is no issues and warnings in `mix compile` - I can run `mix esbuild default --minify` and it recompiles my app.js file

```
sigmath git: mix esbuild default --minify

  ../priv/static/assets/app.js  6.9mb ⚠️

⚡ Done in 571ms
```

