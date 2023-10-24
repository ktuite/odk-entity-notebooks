# odk-entity-notebooks

PyODK notebooks demonstrating example dev scenarios with ODK entity forms.

## Setup

### Create a virtual environment
This command will use your main installation of python (you can also specify a different python executable, e.g. `python3`) to create a virtual environment folder called `venv`.

```
python -m venv venv
```


### Activate/start the virtual environment

Whenever you come back to this directory to work with this code, you will need to enter the virtual environment. 

```
source venv/bin/activate
```

### Install the requirements

```
(venv) $ pip install -r requirements.txt
```

### Deactivate the virtual environment

This generally isn't necessary (you can just close the terminal window) but if you need to exit the virtual environment without closing it, you can type `deactivate`.

### Set up PyODK credentials

PyODK normally looks for a config file named `.pyodk_config.toml` but I found it helpful to make a few different named config files for different servers. Copy `dev.toml.default` into a file called `dev.toml` with your own local dev server (running locally on port `8383`) credentials or create your own.

```
[central]
base_url = "http://localhost:8383"
username = "<your email>"
password = "<your password>"
```

## Running the notebooks

Whenever you come back to this folder, you will need to start up the virtual environment again.

```
source venv/bin/activate
```

Start the notebook server

```
jupyter notebook
```

Which will give you a URL with a token, e.g. `http://localhost:8888/tree?token=<some token here>`. Open this link and then browse to the desired notebook.