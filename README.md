# Path Director

Path Director is a simple Python package for easily retrieving and creating paths for various commonly used directories,
such as application data, downloads, music, and photos. This package aims to simplify the process of managing file paths
in your projects.

# Features

Retrieve paths for application data, downloads, music, and photos directories.
Create directories if they do not exist.
Installation
You can install Path Director using pip:

```sh
pip install pathdirector
```

# Usage

Here's how you can use Path Director in your Python projects:

Importing the Package
First, import the methods from the package:

```python
from pathdirector.application_dir import get_application_dir
from pathdirector.sys_dir import (
    get_download_dir,
    get_videos_dir,
    get_music_dir,
    get_pictures_dir
)
```

Getting Directory Paths
You can get the paths for various directories as follows:

```python
# Get the application data path
app_data_path = get_application_dir(appname='appname', roaming=False)
print(f"Application Data Path: {app_data_path}")

# Get the downloads path
downloads_path = get_download_dir()
print(f"Downloads Path: {downloads_path}")

# Get the music path
music_path = get_music_dir()
print(f"Music Path: {music_path}")

# Get the photos path
photos_path = get_pictures_dir()
print(f"Photos Path: {photos_path}")

# Get the videos path
videos_path = get_videos_dir()
print(f"Videos Path: {videos_path}")
```

# Complete Example

Here is a complete example demonstrating how to use Path Director:

```python
from pathdirector.application_dir import get_application_dir
from pathdirector.sys_dir import (
    get_download_dir,
    get_videos_dir,
    get_music_dir,
    get_pictures_dir
)

# Retrieve or create directories
directories = {
    "Application Data": get_application_dir('appname'),
    "Downloads": get_download_dir(),
    "Music": get_music_dir(),
    "Photos": get_pictures_dir(),
    "Videos": get_videos_dir()
}

for name, path in directories.items():
    print(f"{name} Path: {path}")
```

# Contributing

Contributions are welcome! If you have any suggestions, bug reports, or improvements, feel free to open an issue or
submit a pull request.

# License

This project is licensed under the MIT License. See the LICENSE file for details.

Enjoy using Path Director! If you have any questions or need further assistance, please don't hesitate to reach out.

This version maintains a clear structure, making it easier for users to understand and use your package.






