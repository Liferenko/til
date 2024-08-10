## command not found: wasm-pack

!NB! for macOS and zsh AND for rust installed with ASDF

1. remove `export PATH="$PATH:/.cargo" and any rust-related PATH updates (asdf resolve it by itself)
2. run `asdf reshim rust`
3. wasm-pack works
