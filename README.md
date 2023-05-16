
# Selenium Automation README

This repository contains a Python code snippet for automating web interactions using Selenium.

## Requirements

- Python 3.x
- Selenium package (`pip install selenium`)
- Undetected Chrome Driver package (`pip install undetected-chromedriver`)
- Webdriver Manager for Chrome (`pip install webdriver-manager`)

## Installation

1. Clone this repository:

   ```
   git clone https://github.com/your-username/your-repository.git
   ```


## Usage

The main file `selenium_automation.py` provides functions to establish a connection with Selenium using the Chrome driver and perform various automation tasks. Here's an overview of the available functions:

### `conn_link`

Establishes a connection with Selenium using the specified Chrome webdriver.

Parameters:
- `headless` (bool): Whether to run in headless mode (without a browser window). Defaults to `True`.
- `**kwargs`: Additional keyword arguments to customize the Chrome options.

Returns:
- `webdriver.Chrome`: The Selenium WebDriver instance for Chrome.

### `conn_uc`

Establishes a Selenium connection using the undetected_chromedriver module.

Parameters:
- `headless` (bool): Whether to run in headless mode (without a browser window). Defaults to `True`.
- `folder` (bool or str): Folder path where the UC profile data will be stored. If `False`, it uses the default folder `./uc`. If a custom folder path is provided, it will be used. Defaults to `False`.

Returns:
- `undetected_chromedriver.Chrome`: The Selenium WebDriver instance for UC (undetected_chromedriver).

### `click`

Clicks on a Selenium element based on the selector type and path.

Parameters:
- `driver` (`webdriver.Chrome`): The Selenium driver to run the automation.
- `selector_type` (str): The type of selector to use ('id', 'class', 'xpath', etc.).
- `path` (str): The value of the selector to use.
- `wait_time` (float): Waiting time before giving an error. Defaults to 30.
- `control` (Optional[int]): Position of the element in a list (optional).
- `log` (bool): Whether to log exceptions or not.

Returns:
- `bool`: True if the click was successful, False otherwise.

### `submit`

Submits a form element identified by the given selector and path in Selenium.

Parameters:
- `driver` (`webdriver.Chrome`): The Selenium WebDriver instance.
- `selector_type` (str): The type of selector to use (e.g., "xpath", "css_selector", "id", etc.).
- `path` (str): The path or value of the selector.
- `wait_time` (int): The maximum time to wait for the element to be clickable (in seconds). Defaults to 30.

Returns:
- `bool`: True if the submission is successful, False otherwise.

### `keys`

Sends keys to an element identified by the given selector and path in Selenium.

Parameters:
- `driver` (`webdriver.Chrome`): The Selenium WebDriver instance.
- `selector_type` (str): The type of selector to use (e.g., "xpath", "css_selector", "id", etc.).
- `path` (str): The path or value of the selector.
- `keys` (str): The keys to send
