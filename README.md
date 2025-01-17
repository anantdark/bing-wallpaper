# Bing Wallpaper Changer

![wall3](https://github.com/anantdark/bing-wallpaper/assets/66427020/db356646-25a9-4fc0-8a29-23533aceac23)


Bing Wallpaper Changer is a Python script that automatically updates your wallpaper daily using Bing's daily image.


## Compatibility

- Operating System: Linux (tested on Debian-based systems)
- Python: 3.x

Python script can be run manually on windows, installer will only work on linux based systems.

## Installation

1. Clone or download this repository to your local machine.
    ```commandline
    git clone https://github.com/anantdark/bing-wallpaper.git
    ```

2. Navigate to the downloaded directory:
    ```commandline
   cd bing-wallpaper
   ```
3. Make the script executable by running the following command:
   ```commandline
   sudo chmod +x install.sh
   ```

4. Run the following command to install the wallpaper changer:
    ```commandline
    sudo ./install.sh --install  
    ```

    This will prompt you for sudo access and install the necessary files and services.


5. Once the installation is complete, the wallpaper changer will start automatically. It will update your wallpaper with Bing's daily image each day.

## ~~Note: Script scheduling is a work in progress.~~

~~I have tried to implement a systemctl service and a cron job for scheduling the task but in both cases the script is unable to access the display server. I also tried exporting the display server `export DISPLAY=:0` but that didn't work atleast on my system.~~

Therefore currently i am going with a desktop entry that will show the script as an "app" in the applications menu which can be launched to change the wallpaper.
![Screenshot from 2023-06-13 11-42-07](https://github.com/anantdark/bing-wallpaper/assets/66427020/1c639d5d-c8ec-44f2-bb2d-c8cb6f12b0c5)

## Update:

The solution was so simple I don't know how i missed it, I just had to create an entry in startup applications for it to run the script on startup.

## TL;DR: Scheduling is working now.


## Uninstallation

1. Open a terminal and navigate to the downloaded directory:
    ```commandline
   cd /path/to/wallpaperchanger
   ```

2. Run the following command to uninstall the wallpaper changer:

    ```commandline
   sudo ./install.sh --uninstall
   ```

This will prompt you for sudo access and remove the installed files and services.

## Configuration

By default, the wallpaper changer downloads the daily image from Bing and sets it as your wallpaper. If you wish to customize the behavior, you can modify the `main.py` file.

You can change the image source, update frequency, or any other settings according to your preferences.

## Dependencies

The wallpaper changer requires the following dependencies to run:

- Python 3
- BeautifulSoup (`pip install beautifulsoup4`)
- PyGObject (`pip install PyGObject`)

## License

This project is licensed under the [GPL License](https://www.gnu.org/licenses/gpl-3.0.en.html#license-text).

## Contributing

Contributions are welcome! If you find any issues or have suggestions for improvements, please open an issue or submit a pull request.

## Credits

- The Bing daily image is used under the terms of the [Bing Image Archive API](https://docs.microsoft.com/en-us/bing/search-apis/bing-image-search/reference/queryexpansion).
- The application icon is part of icon pack by [Vinceliuice](https://github.com/vinceliuice)
- The BeautifulSoup library is used for parsing HTML content in Python.
- Project is inspired(not copied) by similar projects by [Utkarsh](https://github.com/utkarshgpta/bing-desktop-wallpaper-changer) and [neffo](https://github.com/neffo/bing-wallpaper-gnome-extension)

## Author:
Project written by Anant.

