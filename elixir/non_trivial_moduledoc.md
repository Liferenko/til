# Another way to write `@moduledoc`


```
defmodule Bypass do
  @external_resource "README.md"
  @moduledoc "README.md"
             |> File.read!()
             |> String.split("<!-- MDOC !-->")
             |> Enum.fetch!(1)

```

Found in `Bypass` lib - https://github.com/PSPDFKit-labs/bypass/blob/master/lib/bypass.ex#L2
