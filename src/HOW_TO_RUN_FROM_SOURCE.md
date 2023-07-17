If you want to use debbit on mac/Windows please download a release from https://github.com/jakehilborn/debbit/releases  
If you want to develop debbit or use on Linux follow instructions below.

# One time setup
1. Clone this GitHub repo or download the source code.
1. Install the latest version of Firefox.
1. Copy and rename the file `sample_config.txt` to `config.txt` (or `config.yml`) in the same directory.
1. Configure your python3 environment and dependencies.

    These instructions will vary somewhat depending on your platform. For example,
    if your system already has Python3 then you'll use `pip` instead of `pip3`. If
    you don't have pip installed, search on Google for how to install pip.

    ```
    debbit/src
    pip3 install --user pipenv
    pip3 install --user --upgrade pipenv
    ```

    or 

    ```
    pip3 -m venv .venv
    ./.venv/Scripts/Activate.ps1
    ```

# Routinely
When dependencies are updated, and on first-time setup, you'll need to run the following:

```
cd debbit/src
pipenv install
```

or

```
./.venv/Scripts/Activate.ps1
pip install -r requirements.txt
```

# Every Time: run debbit via pipenv

`pipenv run python debbit.py`

You can also use `pipenv shell` then `python debbit.py` if you want to keep the `pipenv` environment around. 

or

```
./.venv/Scripts/Activate.ps1
python debbit.py
```