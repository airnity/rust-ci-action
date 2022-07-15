# Rust CI action

Action to run multiple Rusr CI commands. In order:

- `cargo check`
- `cargo fmt -- --check`
- `cargo clippy -- -D warnings`
- `cargo build`
- `cargo test`
- `cargo bench`

## Inputs

### `release`

Whether to perform release or not
_Default_: `false`


### `working-directory`

The directory to work on.
_Default_: `.`


### `bench-cache-key-suffix`

Suffix to add to the build cache key
_Default_: ""


## Example usage

```yaml
- name: Run Rust CI
  uses: airnity/elixir-rust-action@v4
  with:
    release: "True"
```