# Configuration

1. Install pyenv

    ```bash
    curl https://pyenv.run | bash
    ```

    Then add the following to your `~/.bashrc` or equivalent:

    ```bash
    export PYENV_ROOT="$HOME/.pyenv"
    command -v pyenv >/dev/null || export PATH="$PYENV_ROOT/bin:$PATH"
    eval "$(pyenv init -)"
    eval "$(pyenv virtualenv-init -)"
    ```

2. Install python via pyenv

    ```bash
    # this will install the python in version 
    # specified in .python-version file
    pyenv install
    ```

3. Install poetry inside pyenv environment

    ```bash
    pip install poetry
    ``` 

4. Install dependencies

    ```bash
    poetry install
    ```

5. Configure vscode to use poetry environment

    First run:

    ```
    poetry env info --path
    ```

    and copy the output and use it to create a new python interpreter in vscode.

    Then in vscode, open the command palette and select `Python: Select Interpreter` and select "Enter interpreter path" and paste the path you copied earlier.