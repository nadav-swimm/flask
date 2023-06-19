---
id: 9wg5hgqg
title: how to setup a new env
file_version: 1.1.2
app_version: 1.11.0
---

# File Structure of a New Environment

The file structure of a new environment in our repo follows a specific convention to ensure consistency and ease of maintenance.

The root directory of the environment contains several files and folders that are essential for the environment to function properly. These include:

*   `requirements.txt`: This file contains a list of all the Python packages required for the environment to run. It is generated automatically using the `pip freeze` command and should be updated whenever a new package is added or removed from the environment.

*   `config.yaml`: This file contains all the configuration settings for the environment. It includes settings such as database connection strings, API keys, and other environment-specific variables.

*   `README.md`: This file contains documentation for the environment, including instructions on how to set it up and use it.

*   `src/`: This folder contains all the source code for the environment. It is organized into subfolders based on functionality, with each subfolder containing its own `__init__.py` file.

*   `tests/`: This folder contains all the unit tests for the environment. The tests are organized into subfolders based on the functionality they test, with each subfolder containing its own `__init__.py` file.

## Helpers

[here](https://swimm-web-app.web.app/workspaces/H0nYogF29jh747xcua9g/repos/Z2l0aHViJTNBJTNBZmxhc2slM0ElM0FuYWRhdi1zd2ltbQ==/branch/main/docs/9wg5hgqg/edit#snippet-245yuT)

<br/>

This code defines a function `get_load_dotenv` which checks whether the user has disabled loading dotenv files by setting the environment variable `FLASK_SKIP_DOTENV`. The function returns a boolean value indicating whether or not to load the files, with `True` being the default behavior.
<!-- NOTE-swimm-snippet: the lines below link your snippet to Swimm -->
### 📄 src/flask/helpers.py
```python
49     def get_load_dotenv(default: bool = True) -> bool:
50         """Get whether the user has disabled loading dotenv files by setting
51         :envvar:`FLASK_SKIP_DOTENV`. The default is ``True``, load the
52         files.
```

<br/>

By following this file structure convention, we ensure that all new environments are consistent and easy to maintain.

## What happens when FLASK\_SKIP\_DOTENV is set to True

When the user sets the environment variable FLASK\_SKIP\_DOTENV to True, the function get\_load\_dotenv() returns False, which disables the loading of dotenv files. By default, get\_load\_dotenv() returns True, which enables the loading of dotenv files.

To further elaborate, the loading of dotenv files can be useful for configuring the application's environment variables. In fact, it is highly recommended to load dotenv files for better management of environment variables.

# Conventions to Follow When Setting up a New Environment

When setting up a new environment, there are certain conventions that should be followed to ensure consistency across the codebase. These conventions include:

*   **Loading dotenv files**: To determine whether the user has disabled loading dotenv files by setting `FLASK_SKIP_DOTENV`, the `get_load_dotenv` function from `src/flask/helpers.py` is used.
*   **Specifying URL schemes**: When specifying `_scheme`, `_external` must be set to `True`. If `_external` is not set to `True`, a `ValueError` will be raised. The `url_adapter.url_scheme` attribute is used to set the URL scheme.
*   **Using generators**: Generators are used in the codebase, and the `next` function is used to advance the generator to the next yield statement.

By following these conventions, the codebase remains consistent and easy to maintain.

<br/>

## How to check if loading dotenv files is disabled

To check if the user has disabled loading dotenv files by setting `FLASK_SKIP_DOTENV`, use the `get_load_dotenv()` function from `src/flask/helpers.py`. This function returns a boolean value indicating whether the user has disabled loading dotenv files or not.

[Helpers](https://swimm-web-app.web.app/workspaces/H0nYogF29jh747xcua9g/repos/Z2l0aHViJTNBJTNBZmxhc2slM0ElM0FuYWRhdi1zd2ltbQ==/branch/main/docs/9wg5hgqg/edit#heading-ukgUh)

<br/>

This code snippet checks if `_scheme` is not `None`, and if `_external` is `False`, it raises an error. It then sets `url_adapter.url_scheme` to the value of `_scheme`.
<!-- NOTE-swimm-snippet: the lines below link your snippet to Swimm -->
### 📄 src/flask/helpers.py
```python
315        if scheme is not None:
316            if not external:
317                raise ValueError("When specifying _scheme, _external must be True")
318            old_scheme = url_adapter.url_scheme
319            url_adapter.url_scheme = scheme
320    
```

<br/>

This code initializes a generator object `wrapped_g` and calls its first iteration using the `next()` function.
<!-- NOTE-swimm-snippet: the lines below link your snippet to Swimm -->
### 📄 src/flask/helpers.py
```python
138        wrapped_g = generator()
139        next(wrapped_g)
```

<br/>

Here's an example of how to use the `get_load_dotenv()` function:

For more advanced usage examples and edge cases, refer to the 'Our X API' or 'X API Overview' sections of the internal API document.

<br/>

This file was generated by Swimm. [Click here to view it in the app](https://swimm-web-app.web.app/repos/Z2l0aHViJTNBJTNBZmxhc2slM0ElM0FuYWRhdi1zd2ltbQ==/docs/9wg5hgqg).
