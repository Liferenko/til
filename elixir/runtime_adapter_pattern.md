## Run-time Adapter Pattern


From a book "Elixir Patterns", chapter 8


```elixir
defmodule StripeClient.Adapter do
  @doc "Create a customer in Stripe"
  @callback create_customer(params :: map()) ::
              {:ok, customer :: map()} | {:error, reason :: String.t()}

  @doc "Delete a customer in Stripe"
  @callback delete_customer(id :: String.t()) ::
    :ok | {:error, reason :: String.t()}
end
```

```elixir
defmodule StripeClient do
  @behaviour StripeClient.Adapter

  # Our Stripe client implements the same behaviour as the adapter implementations.
  @impl StripeClient.Adapter
  def create_customer(params) do
    adapter().create_customer(params)
  end

  @impl StripeClient.Adapter
  def delete_customer(id) do
    adapter().delete_customer(id)
  end

  # The `adapter/0` function is how we select our configured adapter at run-time.
  defp adapter do
    :my_app
    |> Application.fetch_env!(__MODULE__)
    |> Keyword.fetch!(:adapter)
  end
end
```

Additionally for the Adapter you'll create ....Adapter.Dev with fake responses and ....Adapter.HTTP with real-world implementations.

More in the book
