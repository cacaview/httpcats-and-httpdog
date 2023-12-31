# httpcats-and-httpdog

![Python](https://img.shields.io/badge/python-3.10%2B-blue.svg)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](https://opensource.org/licenses/MIT)

这里有中文版本：[readme-zh](readme-zh.md)

`httpcats-and-httpdog` is a Python package for retrieving images corresponding to HTTP response status codes. It allows you to get images from [httpcats](https://httpcats.com) or [httpdog](https://http.dog) based on the provided HTTP response status codes.

## Installation

You can install the `httpcats-and-httpdog` package via `pip`:

```
pip install httpcats-and-httpdog
```

## Usage

```python
from httpcats_and_httpdog import get_image

# Get image data from httpcats
status_code = "200"
image_bytes = get_image("httpcats", status_code)

# Get image data from httpdog
status_code = "200"
image_bytes = get_image("httpdog", status_code)
```

The `get_image` function takes three arguments: the service name (`httpcats` or `httpdog`), HTTP response status code, and image format (optional, default is `.jpg`). It returns the byte data of the corresponding image, which you can further process or save as needed.

## Error Handling

When calling the `get_image` function, it raises a `ValueError` if the input status code is not a three-digit number or if downloading the image fails. Please ensure to provide the correct status code and check that your network connection is working properly.
