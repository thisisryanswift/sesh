# sesh

A unified session manager that combines [zoxide](https://github.com/ajeetdsouza/zoxide), [try](https://github.com/tobi/try), and [Zellij](https://zellij.dev/) for seamless project navigation and experiment creation.

## What it does

- **Pick an existing project** from your zoxide history → opens in a Zellij session
- **Type a new name** → creates a dated experiment directory (like `2025-12-06-my-idea`), adds it to zoxide, and opens in a Zellij session

Perfect for developers who constantly switch between projects and spin up quick experiments.

## Demo

```
$ sesh
# Shows fzf picker with all your projects
# Select one → attaches to Zellij session
# Type "redis-test" → creates ~/src/tries/2025-12-06-redis-test/ and opens session
```

## Requirements

- [zoxide](https://github.com/ajeetdsouza/zoxide) - smarter cd command
- [fzf](https://github.com/junegunn/fzf) - fuzzy finder
- [Zellij](https://zellij.dev/) - terminal multiplexer

Optional:
- [try](https://github.com/tobi/try) - if you want the full experiment management experience

## Installation

```bash
# Download the script
curl -sL https://raw.githubusercontent.com/rswiftoffice/sesh/main/sesh > ~/.local/bin/sesh
chmod +x ~/.local/bin/sesh

# Or clone and symlink
git clone https://github.com/rswiftoffice/sesh.git
ln -s $(pwd)/sesh/sesh ~/.local/bin/sesh
```

## Configuration

Set `TRY_PATH` to change where new experiments are created:

```bash
export TRY_PATH=~/experiments  # default: ~/src/tries
```

## Credits

- Original sesh concept by [Omerxx](https://github.com/omerxx/dotfiles/blob/master/zellij/sesh)
- Experiment directory concept inspired by [try](https://github.com/tobi/try) by Tobi Lütke

## License

MIT
