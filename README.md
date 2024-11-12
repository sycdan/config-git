# Git Config

```bash
ln ~/code/GitConfig/.gitconfig ~/.gitconfig
```

## Hooks

To register the hooks for all repos:

`git config --global core.hooksPath ~/code/GitConfig/Hooks`

To register them for only one, run the same command just without the `--global` part, from within a repo folder.

## Formatting

Any staged files will be formatted based on their extension:

- `.cs` - [CSharpier](https://csharpier.com/)

Formatting can be disabled for specific file extensions by adding them to an environment variable:

`SYCDAN_SKIPFORMAT=cs,md,yaml`

### CSharpier

If you run `csharpier` regularly during development (for example using format-on-save), create a symlink to the config file in the folder where your repos are stored, e.g.:

`ln ~/code/GitConfig/Hooks/.csharpierrc.json ~/code`
