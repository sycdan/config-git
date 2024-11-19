# Git Config

Create a symlink to the global `gitconfig` file in your home folder:

```bash
ln ~/code/GitConfig/.gitconfig ~/.gitconfig
```

## Hooks

To register the hooks for all repos:

```bash
git config --global core.hooksPath ~/code/GitConfig/hooks
```

To register them for only one, run the same command just without the `--global` part, from within a repo folder.

Make the scripts executable:

```bash
chmod +x ~/code/GitConfig/hooks/pre-commit
```

## Formatting

Any staged files will be formatted based on their extension:

- `.cs` - [CSharpier](https://csharpier.com/)

Formatting can be disabled for specific file extensions by adding them to an environment variable:

```bash
export GITCONFIG_SKIPFORMAT=cs,md,yaml
```

### CSharpier

If you run `csharpier` regularly during development (for example using format-on-save), create a symlink to the config file in the folder where your repos are stored, e.g.:

```bash
ln ~/code/GitConfig/hooks/.csharpierrc.json ~/code
```
