# Election Analysis by Districts

Code helps to visualize election results from the german parliament elections on district (Wahlkreis) level. 
Basic recommendation algorithm which helps to push back undemocratic parties in certain districts by helping democratic parties to power up together to fight back Direktmandate. This could be implemented by "voter swapping" in different districts. I.e. democratic Party A recommends democratic Party B in District I and democratic Party B recommends democratic Party A in District II and therefore undemocratic Party C won't win in both of them.

## Election districts without voting recommendations (based on 2017 results)
![Election districts without voting recommendations](https://github.com/matthiaskiller/election-analysis/blob/main/map_2.png?raw=true)

## Election districts after applying voting recommendations (based on 2017 results)
![Election districts after applying voting recommendations](https://github.com/matthiaskiller/election-analysis/blob/main/map.png?raw=true)

## Setup 

### Conda installation
Run:

```conda env create -f environment.yml```

### Pre-commit hook 
To maintain a clean and standardized environment and codebase please use pre-commit hooks (see the Development section for more details). To use pre-commit hooks we need to run:

`pre-commit install`

## Development

### Styling and formatting
```sh
black . # In place formatter, adheres mostly to PEP8
flake8  # Code linter with stylistic conventions adhering to PEP8
isort . # Sorts and formats imports in python files
```

### Make commands
You can use `make` to execute targets defined in the `Makefile`. If make is not installed, run `sudo apt install make`.
```sh
# See available make commands
make help
# Execute several clean commands
make clean
# Execute style formatting
make style
# Execute all pre-commit hooks
make pre-commit
```

### Configs
The development tools are configured in the following files. While trying to adhere to standards, we made some exceptions and ignored some directories.
```sh
.flake8 # flake8
pyproject.toml # black, isort, pytest
Makefile # make
.pre-commit-config
```
</details>

### IDE settings (VScode, Pycharm)
You can also change settings in your IDE to do auto formatting (black) on save and run flake8 on save if you do not want to run them via terminal. Here are articles to setup [black on Pycharm](https://akshay-jain.medium.com/pycharm-black-with-formatting-on-auto-save-4797972cf5de), [black on VScode](https://dev.to/adamlombard/how-to-use-the-black-python-code-formatter-in-vscode-3lo0), [flake8 on VScode](https://code.visualstudio.com/docs/python/linting).


