# Working with pre-commit

To work with pre commit in your repo in general you need to install the pre-commit cli tool

Using pip:

```bash
pip install pre-commit
```

Using homebrew:

```bash
brew install pre-commit
```

For more info check out their [docs](https://pre-commit.com/#quick-start)

In order to run pre-commit in your repo you will need a `.pre-commit-config.yaml` in your repo.

This is not enough, since usually you will also need to install the type of hook to run.

IE: The hook commitizen requires the hook `pre-commit` installed in your repo. Usually when you run `pre-commit install` after providing the `.pre-commit-config.yaml` is enough to install the required hooks, but sometimes you will need to install specific hooks like `prepare-commit-msg`, to see a list of these hooks check `pre-commit install -t --help`, these hooks gets installed in the `.git/hooks` folder in your current repo. So keep in mind every time you have a new project to run `pre-commit install` after providing the `.pre-commit-config.yaml`.
